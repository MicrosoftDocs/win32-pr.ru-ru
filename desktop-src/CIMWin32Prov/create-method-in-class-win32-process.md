---
description: Создание&\# 8194; Метод класса WMI создает новый процесс.
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Метод Create класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655817"
---
# <a name="create-method-of-the-win32_process-class"></a><span data-ttu-id="353ae-103">Метод Create \_ класса Process Win32</span><span class="sxs-lookup"><span data-stu-id="353ae-103">Create method of the Win32\_Process class</span></span>

<span data-ttu-id="353ae-104">Метод **создания** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) создает новый процесс.</span><span class="sxs-lookup"><span data-stu-id="353ae-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new process.</span></span>

<span data-ttu-id="353ae-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="353ae-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="353ae-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="353ae-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="353ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="353ae-107">Syntax</span></span>


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a><span data-ttu-id="353ae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="353ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="353ae-109">*Командная строка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="353ae-109">*CommandLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="353ae-110">Командная строка для выполнения.</span><span class="sxs-lookup"><span data-stu-id="353ae-110">Command line to execute.</span></span> <span data-ttu-id="353ae-111">Система добавляет в командную строку символ null, при необходимости обрезая строку, чтобы указать, какой файл фактически использовался.</span><span class="sxs-lookup"><span data-stu-id="353ae-111">The system adds a null character to the command line, trimming the string if necessary, to indicate which file was actually used.</span></span>

</dd> <dt>

<span data-ttu-id="353ae-112">*Куррентдиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="353ae-112">*CurrentDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="353ae-113">Текущий диск и каталог для дочернего процесса.</span><span class="sxs-lookup"><span data-stu-id="353ae-113">Current drive and directory for the child process.</span></span> <span data-ttu-id="353ae-114">Строка требует, чтобы текущий каталог разрешался в известном пути.</span><span class="sxs-lookup"><span data-stu-id="353ae-114">The string requires that the current directory resolves to a known path.</span></span> <span data-ttu-id="353ae-115">Пользователь может указать абсолютный путь или путь относительно текущего рабочего каталога.</span><span class="sxs-lookup"><span data-stu-id="353ae-115">A user can specify an absolute path or a path relative to the current working directory.</span></span> <span data-ttu-id="353ae-116">Если этот параметр имеет **значение NULL**, то новый процесс будет иметь тот же путь, что и вызывающий процесс.</span><span class="sxs-lookup"><span data-stu-id="353ae-116">If this parameter is **NULL**, the new process will have the same path as the calling process.</span></span> <span data-ttu-id="353ae-117">Этот параметр предоставляется в основном для оболочек, которые должны запускать приложение и указывать исходный диск и рабочий каталог приложения.</span><span class="sxs-lookup"><span data-stu-id="353ae-117">This option is provided primarily for shells that must start an application and specify the application's initial drive and working directory.</span></span>

</dd> <dt>

<span data-ttu-id="353ae-118">*Процессстартупинформатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="353ae-118">*ProcessStartupInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="353ae-119">Конфигурация запуска процесса Windows.</span><span class="sxs-lookup"><span data-stu-id="353ae-119">The startup configuration of a Windows process.</span></span> <span data-ttu-id="353ae-120">Дополнительные сведения см. в разделе [**Win32 \_ процессстартуп**](win32-processstartup.md).</span><span class="sxs-lookup"><span data-stu-id="353ae-120">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md).</span></span>

</dd> <dt>

<span data-ttu-id="353ae-121">Идентификатор *процесса* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="353ae-121">*ProcessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="353ae-122">Глобальный идентификатор процесса, который можно использовать для идентификации процесса.</span><span class="sxs-lookup"><span data-stu-id="353ae-122">Global process identifier that can be used to identify a process.</span></span> <span data-ttu-id="353ae-123">Значение допустимо с момента создания процесса до момента завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="353ae-123">The value is valid from the time the process is created until the time the process is terminated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="353ae-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="353ae-124">Return value</span></span>

<span data-ttu-id="353ae-125">Возвращает значение 0 (ноль), если процесс был успешно создан, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="353ae-125">Returns a value of 0 (zero) if the process was successfully created, and any other number to indicate an error.</span></span> <span data-ttu-id="353ae-126">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="353ae-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="353ae-127">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="353ae-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="353ae-128">**Успешное завершение** (0)</span><span class="sxs-lookup"><span data-stu-id="353ae-128">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="353ae-129">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="353ae-129">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="353ae-130">**Недостаточно прав доступа** (3)</span><span class="sxs-lookup"><span data-stu-id="353ae-130">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="353ae-131">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="353ae-131">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="353ae-132">**Путь не найден** (9)</span><span class="sxs-lookup"><span data-stu-id="353ae-132">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="353ae-133">**Недопустимый параметр** (21)</span><span class="sxs-lookup"><span data-stu-id="353ae-133">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="353ae-134">**Другие** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="353ae-134">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="353ae-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="353ae-135">Remarks</span></span>

<span data-ttu-id="353ae-136">Чтобы настроить процесс перед вызовом этого метода, можно создать экземпляр класса [**Win32 \_ процессстартуп**](win32-processstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="353ae-136">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process before calling this method.</span></span>

<span data-ttu-id="353ae-137">Полный путь должен быть указан в случаях, когда запускаемая программа не находится в пути поиска Winmgmt.exe.</span><span class="sxs-lookup"><span data-stu-id="353ae-137">A fully qualified path must be specified in cases where the program to be launched is not in the search path of Winmgmt.exe.</span></span> <span data-ttu-id="353ae-138">Если вновь созданный процесс пытается взаимодействовать с объектами в целевой системе без соответствующих прав доступа, он завершается без уведомления для этого метода.</span><span class="sxs-lookup"><span data-stu-id="353ae-138">If the newly created process attempts to interact with objects on the target system without the appropriate access privileges, it is terminated without notification to this method.</span></span>

<span data-ttu-id="353ae-139">По соображениям безопасности метод **Win32 \_ . Create** не может использоваться для удаленного запуска интерактивного процесса.</span><span class="sxs-lookup"><span data-stu-id="353ae-139">For security reasons the **Win32\_Process.Create** method cannot be used to start an interactive process remotely.</span></span>

<span data-ttu-id="353ae-140">Процессы, созданные с помощью метода **\_ процесса Win32. Create** , ограничиваются объектом задания, если не задан флаг **Create \_ бреакавай \_ FROM \_ Job** .</span><span class="sxs-lookup"><span data-stu-id="353ae-140">Processes created with the **Win32\_Process.Create** method are limited by the job object unless the **CREATE\_BREAKAWAY\_FROM\_JOB** flag is specified.</span></span> <span data-ttu-id="353ae-141">Дополнительные сведения см. в разделе [**Win32 \_ процессстартуп**](win32-processstartup.md) and [**\_ \_ провидерхосткуотаконфигуратион**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span><span class="sxs-lookup"><span data-stu-id="353ae-141">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md) and [**\_\_ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span></span>

## <a name="examples"></a><span data-ttu-id="353ae-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="353ae-142">Examples</span></span>

<span data-ttu-id="353ae-143">В следующем примере VBScript показано, как вызвать метод CIM, как если бы он был методом автоматизации SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="353ae-143">The following VBScript example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



<span data-ttu-id="353ae-144">В следующем примере Perl показано, как вызвать метод CIM, как если бы он был методом автоматизации SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="353ae-144">The following Perl example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="353ae-145">В следующем примере кода VBScript создается процесс «блокнот» на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="353ae-145">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="353ae-146">[**Win32 \_ Процессстартуп**](win32-processstartup.md) используется для настройки параметров процесса.</span><span class="sxs-lookup"><span data-stu-id="353ae-146">[**Win32\_ProcessStartup**](win32-processstartup.md) is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="353ae-147">Требования</span><span class="sxs-lookup"><span data-stu-id="353ae-147">Requirements</span></span>



| <span data-ttu-id="353ae-148">Требование</span><span class="sxs-lookup"><span data-stu-id="353ae-148">Requirement</span></span> | <span data-ttu-id="353ae-149">Значение</span><span class="sxs-lookup"><span data-stu-id="353ae-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="353ae-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="353ae-150">Minimum supported client</span></span><br/> | <span data-ttu-id="353ae-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="353ae-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="353ae-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="353ae-152">Minimum supported server</span></span><br/> | <span data-ttu-id="353ae-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="353ae-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="353ae-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="353ae-154">Namespace</span></span><br/>                | <span data-ttu-id="353ae-155">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="353ae-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="353ae-156">MOF</span><span class="sxs-lookup"><span data-stu-id="353ae-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="353ae-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="353ae-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="353ae-158">DLL</span><span class="sxs-lookup"><span data-stu-id="353ae-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="353ae-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="353ae-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="353ae-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="353ae-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="353ae-161">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="353ae-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="353ae-162">**\_Процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="353ae-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="353ae-163">Задачи WMI: процессы</span><span class="sxs-lookup"><span data-stu-id="353ae-163">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

