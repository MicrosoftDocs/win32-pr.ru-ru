---
description: '\_ \_ программа типа содержимого \_ WPD'
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ddf3c5d406c16891c692e84fb37c4d21757f702
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423774"
---
# <a name="wpd_content_type_program"></a><span data-ttu-id="eeaed-103">\_ \_ программа типа содержимого \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-103">WPD\_CONTENT\_TYPE\_PROGRAM</span></span>

<span data-ttu-id="eeaed-104">Объект, описывающий его тип как \_ программа типа содержимого WPD, \_ \_ представляет исполняемую программу.</span><span class="sxs-lookup"><span data-stu-id="eeaed-104">An object that describes its type as WPD\_CONTENT\_TYPE\_PROGRAM represents an executable program.</span></span>

<span data-ttu-id="eeaed-105">Этот тип объекта поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="eeaed-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="eeaed-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="eeaed-106">Property Name</span></span>     | <span data-ttu-id="eeaed-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="eeaed-107">Required or Optional</span></span>      |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="eeaed-108">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="eeaed-109">Требуется, но только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eeaed-109">Required, but read-only.</span></span> <span data-ttu-id="eeaed-110">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="eeaed-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="eeaed-111">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="eeaed-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eeaed-112">Required.</span></span>                                                                          |
| [<span data-ttu-id="eeaed-113">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="eeaed-114">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="eeaed-114">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="eeaed-115">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="eeaed-116">Обязательно, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eeaed-116">Required, read-only.</span></span> <span data-ttu-id="eeaed-117">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="eeaed-117">A client cannot set this property even at creation time.</span></span>      |
| [<span data-ttu-id="eeaed-118">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="eeaed-119">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eeaed-119">Required.</span></span>                                                                          |
| [<span data-ttu-id="eeaed-120">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="eeaed-121">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eeaed-121">Required.</span></span>                                                                          |
| [<span data-ttu-id="eeaed-122">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="eeaed-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="eeaed-123">Требуется, если объект скрыт.</span><span class="sxs-lookup"><span data-stu-id="eeaed-123">Required if the object is hidden.</span></span>                                                  |
| [<span data-ttu-id="eeaed-124">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="eeaed-125">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="eeaed-125">Required if the object is a system object (represents a system file).</span></span>              |
| [<span data-ttu-id="eeaed-126">\_размер объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="eeaed-127">Требуется, если у объекта есть по крайней мере один ресурс.</span><span class="sxs-lookup"><span data-stu-id="eeaed-127">Required if the object has at least one resource.</span></span>                                  |
| [<span data-ttu-id="eeaed-128">\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="eeaed-129">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="eeaed-129">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="eeaed-130">\_объект WPD \_ не \_ поднимается</span><span class="sxs-lookup"><span data-stu-id="eeaed-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="eeaed-131">Рекомендуется, если объект не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="eeaed-131">Recommended if the object is not meant for consumption by the device.</span></span>              |
| [<span data-ttu-id="eeaed-132">\_ \_ ссылки на объекты WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="eeaed-133">Требуется, если объект содержит ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="eeaed-133">Required if the object has references to other objects.</span></span>                            |
| [<span data-ttu-id="eeaed-134">\_ \_ Ключевые слова объекта WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="eeaed-135">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eeaed-135">Optional.</span></span>                                                                          |
| [<span data-ttu-id="eeaed-136">\_ \_ идентификатор синхронизации объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="eeaed-137">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eeaed-137">Optional.</span></span>                                                                          |
| [<span data-ttu-id="eeaed-138">\_объект WPD \_ \_ защищен DRM \_</span><span class="sxs-lookup"><span data-stu-id="eeaed-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="eeaed-139">Требуется, если объект защищен с помощью технологии DRM.</span><span class="sxs-lookup"><span data-stu-id="eeaed-139">Required if the object is protected by DRM technology.</span></span>                             |
| [<span data-ttu-id="eeaed-140">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="eeaed-141">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eeaed-141">Optional.</span></span>                                                                          |
| [<span data-ttu-id="eeaed-142">\_ \_ Дата изменения объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="eeaed-143">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="eeaed-143">Recommended.</span></span>                                                                       |
| [<span data-ttu-id="eeaed-144">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="eeaed-145">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eeaed-145">Optional.</span></span>                                                                          |
| [<span data-ttu-id="eeaed-146">\_ \_ обратные ссылки объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="eeaed-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="eeaed-147">Рекомендуется, если на объект ссылается другой объект.</span><span class="sxs-lookup"><span data-stu-id="eeaed-147">Recommended if the object is referenced by another object.</span></span>                         |
| [<span data-ttu-id="eeaed-148">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="eeaed-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="eeaed-149">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eeaed-149">Optional.</span></span>                                                                          |
| [<span data-ttu-id="eeaed-150">Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса</span><span class="sxs-lookup"><span data-stu-id="eeaed-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="eeaed-151">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eeaed-151">Optional.</span></span>                                                                          |
| [<span data-ttu-id="eeaed-152">\_объект WPD \_ может \_ удалить</span><span class="sxs-lookup"><span data-stu-id="eeaed-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="eeaed-153">Требуется, если объект не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="eeaed-153">Required if the object cannot be deleted.</span></span>                                          |
| [<span data-ttu-id="eeaed-154">\_ \_ языковой стандарт объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="eeaed-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="eeaed-155">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="eeaed-155">Optional.</span></span>                                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="eeaed-156">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eeaed-156">Typical Resources</span></span>

<span data-ttu-id="eeaed-157">Эти объекты обычно включают в себя следующие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="eeaed-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="eeaed-158">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="eeaed-158">Resource Name</span></span>                                          | <span data-ttu-id="eeaed-159">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="eeaed-159">Required or Optional</span></span> | <span data-ttu-id="eeaed-160">Описание</span><span class="sxs-lookup"><span data-stu-id="eeaed-160">Description</span></span>                |
|--------------------------------------------------------|----------------------|----------------------------|
| [<span data-ttu-id="eeaed-161">**\_ресурс \_ по умолчанию для WPD**</span><span class="sxs-lookup"><span data-stu-id="eeaed-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="eeaed-162">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eeaed-162">Required.</span></span>            | <span data-ttu-id="eeaed-163">Содержит файл программы.</span><span class="sxs-lookup"><span data-stu-id="eeaed-163">Contains the program file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="eeaed-164">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="eeaed-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeaed-165">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="eeaed-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



