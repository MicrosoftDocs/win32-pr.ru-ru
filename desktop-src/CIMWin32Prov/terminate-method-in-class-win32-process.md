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
# <a name="terminate-method-of-the-win32_process-class"></a><span data-ttu-id="18fa6-103">Метод Terminate \_ класса процесса Win32</span><span class="sxs-lookup"><span data-stu-id="18fa6-103">Terminate method of the Win32\_Process class</span></span>

<span data-ttu-id="18fa6-104">Метод **Terminate** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) завершает процесс и все его потоки.</span><span class="sxs-lookup"><span data-stu-id="18fa6-104">The **Terminate** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method terminates a process and all of its threads.</span></span>

<span data-ttu-id="18fa6-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="18fa6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="18fa6-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="18fa6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="18fa6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18fa6-107">Syntax</span></span>


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a><span data-ttu-id="18fa6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="18fa6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18fa6-109">*Причина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18fa6-109">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18fa6-110">Код выхода для процесса и для всех потоков, завершенных в результате этого вызова.</span><span class="sxs-lookup"><span data-stu-id="18fa6-110">Exit code for the process and for all of the threads terminated as a result of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18fa6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18fa6-111">Return value</span></span>

<span data-ttu-id="18fa6-112">Возвращает значение 0 (нуль), если процесс был успешно завершен, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="18fa6-112">Returns a value of 0 (zero) if the process was successfully terminated, and any other number to indicate an error.</span></span> <span data-ttu-id="18fa6-113">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="18fa6-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="18fa6-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="18fa6-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="18fa6-115">**Успешное завершение** (0)</span><span class="sxs-lookup"><span data-stu-id="18fa6-115">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18fa6-116">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="18fa6-116">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18fa6-117">**Недостаточно прав доступа** (3)</span><span class="sxs-lookup"><span data-stu-id="18fa6-117">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18fa6-118">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="18fa6-118">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="18fa6-119">**Путь не найден** (9)</span><span class="sxs-lookup"><span data-stu-id="18fa6-119">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="18fa6-120">**Недопустимый параметр** (21)</span><span class="sxs-lookup"><span data-stu-id="18fa6-120">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="18fa6-121">**Другие** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="18fa6-121">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="18fa6-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18fa6-122">Remarks</span></span>

<span data-ttu-id="18fa6-123">**Обзор**</span><span class="sxs-lookup"><span data-stu-id="18fa6-123">**Overview**</span></span>

<span data-ttu-id="18fa6-124">Проблемы с компьютером часто возникают из-за процесса, который больше не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="18fa6-124">Computer problems are often due to a process that is no longer working as expected.</span></span> <span data-ttu-id="18fa6-125">Например, процесс может вызвать утечку памяти или перестать отвечать на вводимые пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="18fa6-125">For example, the process might be leaking memory, or it might have stopped responding to user input.</span></span> <span data-ttu-id="18fa6-126">При возникновении таких проблем процесс должен быть завершен.</span><span class="sxs-lookup"><span data-stu-id="18fa6-126">When problems such as these occur, the process must be terminated.</span></span> <span data-ttu-id="18fa6-127">Хотя это может показаться достаточно простой задачей, завершение процесса может усложнить несколько факторов:</span><span class="sxs-lookup"><span data-stu-id="18fa6-127">Although this might seem like a simple enough task, terminating a process can be complicated by several factors:</span></span>

-   <span data-ttu-id="18fa6-128">Процесс может быть завис и, следовательно, больше не реагирует на команды меню или клавиатуры для закрытия приложения.</span><span class="sxs-lookup"><span data-stu-id="18fa6-128">The process might be hung and therefore no longer responds to menu or keyboard commands for closing the application.</span></span> <span data-ttu-id="18fa6-129">Это делает все, но невозможным для обычного пользователя закрыть приложение и завершить процесс.</span><span class="sxs-lookup"><span data-stu-id="18fa6-129">This makes it all but impossible for the typical user to dismiss the application and terminate the process.</span></span>
-   <span data-ttu-id="18fa6-130">Процесс может быть потерян.</span><span class="sxs-lookup"><span data-stu-id="18fa6-130">The process might be orphaned.</span></span> <span data-ttu-id="18fa6-131">Например, скрипт может создать экземпляр Word, а затем выйти, не уничтожая этот экземпляр.</span><span class="sxs-lookup"><span data-stu-id="18fa6-131">For example, a script might create an instance of Word and then exit without destroying that instance.</span></span> <span data-ttu-id="18fa6-132">По сути, Word продолжает работать на компьютере, даже если пользовательский интерфейс не виден.</span><span class="sxs-lookup"><span data-stu-id="18fa6-132">In effect, Word remains running on the computer, even though no user interface is visible.</span></span> <span data-ttu-id="18fa6-133">Поскольку пользовательский интерфейс отсутствует, для завершения процесса нет доступных команд меню и клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="18fa6-133">Because there is no user interface, there are no menu or keyboard commands available to terminate the process.</span></span>
-   <span data-ttu-id="18fa6-134">Возможно, вы не узнаете, какой процесс необходимо завершить.</span><span class="sxs-lookup"><span data-stu-id="18fa6-134">You might not know which process needs to be terminated.</span></span> <span data-ttu-id="18fa6-135">Например, может потребоваться завершить работу всех программ, превышающих указанный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="18fa6-135">For example, you might want to terminate all programs that are exceeding a specified amount of memory.</span></span>
-   <span data-ttu-id="18fa6-136">Поскольку диспетчер задач позволяет прерывать только созданные процессы, возможно, не удастся завершить процесс, даже если вы являетесь администратором компьютера.</span><span class="sxs-lookup"><span data-stu-id="18fa6-136">Because Task Manager allows you to terminate only those processes that you created, you might not be able to terminate a process, even if you are an administrator on the computer.</span></span>

<span data-ttu-id="18fa6-137">Сценарии позволяют преодолеть все эти потенциальные препятствия, предоставляя вам значительное административное управление компьютерами.</span><span class="sxs-lookup"><span data-stu-id="18fa6-137">Scripts enable you to overcome all of these potential obstacles, providing you with considerable administrative control over your computers.</span></span> <span data-ttu-id="18fa6-138">Например, если вы подозреваете, что пользователи играют игры, запрещенные в Организации, можно легко написать сценарий для подключения к каждому компьютеру, определить, работает ли игра, и немедленно завершить процесс.</span><span class="sxs-lookup"><span data-stu-id="18fa6-138">For example, if you suspect users are playing games that have been prohibited in your organization, you can easily write a script to connect to each computer, identify whether the game is running, and immediately terminate the process.</span></span>

<span data-ttu-id="18fa6-139">**Использование метода Terminate**</span><span class="sxs-lookup"><span data-stu-id="18fa6-139">**Using the Terminate Method**</span></span>

<span data-ttu-id="18fa6-140">Процесс можно завершить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="18fa6-140">You can terminate a process by:</span></span>

-   <span data-ttu-id="18fa6-141">Завершение процесса, выполняющегося в данный момент.</span><span class="sxs-lookup"><span data-stu-id="18fa6-141">Terminating a process that is currently running.</span></span> <span data-ttu-id="18fa6-142">Например, может потребоваться завершить диагностическую программу, работающую на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="18fa6-142">For example, you might need to terminate a diagnostic program running on a remote computer.</span></span> <span data-ttu-id="18fa6-143">Если нет способа удаленного управления приложением, можно просто завершить процесс для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="18fa6-143">If there is no way to control the application remotely, you can simply terminate the process for that application.</span></span>
-   <span data-ttu-id="18fa6-144">Предотвращение запуска процесса на первом месте.</span><span class="sxs-lookup"><span data-stu-id="18fa6-144">Preventing a process from running in the first place.</span></span> <span data-ttu-id="18fa6-145">Постоянно отслеживая процесс создания процессов на компьютере, вы можете определять и мгновенно завершать любой процесс сразу после его запуска.</span><span class="sxs-lookup"><span data-stu-id="18fa6-145">By continuously monitoring process creation on a computer, you can identify and instantly terminate any process as soon as it starts.</span></span> <span data-ttu-id="18fa6-146">Это гарантирует, что определенные приложения (такие как программы, которые загружают большие файлы мультимедиа через Интернет) никогда не запускаются на определенных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="18fa6-146">This provides one method of ensuring that certain applications (such as programs that download large media files over the Internet) are never run on certain computers.</span></span>

> [!Note]  
> <span data-ttu-id="18fa6-147">Групповая политика также можно использовать для ограничения программ, выполняемых на компьютере.</span><span class="sxs-lookup"><span data-stu-id="18fa6-147">Group Policy can also be used to restrict the programs that run on a computer.</span></span> <span data-ttu-id="18fa6-148">Однако групповая политика может ограничивать только программы, выполняемые с помощью меню «Пуск» или проводника Windows; Он не влияет на программы, запущенные с помощью других средств, таких как Командная строка.</span><span class="sxs-lookup"><span data-stu-id="18fa6-148">However, Group Policy can restrict only the programs run using either the Start menu or Windows Explorer; it has no effect on programs started using other means, such as the command line.</span></span> <span data-ttu-id="18fa6-149">WMI, напротив, может препятствовать выполнению процесса независимо от того, как был запущен процесс.</span><span class="sxs-lookup"><span data-stu-id="18fa6-149">By contrast, WMI can prevent a process from running regardless of how the process was started.</span></span>

 

<span data-ttu-id="18fa6-150">**Завершение процесса, владельцем которого вы не владеете**</span><span class="sxs-lookup"><span data-stu-id="18fa6-150">**Terminating a Process You Do Not Own**</span></span>

<span data-ttu-id="18fa6-151">Чтобы завершить процесс, который не владеет, включите привилегию **SeDebugPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="18fa6-151">To terminate a process that you do not own, enable the **SeDebugPrivilege** privilege.</span></span> <span data-ttu-id="18fa6-152">В VBScript эту привилегию можно включить с помощью следующих строк кода:</span><span class="sxs-lookup"><span data-stu-id="18fa6-152">In VBScript, you can enable this privilege with the following lines of code:</span></span>


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



<span data-ttu-id="18fa6-153">Дополнительные сведения о включении этой привилегии в C++ см. [в разделе Включение и отключение привилегий в c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="18fa6-153">For more information about enabling this privilege in C++, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

## <a name="examples"></a><span data-ttu-id="18fa6-154">Примеры</span><span class="sxs-lookup"><span data-stu-id="18fa6-154">Examples</span></span>

<span data-ttu-id="18fa6-155">Образец кода [завершения выполнения процесса на нескольких серверах](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) PowerShell в коллекции TechNet завершает процесс, работающий на одном или нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="18fa6-155">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) PowerShell code sample on TechNet Gallery terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="18fa6-156">Следующий пример сценария VBScript завершает процесс, в котором выполняется приложение, Diagnose.exe в данный момент.</span><span class="sxs-lookup"><span data-stu-id="18fa6-156">The following VBScript sample terminates the process in which the application Diagnose.exe is currently running.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



<span data-ttu-id="18fa6-157">Следующий пример VBScript использует временный потребитель событий для завершения процесса сразу после его запуска.</span><span class="sxs-lookup"><span data-stu-id="18fa6-157">The following VBScript sample uses a temporary event consumer to terminate a process as soon as it starts.</span></span>


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



<span data-ttu-id="18fa6-158">Следующий пример кода VBScript подключается к удаленному компьютеру и прерывает Notepad.exe на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="18fa6-158">The following VBScript code example connects to a remote computer and terminates Notepad.exe on that computer.</span></span>


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



<span data-ttu-id="18fa6-159">Следующий код C++ завершает процесс Notepad.exe на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="18fa6-159">The following C++ code terminates the Notepad.exe process on the local computer.</span></span> <span data-ttu-id="18fa6-160">Укажите обработчик процесса или (идентификатор процесса) в коде, чтобы завершить процесс.</span><span class="sxs-lookup"><span data-stu-id="18fa6-160">Specify a or process handle (process id) in the code to terminate the process.</span></span> <span data-ttu-id="18fa6-161">Это значение можно найти в свойстве Handle класса [**\_ процесса Win32**](win32-process.md) (ключевое свойство для класса).</span><span class="sxs-lookup"><span data-stu-id="18fa6-161">This value can be found in the handle property in the [**Win32\_Process**](win32-process.md) class (the key property for the class).</span></span> <span data-ttu-id="18fa6-162">Указав значение для свойства Handle, вы предоставляете путь к экземпляру класса, который необходимо завершить.</span><span class="sxs-lookup"><span data-stu-id="18fa6-162">By specifying a value for the Handle property, you are supplying a path to the instance of the class that you want to terminate.</span></span> <span data-ttu-id="18fa6-163">Дополнительные сведения о подключении к удаленному компьютеру см. в разделе [пример. получение данных WMI с удаленного компьютера](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="18fa6-163">For more information about connecting to a remote computer, see [Example: Getting WMI Data From a Remote Computer](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="18fa6-164">Требования</span><span class="sxs-lookup"><span data-stu-id="18fa6-164">Requirements</span></span>



| <span data-ttu-id="18fa6-165">Требование</span><span class="sxs-lookup"><span data-stu-id="18fa6-165">Requirement</span></span> | <span data-ttu-id="18fa6-166">Значение</span><span class="sxs-lookup"><span data-stu-id="18fa6-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18fa6-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18fa6-167">Minimum supported client</span></span><br/> | <span data-ttu-id="18fa6-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18fa6-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18fa6-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18fa6-169">Minimum supported server</span></span><br/> | <span data-ttu-id="18fa6-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18fa6-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18fa6-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18fa6-171">Namespace</span></span><br/>                | <span data-ttu-id="18fa6-172">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="18fa6-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18fa6-173">MOF</span><span class="sxs-lookup"><span data-stu-id="18fa6-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18fa6-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18fa6-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18fa6-175">DLL</span><span class="sxs-lookup"><span data-stu-id="18fa6-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18fa6-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18fa6-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18fa6-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18fa6-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="18fa6-178">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18fa6-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="18fa6-179">**\_Процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="18fa6-179">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="18fa6-180">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="18fa6-180">WMI Tasks: Performance Monitoring</span></span>](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[<span data-ttu-id="18fa6-181">Задачи WMI: процессы</span><span class="sxs-lookup"><span data-stu-id="18fa6-181">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

