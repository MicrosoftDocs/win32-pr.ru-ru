---
title: Объект Enumerator (Всмандисп. h)
description: Представляет поток результатов, возвращенных операциями, например операция извлечения.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows объекта перечислителя
- Объект перечислителя служба удаленного управления Windows, описание
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071942"
---
# <a name="enumerator-object"></a><span data-ttu-id="a1d0a-105">Enumerator - объект</span><span class="sxs-lookup"><span data-stu-id="a1d0a-105">Enumerator object</span></span>

<span data-ttu-id="a1d0a-106">Представляет поток результатов, возвращенных операциями, например операция извлечения.</span><span class="sxs-lookup"><span data-stu-id="a1d0a-106">Represents a stream of results returned from operations, such as a Pull operation.</span></span> <span data-ttu-id="a1d0a-107">Например, метод [**Session. Enumerate**](session-enumerate.md) возвращает несколько результатов.</span><span class="sxs-lookup"><span data-stu-id="a1d0a-107">For example, the [**Session.Enumerate**](session-enumerate.md) method returns multiple results.</span></span>

## <a name="members"></a><span data-ttu-id="a1d0a-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="a1d0a-108">Members</span></span>

<span data-ttu-id="a1d0a-109">Объект **перечислителя** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a1d0a-109">The **Enumerator** object has these types of members:</span></span>

-   [<span data-ttu-id="a1d0a-110">Методы</span><span class="sxs-lookup"><span data-stu-id="a1d0a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a1d0a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a1d0a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a1d0a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="a1d0a-112">Methods</span></span>

<span data-ttu-id="a1d0a-113">Объект **перечислителя** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="a1d0a-113">The **Enumerator** object has these methods.</span></span>



| <span data-ttu-id="a1d0a-114">Метод</span><span class="sxs-lookup"><span data-stu-id="a1d0a-114">Method</span></span>                                  | <span data-ttu-id="a1d0a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a1d0a-115">Description</span></span>                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1d0a-116">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="a1d0a-116">**ReadItem**</span></span>](enumerator-readitem.md) | <span data-ttu-id="a1d0a-117">Извлекает элемент из ресурса и возвращает XML-представление элемента.</span><span class="sxs-lookup"><span data-stu-id="a1d0a-117">Retrieves an item from the resource and returns an XML representation of the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a1d0a-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="a1d0a-118">Properties</span></span>

<span data-ttu-id="a1d0a-119">Объект **перечислителя** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a1d0a-119">The **Enumerator** object has these properties.</span></span>



| <span data-ttu-id="a1d0a-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="a1d0a-120">Property</span></span>                                                     | <span data-ttu-id="a1d0a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="a1d0a-121">Description</span></span>                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1d0a-122">**атендофстреам**</span><span class="sxs-lookup"><span data-stu-id="a1d0a-122">**AtEndOfStream**</span></span>](enumerator-atendofstream.md)<br/> | <span data-ttu-id="a1d0a-123">Возвращает логическое значение, указывающее, имеется ли в коллекции больше элементов.</span><span class="sxs-lookup"><span data-stu-id="a1d0a-123">Gets a Boolean value that indicates whether there are more items in the collection.</span></span><br/> |
| [<span data-ttu-id="a1d0a-124">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="a1d0a-124">**Error**</span></span>](enumerator-error.md)<br/>                 | <span data-ttu-id="a1d0a-125">Возвращает XML-представление дополнительных сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a1d0a-125">Gets an XML representation of additional error information.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="a1d0a-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1d0a-126">Remarks</span></span>

<span data-ttu-id="a1d0a-127">Чтобы запустить перечисление, используйте [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="a1d0a-127">To start an enumeration, use [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="a1d0a-128">Для выполнения операции [*WS-enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) , которая возобновляет чтение элементов в перечислении, используйте [**перечислитель. ReadItem**](enumerator-readitem.md).</span><span class="sxs-lookup"><span data-stu-id="a1d0a-128">To do a [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) operation that continues reading items in the enumeration, use [**Enumerator.ReadItem**](enumerator-readitem.md).</span></span>

<span data-ttu-id="a1d0a-129">Объект **перечислителя** соответствует интерфейсу [**ивсманенумератор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .</span><span class="sxs-lookup"><span data-stu-id="a1d0a-129">The **Enumerator** object corresponds to the [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="a1d0a-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="a1d0a-130">Examples</span></span>

<span data-ttu-id="a1d0a-131">В следующем примере кода VBScript перечисляются все диски на удаленном компьютере, указанные полным доменным именем (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="a1d0a-131">The following VBScript code example enumerates all the disks on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="a1d0a-132">Подпрограмма DisplayOutput форматирует выходные данные таким же образом, как средство WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="a1d0a-132">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


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



## <a name="requirements"></a><span data-ttu-id="a1d0a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a1d0a-133">Requirements</span></span>



| <span data-ttu-id="a1d0a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a1d0a-134">Requirement</span></span> | <span data-ttu-id="a1d0a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a1d0a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d0a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1d0a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d0a-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1d0a-137">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a1d0a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1d0a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d0a-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1d0a-139">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a1d0a-140">Header</span><span class="sxs-lookup"><span data-stu-id="a1d0a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1d0a-141"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1d0a-141"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1d0a-142">IDL</span><span class="sxs-lookup"><span data-stu-id="a1d0a-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a1d0a-143"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a1d0a-143"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a1d0a-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a1d0a-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1d0a-145"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1d0a-145"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1d0a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a1d0a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1d0a-147"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1d0a-147"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1d0a-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1d0a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d0a-149">API сценариев WinRM</span><span class="sxs-lookup"><span data-stu-id="a1d0a-149">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="a1d0a-150">Перечисление или вывод всех экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="a1d0a-150">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="a1d0a-151">Создание сценариев в служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="a1d0a-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





