---
description: Удаляет существующие пары "ключ-значение" из виртуальной машины.
ms.assetid: B2ECF609-89BB-4117-982B-EF56D51E1321
title: Метод Ремовеквпитемс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4921805ade9538a4e05a15331f707b9356411aa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546823"
---
# <a name="removekvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f6928-103">Метод Ремовеквпитемс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f6928-103">RemoveKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f6928-104">Удаляет существующие пары "ключ-значение" из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f6928-104">Removes existing key-value pairs from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6928-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6928-105">Syntax</span></span>


```mof
uint32 RemoveKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f6928-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6928-107">*Параметра targetsystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6928-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6928-108">Тип: **[ **CIM \_ ComputerSystem** .](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="f6928-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="f6928-109">Ссылка на виртуальную машину, на которой будут удалены пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="f6928-109">A reference to the virtual machine on which the key-value pairs will be removed.</span></span>

</dd> <dt>

<span data-ttu-id="f6928-110">*Элементы* \[ данные окне\]</span><span class="sxs-lookup"><span data-stu-id="f6928-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6928-111">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f6928-111">Type: **string\[\]**</span></span>

<span data-ttu-id="f6928-112">Массив удаляемых пар "ключ-значение" (необходимо совпадение только ключей).</span><span class="sxs-lookup"><span data-stu-id="f6928-112">An array of key-value pairs to be removed (only the keys need to match).</span></span> <span data-ttu-id="f6928-113">Каждый элемент массива является внедренным экземпляром класса [**мсвм \_ квпексчанжедатаитем**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f6928-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="f6928-114">Этот метод завершается ошибкой, если любая из указанных пар "ключ-значение" не существует в целевой системе.</span><span class="sxs-lookup"><span data-stu-id="f6928-114">This method fails if any of the specified key-value pairs does not exist on the target system.</span></span> <span data-ttu-id="f6928-115">Этот массив может содержать не более 128 элементов.</span><span class="sxs-lookup"><span data-stu-id="f6928-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="f6928-116">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f6928-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6928-117">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="f6928-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="f6928-118">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6928-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6928-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6928-119">Return value</span></span>

<span data-ttu-id="f6928-120">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6928-120">Type: **uint32**</span></span>

<span data-ttu-id="f6928-121">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f6928-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f6928-122">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f6928-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f6928-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-124">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f6928-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-125">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f6928-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-126">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f6928-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-127">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f6928-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-128">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f6928-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-129">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f6928-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-130">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f6928-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-131">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f6928-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-132">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f6928-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-133">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f6928-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f6928-134">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f6928-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f6928-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6928-135">Remarks</span></span>

<span data-ttu-id="f6928-136">Доступ к классу [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="f6928-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f6928-137">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f6928-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="f6928-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="f6928-138">Examples</span></span>

<span data-ttu-id="f6928-139">В следующем примере на C# удаляются пары "ключ-значение" из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f6928-139">The following C# sample removes key-value pairs from a virtual machine.</span></span> <span data-ttu-id="f6928-140">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f6928-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6928-141">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="f6928-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void RemoveKvpItems(string vmName, string itemName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("RemoveKvpItems");
    ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

    ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();

    dataItem["Data"] = "";
    dataItem["Name"] = itemName;
    dataItem["Source"] = 0;

    string[] dataItems = new string[1];
    dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    inParams["TargetSystem"] = vm.Path.Path;
    inParams["DataItems"] = dataItems;

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("RemoveKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("KvpItems were removed successfully.");

        }
        else
        {
            Console.WriteLine("Failed to remove KvpItems");
        }
    } 
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("KvpItems were removed successfully.");
    }
    else
    {
        Console.WriteLine("Remove KvpItems failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    dataItem.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
    
}
```



<span data-ttu-id="f6928-142">Следующий пример Visual Basic Scripting Edition (VBScript) удаляет пары "ключ-значение" из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f6928-142">The following Visual Basic Scripting Edition (VBScript) sample removes key-value pairs from a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6928-143">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="f6928-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


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

    dim computer, vmName, itemName, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if RemoveKvpItems(myVm, itemName) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "RemoveKvpItems failed"
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
' RemoveKvpItems
'-----------------------------------------------------------------
Function RemoveKvpItems(computerSystem, itemName)

    dim dataItem, dataItems, objInParam, objOutParams
    
    RemoveKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = ""
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("RemoveKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.dataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("RemoveKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            RemoveKvpItems = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        RemoveKvpItems = true
    else
        WriteLog Format1("RemoveKvpItems failed with {0}", objOutParams.ReturnValue )
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
    set fileStream = fileSystem.OpenTextFile(".\RemoveKvpItems.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="f6928-144">Требования</span><span class="sxs-lookup"><span data-stu-id="f6928-144">Requirements</span></span>



| <span data-ttu-id="f6928-145">Требование</span><span class="sxs-lookup"><span data-stu-id="f6928-145">Requirement</span></span> | <span data-ttu-id="f6928-146">Значение</span><span class="sxs-lookup"><span data-stu-id="f6928-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6928-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6928-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f6928-148">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f6928-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6928-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6928-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f6928-150">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f6928-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6928-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f6928-151">Namespace</span></span><br/>                | <span data-ttu-id="f6928-152">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f6928-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6928-153">MOF</span><span class="sxs-lookup"><span data-stu-id="f6928-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6928-154"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6928-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6928-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f6928-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6928-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6928-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6928-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6928-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6928-158">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="f6928-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

