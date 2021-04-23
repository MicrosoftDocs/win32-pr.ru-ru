---
title: Константы перечисления (Всмандисп. h)
description: Перечисление содержит константы, перечисленные в следующем списке, которые используются в параметре Flags путем вызова метода Session. Enumerate и IWSManSession Enumerate.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415141"
---
# <a name="enumeration-constants"></a><span data-ttu-id="e1094-103">Константы перечисления</span><span class="sxs-lookup"><span data-stu-id="e1094-103">Enumeration Constants</span></span>

<span data-ttu-id="e1094-104">Перечисление **\_ \_ всманенумфлагс** содержит константы, перечисленные в следующем списке, которые используются в параметре *flags* при вызове метода [**Session. Enumerate**](session-enumerate.md) и [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="e1094-104">The **\_\_WSManEnumFlags** enumeration contains constants, as listed in the following list, used in the *flags* parameter by calls to [**Session.Enumerate**](session-enumerate.md) and [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

<span data-ttu-id="e1094-105">Имейте в виду, что **всманфлагретурнобжект** и **всманфлагхиерарчидип** являются по умолчанию, если не задан параметр *flags* .</span><span class="sxs-lookup"><span data-stu-id="e1094-105">Be aware that **WSManFlagReturnObject** and **WSManFlagHierarchyDeep** are the default if the *flags* parameter is not specified.</span></span>

<dl> <dt>

<span data-ttu-id="e1094-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**всманфлагретурнобжект**</span><span class="sxs-lookup"><span data-stu-id="e1094-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1094-107">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="e1094-107">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="e1094-108">Пакеты содержат запрошенные экземпляры XML.</span><span class="sxs-lookup"><span data-stu-id="e1094-108">Batches contain the requested XML instances.</span></span> <span data-ttu-id="e1094-109">Это значение по умолчанию для параметра flag.</span><span class="sxs-lookup"><span data-stu-id="e1094-109">This is the default value for the flag parameter.</span></span>

<span data-ttu-id="e1094-110">Связанный метод создания скриптов — это [**WSMan. енумератионфлагретурнобжект**](wsman-enumerationflagreturnobject.md) , а метод C++ — [**ивсманекс. енумератионфлагретурнобжект**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span><span class="sxs-lookup"><span data-stu-id="e1094-110">The associated scripting method is [**WSMan.EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1094-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**всманфлагнонксмлтекст**</span><span class="sxs-lookup"><span data-stu-id="e1094-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1094-112">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e1094-112">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="e1094-113">Этот флаг управляет тем, как параметр *фильтра* в вызове к [**Session. Enumerate**](session-enumerate.md) интерпретируется службой WinRM.</span><span class="sxs-lookup"><span data-stu-id="e1094-113">This flag controls how the *filter* parameter in the call to [**Session.Enumerate**](session-enumerate.md) is interpreted by WinRM.</span></span>

<span data-ttu-id="e1094-114">Формат фильтра может быть фрагментом XML или строкой обычного текста.</span><span class="sxs-lookup"><span data-stu-id="e1094-114">The format of the filter may be an XML fragment or a string of plain text.</span></span> <span data-ttu-id="e1094-115">Формат определяется [*диалектом фильтра*](windows-remote-management-glossary.md) [*фильтра*](windows-remote-management-glossary.md) , используемого в вызове метода [**Session. Enumerate**](session-enumerate.md) или [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), который относится к выполняемой операции.</span><span class="sxs-lookup"><span data-stu-id="e1094-115">The format is determined by the [*filter dialect*](windows-remote-management-glossary.md) of the [*filter*](windows-remote-management-glossary.md) used in the call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), which is specific to the operation performed.</span></span>

<span data-ttu-id="e1094-116">Если параметр *диалекта* не указан, служба WinRM пытается определить диалект на основе первого символа фильтра.</span><span class="sxs-lookup"><span data-stu-id="e1094-116">If the *dialect* parameter is not specified, WinRM attempts to determine the dialect based on the first character of the filter.</span></span> <span data-ttu-id="e1094-117">Если первый символ <, но фильтр фактически не является фрагментом XML, то следует установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="e1094-117">If the first character is <, but the filter is not actually an XML fragment, then this flag should be set.</span></span> <span data-ttu-id="e1094-118">Например, для фильтра в следующем формате требуется задать **всманфлагнонксмлтекст** , чтобы фильтр был правильно интерпретирован:</span><span class="sxs-lookup"><span data-stu-id="e1094-118">For example, a filter in the following format requires that you set **WSManFlagNonXmlText** so that the filter is correctly interpreted:</span></span>

`<25 && > 1`

<span data-ttu-id="e1094-119">Если фильтр является фрагментом XML, этот флаг не требуется, так как фрагмент начинается с <, который правильно интерпретируется в виде XML.</span><span class="sxs-lookup"><span data-stu-id="e1094-119">If the filter is an XML fragment, then this flag is not required because the fragment starts with <, which WinRM correctly interprets as XML.</span></span> <span data-ttu-id="e1094-120">Например,</span><span class="sxs-lookup"><span data-stu-id="e1094-120">For example,</span></span>

`<filter>select * from aDataStructure</filter>`

<span data-ttu-id="e1094-121">Если фильтр имеет обычный текст, который не начинается с <, этот флаг не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e1094-121">If the filter is in plain text that does not start with <, then this flag is not required.</span></span> <span data-ttu-id="e1094-122">Например,</span><span class="sxs-lookup"><span data-stu-id="e1094-122">For example,</span></span>

`select * from aDataStructure`

<span data-ttu-id="e1094-123">Связанный метод создания скриптов — это [**WSMan. енумератионфлагнонксмлтекст**](wsman-enumerationflagnonxmltext.md) , а метод C++ — [**ивсманекс. енумератионфлагнонксмлтекст**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span><span class="sxs-lookup"><span data-stu-id="e1094-123">The associated scripting method is [**WSMan.EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) and the C++ method is [**IWSManEx.EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1094-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**енумератионфлагретурнепр**</span><span class="sxs-lookup"><span data-stu-id="e1094-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1094-125">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="e1094-125">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="e1094-126">Пакеты содержат ссылки на конечные точки (Епрс) для соответствующих экземпляров XML, но не сами экземпляры.</span><span class="sxs-lookup"><span data-stu-id="e1094-126">Batches contain endpoint references (EPRs) for the corresponding XML instances, but not the actual instances.</span></span>

<span data-ttu-id="e1094-127">Связанный метод создания скриптов — это [**WSMan. енумератионфлагретурнепр**](wsman-enumerationflagreturnepr.md) , а метод C++ — [**ивсманекс. енумератионфлагретурнепр**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span><span class="sxs-lookup"><span data-stu-id="e1094-127">The associated scripting method is [**WSMan.EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1094-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**всманфлагретурнобжектандепр**</span><span class="sxs-lookup"><span data-stu-id="e1094-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1094-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="e1094-129">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="e1094-130">Пакеты содержат как запрошенные экземпляры XML, так и соответствующие Епрс, содержащиеся в элементе [*WSMan: Items*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="e1094-130">Batches contain both the requested XML instances and the corresponding EPRs contained in a [*wsman:Items*](windows-remote-management-glossary.md) element.</span></span>

<span data-ttu-id="e1094-131">Связанный метод создания скриптов — это [**WSMan. енумератионфлагретурнобжектандепр**](wsman-enumerationflagreturnobjectandepr.md) , а метод C++ — [**ивсманекс. енумератионфлагретурнобжектандепр**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span><span class="sxs-lookup"><span data-stu-id="e1094-131">The associated scripting method is [**WSMan.EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1094-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**всманфлагхиерарчидип**</span><span class="sxs-lookup"><span data-stu-id="e1094-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1094-133">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="e1094-133">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="e1094-134">Экземпляры производного класса включены и представлены в соответствии с их реальными схемами.</span><span class="sxs-lookup"><span data-stu-id="e1094-134">Derived class instances are included and are represented according to their actual schemas.</span></span>

<span data-ttu-id="e1094-135">Связанный метод создания скриптов — это [**WSMan. енумератионфлагхиерарчидип**](wsman-enumerationflaghierarchydeep.md) , а метод C++ — [**ивсманекс. енумератионфлагхиерарчидип**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span><span class="sxs-lookup"><span data-stu-id="e1094-135">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1094-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**всманфлагхиерарчишаллов**</span><span class="sxs-lookup"><span data-stu-id="e1094-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1094-137">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="e1094-137">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="e1094-138">Экземпляры производного класса исключаются.</span><span class="sxs-lookup"><span data-stu-id="e1094-138">Derived class instances are excluded.</span></span> <span data-ttu-id="e1094-139">Отображаются только экземпляры запрошенного типа.</span><span class="sxs-lookup"><span data-stu-id="e1094-139">Only instances of the requested type are shown.</span></span>

<span data-ttu-id="e1094-140">Связанный метод создания скриптов — это [**WSMan. енумератионфлагхиерарчишаллов**](wsman-enumerationflaghierarchyshallow.md) , а метод C++ — [**ивсманекс. енумератионфлагхиерарчишаллов**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span><span class="sxs-lookup"><span data-stu-id="e1094-140">The associated scripting method is [**WSMan.EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1094-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**всманфлагхиерарчидипбасепропсонли**</span><span class="sxs-lookup"><span data-stu-id="e1094-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1094-142">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="e1094-142">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="e1094-143">Экземпляры производного класса включены и представлены в соответствии со схемой базового класса.</span><span class="sxs-lookup"><span data-stu-id="e1094-143">Derived class instances are included and are represented according to the base class schema.</span></span> <span data-ttu-id="e1094-144">Свойства, определенные в производном классе, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="e1094-144">Properties defined in the derived class are not shown.</span></span>

<span data-ttu-id="e1094-145">Связанный метод создания скриптов — это [**WSMan. енумератионфлагхиерарчидипбасепропсонли**](wsman-enumerationflaghierarchydeepbasepropsonly.md) , а метод C++ — [**ивсманекс. енумератионфлагхиерарчидипбасепропсонли**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span><span class="sxs-lookup"><span data-stu-id="e1094-145">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1094-146">Требования</span><span class="sxs-lookup"><span data-stu-id="e1094-146">Requirements</span></span>



| <span data-ttu-id="e1094-147">Требование</span><span class="sxs-lookup"><span data-stu-id="e1094-147">Requirement</span></span> | <span data-ttu-id="e1094-148">Значение</span><span class="sxs-lookup"><span data-stu-id="e1094-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1094-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1094-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e1094-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1094-150">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e1094-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1094-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e1094-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1094-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e1094-153">Header</span><span class="sxs-lookup"><span data-stu-id="e1094-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1094-154"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1094-154"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1094-155">IDL</span><span class="sxs-lookup"><span data-stu-id="e1094-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1094-156"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1094-156"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1094-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1094-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1094-158">Константы и перечисления WinRM</span><span class="sxs-lookup"><span data-stu-id="e1094-158">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="e1094-159">Перечисление или составление списка всех экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="e1094-159">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="e1094-160">Запрос конкретных экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="e1094-160">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





