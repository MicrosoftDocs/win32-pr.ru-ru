---
description: Объект SWbemProperty представляет отдельное свойство WMI управляемого объекта. Не удается создать этот объект с помощью вызова функции VBScript.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Объект SWbemProperty (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272746"
---
# <a name="swbemproperty-object"></a><span data-ttu-id="49bc9-104">Объект SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="49bc9-104">SWbemProperty object</span></span>

<span data-ttu-id="49bc9-105">Объект **SWbemProperty** представляет отдельное свойство WMI управляемого объекта.</span><span class="sxs-lookup"><span data-stu-id="49bc9-105">The **SWbemProperty** object represents a single WMI property of a managed object.</span></span> <span data-ttu-id="49bc9-106">Не удается создать этот объект с [помощью вызова функции](creating-an-object-using-vbscript.md) VBScript.</span><span class="sxs-lookup"><span data-stu-id="49bc9-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="49bc9-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="49bc9-107">Members</span></span>

<span data-ttu-id="49bc9-108">Объект **SWbemProperty** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="49bc9-108">The **SWbemProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="49bc9-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="49bc9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49bc9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="49bc9-110">Properties</span></span>

<span data-ttu-id="49bc9-111">Объект **SWbemProperty** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="49bc9-111">The **SWbemProperty** object has these properties.</span></span>



| <span data-ttu-id="49bc9-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="49bc9-112">Property</span></span>                                                     | <span data-ttu-id="49bc9-113">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="49bc9-113">Access type</span></span>           | <span data-ttu-id="49bc9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="49bc9-114">Description</span></span>                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49bc9-115">**Цимтипе**</span><span class="sxs-lookup"><span data-stu-id="49bc9-115">**CIMType**</span></span>](swbemproperty-cimtype.md)<br/>          | <span data-ttu-id="49bc9-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="49bc9-116">Read-only</span></span><br/>  | <span data-ttu-id="49bc9-117">Тип этого свойства.</span><span class="sxs-lookup"><span data-stu-id="49bc9-117">Type of this property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="49bc9-118">**IsArray**</span><span class="sxs-lookup"><span data-stu-id="49bc9-118">**IsArray**</span></span>](swbemproperty-isarray.md)<br/>          | <span data-ttu-id="49bc9-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="49bc9-119">Read-only</span></span><br/>  | <span data-ttu-id="49bc9-120">Логическое значение, указывающее, имеет ли это свойство тип массива.</span><span class="sxs-lookup"><span data-stu-id="49bc9-120">Boolean value that indicates if this property has an array type.</span></span><br/>                                                   |
| [<span data-ttu-id="49bc9-121">**Локальный**</span><span class="sxs-lookup"><span data-stu-id="49bc9-121">**IsLocal**</span></span>](swbemproperty-islocal.md)<br/>          | <span data-ttu-id="49bc9-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="49bc9-122">Read-only</span></span><br/>  | <span data-ttu-id="49bc9-123">Логическое значение, указывающее, является ли это свойство локальным.</span><span class="sxs-lookup"><span data-stu-id="49bc9-123">Boolean value that indicates if this property is local.</span></span><br/>                                                            |
| [<span data-ttu-id="49bc9-124">**Имя**</span><span class="sxs-lookup"><span data-stu-id="49bc9-124">**Name**</span></span>](swbemproperty-name.md)<br/>                | <span data-ttu-id="49bc9-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="49bc9-125">Read-only</span></span><br/>  | <span data-ttu-id="49bc9-126">Имя этого свойства WMI.</span><span class="sxs-lookup"><span data-stu-id="49bc9-126">Name of this WMI property.</span></span><br/>                                                                                         |
| [<span data-ttu-id="49bc9-127">**Лета**</span><span class="sxs-lookup"><span data-stu-id="49bc9-127">**Origin**</span></span>](swbemproperty-origin.md)<br/>            | <span data-ttu-id="49bc9-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="49bc9-128">Read-only</span></span><br/>  | <span data-ttu-id="49bc9-129">Содержит исходный класс этого свойства.</span><span class="sxs-lookup"><span data-stu-id="49bc9-129">Contains the originating class of this property.</span></span><br/>                                                                   |
| [<span data-ttu-id="49bc9-130">**Квалификаторы\_**</span><span class="sxs-lookup"><span data-stu-id="49bc9-130">**Qualifiers\_**</span></span>](swbemproperty-qualifiers-.md)<br/> | <span data-ttu-id="49bc9-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="49bc9-131">Read-only</span></span><br/>  | <span data-ttu-id="49bc9-132">Объект [**свбемкуалифиерсет**](swbemqualifierset.md) , являющийся коллекцией квалификаторов для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="49bc9-132">An [**SWbemQualifierSet**](swbemqualifierset.md) object, which is the collection of qualifiers for this property.</span></span><br/> |
| [<span data-ttu-id="49bc9-133">**Значение**</span><span class="sxs-lookup"><span data-stu-id="49bc9-133">**Value**</span></span>](swbemproperty-value.md)<br/>              | <span data-ttu-id="49bc9-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="49bc9-134">Read/write</span></span><br/> | <span data-ttu-id="49bc9-135">Фактическое значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="49bc9-135">Actual value of this property.</span></span> <span data-ttu-id="49bc9-136">Это свойство автоматизации данного объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49bc9-136">This is the default automation property of this object.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="49bc9-137">Требования</span><span class="sxs-lookup"><span data-stu-id="49bc9-137">Requirements</span></span>



| <span data-ttu-id="49bc9-138">Требование</span><span class="sxs-lookup"><span data-stu-id="49bc9-138">Requirement</span></span> | <span data-ttu-id="49bc9-139">Значение</span><span class="sxs-lookup"><span data-stu-id="49bc9-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49bc9-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49bc9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="49bc9-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49bc9-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49bc9-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49bc9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="49bc9-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49bc9-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49bc9-144">Header</span><span class="sxs-lookup"><span data-stu-id="49bc9-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="49bc9-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="49bc9-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="49bc9-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="49bc9-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="49bc9-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="49bc9-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="49bc9-148">DLL</span><span class="sxs-lookup"><span data-stu-id="49bc9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49bc9-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49bc9-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="49bc9-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="49bc9-150">CLSID</span></span><br/>                    | <span data-ttu-id="49bc9-151">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="49bc9-151">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="49bc9-152">IID</span><span class="sxs-lookup"><span data-stu-id="49bc9-152">IID</span></span><br/>                      | <span data-ttu-id="49bc9-153">IID \_ исвбемпроперти</span><span class="sxs-lookup"><span data-stu-id="49bc9-153">IID\_ISWbemProperty</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="49bc9-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49bc9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49bc9-155">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="49bc9-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




