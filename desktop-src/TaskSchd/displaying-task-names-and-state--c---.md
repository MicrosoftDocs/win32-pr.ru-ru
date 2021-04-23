---
title: Отображение имен и состояний задач (C++)
description: В этих двух примерах C++ показано, как перечислить задачи. В одном из примеров показано, как отобразить сведения о задачах в папке задач, а в других примерах показано, как отобразить сведения обо всех выполняющихся задачах.
ms.assetid: 32037133-d3f3-4186-b035-ab01d37ed58d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6189960ef5b6e4ad78e75f156a482481f347b4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779820"
---
# <a name="displaying-task-names-and-states-c"></a><span data-ttu-id="16b31-104">Отображение имен и состояний задач (C++)</span><span class="sxs-lookup"><span data-stu-id="16b31-104">Displaying Task Names and States (C++)</span></span>

<span data-ttu-id="16b31-105">В этих двух примерах C++ показано, как перечислить задачи.</span><span class="sxs-lookup"><span data-stu-id="16b31-105">These two C++ examples show how to enumerate tasks.</span></span> <span data-ttu-id="16b31-106">В одном из примеров показано, как отобразить сведения о задачах в папке задач, а в других примерах показано, как отобразить сведения обо всех выполняющихся задачах.</span><span class="sxs-lookup"><span data-stu-id="16b31-106">One example shows how to display information for tasks in a task folder, and the other examples shows how to display information for all running tasks.</span></span>

<span data-ttu-id="16b31-107">В следующей процедуре описывается отображение имен и состояний задач для всех задач в папке задачи.</span><span class="sxs-lookup"><span data-stu-id="16b31-107">The following procedure describes how to display task names and state for all the tasks in a task folder.</span></span>

<span data-ttu-id="16b31-108">**Отображение имен и состояний задач для всех задач в папке задач**</span><span class="sxs-lookup"><span data-stu-id="16b31-108">**To display task names and state for all the tasks in a task folder**</span></span>

1.  <span data-ttu-id="16b31-109">Инициализация COM и Настройка общей безопасности COM.</span><span class="sxs-lookup"><span data-stu-id="16b31-109">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="16b31-110">Создайте объект [**GetFolder интерфейса ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="16b31-110">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="16b31-111">Этот объект позволяет подключиться к службе планировщик задач и получить доступ к определенной папке задач.</span><span class="sxs-lookup"><span data-stu-id="16b31-111">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

3.  <span data-ttu-id="16b31-112">Получите папку задач, содержащую задачи, сведения о которых требуется получить.</span><span class="sxs-lookup"><span data-stu-id="16b31-112">Get a task folder that holds the tasks you want information about.</span></span>

    <span data-ttu-id="16b31-113">Используйте метод [**GetFolder интерфейса ITaskService:: Onfolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) , чтобы получить папку.</span><span class="sxs-lookup"><span data-stu-id="16b31-113">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder.</span></span>

4.  <span data-ttu-id="16b31-114">Получение коллекции задач из папки.</span><span class="sxs-lookup"><span data-stu-id="16b31-114">Get the collection of tasks from the folder.</span></span>

    <span data-ttu-id="16b31-115">Используйте метод [**ITaskFolder::-Tasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) , чтобы получить коллекцию задач ([**ирегистередтаскколлектион**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)).</span><span class="sxs-lookup"><span data-stu-id="16b31-115">Use the [**ITaskFolder::GetTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) method to get the collection of tasks ([**IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)).</span></span>

5.  <span data-ttu-id="16b31-116">Получение числа задач в коллекции и перечисление всех задач в коллекции.</span><span class="sxs-lookup"><span data-stu-id="16b31-116">Get the number of tasks in the collection, and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="16b31-117">Чтобы получить экземпляр [**ирегистередтаск**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) , используйте [**свойство Item объекта ирегистередтаскколлектион**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) .</span><span class="sxs-lookup"><span data-stu-id="16b31-117">Use the [**Item Property of IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) to get an [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) instance.</span></span> <span data-ttu-id="16b31-118">Каждый экземпляр будет содержать задачу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="16b31-118">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="16b31-119">Затем можно отобразить сведения (значения свойств) из каждой зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="16b31-119">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="16b31-120">В следующем примере C++ показано, как отобразить имя и состояние всех задач в корневой папке задачи.</span><span class="sxs-lookup"><span data-stu-id="16b31-120">The following C++ example shows how to display the name and state of all the tasks in the root task folder.</span></span>


```C++
/********************************************************************
 This sample enumerates through the tasks on the local computer and 
 displays their name and state. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")


using namespace std;

int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
          CoUninitialize();
          return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    
    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
    
    //  -------------------------------------------------------
    //  Get the registered tasks in the folder.
    IRegisteredTaskCollection* pTaskCollection = NULL;
    hr = pRootFolder->GetTasks( NULL, &pTaskCollection );

    pRootFolder->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get the registered tasks.: %x", hr);
        CoUninitialize();
        return 1;
    }

    LONG numTasks = 0;
    hr = pTaskCollection->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pTaskCollection->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of Tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRegisteredTask* pRegisteredTask = NULL;
        hr = pTaskCollection->get_Item( _variant_t(i+1), &pRegisteredTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRegisteredTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRegisteredTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRegisteredTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pTaskCollection->Release();
    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="16b31-121">В следующей процедуре описывается отображение имен и состояний задач для всех выполняемых задач.</span><span class="sxs-lookup"><span data-stu-id="16b31-121">The following procedure describes how to display task names and state for all running tasks.</span></span>

<span data-ttu-id="16b31-122">**Отображение имен и состояний задач для всех выполняемых задач**</span><span class="sxs-lookup"><span data-stu-id="16b31-122">**To display task names and state for all running tasks**</span></span>

1.  <span data-ttu-id="16b31-123">Инициализация COM и Настройка общей безопасности COM.</span><span class="sxs-lookup"><span data-stu-id="16b31-123">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="16b31-124">Создайте объект [**GetFolder интерфейса ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="16b31-124">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="16b31-125">Этот объект позволяет подключиться к службе планировщик задач и получить доступ к определенной папке задач.</span><span class="sxs-lookup"><span data-stu-id="16b31-125">This object allows you to connect to the Task Scheduler service and access a specific task folder.</span></span>

3.  <span data-ttu-id="16b31-126">Используйте метод [**GetFolder интерфейса ITaskService:: жетруннингтаскс**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) , чтобы получить коллекцию всех выполняемых задач ([**ируннингтаскколлектион**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)).</span><span class="sxs-lookup"><span data-stu-id="16b31-126">Use the [**ITaskService::GetRunningTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) method to get a collection of all the running tasks ([**IRunningTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)).</span></span> <span data-ttu-id="16b31-127">Можно указать, чтобы получать экземпляры выполняемой задачи: включая или исключая скрытые задачи.</span><span class="sxs-lookup"><span data-stu-id="16b31-127">You can specify to get instances of running task either including or excluding hidden tasks.</span></span>
4.  <span data-ttu-id="16b31-128">Получение числа задач в коллекции и перечисление всех задач в коллекции.</span><span class="sxs-lookup"><span data-stu-id="16b31-128">Get the number of tasks in the collection, and enumerate through each task in the collection.</span></span>

    <span data-ttu-id="16b31-129">Чтобы получить экземпляр [**ируннингтаск**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) , используйте [**свойство Item объекта ируннингтаскколлектион**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) .</span><span class="sxs-lookup"><span data-stu-id="16b31-129">Use the [**Item property of IRunningTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) to get an [**IRunningTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) instance.</span></span> <span data-ttu-id="16b31-130">Каждый экземпляр будет содержать задачу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="16b31-130">Each instance will contain a task in the collection.</span></span> <span data-ttu-id="16b31-131">Затем можно отобразить сведения (значения свойств) из каждой зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="16b31-131">You can then display the information (property values) from each registered task.</span></span>

<span data-ttu-id="16b31-132">В следующем примере C++ показано, как отобразить имя и состояние всех выполняемых задач, включая скрытые задачи.</span><span class="sxs-lookup"><span data-stu-id="16b31-132">The following C++ example shows how to display the name and state of all the running tasks, including hidden tasks.</span></span>


```C++
/********************************************************************
 This sample enumerates through all running tasks on the local computer and 
 displays their name and state. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")


using namespace std;

int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
          CoUninitialize();
          return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

       // Get the running tasks.
       IRunningTaskCollection* pRunningTasks = NULL;
       hr = pService->GetRunningTasks(TASK_ENUM_HIDDEN, &pRunningTasks);

    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
        
    LONG numTasks = 0;
    hr = pRunningTasks->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pRunningTasks->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of running tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRunningTask* pRunningTask = NULL;
        hr = pRunningTasks->get_Item( _variant_t(i+1), &pRunningTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRunningTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRunningTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRunningTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pRunningTasks->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="16b31-133">См. также</span><span class="sxs-lookup"><span data-stu-id="16b31-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b31-134">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="16b31-134">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




