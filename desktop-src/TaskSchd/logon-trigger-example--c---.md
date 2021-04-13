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
# <a name="logon-trigger-example-c"></a>Пример триггера LOGON (C++)

В этом примере C++ показано, как создать задачу, которая запланирована на выполнение программы «Блокнот» при входе пользователя в систему. Задача содержит триггер входа, указывающий начальную границу задачи для запуска, и идентификатор пользователя, указывающий пользователя. Задача регистрируется с помощью группы администраторов в качестве контекста безопасности для выполнения задачи.

Следующая процедура описывает, как запланировать задачу запуска исполняемого файла при входе пользователя в систему.

**Планирование запуска программы «Блокнот» при входе пользователя**

1.  Инициализация COM и Настройка общей безопасности COM.
2.  Создайте объект [**GetFolder интерфейса ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .

    Этот объект позволяет создавать задачи в указанной папке.

3.  Получите папку задачи, в которой будет создана задача.

    Используйте метод [**GetFolder интерфейса ITaskService::**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) GetObject для получения папки и метод [**GetFolder интерфейса ITaskService::**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) Create, чтобы создать объект [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .

4.  Определите сведения о задаче с помощью объекта [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) , например сведения о регистрации для задачи.

    Чтобы определить сведения о задаче, используйте [**свойство регистратионинфо объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) и другие свойства интерфейса [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .

5.  Создайте триггер входа с помощью [**свойства Triggers объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) , чтобы получить доступ к интерфейсу [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) для задачи.

    Используйте метод [**ITriggerCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) , чтобы указать, что вы хотите создать триггер входа. Можно задать начальную границу и свойство [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) для триггера таким образом, чтобы действия задачи были запланированы на выполнение при входе пользователя в систему после начальной границы.

6.  Создайте действие для выполнения задачи с помощью [**свойства Actions объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) , чтобы получить доступ к интерфейсу [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) для задачи. Используйте метод [**IActionCollection:: Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) , чтобы указать тип действия, которое требуется создать. В этом примере используется объект [**иексекактион**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) , который представляет действие, выполняющее операцию командной строки.
7.  Зарегистрируйте задачу с помощью метода [**ITaskFolder:: регистертаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

В следующем примере C++ показано, как запланировать задачу для выполнения в блокноте при входе пользователя в систему.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




