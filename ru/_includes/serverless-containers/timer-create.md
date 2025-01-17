Создайте [таймер](../../serverless-containers/concepts/trigger/timer.md) — триггер, который будет вызывать [контейнер](../../serverless-containers/concepts/container.md) {{ serverless-containers-name }} по расписанию.

О том, как создать таймер, который будет вызывать функцию, читайте в [документации {{ sf-name }}](../../functions/operations/trigger/timer-create.md).

## Перед началом работы {#before-you-begin}

{% include [trigger-before-you-begin](./trigger-before-you-begin.md) %}

## Создать триггер {#trigger-create}

{% include [trigger-time](../functions/trigger-time.md) %}

{% list tabs %}

- Консоль управления

    1. В [консоли управления]({{ link-console-main }}) перейдите в каталог, в котором хотите создать триггер.

    1. Выберите сервис **{{ serverless-containers-name }}**.

    1. На панели слева выберите ![image](../../_assets/functions/triggers.svg) **Триггеры**.

    1. Нажмите кнопку **Создать триггер**.

    1. В блоке **Базовые параметры**:

        * Введите имя и описание триггера.
        * В поле **Тип** выберите **Таймер**.
        * В поле **Запускаемый ресурс** выберите **Контейнер**.

    1. В блоке **Настройки таймера** укажите расписание вызова контейнера в формате [cron-выражения](../../functions/concepts/trigger/timer.md#cron-expression).

    1. В блоке **Настройки контейнера** выберите его и укажите:

        * [ревизию контейнера](../../serverless-containers/concepts/container.md#revision);
        * [сервисный аккаунт](../../iam/concepts/users/service-accounts.md), от имени которого будет вызываться контейнер.

    1. (опционально) В блоке **Настройки повторных запросов**:

        * В поле **Интервал** укажите время, через которое будет сделан повторный вызов контейнера, если текущий завершился неуспешно. Допустимые значения — от 10 до 60 секунд, значение по умолчанию — 10 секунд.
        * В поле **Количество попыток** укажите количество повторных вызовов контейнера, которые будут сделаны, прежде чем триггер отправит сообщение в [Dead Letter Queue](../../functions/concepts/dlq.md). Допустимые значения — от 1 до 5, значение по умолчанию — 1.

    1. (опционально) В блоке **Настройки Dead Letter Queue** выберите очередь [Dead Letter Queue](../../functions/concepts/dlq.md) и сервисный аккаунт с правами на запись в нее.

    1. Нажмите кнопку **Создать триггер**.

{% endlist %}

## Проверить результат {#check-result}

{% include [check-result](check-result.md) %}
