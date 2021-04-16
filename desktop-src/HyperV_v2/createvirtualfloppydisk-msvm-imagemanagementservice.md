---
description: Создает файл виртуального гибкого диска.
ms.assetid: C7B5712C-55DD-4784-8B2E-A8DE02E4CFD8
title: Метод Креатевиртуалфлоппидиск класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualFloppyDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 98781a4f72218ee61a4966dc76b21f7417353e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664041"
---
# <a name="createvirtualfloppydisk-method-of-the-msvm_imagemanagementservice-class"></a>Метод Креатевиртуалфлоппидиск \_ класса) мсвм

Создает файл виртуального гибкого диска.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateVirtualFloppyDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Путь* \[ окне\]
</dt> <dd>

Тип: **строка**

Полный путь, указывающий расположение нового файла.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**

Ссылка на задание (может иметь **значение NULL** , если задача завершена).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Этот метод может возвращать одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Сбой** (32768)
</dt> <dt>

**Отказано в доступе** (32769)
</dt> <dt>

**Не поддерживается** (32770)
</dt> <dt>

**Состояние неизвестно** (32771)
</dt> <dt>

**Время ожидания** (32772)
</dt> <dt>

**Недопустимый параметр** (32773)
</dt> <dt>

**Система используется** (32774)
</dt> <dt>

**Недопустимое состояние для этой операции** (32775)
</dt> <dt>

**Неверный тип данных** (32776)
</dt> <dt>

**Система недоступна** (32777)
</dt> <dt>

**Недостаточно памяти** (32778)
</dt> <dt>

**Файл не найден** (32779)
</dt> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

В следующем примере кода C# создается файл виртуального дисковода гибких дисков. Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class CreateVFD
    {
        static void CreateVirtualFlopy(string vhdPath)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

            ManagementBaseObject inParams = imageService.GetMethodParameters("CreateVirtualFloppyDisk");
            inParams["Path"] = vhdPath;
            ManagementBaseObject outParams = imageService.InvokeMethod("CreateVirtualFloppyDisk", inParams, null);
            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("{0} was created successfully.", inParams["Path"]);
                }
                else
                {
                    Console.WriteLine("Unable to create {0}", inParams["Path"]);
                }
            }

            inParams.Dispose();
            outParams.Dispose();
            imageService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 1)
            {
                Console.WriteLine("Usage: CreateVFD path");
                return;
            }
            CreateVirtualFlopy(args[0]);
        }
    }
}

```



В следующем примере Visual Basic Scripting Edition (VBScript) создается файл виртуального гибкого диска.


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096

const method = "CreateVirtualFloppyDisk"
Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vfdPath

    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("Select * from Msvm_ImageManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
       vfdPath = objArgs.Unnamed.Item(0)
    else
       WScript.Echo "usage: cscript CreateVFD.vbs VFDFilePath "
       WScript.Quit(1)
    end if

    if CreateVirtualFloppyDisk(vfdPath) then
        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "CreateVFD failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Execute CreateVirtualFloppyDisk method
'-----------------------------------------------------------------
Function CreateVirtualFloppyDisk(vfdPath)
    WriteLog Format1("Function CreateVirtualFloppyDisk({0})",  vfdPath)
    
    dim objInParam, objOutParams

    CreateVirtualFloppyDisk = false

    set objInParam = managementService.Methods_("CreateVirtualFloppyDisk").InParameters.SpawnInstance_()
    objInParam.Path = vfdPath

    set objOutParams = managementService.ExecMethod_("CreateVirtualFloppyDisk", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VHD {0} was created successfully", vfdPath)
            CreateVirtualFloppyDisk = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)
    WriteLog "Function WMIMethodStarted"
    
    dim wmiStatus
    
    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        else
            WriteLog Format2("Failed to create VFD {0} ConcreteJob with error {1}", vfdPath, wmiStatus)
        end if
   end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    WriteLog "Function WMIJobCompleted"
    dim WMIJob, jobState

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\CreateVFD.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Мсвм \_ )**](msvm-imagemanagementservice.md)
</dt> </dl>

 

