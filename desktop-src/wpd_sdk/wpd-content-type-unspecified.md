---
description: '\_тип содержимого WPD не \_ \_ указан'
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd955ee5ebf31b2348efd3f70c85ae9c004edb83
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423684"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="d3571-103">\_тип содержимого WPD не \_ \_ указан</span><span class="sxs-lookup"><span data-stu-id="d3571-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="d3571-104">Объект, описывающий тип \_ содержимого типа данных WPD \_ \_ , не указан, представляет универсальный объект, который может иметь или не иметь базового физического файла.</span><span class="sxs-lookup"><span data-stu-id="d3571-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="d3571-105">Различие между этим типом и \_ \_ \_ универсальным ФАЙЛОМ типа содержимого WPD \_ заключается в том, что универсальный файловый объект типа "WPD" \_ \_ \_ \_ должен иметь базовый физический файл.</span><span class="sxs-lookup"><span data-stu-id="d3571-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="d3571-106">Этот тип объекта поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d3571-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="d3571-107">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="d3571-107">Property Name</span></span>       | <span data-ttu-id="d3571-108">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="d3571-108">Required or Optional</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="d3571-109">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="d3571-110">Обязательно, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d3571-110">Required, read-only.</span></span> <span data-ttu-id="d3571-111">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="d3571-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="d3571-112">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="d3571-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d3571-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="d3571-114">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="d3571-115">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="d3571-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="d3571-116">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="d3571-117">Обязательно, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d3571-117">Required, read-only.</span></span> <span data-ttu-id="d3571-118">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="d3571-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="d3571-119">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="d3571-120">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d3571-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="d3571-121">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="d3571-122">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d3571-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="d3571-123">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="d3571-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="d3571-124">Требуется, если объект скрыт.</span><span class="sxs-lookup"><span data-stu-id="d3571-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="d3571-125">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="d3571-126">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="d3571-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="d3571-127">\_размер объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="d3571-128">Требуется, если у объекта есть по крайней мере один ресурс.</span><span class="sxs-lookup"><span data-stu-id="d3571-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="d3571-129">\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="d3571-130">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="d3571-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="d3571-131">\_объект WPD \_ не \_ поднимается</span><span class="sxs-lookup"><span data-stu-id="d3571-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="d3571-132">Рекомендуется, если объект не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="d3571-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="d3571-133">\_ \_ ссылки на объекты WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="d3571-134">Требуется, если объект содержит ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="d3571-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="d3571-135">\_ \_ Ключевые слова объекта WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="d3571-136">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d3571-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="d3571-137">\_ \_ идентификатор синхронизации объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="d3571-138">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d3571-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="d3571-139">\_объект WPD \_ \_ защищен DRM \_</span><span class="sxs-lookup"><span data-stu-id="d3571-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="d3571-140">Требуется, если объект защищен с помощью технологии DRM.</span><span class="sxs-lookup"><span data-stu-id="d3571-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="d3571-141">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="d3571-142">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d3571-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="d3571-143">\_ \_ Дата изменения объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="d3571-144">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="d3571-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="d3571-145">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="d3571-146">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d3571-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="d3571-147">\_ \_ обратные ссылки объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="d3571-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="d3571-148">Рекомендуется, если на объект ссылается другой объект.</span><span class="sxs-lookup"><span data-stu-id="d3571-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="d3571-149">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d3571-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="d3571-150">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d3571-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="d3571-151">Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса</span><span class="sxs-lookup"><span data-stu-id="d3571-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="d3571-152">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d3571-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="d3571-153">\_объект WPD \_ может \_ удалить</span><span class="sxs-lookup"><span data-stu-id="d3571-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="d3571-154">Требуется, если объект не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="d3571-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="d3571-155">\_ \_ языковой стандарт объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="d3571-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="d3571-156">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d3571-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="d3571-157">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d3571-157">Typical Resources</span></span>

<span data-ttu-id="d3571-158">Эти объекты обычно включают в себя следующие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d3571-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="d3571-159">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="d3571-159">Resource Name</span></span>                                          | <span data-ttu-id="d3571-160">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="d3571-160">Required or Optional</span></span>                             | <span data-ttu-id="d3571-161">Описание</span><span class="sxs-lookup"><span data-stu-id="d3571-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="d3571-162">**\_ресурс \_ по умолчанию для WPD**</span><span class="sxs-lookup"><span data-stu-id="d3571-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="d3571-163">Требуется, если объект поддерживается двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="d3571-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="d3571-164">Содержит двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="d3571-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d3571-165">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d3571-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3571-166">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="d3571-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



