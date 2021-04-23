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
ms.openlocfilehash: e7a8f22977f8cfd2d40b3c37a1cc8d7bcb5259e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411107"
---
# <a name="displaying-task-names-and-states-scripting"></a><span data-ttu-id="d2622-103">Отображение имен и состояний задач (написание сценариев)</span><span class="sxs-lookup"><span data-stu-id="d2622-103">Displaying Task Names and States (Scripting)</span></span>

<span data-ttu-id="d2622-104">В этом примере сценария показано, как перечислить задачи в папке задачи и отобразить значения свойств из каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="d2622-104">This scripting example shows how to enumerate tasks in a task folder and display property values from each task.</span></span>

<span data-ttu-id="d2622-105">В следующей процедуре описывается отображение имен и состояний задач для всех задач в папке задачи.</span><span class="sxs-lookup"><span data-stu-id="d2622-105">The following procedure describes how to display task names and states for all the tasks in a task folder.</span></span>

<span data-ttu-id="d2622-106">**Отображение имен и состояний задач для всех задач в папке задач**</span><span class="sxs-lookup"><span data-stu-id="d2622-106">**To display task names and state for all the tasks in a task folder**</span></span>

1.  <span data-ttu-id="d2622-107">Создайте объект [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d2622-107">Create the [**TaskService**](taskservice.md) object.</span></span>

    <span data-ttu-id="d2622-108">Этот объект позволяет подключиться к службе планировщик задач и получить доступ к определенной папке задач.</span><span class="sxs-lookup"><span data-stu-id="d2622-108">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

2.  <span data-ttu-id="d2622-109">Получите папку задач, содержащую задачи, сведения о которых требуется получить.</span><span class="sxs-lookup"><span data-stu-id="d2622-109">Get a task folder that holds the tasks you want information about.</span></span>

    <span data-ttu-id="d2622-110">Чтобы получить папку, используйте метод [**TaskService. \* Folder**](taskservice-getfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="d2622-110">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder.</span></span>

3.  <span data-ttu-id="d2622-111">Получение коллекции задач из папки.</span><span class="sxs-lookup"><span data-stu-id="d2622-111">Get the collection of tasks from the folder.</span></span>

    <span data-ttu-id="d2622-112">Используйте метод [**таскфолдер.**](taskfolder-gettasks.md) регистередтаскколлектион для получения коллекции Tasks ([](registeredtaskcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="d2622-112">Use the [**TaskFolder.GetTasks**](taskfolder-gettasks.md) method to get the collection of tasks ([**RegisteredTaskCollection**](registeredtaskcollection.md)).</span></span>

4.  <span data-ttu-id="d2622-113">Получение числа задач в коллекции и перечисление всех задач в коллекции.</span><span class="sxs-lookup"><span data-stu-id="d2622-113">Get the number of tasks in the collection and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="d2622-114">Используйте коллекцию объектов [**регистередтаскколлектион**](registeredtaskcollection.md) для получения экземпляра объекта [**регистередтаск**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="d2622-114">Use the [**RegisteredTaskCollection**](registeredtaskcollection.md) collection of objects to get a [**RegisteredTask**](registeredtask.md) object instance.</span></span> <span data-ttu-id="d2622-115">Каждый экземпляр будет содержать задачу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="d2622-115">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="d2622-116">Затем можно отобразить сведения (значения свойств) из каждой зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="d2622-116">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="d2622-117">В следующем примере на языке VBScript показано, как выполнить перечисление коллекции зарегистрированных задач в корневой папке задач и отобразить имя и состояние каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="d2622-117">The following VBScript example shows how to enumerate through a collection of registered tasks in the root task folder and display the name and state for each task.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d2622-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d2622-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2622-119">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="d2622-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




