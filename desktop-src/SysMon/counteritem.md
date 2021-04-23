---
title: Объект Каунтеритем (Исисмон. h)
description: Этот класс используется для извлечения пути и значения счетчика, а также для указания цвета, используемого для отображения счетчика. Чтобы получить этот объект, вызовите Counters. Item.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- Сисмон объекта Каунтеритем
- Каунтеритем объект Сисмон, описание
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802585"
---
# <a name="counteritem-object"></a><span data-ttu-id="1c042-106">Объект Каунтеритем</span><span class="sxs-lookup"><span data-stu-id="1c042-106">CounterItem object</span></span>

<span data-ttu-id="1c042-107">Этот класс используется для извлечения пути и значения счетчика, а также для указания цвета, используемого для отображения счетчика.</span><span class="sxs-lookup"><span data-stu-id="1c042-107">Use this class to retrieve the path and value of a counter and to specify the color used to graph the counter.</span></span>

<span data-ttu-id="1c042-108">Чтобы получить этот объект, вызовите [**Counters. Item**](counters-item.md).</span><span class="sxs-lookup"><span data-stu-id="1c042-108">To retrieve this object, call [**Counters.Item**](counters-item.md).</span></span>

## <a name="members"></a><span data-ttu-id="1c042-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="1c042-109">Members</span></span>

<span data-ttu-id="1c042-110">Объект **каунтеритем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1c042-110">The **CounterItem** object has these types of members:</span></span>

-   [<span data-ttu-id="1c042-111">Методы</span><span class="sxs-lookup"><span data-stu-id="1c042-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1c042-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c042-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1c042-113">Методы</span><span class="sxs-lookup"><span data-stu-id="1c042-113">Methods</span></span>

<span data-ttu-id="1c042-114">Объект **каунтеритем** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="1c042-114">The **CounterItem** object has these methods.</span></span>



| <span data-ttu-id="1c042-115">Метод</span><span class="sxs-lookup"><span data-stu-id="1c042-115">Method</span></span>                                             | <span data-ttu-id="1c042-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1c042-116">Description</span></span>                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="1c042-117">**жетдатаат**</span><span class="sxs-lookup"><span data-stu-id="1c042-117">**GetDataAt**</span></span>](counteritem-getdataat.md)         | <span data-ttu-id="1c042-118">Извлекает данные счетчиков из определенной точки линейного графика.</span><span class="sxs-lookup"><span data-stu-id="1c042-118">Retrieves the counter data from a specific point in the line graph.</span></span><br/> |
| [<span data-ttu-id="1c042-119">**Статистика**</span><span class="sxs-lookup"><span data-stu-id="1c042-119">**GetStatistics**</span></span>](counteritem-getstatistics.md) | <span data-ttu-id="1c042-120">Возвращает среднее, максимальное и минимальное значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="1c042-120">Retrieves the average, maximum, and minimum values for the counter.</span></span><br/> |
| [<span data-ttu-id="1c042-121">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="1c042-121">**GetValue**</span></span>](counteritem-getvalue.md)           | <span data-ttu-id="1c042-122">Извлекает Последнее значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="1c042-122">Retrieves the last value of the counter.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="1c042-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c042-123">Properties</span></span>

<span data-ttu-id="1c042-124">Объект **каунтеритем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1c042-124">The **CounterItem** object has these properties.</span></span>



| <span data-ttu-id="1c042-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="1c042-125">Property</span></span>                                                  | <span data-ttu-id="1c042-126">Описание</span><span class="sxs-lookup"><span data-stu-id="1c042-126">Description</span></span>                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="1c042-127">**Цвет**</span><span class="sxs-lookup"><span data-stu-id="1c042-127">**Color**</span></span>](counteritem-color.md)<br/>             | <span data-ttu-id="1c042-128">Возвращает или задает цвет, используемый для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="1c042-128">Retrieves or sets the color used to graph the counter value.</span></span><br/>         |
| [<span data-ttu-id="1c042-129">**линестиле**</span><span class="sxs-lookup"><span data-stu-id="1c042-129">**LineStyle**</span></span>](counteritem-linestyle.md)<br/>     | <span data-ttu-id="1c042-130">Возвращает или задает стиль линии, используемый для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="1c042-130">Retrieves or sets the line style used to graph the counter value.</span></span><br/>    |
| [<span data-ttu-id="1c042-131">**Путь**</span><span class="sxs-lookup"><span data-stu-id="1c042-131">**Path**</span></span>](counteritem-path.md)<br/>               | <span data-ttu-id="1c042-132">Получает путь к счетчику.</span><span class="sxs-lookup"><span data-stu-id="1c042-132">Retrieves the path of the counter.</span></span><br/>                                   |
| [<span data-ttu-id="1c042-133">**скалефактор**</span><span class="sxs-lookup"><span data-stu-id="1c042-133">**ScaleFactor**</span></span>](counteritem-scalefactor.md)<br/> | <span data-ttu-id="1c042-134">Возвращает или задает коэффициент масштабирования, используемый для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="1c042-134">Retrieves or sets the scale factor used to graph the counter value.</span></span><br/>  |
| [<span data-ttu-id="1c042-135">**Выбрано**</span><span class="sxs-lookup"><span data-stu-id="1c042-135">**Selected**</span></span>](counteritem-selected.md)<br/>       | <span data-ttu-id="1c042-136">Возвращает или задает значение, указывающее, выбран ли счетчик.</span><span class="sxs-lookup"><span data-stu-id="1c042-136">Retrieves or sets a value that indicates if the counter is selected.</span></span><br/> |
| [<span data-ttu-id="1c042-137">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1c042-137">**Value**</span></span>](counteritem-value.md)<br/>             | <span data-ttu-id="1c042-138">Извлекает текущее значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="1c042-138">Retrieves the current value of the counter.</span></span><br/>                          |
| [<span data-ttu-id="1c042-139">**Visible**</span><span class="sxs-lookup"><span data-stu-id="1c042-139">**Visible**</span></span>](counteritem-visible.md)<br/>         | <span data-ttu-id="1c042-140">Возвращает или задает значение, указывающее, отображается ли счетчик в графе.</span><span class="sxs-lookup"><span data-stu-id="1c042-140">Retrieves or sets a value that indicates if the counter is graphed.</span></span><br/>  |
| [<span data-ttu-id="1c042-141">**Ширина**</span><span class="sxs-lookup"><span data-stu-id="1c042-141">**Width**</span></span>](counteritem-width.md)<br/>             | <span data-ttu-id="1c042-142">Возвращает или задает толщину линии, используемую для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="1c042-142">Retrieves or sets the line width used to graph the counter value.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="1c042-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c042-143">Remarks</span></span>

<span data-ttu-id="1c042-144">[**Значение**](counteritem-value.md) является свойством по умолчанию **каунтеритем**.</span><span class="sxs-lookup"><span data-stu-id="1c042-144">[**Value**](counteritem-value.md) is the default property of **CounterItem**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c042-145">Требования</span><span class="sxs-lookup"><span data-stu-id="1c042-145">Requirements</span></span>



| <span data-ttu-id="1c042-146">Требование</span><span class="sxs-lookup"><span data-stu-id="1c042-146">Requirement</span></span> | <span data-ttu-id="1c042-147">Значение</span><span class="sxs-lookup"><span data-stu-id="1c042-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c042-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c042-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1c042-149">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1c042-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1c042-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c042-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1c042-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1c042-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c042-152">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1c042-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c042-153"><dt>Исисмон. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c042-153"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1c042-154">DLL</span><span class="sxs-lookup"><span data-stu-id="1c042-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c042-155"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1c042-155"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c042-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c042-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c042-157">Классы СИСМОН</span><span class="sxs-lookup"><span data-stu-id="1c042-157">SYSMON Classes</span></span>](sysmon-classes.md)
</dt> </dl>

 

 





