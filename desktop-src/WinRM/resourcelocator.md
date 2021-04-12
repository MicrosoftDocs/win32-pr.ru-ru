---
title: Объект ResourceLocator (Всмандисп. h)
description: Предоставляет путь к ресурсу. Вы можете использовать объект ResourceLocator вместо URI ресурса в операциях с объектами сеанса, таких как Session. Get, Session. Where или Session. Enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows объекта ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, описание
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135311"
---
# <a name="resourcelocator-object"></a><span data-ttu-id="55099-106">Объект ResourceLocator</span><span class="sxs-lookup"><span data-stu-id="55099-106">ResourceLocator object</span></span>

<span data-ttu-id="55099-107">Объект, предоставляющий путь к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="55099-107">An object that supplies the path to a resource.</span></span> <span data-ttu-id="55099-108">Вы можете использовать объект **ResourceLocator** вместо [*URI ресурса*](windows-remote-management-glossary.md) в операциях с объектами [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="55099-108">You can use a **ResourceLocator** object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="55099-109">Этот объект позволяет выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="55099-109">This object enables you to:</span></span>

-   <span data-ttu-id="55099-110">Добавьте один или несколько [*селекторов*](windows-remote-management-glossary.md) , которые указывают конкретный экземпляр ресурса.</span><span class="sxs-lookup"><span data-stu-id="55099-110">Add one or more [*selectors*](windows-remote-management-glossary.md) that identify a particular instance of a resource.</span></span> <span data-ttu-id="55099-111">Это то же самое, что и указание значения ключа в универсальном коде ресурса (URI) ресурса, использующего ключи.</span><span class="sxs-lookup"><span data-stu-id="55099-111">This is the same as supplying a key value in the resource URI for a resource that uses keys.</span></span> <span data-ttu-id="55099-112">Дополнительные сведения см. в разделе [**ResourceLocator. аддселектор**](resourcelocator-addselector.md).</span><span class="sxs-lookup"><span data-stu-id="55099-112">For more information, see [**ResourceLocator.AddSelector**](resourcelocator-addselector.md).</span></span> <span data-ttu-id="55099-113">Аналогичную операцию можно выполнить с помощью параметра *Filter* в вызове [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="55099-113">You can do a similar operation using the *filter* parameter in a call to [**Session.Enumerate**](session-enumerate.md).</span></span>
-   <span data-ttu-id="55099-114">Укажите путь [*фрагмента*](windows-remote-management-glossary.md) и диалект, чтобы получить только одно свойство ресурса.</span><span class="sxs-lookup"><span data-stu-id="55099-114">Specify a [*fragment*](windows-remote-management-glossary.md) path and dialect to get only one property of a resource.</span></span> <span data-ttu-id="55099-115">Можно также указать один или все элементы свойства массива, указав индекс массива.</span><span class="sxs-lookup"><span data-stu-id="55099-115">You can also specify one or all of the elements of an array property by supplying the array index.</span></span> <span data-ttu-id="55099-116">Дополнительные сведения см. в разделе [**ResourceLocator. фрагментпас**](resourcelocator-fragmentpath.md).</span><span class="sxs-lookup"><span data-stu-id="55099-116">For more information, see [**ResourceLocator.FragmentPath**](resourcelocator-fragmentpath.md).</span></span>
-   <span data-ttu-id="55099-117">Добавьте один или несколько [*параметров*](windows-remote-management-glossary.md) , которые могут потребоваться источнику данных для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="55099-117">Add one or more [*options*](windows-remote-management-glossary.md) that a data source may require to process a request.</span></span> <span data-ttu-id="55099-118">Дополнительные сведения см. в разделе [**ResourceLocator. аддоптион**](resourcelocator-addoption.md).</span><span class="sxs-lookup"><span data-stu-id="55099-118">For more information, see [**ResourceLocator.AddOption**](resourcelocator-addoption.md).</span></span>

<span data-ttu-id="55099-119">Дополнительные сведения см. в разделе [запрос конкретных экземпляров ресурса](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="55099-119">For more information, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

## <a name="members"></a><span data-ttu-id="55099-120">Элементы</span><span class="sxs-lookup"><span data-stu-id="55099-120">Members</span></span>

<span data-ttu-id="55099-121">Объект **ResourceLocator** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="55099-121">The **ResourceLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="55099-122">Методы</span><span class="sxs-lookup"><span data-stu-id="55099-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="55099-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="55099-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="55099-124">Методы</span><span class="sxs-lookup"><span data-stu-id="55099-124">Methods</span></span>

<span data-ttu-id="55099-125">Объект **ResourceLocator** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="55099-125">The **ResourceLocator** object has these methods.</span></span>



| <span data-ttu-id="55099-126">Метод</span><span class="sxs-lookup"><span data-stu-id="55099-126">Method</span></span>                                                   | <span data-ttu-id="55099-127">Описание</span><span class="sxs-lookup"><span data-stu-id="55099-127">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55099-128">**аддоптион**</span><span class="sxs-lookup"><span data-stu-id="55099-128">**AddOption**</span></span>](resourcelocator-addoption.md)           | <span data-ttu-id="55099-129">Добавляет дополнительные данные, необходимые для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="55099-129">Adds additional data required to process the request.</span></span><br/>                                                                   |
| [<span data-ttu-id="55099-130">**аддселектор**</span><span class="sxs-lookup"><span data-stu-id="55099-130">**AddSelector**</span></span>](resourcelocator-addselector.md)       | <span data-ttu-id="55099-131">Добавляет [*селектор*](windows-remote-management-glossary.md) в объект **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="55099-131">Adds a [*selector*](windows-remote-management-glossary.md) to the **ResourceLocator** object.</span></span><br/>     |
| [<span data-ttu-id="55099-132">**клеароптионс**</span><span class="sxs-lookup"><span data-stu-id="55099-132">**ClearOptions**</span></span>](resourcelocator-clearoptions.md)     | <span data-ttu-id="55099-133">Удаляет все [*Параметры*](windows-remote-management-glossary.md) из объекта **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="55099-133">Removes any [*options*](windows-remote-management-glossary.md) from the **ResourceLocator** object.</span></span><br/> |
| [<span data-ttu-id="55099-134">**клеарселекторс**</span><span class="sxs-lookup"><span data-stu-id="55099-134">**ClearSelectors**</span></span>](resourcelocator-clearselectors.md) | <span data-ttu-id="55099-135">Удаляет все селекторы из объекта **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="55099-135">Removes all the selectors from a **ResourceLocator** object.</span></span><br/>                                                            |



 

### <a name="properties"></a><span data-ttu-id="55099-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="55099-136">Properties</span></span>

<span data-ttu-id="55099-137">Объект **ResourceLocator** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="55099-137">The **ResourceLocator** object has these properties.</span></span>



| <span data-ttu-id="55099-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="55099-138">Property</span></span>                                                                          | <span data-ttu-id="55099-139">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="55099-139">Access type</span></span>           | <span data-ttu-id="55099-140">Описание</span><span class="sxs-lookup"><span data-stu-id="55099-140">Description</span></span>                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55099-141">**фрагментдиалект**</span><span class="sxs-lookup"><span data-stu-id="55099-141">**FragmentDialect**</span></span>](resourcelocator-fragmentdialect.md)<br/>             | <span data-ttu-id="55099-142">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="55099-142">Read/write</span></span><br/> | <span data-ttu-id="55099-143">Возвращает или задает диалект языка для [*фрагмента*](windows-remote-management-glossary.md) [*ресурса*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="55099-143">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md).</span></span><br/> |
| [<span data-ttu-id="55099-144">**фрагментпас**</span><span class="sxs-lookup"><span data-stu-id="55099-144">**FragmentPath**</span></span>](resourcelocator-fragmentpath.md)<br/>                   | <span data-ttu-id="55099-145">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="55099-145">Read/write</span></span><br/> | <span data-ttu-id="55099-146">Возвращает или задает путь к [*фрагменту*](windows-remote-management-glossary.md) или свойству [*ресурса*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="55099-146">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property.</span></span><br/> |
| [<span data-ttu-id="55099-147">**мустундерстандоптионс**</span><span class="sxs-lookup"><span data-stu-id="55099-147">**MustUnderstandOptions**</span></span>](resourcelocator-mustunderstandoptions.md)<br/> | <span data-ttu-id="55099-148">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="55099-148">Read/write</span></span><br/> | <span data-ttu-id="55099-149">Возвращает или задает значение **мустундерстандоптионс** для объекта **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="55099-149">Gets or sets the **MustUnderstandOptions** value for the **ResourceLocator** object.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="55099-150">**ResourceURI**</span><span class="sxs-lookup"><span data-stu-id="55099-150">**ResourceURI**</span></span>](resourcelocator-resourceuri.md)<br/>                     | <span data-ttu-id="55099-151">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="55099-151">Read/write</span></span><br/> | <span data-ttu-id="55099-152">Возвращает или задает [*URI ресурса*](windows-remote-management-glossary.md) в объекте **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="55099-152">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a **ResourceLocator** object.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="55099-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55099-153">Remarks</span></span>

<span data-ttu-id="55099-154">Объект **ResourceLocator** соответствует интерфейсу **ивсманресаурцелокатор** .</span><span class="sxs-lookup"><span data-stu-id="55099-154">The **ResourceLocator** object corresponds to the **IWSManResourceLocator** interface.</span></span>

## <a name="examples"></a><span data-ttu-id="55099-155">Примеры</span><span class="sxs-lookup"><span data-stu-id="55099-155">Examples</span></span>

<span data-ttu-id="55099-156">Следующий пример кода VBScript получает свойства **нумберофлогикалпроцессорс** и **нумберофкорес** из определенного экземпляра [**\_ процессора Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="55099-156">The following VBScript code example obtains the **NumberOfLogicalProcessors** and **NumberOfCores** properties from a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************

Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" )    
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile )           
End Sub
```



## <a name="requirements"></a><span data-ttu-id="55099-157">Требования</span><span class="sxs-lookup"><span data-stu-id="55099-157">Requirements</span></span>



| <span data-ttu-id="55099-158">Требование</span><span class="sxs-lookup"><span data-stu-id="55099-158">Requirement</span></span> | <span data-ttu-id="55099-159">Значение</span><span class="sxs-lookup"><span data-stu-id="55099-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55099-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55099-160">Minimum supported client</span></span><br/> | <span data-ttu-id="55099-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55099-161">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="55099-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55099-162">Minimum supported server</span></span><br/> | <span data-ttu-id="55099-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55099-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="55099-164">Header</span><span class="sxs-lookup"><span data-stu-id="55099-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="55099-165"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="55099-165"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="55099-166">IDL</span><span class="sxs-lookup"><span data-stu-id="55099-166">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55099-167"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55099-167"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="55099-168">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55099-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="55099-169"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="55099-169"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="55099-170">DLL</span><span class="sxs-lookup"><span data-stu-id="55099-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55099-171"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55099-171"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="55099-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55099-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55099-173">API сценариев WinRM</span><span class="sxs-lookup"><span data-stu-id="55099-173">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> </dl>

 

