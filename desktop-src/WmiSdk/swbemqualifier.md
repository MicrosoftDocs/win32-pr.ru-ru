---
description: Свойства объекта Свбемкуалифиер можно использовать для представления одного квалификатора класса, экземпляра, свойства или параметра метода WMI. Не удается создать этот объект с помощью вызова функции VBScript.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Объект Свбемкуалифиер (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263791"
---
# <a name="swbemqualifier-object"></a><span data-ttu-id="7c92a-104">Объект Свбемкуалифиер</span><span class="sxs-lookup"><span data-stu-id="7c92a-104">SWbemQualifier object</span></span>

<span data-ttu-id="7c92a-105">Свойства объекта **свбемкуалифиер** можно использовать для представления одного квалификатора класса, экземпляра, свойства или параметра метода WMI.</span><span class="sxs-lookup"><span data-stu-id="7c92a-105">You can use the properties of the **SWbemQualifier** object to represent a single qualifier of a WMI class, instance, property, or method parameter.</span></span> <span data-ttu-id="7c92a-106">Не удается создать этот объект с [помощью вызова функции](creating-an-object-using-vbscript.md) VBScript.</span><span class="sxs-lookup"><span data-stu-id="7c92a-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="7c92a-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="7c92a-107">Members</span></span>

<span data-ttu-id="7c92a-108">Объект **свбемкуалифиер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7c92a-108">The **SWbemQualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="7c92a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="7c92a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c92a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7c92a-110">Properties</span></span>

<span data-ttu-id="7c92a-111">Объект **свбемкуалифиер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7c92a-111">The **SWbemQualifier** object has these properties.</span></span>



| <span data-ttu-id="7c92a-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="7c92a-112">Property</span></span>                                                                       | <span data-ttu-id="7c92a-113">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7c92a-113">Access type</span></span>           | <span data-ttu-id="7c92a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7c92a-114">Description</span></span>                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c92a-115">**Изменено**</span><span class="sxs-lookup"><span data-stu-id="7c92a-115">**IsAmended**</span></span>](swbemqualifier-isamended.md)<br/>                       | <span data-ttu-id="7c92a-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c92a-116">Read-only</span></span><br/>  | <span data-ttu-id="7c92a-117">Логическое значение, указывающее, был ли этот квалификатор локализован с помощью операции MERGE.</span><span class="sxs-lookup"><span data-stu-id="7c92a-117">Boolean value that indicates if this qualifier has been localized using a merge operation.</span></span><br/> |
| [<span data-ttu-id="7c92a-118">**Локальный**</span><span class="sxs-lookup"><span data-stu-id="7c92a-118">**IsLocal**</span></span>](swbemqualifier-islocal.md)<br/>                           | <span data-ttu-id="7c92a-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c92a-119">Read-only</span></span><br/>  | <span data-ttu-id="7c92a-120">Логическое значение, указывающее, является ли этот квалификатор локальным.</span><span class="sxs-lookup"><span data-stu-id="7c92a-120">Boolean value that indicates if this qualifier is local.</span></span><br/>                                   |
| [<span data-ttu-id="7c92a-121">**Допускающий переопределение**</span><span class="sxs-lookup"><span data-stu-id="7c92a-121">**IsOverridable**</span></span>](swbemqualifier-isoverridable.md)<br/>               | <span data-ttu-id="7c92a-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7c92a-122">Read/write</span></span><br/> | <span data-ttu-id="7c92a-123">Логическое значение, указывающее, можно ли переопределить этот квалификатор при распространении.</span><span class="sxs-lookup"><span data-stu-id="7c92a-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span><br/>          |
| [<span data-ttu-id="7c92a-124">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7c92a-124">**Name**</span></span>](swbemqualifier-name.md)<br/>                                 | <span data-ttu-id="7c92a-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c92a-125">Read-only</span></span><br/>  | <span data-ttu-id="7c92a-126">Имя этого квалификатора.</span><span class="sxs-lookup"><span data-stu-id="7c92a-126">Name of this qualifier.</span></span><br/>                                                                    |
| [<span data-ttu-id="7c92a-127">**пропагатестоинстанце**</span><span class="sxs-lookup"><span data-stu-id="7c92a-127">**PropagatesToInstance**</span></span>](swbemqualifier-propagatestoinstance.md)<br/> | <span data-ttu-id="7c92a-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7c92a-128">Read/write</span></span><br/> | <span data-ttu-id="7c92a-129">Логическое значение, указывающее, может ли этот квалификатор распространяться на экземпляр.</span><span class="sxs-lookup"><span data-stu-id="7c92a-129">Boolean value that indicates if this qualifier can be propagated to an instance.</span></span><br/>           |
| [<span data-ttu-id="7c92a-130">**пропагатестосубкласс**</span><span class="sxs-lookup"><span data-stu-id="7c92a-130">**PropagatesToSubClass**</span></span>](swbemqualifier-propagatestosubclass.md)<br/> | <span data-ttu-id="7c92a-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7c92a-131">Read-only</span></span><br/>  | <span data-ttu-id="7c92a-132">Логическое значение, указывающее, можно ли распространить этот квалификатор в подкласс.</span><span class="sxs-lookup"><span data-stu-id="7c92a-132">Boolean value that indicates if this qualifier can be propagated to a subclass.</span></span><br/>            |
| [<span data-ttu-id="7c92a-133">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7c92a-133">**Value**</span></span>](swbemqualifier-value.md)<br/>                               | <span data-ttu-id="7c92a-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7c92a-134">Read/write</span></span><br/> | <span data-ttu-id="7c92a-135">Значение Variant этого квалификатора.</span><span class="sxs-lookup"><span data-stu-id="7c92a-135">Variant value of this qualifier.</span></span> <span data-ttu-id="7c92a-136">Это свойство данного объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c92a-136">This is the default property of this object.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="7c92a-137">Требования</span><span class="sxs-lookup"><span data-stu-id="7c92a-137">Requirements</span></span>



| <span data-ttu-id="7c92a-138">Требование</span><span class="sxs-lookup"><span data-stu-id="7c92a-138">Requirement</span></span> | <span data-ttu-id="7c92a-139">Значение</span><span class="sxs-lookup"><span data-stu-id="7c92a-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c92a-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c92a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7c92a-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c92a-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c92a-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c92a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7c92a-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c92a-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c92a-144">Header</span><span class="sxs-lookup"><span data-stu-id="7c92a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c92a-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c92a-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c92a-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7c92a-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c92a-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c92a-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c92a-148">DLL</span><span class="sxs-lookup"><span data-stu-id="7c92a-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c92a-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c92a-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c92a-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="7c92a-150">CLSID</span></span><br/>                    | <span data-ttu-id="7c92a-151">\_СВБЕМКУАЛИФИЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="7c92a-151">CLSID\_SWbemQualifier</span></span><br/>                                                        |
| <span data-ttu-id="7c92a-152">IID</span><span class="sxs-lookup"><span data-stu-id="7c92a-152">IID</span></span><br/>                      | <span data-ttu-id="7c92a-153">IID \_ исвбемкуалифиер</span><span class="sxs-lookup"><span data-stu-id="7c92a-153">IID\_ISWbemQualifier</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="7c92a-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c92a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c92a-155">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="7c92a-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




