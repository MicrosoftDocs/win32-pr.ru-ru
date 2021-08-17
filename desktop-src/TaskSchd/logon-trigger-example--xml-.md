---
title: Пример триггера LOGON (XML)
description: в этом примере XML определяет задачу, которая запускается Блокнот при входе пользователя в систему.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7e92216748a799c5cf8a3ae32393db2b33c680861b2a5d3249eb19c527474e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760061"
---
# <a name="logon-trigger-example-xml"></a>Пример триггера LOGON (XML)

в этом примере XML определяет задачу, которая запускается Блокнот при входе пользователя в систему.

Чтобы зарегистрировать задачу, определенную в формате XML, можно использовать функцию [**ITaskFolder:: регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**таскфолдер. регистертаск**](taskfolder-registertask.md) для создания скриптов) или средство командной строки Schtasks.exe. при использовании средства Schtasks.exe (расположенного в каталоге C: \\ Windows \\ System32) можно зарегистрировать задачу с помощью следующей команды: **schtasks/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>определение задачи для запуска Блокнот при загрузке системы

в следующем примере XML показано, как определить задачу с одним действием выполнения (начиная Блокнот), одним триггером входа, запускающим задачу при входе пользователя в систему, и несколькими другими параметрами задач, влияющими на способ обработки задачи с помощью планировщик задач.

> [!Note]  
> В качестве значения элемента **UserID** задайте имя пользователя на компьютере, на котором зарегистрирована задача.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
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
-   [**Логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md): определяет триггер входа. В этом случае используются три дочерних элемента: Начальная и конечная границы, указывающие, когда триггер активируется и деактивируется, и элемент [**UserID**](taskschedulerschema-userid-logontriggertype-element.md) , который является идентификатором пользователя. Задача запускается, когда пользователь входит в систему на компьютере.
-   [**Участник**](taskschedulerschema-principal-principaltype-element.md): определяет контекст безопасности, в котором выполняется задача.
-   [**Параметры**](taskschedulerschema-settings-tasktype-element.md): определяет параметры задачи, которые планировщик задач использует для выполнения задачи.
-   [**Действия**](taskschedulerschema-actions-tasktype-element.md): определяет действия, выполняемые задачей. в этом случае выполняется Блокнот.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




