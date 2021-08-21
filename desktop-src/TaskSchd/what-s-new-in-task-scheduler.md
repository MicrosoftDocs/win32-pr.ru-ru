---
title: Новые возможности планировщик задач
description: Список новых функциональных возможностей, появившихся в разных версиях планировщик задач.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Планировщик задач планировщик задач, новые возможности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3592cc5efd08afe4737e9af429d52fa41216b6c756a64faeaa45f6cc5c0774b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354786"
---
# <a name="whats-new-in-task-scheduler"></a>Новые возможности планировщик задач

Следующие изменения обобщают новые возможности в разных версиях планировщик задач.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (и Windows Server 2016)

В Windows 10 появились следующие изменения планировщик задач.

-   если используется экономия заряда, Windows планировщик задач задачи запускаются только в том случае, если задано следующее:

    -   Не задано для **запуска задачи только в том случае, если компьютер бездействует...** (задача не использует [**идлесеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   Не задано для запуска во время автоматического обслуживания (задача не использует [**маинтенанцесеттингс**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   Задается для **запуска только при входе пользователя в систему** (задача [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) — **\_ \_ Интерактивный \_ маркер входа в систему** или **\_ \_ Группа входа задач**).

    Все остальные триггеры откладываются до тех пор, пока не будет снята экономия заряда. Дополнительные сведения о доступе к состоянию заставки аккумулятора в приложении см. в разделе [**\_ \_ состояние питания системы**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Общие сведения о экономии заряда батареи см. [в разделе Заставка аккумулятора (в руководстве по компонентам оборудования)](/windows-hardware/design/component-guidelines/battery-saver).

-   по соображениям безопасности пользователь без прав администратора не может просматривать Windows планировщик задач задачи, созданной другим пользователем, и управлять ей.

## <a name="windows-8"></a>Windows 8

В Windows 8 появились следующие изменения планировщик задач 2,0:

-   Поддержка PowerShell: пользователи могут управлять (создавать, удалять, изменять, явно запускать, прекращать и т. д.). Windows Планировщик задач задач с помощью модуля PowerShell Счедуледтаскс.
-   Управляемые пароли. Администраторы могут использовать Active Directory управляемые учетные записи паролей в качестве участников задач. Для этих задач больше не требуется принудительная политика сброса пароля.
-   Изменения API: появились два новых параметра задачи с интерфейсом [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .
    -   [**Маинтенанцесеттингс**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings). задачи, использующие эти параметры, рассматриваются как новые типы запланированных задач, которые вызываются во время автоматического обслуживания ОС в соответствии с заданными периодичностью и крайним сроком.
    -   [**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile). задания, которые являются временными, всегда отключаются при загрузке ОС и должны быть явно повторно включены при необходимости. Временные задачи используются отказоустойчивыми кластерами, чтобы гарантировать, что в кластере одновременно планируется только один экземпляр задачи.
-   Механизм единого планирования теперь поддерживает следующие функции:
    -   Тип входа S4U с помощью элемента [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .
    -   Значения запроса XPath для триггеров событий с помощью элемента [**валуекуериес**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .
    -   Не разрешать жесткое завершение задачи с помощью элемента [**алловхардтерминате**](taskschedulerschema-allowhardterminate-settingstype-element.md) .
-   Функции, устаревшие в этом выпуске
    -   действие: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (в качестве обходного пути можно использовать [**иексекактион**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) с командлетом [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) ).
    -   Действие: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   AT.exe cmdline, программа

## <a name="windows-7"></a>Windows 7

в Windows 7 появились следующие изменения планировщик задач 2,0:

-   С помощью единого механизма планирования, предоставляемого базовой операционной системой.
-   Возможность отклонять запуск задач в удаленных приложениях, интегрированных локально (на шинах) сеансах.
-   Усиление безопасности задач (для задач, выполняемых как "СЕТЕВая служба" или "только ЛОКАЛЬная служба"):

    -   Возможность назначения задаче типа идентификатора безопасности (например, неограниченности или отсутствия).
    -   Разрешить разработчикам задач запрашивать точный набор привилегий, необходимых для их задачи.

-   Изменения API:

    -   Поддержка усиления безопасности для задач. Новая функция усиления безопасности задач появилась в новом интерфейсе IPrincipal2.
    -   Появились два новых параметра задачи с новым интерфейсом ITaskSettings2.

        -   Дисалловстартонремотеаппсессион. новый параметр Дисалловстартонремотеаппсессион может отклонить запуск задачи, если он активирован в [удаленных приложениях, интегрированных локально (шина)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .
        -   усеунифиедсчедулинженгине. использование параметра усеунифиедсчедулинженгине обеспечивает согласованное поведение для Windows задач и служб, поскольку управление им осуществляется единообразно с помощью общего механизма планирования на уровне системы. Хотя рекомендуется использовать унифицированный механизм, он не поддерживает некоторые функции планировщик задач. Если сочетание свойств не разрешит выполнение задачи в едином механизме, регистрация такого объекта будет отклонена.
        -   Функции задач, которые не поддерживаются единым ядром планирования, включают:

            -   Типы входа:

                -   [\_ \_ Интерактивный маркер входа для задачи \_ \_ или \_ пароль](./taskschedulerschema-logontype-principaltype-element.md)

            -   Политика нескольких экземпляров:

                -   [**\_экземпляры задач \_ прекращают \_ существующие**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Действия:

                -   [Отправка электронного сообщения](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Отображение сообщения](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Параметры:

                -   [Сетевые параметры задачи](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [Запретить жесткое завершение задачи](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Триггеры:

                -   [Ограничение времени выполнения триггера](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Шаблоны повторений для триггеров календаря]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [Значения запроса XPath для триггеров событий]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   [Ежемесячные](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) и месячные типы триггеров [дней недели](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md)

## <a name="windows-vista"></a>Windows Vista

планировщик задач API 2,0 следует использовать при разработке приложений, использующих службу планировщик задач в Windows Vista. Дополнительные сведения см. в разделе [Справочник по планировщик задач](task-scheduler-reference.md) и [Использование планировщик задач](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP и Windows Server 2003

API-интерфейс планировщик задач 2,0 недоступен. Используйте планировщик задач 1,0.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> <dt>

[Сведения о планировщик задач](about-the-task-scheduler.md)
</dt> </dl>

 

 
