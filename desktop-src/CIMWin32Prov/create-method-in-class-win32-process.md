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
# <a name="create-method-of-the-win32_process-class"></a>Метод Create \_ класса Process Win32

Метод **создания** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) создает новый процесс.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Командная строка* \[ окне\]
</dt> <dd>

Командная строка для выполнения. Система добавляет в командную строку символ null, при необходимости обрезая строку, чтобы указать, какой файл фактически использовался.

</dd> <dt>

*Куррентдиректори* \[ окне\]
</dt> <dd>

Текущий диск и каталог для дочернего процесса. Строка требует, чтобы текущий каталог разрешался в известном пути. Пользователь может указать абсолютный путь или путь относительно текущего рабочего каталога. Если этот параметр имеет **значение NULL**, то новый процесс будет иметь тот же путь, что и вызывающий процесс. Этот параметр предоставляется в основном для оболочек, которые должны запускать приложение и указывать исходный диск и рабочий каталог приложения.

</dd> <dt>

*Процессстартупинформатион* \[ окне\]
</dt> <dd>

Конфигурация запуска процесса Windows. Дополнительные сведения см. в разделе [**Win32 \_ процессстартуп**](win32-processstartup.md).

</dd> <dt>

Идентификатор *процесса* \[ заполняет\]
</dt> <dd>

Глобальный идентификатор процесса, который можно использовать для идентификации процесса. Значение допустимо с момента создания процесса до момента завершения процесса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (ноль), если процесс был успешно создан, и любое другое число для указания ошибки. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

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

Чтобы настроить процесс перед вызовом этого метода, можно создать экземпляр класса [**Win32 \_ процессстартуп**](win32-processstartup.md) .

Полный путь должен быть указан в случаях, когда запускаемая программа не находится в пути поиска Winmgmt.exe. Если вновь созданный процесс пытается взаимодействовать с объектами в целевой системе без соответствующих прав доступа, он завершается без уведомления для этого метода.

По соображениям безопасности метод **Win32 \_ . Create** не может использоваться для удаленного запуска интерактивного процесса.

Процессы, созданные с помощью метода **\_ процесса Win32. Create** , ограничиваются объектом задания, если не задан флаг **Create \_ бреакавай \_ FROM \_ Job** . Дополнительные сведения см. в разделе [**Win32 \_ процессстартуп**](win32-processstartup.md) and [**\_ \_ провидерхосткуотаконфигуратион**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).

## <a name="examples"></a>Примеры

В следующем примере VBScript показано, как вызвать метод CIM, как если бы он был методом автоматизации SWbemObject.


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



В следующем примере Perl показано, как вызвать метод CIM, как если бы он был методом автоматизации SWbemObject.


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



В следующем примере кода VBScript создается процесс «блокнот» на локальном компьютере. [**Win32 \_ Процессстартуп**](win32-processstartup.md) используется для настройки параметров процесса.


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

[Задачи WMI: процессы](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

