---
title: Пример триггера LOGON (C++)
description: В этом примере C++ показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при входе пользователя в систему.
ms.assetid: 15647234-8d1f-4d75-b215-92927b300c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137155a28a84a981b6013b6651f327a8c6bb4474
ms.sourcegitcommit: f19e3b30abea739d83178cdc8f2478eb4905f1d0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2020
ms.locfileid: "104339551"
---
# <a name="logon-trigger-example-c"></a><span data-ttu-id="397d3-103">Пример триггера LOGON (C++)</span><span class="sxs-lookup"><span data-stu-id="397d3-103">Logon Trigger Example (C++)</span></span>

<span data-ttu-id="397d3-104">В этом примере C++ показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="397d3-104">This C++ example shows how to create a task that is scheduled to execute Notepad when a user logs on.</span></span> <span data-ttu-id="397d3-105">Задача содержит триггер входа, указывающий начальную границу задачи для запуска, и идентификатор пользователя, указывающий пользователя.</span><span class="sxs-lookup"><span data-stu-id="397d3-105">The task contains a logon trigger that specifies a start boundary for the task to start and a user identifier that specifies the user.</span></span> <span data-ttu-id="397d3-106">Задача регистрируется с помощью группы администраторов в качестве контекста безопасности для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="397d3-106">The task is registered using the Administrators group as a security context to run the task.</span></span>

<span data-ttu-id="397d3-107">Следующая процедура описывает, как запланировать задачу запуска исполняемого файла при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="397d3-107">The following procedure describes how to schedule a task to start an executable when a user logs on.</span></span>

<span data-ttu-id="397d3-108">**Планирование запуска программы «Блокнот» при входе пользователя**</span><span class="sxs-lookup"><span data-stu-id="397d3-108">**To schedule Notepad to start when a user logs on**</span></span>

1.  <span data-ttu-id="397d3-109">Инициализация COM и Настройка общей безопасности COM.</span><span class="sxs-lookup"><span data-stu-id="397d3-109">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="397d3-110">Создайте объект [**GetFolder интерфейса ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="397d3-110">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="397d3-111">Этот объект позволяет создавать задачи в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="397d3-111">This object allows you to create tasks in a specified folder.</span></span>

3.  <span data-ttu-id="397d3-112">Получите папку задачи, в которой будет создана задача.</span><span class="sxs-lookup"><span data-stu-id="397d3-112">Get a task folder to create a task in.</span></span>

    <span data-ttu-id="397d3-113">Используйте метод [**GetFolder интерфейса ITaskService::**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) GetObject для получения папки и метод [**GetFolder интерфейса ITaskService::**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) Create, чтобы создать объект [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="397d3-113">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>

4.  <span data-ttu-id="397d3-114">Определите сведения о задаче с помощью объекта [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) , например сведения о регистрации для задачи.</span><span class="sxs-lookup"><span data-stu-id="397d3-114">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span>

    <span data-ttu-id="397d3-115">Чтобы определить сведения о задаче, используйте [**свойство регистратионинфо объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) и другие свойства интерфейса [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="397d3-115">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define the task information.</span></span>

5.  <span data-ttu-id="397d3-116">Создайте триггер входа с помощью [**свойства Triggers объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) , чтобы получить доступ к интерфейсу [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) для задачи.</span><span class="sxs-lookup"><span data-stu-id="397d3-116">Create a logon trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) interface for the task.</span></span>

    <span data-ttu-id="397d3-117">Используйте метод [**ITriggerCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) , чтобы указать, что вы хотите создать триггер входа.</span><span class="sxs-lookup"><span data-stu-id="397d3-117">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method to specify that you want to create a logon trigger.</span></span> <span data-ttu-id="397d3-118">Можно задать начальную границу и свойство [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) для триггера таким образом, чтобы действия задачи были запланированы на выполнение при входе пользователя в систему после начальной границы.</span><span class="sxs-lookup"><span data-stu-id="397d3-118">You can set the start boundary and the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property for the trigger so that the task's actions will be scheduled to execute when the user logs on after the start boundary.</span></span>

6.  <span data-ttu-id="397d3-119">Создайте действие для выполнения задачи с помощью [**свойства Actions объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) , чтобы получить доступ к интерфейсу [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) для задачи.</span><span class="sxs-lookup"><span data-stu-id="397d3-119">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface for the task.</span></span> <span data-ttu-id="397d3-120">Используйте метод [**IActionCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) , чтобы указать тип действия, которое требуется создать.</span><span class="sxs-lookup"><span data-stu-id="397d3-120">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="397d3-121">В этом примере используется объект [**иексекактион**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) , который представляет действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="397d3-121">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>
7.  <span data-ttu-id="397d3-122">Зарегистрируйте задачу с помощью метода [**ITaskFolder:: регистертаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="397d3-122">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="397d3-123">В следующем примере C++ показано, как запланировать задачу для выполнения в блокноте при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="397d3-123">The following C++ example shows how to schedule a task to execute Notepad when a user logs on.</span></span>


```C++
/**********************************************************************
 This sample schedules a task to start notepad.exe when a user logs on. 
**********************************************************************/

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
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"Logon Trigger Test Task";

    //  Get the windows directory and set the path to notepad.exe.
    wstring wstrExecutablePath = _wgetenv( L"WINDIR");
    wstrExecutablePath += L"\\SYSTEM32\\NOTEPAD.EXE";


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
          printf("Failed to create an instance of ITaskService: %x", hr);
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
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }
    
    //  If the same task exists, remove it.
    pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
    //  Create the task builder object to create the task.
    ITaskDefinition *pTask = NULL;
    hr = pService->NewTask( 0, &pTask );

    pService->Release();  // COM clean up.  Pointer is no longer used.
    if (FAILED(hr))
    {
        printf("Failed to create a task definition: %x", hr);
        pRootFolder->Release();
        CoUninitialize();
        return 1;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    IRegistrationInfo *pRegInfo= NULL;
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        printf("\nCannot get identification pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pRegInfo->put_Author(L"Author Name");
    pRegInfo->Release();  
    if( FAILED(hr) )
    {
        printf("\nCannot put identification info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create the settings for the task
    ITaskSettings *pSettings = NULL;
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        printf("\nCannot get settings pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set setting values for the task. 
    hr = pSettings->put_StartWhenAvailable(VARIANT_TRUE);
    pSettings->Release();  
    if( FAILED(hr) )
    {
        printf("\nCannot put setting info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the trigger collection to insert the logon trigger.
    ITriggerCollection *pTriggerCollection = NULL;
    hr = pTask->get_Triggers( &pTriggerCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get trigger collection: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Add the logon trigger to the task.
    ITrigger *pTrigger = NULL;
    hr = pTriggerCollection->Create( TASK_TRIGGER_LOGON, &pTrigger );
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    ILogonTrigger *pLogonTrigger = NULL;       
    hr = pTrigger->QueryInterface( 
            IID_ILogonTrigger, (void**) &pLogonTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for ILogonTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pLogonTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
       printf("\nCannot put the trigger ID: %x", hr);
    
    //  Set the task to start at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below
    //  is January 1st 2005 at 12:05
    hr = pLogonTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    if( FAILED(hr) )
       printf("\nCannot put the start boundary: %x", hr);
    
    hr = pLogonTrigger->put_EndBoundary( _bstr_t(L"2015-05-02T08:00:00") );
    if( FAILED(hr) )
       printf("\nCannot put the end boundary: %x", hr);    
    
    //  Define the user.  The task will execute when the user logs on.
    //  The specified user must be a user on this computer.  
    hr = pLogonTrigger->put_UserId( _bstr_t( L"DOMAIN\\UserName" ) );  
    pLogonTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot add user ID to logon trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Add an Action to the task. This task will execute notepad.exe.     
    IActionCollection *pActionCollection = NULL;

    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get Task collection pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
        
    //  Create the action, specifying that it is an executable action.
    IAction *pAction = NULL;
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    pActionCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the action: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    IExecAction *pExecAction = NULL;
    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( 
        IID_IExecAction, (void**) &pExecAction );
    pAction->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for IExecAction: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) );
    pExecAction->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot set path of executable: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(L"S-1-5-32-544"),
            _variant_t(), 
            TASK_LOGON_GROUP,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        printf("\nError saving the Task : %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    printf("\n Success! Task successfully registered. " );

    // Clean up
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="397d3-124">См. также</span><span class="sxs-lookup"><span data-stu-id="397d3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="397d3-125">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="397d3-125">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




