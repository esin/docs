---
editable: false
---

# Правила тарификации для {{ ml-platform-name }}


## Из чего складывается стоимость использования {{ ml-platform-name }} {#rules}

При работе с платформой {{ ml-platform-name }} вы платите за использование вычислительных ресурсов — посекундно тарифицируется время вычисления или работы инстансов.

### Единица тарификации {#unit}

Единица тарификации — это один тарифицирующий юнит. Количество тарифицирующих юнитов, затраченных на вычисление, зависит от:
* мощности используемых вычислительных ресурсов;
* времени, затраченного на вычисление.

  Время вычисления округляется до целого числа секунд в большую сторону.

Стоимость одного тарифицирующего юнита — это стоимость использования 1 ядра CPU в течение 1 секунды. Количество юнитов зависит от конфигурации вычислительных ресурсов.

### {{ ds-nb }} {#dedicated}

При вычислениях и обучении моделей в ноутбуках {{ ml-platform-name }} вы оплачиваете все время использования ВМ с момента запуска первых вычислений в ноутбуке до освобождения ВМ вне зависимости от того, проводились ли вычисления после первого запуска. Если вы производите вычисления с помощью кластеров {{ dataproc-name }}, они [оплачиваются отдельно](#data-proc).

Также отдельно оплачивается [хранение данных](#storage) в датасетах и расширение хранилища проекта.

### Запуск заданий {{ ml-platform-name }} Jobs {#jobs}

При удаленном запуске вычислений с помощью [{{ ml-platform-name }} Jobs](concepts/jobs/index.md) вы платите за время вычислений на выбранной конфигурации вычислительных ресурсов. Дополнительно оплачивается [хранение данных](#prices-jobs), необходимых для запуска заданий: кеш, логи, входные данные и результаты выполнения задания.

### Эксплуатация моделей {#node}

При развертывании эксплуатации моделей вы платите за время работы каждого инстанса ноды — от момента запуска до момента удаления. 

### Использование кластеров {{ dataproc-name }} {#data-proc}

При вычислениях на кластерах {{ dataproc-name }} в стоимость входят:
* Вычислительные ресурсы выбранной конфигурации {{ ml-platform-name }}.
* Все время существования кластера {{ dataproc-name }} по [правилам тарификации {{ dataproc-full-name }}](../data-proc/pricing.md).

Подробнее об [интеграции с {{ dataproc-name }}](concepts/data-proc.md).

### Использование дискового пространства {#storage}

Каждый проект {{ ml-platform-name }} имеет хранилище, в рамках которого хранение данных не тарифицируется. При увеличении [квоты]({{ link-console-quotas }}) на размер проекта весь запрошенный [объем хранилища](#prices-storage) свыше {{ ml-project-size }} оплачивается отдельно. Подробнее с квотами и лимитами сервиса можно ознакомиться в разделе [{#T}](concepts/limits.md).

[Хранение данных внутри датасетов](#prices-storage) оплачивается отдельно.

Если вам требуется хранить большие объемы данных, вы можете использовать сервис {{ objstorage-full-name }}. В этом случае хранение данных будет тарифицироваться по [правилам тарификации {{ objstorage-name }}](../storage/pricing.md).

[Хранение моделей](#prices-storage) оплачивается отдельно. Тарификация зависит от размера модели, размер рассчитывается в ГБ и округляется до целого значения в большую сторону. 

{% include [pricing-gb-size](../_includes/pricing-gb-size.md) %}

Цены за месяц использования формируются из расчета 720 часов в месяц.

## Примеры расчета стоимости {#price-example}

### {{ ds-nb }} {#price-example-notebook}

Стоимость использования {{ ml-platform-name }} со следующими параметрами:

* **Вычислительные ресурсы:** конфигурация g1.1 с 8 CPU и 1 GPU.
* **Время использования ВМ:** 10 мин.

Расчет стоимости:

> 72 × 600 = 43 200 юнитов за использование ВМ
> 43 200 × 0,0012 = 51,8400&nbsp;₽
>
> Итого: 51,8400&nbsp;₽ — стоимость использования {{ ml-platform-name }}.

Где:
* 72 — количество юнитов за конфигурацию g1.1.
* 600 — время использования ВМ в секундах.
* 0,0012 ₽ — стоимость 1 юнита.

### {{ ds-inf }} {#price-example-node}

Стоимость использования {{ ds-inf }} со следующими параметрами:

* **Количество инстансов в ноде:** 2.
* **Конфигурация инстансов:** g1.1 с 8 CPU и 1 GPU.
* **Время работы ноды:** 2 дня 3 часа 36 минут.

Перевод времени работы ноды в секунды:

> 2 × (24 × 60 × 60) + 3 × (60 × 60) + 36 × 60 =172 800 + 10 800 + 2 160= 185 760

Где:
* (24 × 60 × 60) — количество секунд в сутках.
* (60 × 60) — количество секунд в 1 часе.
* 60 — количество секунд в 1 минуте.

Расчет стоимости:

> 72 × 185 760 × 2 = 26 749 440 юнитов за работу ноды
> 26 749 440 × 0,0012 = 32 099,3280&nbsp;₽
>
> Итого: 32 099,3280&nbsp;₽ – стоимость использования {{ ml-platform-name }}.

Где:
* 72 — количество юнитов за конфигурацию g1.1.
* 185 760 — время работы ноды в секундах.
* 2 — количество инстансов в ноде.
* 0,0012 ₽ — стоимость 1 юнита.

## Цены {#prices}

Цены использования конфигураций действуют при запуске вычислений в [{{ ds-nb }}](concepts/project.md#mode), запуске заданий [{{ ds-jobs }}](concepts/jobs/index.md) и работе [{{ ds-inf }}](../datasphere/concepts/deploy/index.md).


{% include [rub-unit-and-resource.md](../_pricing/datasphere/rub-unit-and-resource.md) %}




### Хранение данных внутри {{ ml-platform-name }} {#prices-storage}


{% include [rub-storage.md](../_pricing/datasphere/rub-storage.md) %}




### Исходящий трафик {#prices-traffic}


{% include notitle [rub-egress-traffic.md](../_pricing/rub-egress-traffic.md) %}




