---
title: Пример триггера регистрации (XML)
description: в этом примере XML определяет задачу, которая запускается Блокнот при регистрации задачи.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b111f5c8c0801bb404e12cee20faf19208d7372d1a3980f7368c6efd2bcbfd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759585"
---
# <a name="registration-trigger-example-xml"></a>Пример триггера регистрации (XML)

в этом примере XML определяет задачу, которая запускается Блокнот при регистрации задачи.

Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe. при использовании средства Schtasks.exe (расположенного в каталоге C: \\ Windows \\ System32) можно зарегистрировать задачу с помощью следующей команды: **schtasks/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

> [!Note]  
> При обновлении задачи с триггером регистрации задача будет выполнена после обновления.

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a>определение задачи для запуска Блокнот при регистрации

в следующем примере XML показано, как определить задачу с одним действием выполнения (запуск Блокнот), одним триггером регистрации, который запускает задачу при регистрации, а также несколько других параметров задач, влияющих на то, как задача обрабатывается планировщик задач.

> [!Note]  
> При обновлении задачи с триггером регистрации задача будет выполнена после обновления.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a>Элементы схемы TaskScheduler

Ниже приведены некоторые важные элементы, которые следует помнить при использовании этого примера.

-   [**Регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md): содержит сведения о регистрации задачи.
-   [**Триггеры**](taskschedulerschema-triggers-tasktype-element.md): определяет триггер, который запускает задачу.
-   [**Регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md): определяет триггер регистрации. В этом случае используются только два дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется.
-   [**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.
-   [**Параметры**](taskschedulerschema-settings-tasktype-element.md): определяет параметры задачи, которые планировщик задач использует для выполнения задачи.
-   [**Действия**](taskschedulerschema-actions-tasktype-element.md): определяет действия, выполняемые задачей. в этом случае выполняется Блокнот.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




