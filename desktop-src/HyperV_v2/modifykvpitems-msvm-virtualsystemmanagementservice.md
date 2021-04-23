---
description: Изменяет существующие пары "ключ-значение" на виртуальной машине.
ms.assetid: A014F681-4429-4982-95AA-DF371925BB3B
title: Метод Модификвпитемс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6269e1a7794b6f04de606d13c90ef8dac1777369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683972"
---
# <a name="modifykvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6b376-103">Метод Модификвпитемс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="6b376-103">ModifyKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6b376-104">Изменяет существующие пары "ключ-значение" на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6b376-104">Modifies existing key-value pairs on a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b376-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b376-105">Syntax</span></span>


```mof
uint32 ModifyKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6b376-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b376-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b376-107">*Параметра targetsystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b376-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b376-108">Тип: **[ **CIM \_ ComputerSystem** .](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="6b376-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="6b376-109">Ссылка на виртуальную машину, на которой будут изменены пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="6b376-109">A reference to the virtual machine on which the key-value pairs will be modified.</span></span>

</dd> <dt>

<span data-ttu-id="6b376-110">*Элементы* \[ данные окне\]</span><span class="sxs-lookup"><span data-stu-id="6b376-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b376-111">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="6b376-111">Type: **string\[\]**</span></span>

<span data-ttu-id="6b376-112">Массив пар "ключ-значение", которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="6b376-112">An array of key-value pairs to be modified.</span></span> <span data-ttu-id="6b376-113">Каждый элемент массива является внедренным экземпляром класса [**мсвм \_ квпексчанжедатаитем**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6b376-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="6b376-114">Этот метод завершается ошибкой, если любая из указанных пар "ключ-значение" не существует в целевой системе.</span><span class="sxs-lookup"><span data-stu-id="6b376-114">This method fails if any of the specified key-value pairs does not exist on the target system.</span></span> <span data-ttu-id="6b376-115">Этот массив может содержать не более 128 элементов.</span><span class="sxs-lookup"><span data-stu-id="6b376-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="6b376-116">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b376-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b376-117">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="6b376-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="6b376-118">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6b376-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b376-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b376-119">Return value</span></span>

<span data-ttu-id="6b376-120">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b376-120">Type: **uint32**</span></span>

<span data-ttu-id="6b376-121">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6b376-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6b376-122">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="6b376-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="6b376-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-124">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="6b376-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-125">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="6b376-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-126">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="6b376-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-127">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="6b376-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-128">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="6b376-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-129">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="6b376-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-130">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="6b376-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-131">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="6b376-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-132">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="6b376-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-133">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="6b376-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6b376-134">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="6b376-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6b376-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b376-135">Remarks</span></span>

<span data-ttu-id="6b376-136">Доступ к классу [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="6b376-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6b376-137">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6b376-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="6b376-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="6b376-138">Examples</span></span>

<span data-ttu-id="6b376-139">Следующий пример на C# изменяет пары "ключ-значение" на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6b376-139">The following C# sample modifies key-value pairs on a virtual machine.</span></span> <span data-ttu-id="6b376-140">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="6b376-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b376-141">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="6b376-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class ModifyKvpItemsClass
    {
        static void ModifyKvpItems(string vmName, string itemName, string itemValue)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
            ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("ModifyKvpItems");
            ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

            ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();
            
            dataItem["Data"] = itemValue;
            dataItem["Name"] = itemName;
            dataItem["Source"] = 0;

            string[] dataItems = new string[1];
            dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            inParams["TargetSystem"] = vm.Path.Path;
            inParams["DataItems"] = dataItems;

            ManagementBaseObject outParams = virtualSystemService.InvokeMethod("ModifyKvpItems", inParams, null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("KvpItems were modified successfully.");
                }
                else
                {
                    Console.WriteLine("Failed to modify KvpItems");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine("KvpItems were modified successfully.");
            }
            else
            {
                Console.WriteLine("Modify virtual system kvp items failed with error {0}", outParams["ReturnValue"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            vm.Dispose();
            dataItem.Dispose();
            virtualSystemService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 3)
            {
                Console.WriteLine("Usage: ModifyKvpItems vmName itemName itemValue");
                return;
            }
            ModifyKvpItems(args[0], args[1], args[2]);
        }
    }
}
```



<span data-ttu-id="6b376-142">Следующий пример Visual Basic Scripting Edition (VBScript) изменяет пары "ключ-значение" на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6b376-142">The following Visual Basic Scripting Edition (VBScript) sample modifies key-value pairs on a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b376-143">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="6b376-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, vmName, itemName, itemValue, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
        itemValue = objArgs.Unnamed.Item(2)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName itemValue"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if ModifyKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "ModifyKvpItems failed"
        WScript.Quit(1)
    end if


End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    dim query
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' RemoveVirtualSystemResource
'-----------------------------------------------------------------
Function ModifyKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    ModifyKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("ModifyKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.dataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("ModifyKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            ModifyKvpItems = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        ModifyKvpItems = true
    else
        WriteLog Format1("ModifyKvpItems failed with {0}", objOutParams.ReturnValue)
    end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)

    dim WMIJob, jobState
    WMIJobCompleted = true

    set WMIJob = objWMIService.Get(outParam.Job)
    
    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (WMIJob.JobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WMIJobCompleted = false
    end if
    
End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\ModifyKvpItems.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="6b376-144">Требования</span><span class="sxs-lookup"><span data-stu-id="6b376-144">Requirements</span></span>



| <span data-ttu-id="6b376-145">Требование</span><span class="sxs-lookup"><span data-stu-id="6b376-145">Requirement</span></span> | <span data-ttu-id="6b376-146">Значение</span><span class="sxs-lookup"><span data-stu-id="6b376-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b376-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b376-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6b376-148">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6b376-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6b376-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b376-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6b376-150">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6b376-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b376-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b376-151">Namespace</span></span><br/>                | <span data-ttu-id="6b376-152">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6b376-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6b376-153">MOF</span><span class="sxs-lookup"><span data-stu-id="6b376-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b376-154"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b376-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b376-155">DLL</span><span class="sxs-lookup"><span data-stu-id="6b376-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b376-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b376-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6b376-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b376-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b376-158">**Модификвпитемс (v1)**</span><span class="sxs-lookup"><span data-stu-id="6b376-158">**ModifyKvpItems (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifykvpitems-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="6b376-159">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="6b376-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

