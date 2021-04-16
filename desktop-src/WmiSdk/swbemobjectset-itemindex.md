---
description: Возвращает SWbemObject, связанный с указанным индексом в коллекцию.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: SWbemObjectSet. Итеминдекс, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702885"
---
# <a name="swbemobjectsetitemindex-method"></a><span data-ttu-id="d6476-103">SWbemObjectSet. Итеминдекс, метод</span><span class="sxs-lookup"><span data-stu-id="d6476-103">SWbemObjectSet.ItemIndex method</span></span>

<span data-ttu-id="d6476-104">Метод **итеминдекс** возвращает [**SWbemObject**](swbemobject.md) , связанный с указанным индексом, в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="d6476-104">The **ItemIndex** method returns the [**SWbemObject**](swbemobject.md) associated with the specified index into the collection.</span></span> <span data-ttu-id="d6476-105">Индекс указывает на расположение элемента в коллекции.</span><span class="sxs-lookup"><span data-stu-id="d6476-105">The index indicates the position of the element within the collection.</span></span> <span data-ttu-id="d6476-106">Нумерация коллекций начинается с нуля.</span><span class="sxs-lookup"><span data-stu-id="d6476-106">Collection numbering starts at zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6476-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6476-107">Syntax</span></span>


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="d6476-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6476-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6476-109">*линдекс*</span><span class="sxs-lookup"><span data-stu-id="d6476-109">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="d6476-110">Индекс элемента в коллекции.</span><span class="sxs-lookup"><span data-stu-id="d6476-110">Index of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6476-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6476-111">Return value</span></span>

<span data-ttu-id="d6476-112">В случае успешного выполнения запрошенный объект [**SWbemObject**](swbemobject.md) возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d6476-112">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6476-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d6476-113">Error codes</span></span>

<span data-ttu-id="d6476-114">После завершения метода [**Item**](swbemobjectset-item.md) объект **Err** может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="d6476-114">Upon completion of the [**Item**](swbemobjectset-item.md) method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="d6476-115">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d6476-115">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d6476-116">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d6476-116">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d6476-117">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d6476-117">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d6476-118">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="d6476-118">Invalid parameter was specified.</span></span> <span data-ttu-id="d6476-119">Эта ошибка возвращается, если указан отрицательный номер индекса.</span><span class="sxs-lookup"><span data-stu-id="d6476-119">This error is returned if a negative index number is supplied.</span></span>

</dd> <dt>

<span data-ttu-id="d6476-120">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d6476-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d6476-121">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="d6476-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6476-122">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="d6476-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d6476-123">Запрошенный элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="d6476-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6476-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6476-124">Remarks</span></span>

<span data-ttu-id="d6476-125">Метод **итеминдекс** позволяет клиентским сценариям WMI и приложениям, написанным на любом языке, единообразно управлять коллекцией, например массивом.</span><span class="sxs-lookup"><span data-stu-id="d6476-125">The **ItemIndex** method allows WMI clients scripts and applications written in any language a uniform way to manipulate a collection like an array.</span></span> <span data-ttu-id="d6476-126">Этот метод можно использовать с коллекциями [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="d6476-126">This method can be used with [**SWbemObjectSet**](swbemobjectset.md) collections.</span></span> <span data-ttu-id="d6476-127">Такие запросы, как [**SwbemServices. ассоЦиаторсоф**](swbemservices-associatorsof.md), [**SwbemServices. референцесто**](swbemservices-referencesto.md), [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md)или [**SWbemServices.Exeккуери**](swbemservices-execquery.md) , возвращают **SWbemObjectSet** коллекции.</span><span class="sxs-lookup"><span data-stu-id="d6476-127">Queries, such as [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md), [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), or [**SWbemServices.ExecQuery**](swbemservices-execquery.md) return **SWbemObjectSet** collections.</span></span> <span data-ttu-id="d6476-128">Метод **итеминдекс** не работает с коллекциями, которые не содержат [**Свбемобжектс**](swbemobject.md), например [**свбеммесодсет**](swbemmethodset.md), [**свбемнамедвалуесет**](swbemnamedvalueset.md), [**свбемпривилежесет**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md)и [**свбемкуалифиерсет**](swbemqualifierset.md).</span><span class="sxs-lookup"><span data-stu-id="d6476-128">The **ItemIndex** method does not work with collections which do not contain [**SWbemObjects**](swbemobject.md), such as [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md), and [**SWbemQualifierSet**](swbemqualifierset.md).</span></span>

<span data-ttu-id="d6476-129">**Итеминдекс** также можно использовать для получения единственного экземпляра одноэлементного класса.</span><span class="sxs-lookup"><span data-stu-id="d6476-129">**ItemIndex** can also be used to obtain the single instance of a singleton class.</span></span>

## <a name="examples"></a><span data-ttu-id="d6476-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="d6476-130">Examples</span></span>

<span data-ttu-id="d6476-131">В следующем примере кода VBScript выполняется запрос коллекции всех экземпляров [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , а затем отображаются имена первых трех процессов.</span><span class="sxs-lookup"><span data-stu-id="d6476-131">The following VBScript code example queries for a collection of all the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instances then displays the names of the first three processes.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



<span data-ttu-id="d6476-132">Для каждой установки операционной системы существует только один экземпляр [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) .</span><span class="sxs-lookup"><span data-stu-id="d6476-132">Only one instance of [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) exists for each operating system installation.</span></span> <span data-ttu-id="d6476-133">Создание пути к [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) для получения единственного экземпляра является неудобным, поэтому сценарии обычно перечисляют набор **Win32 \_ , даже** если доступен только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="d6476-133">Creating the [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) path to obtain the single instance is awkward so scripts normally enumerate **Win32\_OperatingSystem** even though only one instance is available.</span></span> <span data-ttu-id="d6476-134">В следующем примере кода VBScript показано, как использовать метод **итеминдекс** для получения одной **\_ операционной системы Win32** без использования цикла **for each** .</span><span class="sxs-lookup"><span data-stu-id="d6476-134">The following VBScript code example shows how to use the **ItemIndex** method to get to the one **Win32\_OperatingSystem** without using a **For Each** loop.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



<span data-ttu-id="d6476-135">Следующий пример кода VBScript получает экземпляры, связанные с [**Win32 \_ операционной**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)системы, например [**Win32 \_ системоператингсистем**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span><span class="sxs-lookup"><span data-stu-id="d6476-135">The following VBScript code example gets instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), such as [**Win32\_SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



<span data-ttu-id="d6476-136">В следующем примере кода показаны экземпляры, связанные с [**\_ операционной системы Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="d6476-136">The following code example output shows instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a><span data-ttu-id="d6476-137">Требования</span><span class="sxs-lookup"><span data-stu-id="d6476-137">Requirements</span></span>



| <span data-ttu-id="d6476-138">Требование</span><span class="sxs-lookup"><span data-stu-id="d6476-138">Requirement</span></span> | <span data-ttu-id="d6476-139">Значение</span><span class="sxs-lookup"><span data-stu-id="d6476-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6476-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6476-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d6476-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6476-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6476-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6476-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d6476-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6476-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6476-144">Header</span><span class="sxs-lookup"><span data-stu-id="d6476-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6476-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6476-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6476-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d6476-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6476-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6476-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6476-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d6476-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6476-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6476-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6476-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="d6476-150">CLSID</span></span><br/>                    | <span data-ttu-id="d6476-151">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="d6476-151">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="d6476-152">IID</span><span class="sxs-lookup"><span data-stu-id="d6476-152">IID</span></span><br/>                      | <span data-ttu-id="d6476-153">IID \_ исвбемобжектсет</span><span class="sxs-lookup"><span data-stu-id="d6476-153">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="d6476-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6476-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6476-155">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="d6476-155">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

