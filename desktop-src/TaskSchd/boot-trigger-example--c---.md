---
title: Пример триггера Boot (C++)
description: В этом разделе содержится пример кода C++, в котором показано, как создать задачу, которая запланирована на выполнение Notepad.exe при запуске системы.
ms.assetid: d4dbbfe5-bde9-4a1c-8e11-24cd1e14646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbd5a5a73d100394b90e91f8b9c30c1bd495ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888687"
---
# <a name="boot-trigger-example-c"></a><span data-ttu-id="6f7b5-103">Пример триггера Boot (C++)</span><span class="sxs-lookup"><span data-stu-id="6f7b5-103">Boot Trigger Example (C++)</span></span>

<span data-ttu-id="6f7b5-104">В этом разделе содержится пример кода C++, в котором показано, как создать задачу, которая запланирована на выполнение Notepad.exe при запуске системы.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-104">This topic contains a C++ code example that shows how to create a task that is scheduled to execute Notepad.exe when the system is started.</span></span> <span data-ttu-id="6f7b5-105">Задача содержит триггер загрузки, который задает начальную границу и время задержки для запуска задачи после запуска системы.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-105">The task contains a boot trigger that specifies a start boundary and delay time for the task to start after the system is started.</span></span> <span data-ttu-id="6f7b5-106">Задача также содержит действие, указывающее на выполнение задачи Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-106">The task also contains an action that specifies the task execute Notepad.exe.</span></span> <span data-ttu-id="6f7b5-107">Задача регистрируется с использованием учетной записи локальной службы в качестве контекста безопасности для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-107">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="6f7b5-108">Следующая процедура описывает, как запланировать задачу запуска исполняемого файла при запуске системы.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-108">The following procedure describes how to schedule a task to start an executable when the system is started.</span></span>

<span data-ttu-id="6f7b5-109">**Планирование запуска программы «Блокнот» при запуске системы**</span><span class="sxs-lookup"><span data-stu-id="6f7b5-109">**To schedule Notepad to start when the system is started**</span></span>

1.  <span data-ttu-id="6f7b5-110">Инициализация COM и Настройка общей безопасности COM.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-110">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="6f7b5-111">Создайте объект [**GetFolder интерфейса ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="6f7b5-111">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="6f7b5-112">Этот объект позволяет создавать задачи в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-112">This object enables you to create tasks in a specified folder.</span></span>

3.  <span data-ttu-id="6f7b5-113">Получите папку задачи, в которой будет создана задача.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-113">Get a task folder to create a task in.</span></span>

    <span data-ttu-id="6f7b5-114">Используйте метод [**GetFolder интерфейса ITaskService::**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) GetObject для получения папки и метод [**GetFolder интерфейса ITaskService::**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) Create, чтобы создать объект [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="6f7b5-114">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>

4.  <span data-ttu-id="6f7b5-115">Определите сведения о задаче с помощью объекта [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) , например сведения о регистрации для задачи.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-115">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span>

    <span data-ttu-id="6f7b5-116">Чтобы определить сведения о задаче, используйте [**свойство регистратионинфо объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) и другие свойства интерфейса [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="6f7b5-116">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define the task information.</span></span>

5.  <span data-ttu-id="6f7b5-117">Создайте триггер загрузки с помощью [**свойства Triggers объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) , чтобы получить доступ к [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) для задачи.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-117">Create a boot trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) for the task.</span></span>

    <span data-ttu-id="6f7b5-118">Используйте метод [**ITriggerCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) , чтобы указать, что вы хотите создать триггер загрузки.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-118">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method to specify that you want to create a boot trigger.</span></span> <span data-ttu-id="6f7b5-119">Можно задать начальную границу и задержку для триггера, чтобы действия задач выполнялись в указанное время при запуске системы.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-119">You can set the start boundary and delay for the trigger so that the task actions will be scheduled to execute at a specified time when the system is started.</span></span>

6.  <span data-ttu-id="6f7b5-120">Создайте действие для выполнения задачи с помощью [**свойства Actions объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) , чтобы получить доступ к коллекции [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-120">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) collection for the task.</span></span>

    <span data-ttu-id="6f7b5-121">Используйте метод [**IActionCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) , чтобы указать тип действия, которое необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-121">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action you want to create.</span></span> <span data-ttu-id="6f7b5-122">В этом примере используется объект [**иексекактион**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) , который представляет действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-122">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>

7.  <span data-ttu-id="6f7b5-123">Зарегистрируйте задачу с помощью метода [**ITaskFolder:: регистертаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="6f7b5-123">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="6f7b5-124">В следующем примере кода C++ показано, как запланировать выполнение задачи Notepad.exe 30 секунд после запуска системы.</span><span class="sxs-lookup"><span data-stu-id="6f7b5-124">The following C++ code example shows how to schedule a task to execute Notepad.exe 30 seconds after the system is started.</span></span>


```C++
/********************************************************************
 This sample schedules a task to start Notepad.exe 30 seconds after
 the system is started. 
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
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"Boot Trigger Test Task";

    //  Get the Windows directory and set the path to Notepad.exe.
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
    //  Get the pointer to the root task folder.  
    //  This folder will hold the new task that is registered.
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
    //  Get the trigger collection to insert the boot trigger.
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

    //  Add the boot trigger to the task.
    ITrigger *pTrigger = NULL;
    hr = pTriggerCollection->Create( TASK_TRIGGER_BOOT, &pTrigger ); 
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    IBootTrigger *pBootTrigger = NULL;
    hr = pTrigger->QueryInterface( 
        IID_IBootTrigger, (void**) &pBootTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for IBootTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    hr = pBootTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
       printf("\nCannot put the trigger ID: %x", hr);
    
    //  Set the task to start at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below
    //  is January 1st 2005 at 12:05
    hr = pBootTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    if( FAILED(hr) )
       printf("\nCannot put the start boundary: %x", hr);
  
    hr = pBootTrigger->put_EndBoundary( _bstr_t(L"2015-05-02T08:00:00") );
    if( FAILED(hr) )
       printf("\nCannot put the end boundary: %x", hr);

    // Delay the task to start 30 seconds after system start. 
    hr = pBootTrigger->put_Delay( L"PT30S" );
    pBootTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put delay for boot trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    } 
       

    //  ------------------------------------------------------
    //  Add an Action to the task. This task will execute Notepad.exe.     
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
        
    //  Create the action, specifying it as an executable action.
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

    //  Set the path of the executable to Notepad.exe.
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
    VARIANT varPassword;
    varPassword.vt = VT_EMPTY;
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(L"Local Service"), 
            varPassword, 
            TASK_LOGON_SERVICE_ACCOUNT,
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

    //  Clean up.
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    CoUninitialize();
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="6f7b5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="6f7b5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f7b5-126">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="6f7b5-126">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




