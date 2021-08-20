---
title: Автоматическое обслуживание (Cookbook совместимости для Windows)
description: Автоматическое обслуживание
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a839191d84f3f20fcc598b42433c888b090b2b174dd6891c0b5b9fc72f0af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028872"
---
# <a name="automatic-maintenance"></a>Автоматическое обслуживание

## <a name="platforms"></a>Платформы

**клиенты** — Windows 8  
**серверы** — Windows Server 2012  


## <a name="description"></a>Описание

Windows зависит от выполнения действий в папке «входящие» и «обслуживание третьей стороны» для большей части его значений, включая Центр обновления Windows и автоматическое дефрагментацию диска, а также антивирусные обновления и проверки. Кроме того, предприятия часто используют действия по обслуживанию, такие как сканирование защиты доступа к сети (NAP), для обеспечения стандартов безопасности на всех рабочих станциях предприятия.

действие обслуживания в Windows предназначено для запуска в фоновом режиме с ограниченным участием пользователя и минимальным влиянием на производительность и энергопотребление. однако в Windows 7 и более ранних версий по-прежнему оказывают влияние на производительность и энергопотребление из-за недетерминированного и широкого разнообразия расписания нескольких действий по обслуживанию в Windows. Скорость реагирования на пользователей уменьшается при выполнении действия обслуживания, когда пользователи активно используют компьютер. кроме того, приложения часто запрашивают у пользователя обновление программного обеспечения и запускают фоновое обслуживание, а также направляют пользователей в несколько функций, включая центр поддержки, панель управления, Центр обновления Windows, планировщик задач оснастку MMC и сторонние элементы управления.

цель автоматического обслуживания состоит в том, чтобы объединить все действия, выполняемые в фоновом режиме, в Windows и помочь сторонним разработчикам добавить свое действие по обслуживанию Windows без негативного влияния на производительность и эффективность энергопотребления. Кроме того, автоматическое обслуживание позволяет пользователям и предприятиям управлять планированием и настройкой действий по обслуживанию.

**Основные проблемы**

Автоматическое обслуживание предназначено для решения этих проблем с действиями обслуживания в Windows:

-   Расписание крайнего срока
-   Конфликты использования ресурсов
-   Эффективность энергопотребления
-   Прозрачность для пользователя

## <a name="functionality"></a>функциональное назначение;

Автоматическое обслуживание способствует повышению эффективности простоя и позволяет выполнять все действия своевременно и по расстановке приоритетов. кроме того, он обеспечивает унифицированную видимость и контроль над деятельностью по обслуживанию, а также позволяет сторонним разработчикам добавлять свои действия по обслуживанию в Windows без негативного влияния на производительность и экономию энергии. Для этого он предоставляет полностью автоматический режим, автоматический режим, автоматическую приостанавливаться, крайние сроки и уведомления, а также корпоративный контроль. Они описаны ниже.

**Полностью автоматический режим**

Этот режим по умолчанию обеспечивает интеллектуальное планирование во время простоя ПК и в запланированное время — выполнение и автоматическую приостановку действий по обслуживанию без вмешательства пользователя. Пользователь может задать расписание по неделям или по дням. Все действия по обслуживанию являются неинтерактивными и выполняются автоматически.

Компьютер автоматически возобновляет работу из спящего режима, когда система, скорее всего, не используется, при соблюдении политики управления питанием, которая в случае ноутбуков, по умолчанию разрешает пробуждение только в том случае, если включено питание от сети. Все системные ресурсы с высокой степенью энергопотребления используются для выполнения действий по обслуживанию как можно быстрее. Если система была восстановлена из спящего режима для автоматического обслуживания, она запрашивает возврат в спящий режим.

Все необходимые взаимодействия с пользователем, связанные с действиями, такими как Настройка, выполняются за пределами автоматического обслуживания.

**Режим, инициированный пользователем**

Если пользователям необходимо подготовиться к командировке, предполагается, что в течение длительного времени заряжается заряд батареи или вы хотите оптимизировать производительность и скорость реагирования, у них есть возможность запуска автоматического обслуживания по требованию. Пользователи могут настраивать атрибуты автоматического обслуживания, включая автоматическое расписание выполнения. Они могут просматривать текущее состояние автоматического выполнения обслуживания, а также могут прекращать автоматическое обслуживание при необходимости.

**Автоматическая отмена**

Автоматическое обслуживание автоматически прекращает выполнение действий по обслуживанию, если пользователь начинает взаимодействовать с компьютером. Действие обслуживания возобновится, когда система вернется в состояние простоя.

> [!Note]  
> Все действия в автоматическом обслуживании должны поддерживать остановку в течение 2 секунд или меньше. Пользователь должен получать уведомления о том, что действие было остановлено.

 

**Крайние сроки и уведомление**

Критическое действие обслуживания должно выполняться в заранее определенном временном окне. Если критические задачи не удалось запустить в течение заданного времени, автоматическое обслуживание начнется автоматически при следующей доступной возможности простоя системы. Однако если состояние задачи остается за крайний срок, автоматическое обслуживание сообщит пользователю об этом действии и предоставит возможность ручного выполнения автоматического обслуживания. Будут выполнены все задачи, запланированные на обслуживание, хотя наиболее несущественное выполнение задач имеет приоритет. Это действие может повлиять на скорость реагирования и производительность системы. Таким образом, автоматическое обслуживание будет уведомлять пользователя о том, что выполняется критическое действие обслуживания.

**Enterprise элемент управления**

Enterprise ит-специалисты должны уметь определять, когда выполняется автоматическое обслуживание в своих Windowsных системах, применять это расписание через стандартизированные интерфейсы управления и получать данные о событиях состояния попыток автоматического обслуживания. Кроме того, ИТ-специалисты должны иметь возможность удаленного вызова определенной операции автоматического обслуживания через стандартные интерфейсы управления. При каждом выполнении автоматического обслуживания, отчетов о состоянии, включая уведомления, если автоматическое обслуживание не удалось выполнить, так как пользователь вручную приостановил действие, выполняется. ИТ-специалистам следует рассмотреть возможность перемещения сценариев входа в автоматическое обслуживание, чтобы ускорить процесс входа пользователя.

## <a name="creating-an-automatic-maintenance-task"></a>Создание задачи автоматического обслуживания

В этом разделе подробно описано, как разработчики могут создавать задачи с помощью определения задачи в языке XML или C. Помните, что действие обслуживания не должно запускать пользовательский интерфейс, требующий взаимодействия с пользователем, так как автоматическое обслуживание выполняется полностью без вмешательства пользователя и выполняется, когда пользователь отсутствует. В действительности, если пользователь взаимодействует с компьютером во время автоматического обслуживания, все задачи в процессе будут завершаться до следующего периода простоя.

**Использование XML**

Планировщик задач включает встроенное средство командной строки schtasks.exe, которое может импортировать определение задачи в формате XML. Схема для определения задачи описана в статье https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx . Ниже приведен пример задачи автоматического обслуживания, определенной в XML.


```
<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.4" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2011-07-01T11:34:31</Date>
    <Author>IT Deptartment</Author>
  </RegistrationInfo>
  <Principals>
    <Principal id="Author">
      <RunLevel>LeastPrivilege</RunLevel>
      <GroupId>NT AUTHORITY\SYSTEM</GroupId>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <MaintenanceSettings>
      <Period>P2D</Period>
      <Deadline>P14D</Deadline>
    </MaintenanceSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <DisallowStartOnRemoteAppSession>false</DisallowStartOnRemoteAppSession>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>cmd</Command>
      <Arguments>/c timeout -t 60</Arguments>
    </Exec>
  </Actions>
</Task> 
```



чтобы сохранить задачу на Windows компьютере, сохраните приведенный выше XML как текстовый файл и используйте следующую командную строку:

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**Использование C**

Задачу автоматического обслуживания также можно создать с помощью кода на языке C. Ниже приведен пример кода, который можно использовать для настройки параметров автоматического обслуживания задачи.


```
/********************************************************************
This sample creates a maintenance task to start cmd window during maintenance opportunities with periodicity of 2 days and deadline 0f 14 days.
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
//#pragma comment(lib, "taskschd.lib")
//#pragma comment(lib, "comsupp.lib")

int __cdecl 
MainteanceTask( )
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr;

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"MaintenanceTask";

    ITaskService *pService = NULL;
    ITaskFolder *pRootFolder = NULL;
    ITaskDefinition *pTask = NULL;
    ITaskSettings *pSettings = NULL;
    IRegistrationInfo *pRegInfo= NULL;
    IPrincipal *pPrincipal = NULL;
    ITaskSettings3 *pSettings3 = NULL;
    IMaintenanceSettings* pMaintenanceSettings = NULL;
    IActionCollection *pActionCollection = NULL;
    IAction *pAction = NULL;
    IExecAction *pExecAction = NULL;
    IRegisteredTask *pRegisteredTask = NULL;

    wprintf(L"\nCreate Maintenance Task %ws", wszTaskName );

    hr = CoInitializeEx( NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity( NULL,
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
        wprintf(L"\nCoInitializeSecurity failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to create an instance of ITaskService: %x", hr);
        goto CleanUp;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(), _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        wprintf(L"\nITaskService::Connect failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Root folder pointer: %x", hr );
        goto CleanUp;
    }
    
    //  If the same task exists, remove it.
    ( void ) pRootFolder->DeleteTask( _bstr_t(wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    hr = pService->NewTask( 0, &pTask );
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to CoCreate an instance of the TaskService class: %x", hr);
        goto CleanUp;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get identification pointer: %x", hr );
        goto CleanUp;
    }
    
    hr = pRegInfo->put_Author( _bstr_t(L"Author Name") );    
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put identification info: %x", hr );
        goto CleanUp;
    }

    // The task needs to grant explicit FRFX to LOCAL SERVICE (A;;FRFX;;;LS)
    hr = pRegInfo->put_SecurityDescriptor( _variant_t(L"D:P(A;;FA;;;BA)(A;;FA;;;SY)(A;;FRFX;;;LS)") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put security descriptor: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get principal pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put principal info: %x", hr );
        goto CleanUp;
    }  

    //  ------------------------------------------------------
    //  Create the settings for the task
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get settings pointer: %x", hr );
        goto CleanUp;
    }

    hr = pSettings->QueryInterface( __uuidof(ITaskSettings3), (void**) &pSettings3 );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot query ITaskSettings3 interface: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->put_UseUnifiedSchedulingEngine( VARIANT_TRUE );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_UseUnifiedSchedulingEngine: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->CreateMaintenanceSettings( &pMaintenanceSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot CreateMaintenanceSettings: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Period ( _bstr_t(L"P2D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Deadline ( _bstr_t(L"P14D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Task collection pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Create the action, specifying that it is an executable action.
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot create the action: %x", hr );
        goto CleanUp;
    }

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( IID_IExecAction, (void**) &pExecAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nQueryInterface call failed for IExecAction: %x", hr );
        goto CleanUp;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t(L"cmd") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put action path: %x", hr );
        goto CleanUp;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t(wszTaskName),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        wprintf(L"\nError saving the Task : %x", hr );
        goto CleanUp;
    }
    
    wprintf(L"\nSuccess!\n----------------------------------" );

CleanUp:

    if ( pService != NULL ) pService->Release();
    if ( pRootFolder != NULL ) pRootFolder->Release();
    if ( pTask != NULL ) pTask->Release();
    if ( pSettings != NULL ) pSettings->Release();
    if ( pRegInfo != NULL ) pRegInfo->Release();
    if ( pPrincipal != NULL ) pPrincipal->Release();
    if ( pSettings3 != NULL ) pSettings3->Release();
    if ( pMaintenanceSettings != NULL ) pMaintenanceSettings->Release();
    if ( pActionCollection != NULL ) pActionCollection->Release();
    if ( pAction != NULL ) pAction->Release();
    if ( pExecAction != NULL ) pExecAction->Release();
    if ( pRegisteredTask != NULL ) pRegisteredTask->Release();

    CoUninitialize();
    return SUCCEEDED ( hr ) ? 0 : 1;
}
```



## <a name="validating-tasks"></a>Проверка задач

Убедитесь, что задача успешно создана и выполняется как часть обслуживания.

**Проверка создания задачи**

Используйте эту командную строку, чтобы экспортировать определение задачи в файл и убедиться, что определение задачи должно быть ожидаемым:

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**Проверка выполнения задачи**

Запустите эту командную строку, чтобы запустить задачу и проверить, что планировщик задач пользовательский интерфейс (тасксчд. msc) показывает, что задача выполнена:

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>Ресурсы

-   [Расписание задач 2,0](/previous-versions/bb756979(v=msdn.10))

 

 