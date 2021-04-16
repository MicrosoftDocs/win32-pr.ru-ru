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
# <a name="createvirtualfloppydisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="9d798-103">Метод Креатевиртуалфлоппидиск \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="9d798-103">CreateVirtualFloppyDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="9d798-104">Создает файл виртуального гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="9d798-104">Creates a virtual floppy disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d798-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d798-105">Syntax</span></span>


```mof
uint32 CreateVirtualFloppyDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9d798-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d798-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d798-107">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d798-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d798-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d798-108">Type: **string**</span></span>

<span data-ttu-id="9d798-109">Полный путь, указывающий расположение нового файла.</span><span class="sxs-lookup"><span data-stu-id="9d798-109">A fully qualified path that specifies the location of the new file.</span></span>

</dd> <dt>

<span data-ttu-id="9d798-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9d798-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d798-111">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9d798-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="9d798-112">Ссылка на задание (может иметь **значение NULL** , если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="9d798-112">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d798-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d798-113">Return value</span></span>

<span data-ttu-id="9d798-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d798-114">Type: **uint32**</span></span>

<span data-ttu-id="9d798-115">Этот метод может возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9d798-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9d798-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="9d798-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="9d798-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="9d798-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="9d798-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="9d798-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="9d798-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="9d798-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="9d798-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="9d798-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="9d798-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="9d798-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="9d798-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="9d798-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9d798-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="9d798-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="9d798-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d798-130">Remarks</span></span>

<span data-ttu-id="9d798-131">Доступ к классу [**\_ ) мсвм**](msvm-imagemanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="9d798-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9d798-132">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9d798-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="9d798-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="9d798-133">Examples</span></span>

<span data-ttu-id="9d798-134">В следующем примере кода C# создается файл виртуального дисковода гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="9d798-134">The following C# example creates a virtual floppy disk file.</span></span> <span data-ttu-id="9d798-135">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="9d798-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


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



<span data-ttu-id="9d798-136">В следующем примере Visual Basic Scripting Edition (VBScript) создается файл виртуального гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="9d798-136">The following Visual Basic Scripting Edition (VBScript) example creates a virtual floppy disk file.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9d798-137">Требования</span><span class="sxs-lookup"><span data-stu-id="9d798-137">Requirements</span></span>



| <span data-ttu-id="9d798-138">Требование</span><span class="sxs-lookup"><span data-stu-id="9d798-138">Requirement</span></span> | <span data-ttu-id="9d798-139">Значение</span><span class="sxs-lookup"><span data-stu-id="9d798-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d798-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d798-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9d798-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9d798-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9d798-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d798-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9d798-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9d798-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d798-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9d798-144">Namespace</span></span><br/>                | <span data-ttu-id="9d798-145">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9d798-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9d798-146">MOF</span><span class="sxs-lookup"><span data-stu-id="9d798-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d798-147"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d798-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d798-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9d798-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d798-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d798-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9d798-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d798-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="9d798-151">[**\_КОНКРЕТЕЖОБ CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d798-151">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9d798-152">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="9d798-152">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

