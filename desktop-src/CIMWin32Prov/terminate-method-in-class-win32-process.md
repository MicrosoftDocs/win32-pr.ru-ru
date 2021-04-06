---
description: Прекращение&\# 32; Метод класса WMI завершает процесс и все его потоки.
ms.assetid: 6c6b27d4-cf9b-42d7-9136-42641ea56ee8
ms.tgt_platform: multiple
title: Метод Terminate класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Terminate
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 00300ca9656c3b732b9c294aeba9a6c626ac6e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990450"
---
# <a name="terminate-method-of-the-win32_process-class"></a>Метод Terminate \_ класса процесса Win32

Метод **Terminate** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) завершает процесс и все его потоки.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Причина* \[ окне\]
</dt> <dd>

Код выхода для процесса и для всех потоков, завершенных в результате этого вызова.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль), если процесс был успешно завершен, и любое другое число для указания ошибки. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешное завершение** (0)
</dt> <dt>

**Отказано в доступе** (2)
</dt> <dt>

**Недостаточно прав доступа** (3)
</dt> <dt>

**Неизвестный сбой** (8)
</dt> <dt>

**Путь не найден** (9)
</dt> <dt>

**Недопустимый параметр** (21)
</dt> <dt>

**Другие** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Комментарии

**Обзор**

Проблемы с компьютером часто возникают из-за процесса, который больше не работает должным образом. Например, процесс может вызвать утечку памяти или перестать отвечать на вводимые пользователем данные. При возникновении таких проблем процесс должен быть завершен. Хотя это может показаться достаточно простой задачей, завершение процесса может усложнить несколько факторов:

-   Процесс может быть завис и, следовательно, больше не реагирует на команды меню или клавиатуры для закрытия приложения. Это делает все, но невозможным для обычного пользователя закрыть приложение и завершить процесс.
-   Процесс может быть потерян. Например, скрипт может создать экземпляр Word, а затем выйти, не уничтожая этот экземпляр. По сути, Word продолжает работать на компьютере, даже если пользовательский интерфейс не виден. Поскольку пользовательский интерфейс отсутствует, для завершения процесса нет доступных команд меню и клавиатуры.
-   Возможно, вы не узнаете, какой процесс необходимо завершить. Например, может потребоваться завершить работу всех программ, превышающих указанный объем памяти.
-   Поскольку диспетчер задач позволяет прерывать только созданные процессы, возможно, не удастся завершить процесс, даже если вы являетесь администратором компьютера.

Сценарии позволяют преодолеть все эти потенциальные препятствия, предоставляя вам значительное административное управление компьютерами. Например, если вы подозреваете, что пользователи играют игры, запрещенные в Организации, можно легко написать сценарий для подключения к каждому компьютеру, определить, работает ли игра, и немедленно завершить процесс.

**Использование метода Terminate**

Процесс можно завершить следующим образом:

-   Завершение процесса, выполняющегося в данный момент. Например, может потребоваться завершить диагностическую программу, работающую на удаленном компьютере. Если нет способа удаленного управления приложением, можно просто завершить процесс для этого приложения.
-   Предотвращение запуска процесса на первом месте. Постоянно отслеживая процесс создания процессов на компьютере, вы можете определять и мгновенно завершать любой процесс сразу после его запуска. Это гарантирует, что определенные приложения (такие как программы, которые загружают большие файлы мультимедиа через Интернет) никогда не запускаются на определенных компьютерах.

> [!Note]  
> Групповая политика также можно использовать для ограничения программ, выполняемых на компьютере. Однако групповая политика может ограничивать только программы, выполняемые с помощью меню «Пуск» или проводника Windows; Он не влияет на программы, запущенные с помощью других средств, таких как Командная строка. WMI, напротив, может препятствовать выполнению процесса независимо от того, как был запущен процесс.

 

**Завершение процесса, владельцем которого вы не владеете**

Чтобы завершить процесс, который не владеет, включите привилегию **SeDebugPrivilege** . В VBScript эту привилегию можно включить с помощью следующих строк кода:


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



Дополнительные сведения о включении этой привилегии в C++ см. [в разделе Включение и отключение привилегий в c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

## <a name="examples"></a>Примеры

Образец кода [завершения выполнения процесса на нескольких серверах](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) PowerShell в коллекции TechNet завершает процесс, работающий на одном или нескольких компьютерах.

Следующий пример сценария VBScript завершает процесс, в котором выполняется приложение, Diagnose.exe в данный момент.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



Следующий пример VBScript использует временный потребитель событий для завершения процесса сразу после его запуска.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
 & " WITHIN 1 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 If objLatestProcess.TargetInstance.Name = "Download.exe" Then
 objLatestProcess.TargetInstance.Terminate()
 End If
Loop
```



Следующий пример кода VBScript подключается к удаленному компьютеру и прерывает Notepad.exe на этом компьютере.


```VB
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
strUser = InputBox("Enter user name") 
strPassword = InputBox("Enter password") 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
    "root\CIMV2", _ 
    strUser, _ 
    strPassword, _ 
    "MS_409", _ 
    "ntlmdomain:" + strDomain) 
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'notepad.exe'")
For Each objProcess in colProcessList
    objProcess.Terminate()
Next
```



Следующий код C++ завершает процесс Notepad.exe на локальном компьютере. Укажите обработчик процесса или (идентификатор процесса) в коде, чтобы завершить процесс. Это значение можно найти в свойстве Handle класса [**\_ процесса Win32**](win32-process.md) (ключевое свойство для класса). Указав значение для свойства Handle, вы предоставляете путь к экземпляру класса, который необходимо завершить. Дополнительные сведения о подключении к удаленному компьютеру см. в разделе [пример. получение данных WMI с удаленного компьютера](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
             << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------
    // Note: If you are using Windows 2000, specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();
        pSvc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels for the proxy ------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // Set up to call the Win32_Process::Create method
    BSTR ClassName = SysAllocString(L"Win32_Process");

    /* YOU NEED TO CHANGE THE NUMBER VALUE OF THE HANDLE 
       (PROCESS ID) TO THE CORRECT VALUE OF THE PROCESS YOU 
       ARE TRYING TO TERMINATE (this provides a path to
       the class instance you are tying to terminate). */
    BSTR ClassNameInstance = SysAllocString(
        L"Win32_Process.Handle=\"3168\"");

    _bstr_t MethodName = (L"Terminate");
    BSTR ParameterName = SysAllocString(L"Reason");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    IWbemClassObject* pOutMethod = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, &pOutMethod);

    if (FAILED(hres))
    {
        cout << "Could not get the method. Error code = 0x" 
             << hex << hres << endl;
    }

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT pcVal;
    VariantInit(&pcVal);
    V_VT(&pcVal) = VT_I4;

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"Reason", 0,
        &pcVal, 0);

    // Execute Method
    hres = pSvc->ExecMethod(ClassNameInstance, MethodName, 0,
    NULL, pClassInstance, NULL, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&pcVal);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pInParamsDefinition->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;           // Program has failed.
    }


    // Clean up
    //--------------------------
    VariantClear(&pcVal);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pInParamsDefinition->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Процесс Win32**](win32-process.md)
</dt> <dt>

[Задачи WMI: Мониторинг производительности](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[Задачи WMI: процессы](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

