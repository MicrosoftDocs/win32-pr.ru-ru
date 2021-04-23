---
description: '\_ \_ Календарь типа содержимого \_ WPD'
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202b21c0ac690c4a0b9621b876f6926c4c0efe5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702769"
---
# <a name="wpd_content_type_calendar"></a><span data-ttu-id="065ae-103">\_ \_ Календарь типа содержимого \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-103">WPD\_CONTENT\_TYPE\_CALENDAR</span></span>

<span data-ttu-id="065ae-104">Объект, описывающий его тип как \_ тип содержимого \_ WPD \_ Calendar, представляет календарь.</span><span class="sxs-lookup"><span data-stu-id="065ae-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CALENDAR represents a calendar.</span></span> <span data-ttu-id="065ae-105">Объект может представлять собой файл, содержащий сведения календаря, или папку, содержащую другие объекты, связанные с календарем, такие как задачи, встречи и т. д.</span><span class="sxs-lookup"><span data-stu-id="065ae-105">The object can be a file that contains calendar information or a folder that contains other calendar-related objects, such as tasks, appointments, and so on.</span></span>

<span data-ttu-id="065ae-106">Этот тип объекта поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="065ae-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="065ae-107">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="065ae-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="065ae-108">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="065ae-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="065ae-109">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="065ae-110">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="065ae-110">Required.</span></span>                                                             |
| [<span data-ttu-id="065ae-111">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="065ae-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="065ae-112">Required.</span></span>                                                             |
| [<span data-ttu-id="065ae-113">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="065ae-114">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="065ae-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="065ae-115">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="065ae-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="065ae-116">Required.</span></span>                                                             |
| [<span data-ttu-id="065ae-117">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="065ae-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="065ae-118">Required.</span></span>                                                             |
| [<span data-ttu-id="065ae-119">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="065ae-120">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="065ae-120">Required.</span></span>                                                             |
| [<span data-ttu-id="065ae-121">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="065ae-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="065ae-122">Требуется, если объект скрыт.</span><span class="sxs-lookup"><span data-stu-id="065ae-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="065ae-123">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="065ae-124">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="065ae-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="065ae-125">\_размер объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="065ae-126">Требуется, если у объекта есть по крайней мере один ресурс.</span><span class="sxs-lookup"><span data-stu-id="065ae-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="065ae-127">\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="065ae-128">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="065ae-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="065ae-129">\_объект WPD \_ не \_ поднимается</span><span class="sxs-lookup"><span data-stu-id="065ae-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="065ae-130">Рекомендуется, если объект не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="065ae-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="065ae-131">\_ \_ ссылки на объекты WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="065ae-132">Требуется, если объект содержит ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="065ae-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="065ae-133">\_ \_ Ключевые слова объекта WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="065ae-134">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="065ae-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="065ae-135">\_ \_ идентификатор синхронизации объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="065ae-136">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="065ae-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="065ae-137">\_объект WPD \_ \_ защищен DRM \_</span><span class="sxs-lookup"><span data-stu-id="065ae-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="065ae-138">Требуется, если объект защищен с помощью технологии DRM.</span><span class="sxs-lookup"><span data-stu-id="065ae-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="065ae-139">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="065ae-140">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="065ae-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="065ae-141">\_ \_ Дата изменения объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="065ae-142">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="065ae-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="065ae-143">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="065ae-144">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="065ae-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="065ae-145">\_ \_ обратные ссылки объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="065ae-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="065ae-146">Рекомендуется, если на объект ссылается другой объект.</span><span class="sxs-lookup"><span data-stu-id="065ae-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="065ae-147">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="065ae-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="065ae-148">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="065ae-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="065ae-149">Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса</span><span class="sxs-lookup"><span data-stu-id="065ae-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="065ae-150">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="065ae-150">Optional.</span></span>                                                             |
| [<span data-ttu-id="065ae-151">\_объект WPD \_ может \_ удалить</span><span class="sxs-lookup"><span data-stu-id="065ae-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="065ae-152">Требуется, если объект можно удалить.</span><span class="sxs-lookup"><span data-stu-id="065ae-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="065ae-153">\_ \_ языковой стандарт объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="065ae-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="065ae-154">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="065ae-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="065ae-155">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="065ae-155">Typical Resources</span></span>

<span data-ttu-id="065ae-156">Эти объекты обычно включают в себя следующие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="065ae-156">These objects typically include the following resources.</span></span>



| <span data-ttu-id="065ae-157">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="065ae-157">Resource Name</span></span>                                          | <span data-ttu-id="065ae-158">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="065ae-158">Required or Optional</span></span>                             | <span data-ttu-id="065ae-159">Описание</span><span class="sxs-lookup"><span data-stu-id="065ae-159">Description</span></span>        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [<span data-ttu-id="065ae-160">**\_ресурс \_ по умолчанию для WPD**</span><span class="sxs-lookup"><span data-stu-id="065ae-160">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="065ae-161">Требуется, если объект поддерживается двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="065ae-161">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="065ae-162">Содержит данные.</span><span class="sxs-lookup"><span data-stu-id="065ae-162">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="065ae-163">См. также</span><span class="sxs-lookup"><span data-stu-id="065ae-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="065ae-164">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="065ae-164">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



