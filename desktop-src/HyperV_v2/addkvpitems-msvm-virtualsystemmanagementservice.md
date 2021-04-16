---
description: Добавляет пары "ключ-значение" в виртуальную машину.
ms.assetid: D952EC3D-24EB-4A68-8527-5BF522957CB6
title: Метод Аддквпитемс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9e01a02615b8bb395a589160a765dec4e08526e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683438"
---
# <a name="addkvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a5be9-103">Метод Аддквпитемс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="a5be9-103">AddKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a5be9-104">Добавляет пары "ключ-значение" в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a5be9-104">Adds key-value pairs to a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5be9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5be9-105">Syntax</span></span>


```mof
uint32 AddKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a5be9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5be9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5be9-107">*Параметра targetsystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5be9-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5be9-108">Тип: **[ **CIM \_ ComputerSystem** .](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="a5be9-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="a5be9-109">Ссылка на объект [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, в которой будут добавлены пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="a5be9-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object that represents the virtual machine on which the key-value pairs will be added.</span></span>

</dd> <dt>

<span data-ttu-id="a5be9-110">*Элементы* \[ данные окне\]</span><span class="sxs-lookup"><span data-stu-id="a5be9-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5be9-111">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a5be9-111">Type: **string\[\]**</span></span>

<span data-ttu-id="a5be9-112">Массив добавляемых пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="a5be9-112">An array of key-value pairs to be added.</span></span> <span data-ttu-id="a5be9-113">Каждый элемент массива является внедренным экземпляром класса [**мсвм \_ квпексчанжедатаитем**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a5be9-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="a5be9-114">Этот метод завершается ошибкой, если в целевой системе уже существует любая из указанных пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="a5be9-114">This method fails if any of the specified key-value pairs already exists on the target system.</span></span> <span data-ttu-id="a5be9-115">Этот массив может содержать не более 128 элементов.</span><span class="sxs-lookup"><span data-stu-id="a5be9-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="a5be9-116">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a5be9-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5be9-117">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a5be9-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="a5be9-118">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5be9-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5be9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5be9-119">Return value</span></span>

<span data-ttu-id="a5be9-120">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5be9-120">Type: **uint32**</span></span>

<span data-ttu-id="a5be9-121">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a5be9-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a5be9-122">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="a5be9-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="a5be9-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-124">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="a5be9-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-125">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="a5be9-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-126">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="a5be9-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-127">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="a5be9-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-128">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="a5be9-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-129">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="a5be9-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-130">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="a5be9-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-131">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="a5be9-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-132">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="a5be9-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-133">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="a5be9-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a5be9-134">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="a5be9-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a5be9-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5be9-135">Remarks</span></span>

<span data-ttu-id="a5be9-136">Доступ к классу [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="a5be9-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a5be9-137">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a5be9-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="a5be9-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="a5be9-138">Examples</span></span>

<span data-ttu-id="a5be9-139">В следующем примере кода C# в виртуальную машину добавляются пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="a5be9-139">The following C# sample adds key-value pairs to a virtual machine.</span></span> <span data-ttu-id="a5be9-140">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="a5be9-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5be9-141">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="a5be9-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void AddKvpItems(string vmName, string itemName, string itemValue)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("AddKvpItems");
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

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("AddKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Resources were added successfully.");

        }
        else
        {
            Console.WriteLine("Failed to add resources");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Resources were added successfully.");
    }
    else
    {
        Console.WriteLine("Add virtual system Kvp items failed with error {0}", outParams["ReturnValue"]);
    }

    if (inParams != null)
    {
        inParams.Dispose();
    }

    if (outParams != null)
    {
        outParams.Dispose();
    }
}
```



<span data-ttu-id="a5be9-142">Следующий пример Visual Basic Scripting Edition (VBScript) добавляет пары "ключ-значение" в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a5be9-142">The following Visual Basic Scripting Edition (VBScript) sample adds key-value pairs to a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5be9-143">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="a5be9-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


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

    if AddKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "AddKvpItems failed"
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
' AddKvpItems
'-----------------------------------------------------------------
Function AddKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    AddKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("AddKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.DataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("AddKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            AddKvpItems = true
        end if
    elseif (objOutParams.ReturnValue = wmiSuccessful) then
        AddKvpItems = true
    else
        WriteLog Format1("AddKvpItem failed with error {0}", objOutParams.ReturnValue)
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
    set fileStream = fileSystem.OpenTextFile(".\AddKvpItems.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="a5be9-144">Требования</span><span class="sxs-lookup"><span data-stu-id="a5be9-144">Requirements</span></span>



| <span data-ttu-id="a5be9-145">Требование</span><span class="sxs-lookup"><span data-stu-id="a5be9-145">Requirement</span></span> | <span data-ttu-id="a5be9-146">Значение</span><span class="sxs-lookup"><span data-stu-id="a5be9-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5be9-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5be9-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a5be9-148">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a5be9-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a5be9-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5be9-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a5be9-150">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a5be9-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5be9-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5be9-151">Namespace</span></span><br/>                | <span data-ttu-id="a5be9-152">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a5be9-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a5be9-153">MOF</span><span class="sxs-lookup"><span data-stu-id="a5be9-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5be9-154"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5be9-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5be9-155">DLL</span><span class="sxs-lookup"><span data-stu-id="a5be9-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5be9-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5be9-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5be9-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5be9-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5be9-158">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="a5be9-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

