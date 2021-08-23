---
title: Отображение имен и состояний задач (написание сценариев)
description: В этом примере сценария показано, как перечислить задачи в папке задачи и отобразить значения свойств из каждой задачи.
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6f3ec036b1d9d61c387495b48874bf742a9479ae0608f0e5c728a029df24709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002492"
---
# <a name="displaying-task-names-and-states-scripting"></a>Отображение имен и состояний задач (написание сценариев)

В этом примере сценария показано, как перечислить задачи в папке задачи и отобразить значения свойств из каждой задачи.

В следующей процедуре описывается отображение имен и состояний задач для всех задач в папке задачи.

**Отображение имен и состояний задач для всех задач в папке задач**

1.  Создайте объект [**TaskService**](taskservice.md) .

    Этот объект позволяет подключиться к службе планировщик задач и получить доступ к определенной папке задач.

2.  Получите папку задач, содержащую задачи, сведения о которых требуется получить.

    Чтобы получить папку, используйте метод [**TaskService. * Folder**](taskservice-getfolder.md) .

3.  Получение коллекции задач из папки.

    Используйте метод [**таскфолдер.**](taskfolder-gettasks.md) регистередтаскколлектион для получения коллекции Tasks ([](registeredtaskcollection.md)).

4.  Получение числа задач в коллекции и перечисление всех задач в коллекции.

    Используйте коллекцию объектов [**регистередтаскколлектион**](registeredtaskcollection.md) для получения экземпляра объекта [**регистередтаск**](registeredtask.md) . Каждый экземпляр будет содержать задачу в коллекции. Затем можно отобразить сведения (значения свойств) из каждой зарегистрированной задачи.

В следующем примере на языке VBScript показано, как выполнить перечисление коллекции зарегистрированных задач в корневой папке задач и отобразить имя и состояние каждой задачи.


```VB
'---------------------------------------------------------
' This sample enumerates through the tasks on the local computer and
' displays their name and state.
'---------------------------------------------------------


' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

' Get the task folder that contains the tasks. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")
 
Dim taskCollection
Set taskCollection = rootFolder.GetTasks(0)

Dim numberOfTasks
numberOfTasks = taskCollection.Count

If numberOfTasks = 0 Then 
    Wscript.Echo "No tasks are registered."
Else
    WScript.Echo "Number of tasks registered: " & numberOfTasks
    
    Dim registeredTask
    For Each registeredTask In taskCollection
        WScript.Echo "Task Name: " & registeredTask.Name
    
        Dim taskState 
        Select Case registeredTask.State 
            Case "0"
                taskState = "Unknown"
            Case "1"
                taskState = "Disabled"
            Case "2"
                taskState = "Queued"
            Case "3"
                taskState = "Ready"
            Case "4"
                taskState = "Running"
        End Select

        WScript.Echo "    Task State: " & taskState
    Next
End If

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




