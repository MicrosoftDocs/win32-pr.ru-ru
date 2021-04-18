---
description: '\_ \_ \_ универсальный \_ файл типа содержимого WPD'
ms.assetid: e652bebc-fb3d-48cd-af59-3ad97a79711d
title: WPD_CONTENT_TYPE_GENERIC_FILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8575eba29f5b4b92570f6ee8e39a4ad6405ebf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712559"
---
# <a name="wpd_content_type_generic_file"></a><span data-ttu-id="6438b-103">\_ \_ \_ универсальный \_ файл типа содержимого WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-103">WPD\_CONTENT\_TYPE\_GENERIC\_FILE</span></span>

<span data-ttu-id="6438b-104">Объект, описывающий его тип как \_ \_ универсальный файл типа содержимого WPD \_ \_ , представляет универсальный объект с базовым физическим файлом.</span><span class="sxs-lookup"><span data-stu-id="6438b-104">An object that describes its type as WPD\_CONTENT\_TYPE\_GENERIC\_FILE represents a generic object with an underlying physical file.</span></span> <span data-ttu-id="6438b-105">Различие между этим типом и \_ типом содержимого WPD \_ \_ не указано, что неопределенный объект является более универсальным и не обязательно должен иметь базовый файл.</span><span class="sxs-lookup"><span data-stu-id="6438b-105">The difference between this type and WPD\_CONTENT\_TYPE\_UNSPECIFIED is that an UNSPECIFIED object is more generic and is not required to have an underlying file.</span></span> <span data-ttu-id="6438b-106">Этот тип объекта может быть создан для хранения данных неопределенного типа, который не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="6438b-106">This type of object might be created to hold data of an unspecified type that the device is not meant to consume.</span></span>

<span data-ttu-id="6438b-107">Этот тип объекта поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6438b-107">This type of object supports the following properties.</span></span>



| <span data-ttu-id="6438b-108">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="6438b-108">Property Name</span></span>                                                                                                         | <span data-ttu-id="6438b-109">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="6438b-109">Required or Optional</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="6438b-110">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-110">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="6438b-111">Обязательно, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6438b-111">Required, read-only.</span></span> <span data-ttu-id="6438b-112">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="6438b-112">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="6438b-113">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-113">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="6438b-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6438b-114">Required.</span></span>                                                                      |
| [<span data-ttu-id="6438b-115">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-115">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="6438b-116">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="6438b-116">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="6438b-117">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-117">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="6438b-118">Обязательно, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6438b-118">Required, read-only.</span></span> <span data-ttu-id="6438b-119">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="6438b-119">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="6438b-120">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-120">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="6438b-121">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6438b-121">Required.</span></span>                                                                      |
| [<span data-ttu-id="6438b-122">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-122">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="6438b-123">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6438b-123">Required.</span></span>                                                                      |
| [<span data-ttu-id="6438b-124">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="6438b-124">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="6438b-125">Требуется, если объект скрыт.</span><span class="sxs-lookup"><span data-stu-id="6438b-125">Required if the object is hidden.</span></span>                                              |
| [<span data-ttu-id="6438b-126">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-126">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="6438b-127">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="6438b-127">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="6438b-128">\_размер объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-128">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="6438b-129">Требуется, если у объекта есть по крайней мере один ресурс.</span><span class="sxs-lookup"><span data-stu-id="6438b-129">Required if the object has at least one resource.</span></span>                              |
| [<span data-ttu-id="6438b-130">\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-130">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="6438b-131">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="6438b-131">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="6438b-132">\_объект WPD \_ не \_ поднимается</span><span class="sxs-lookup"><span data-stu-id="6438b-132">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="6438b-133">Рекомендуется, если объект не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="6438b-133">Recommended if the object is not meant for consumption by the device.</span></span>          |
| [<span data-ttu-id="6438b-134">\_ \_ ссылки на объекты WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-134">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="6438b-135">Требуется, если объект содержит ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="6438b-135">Required if the object has references to other objects.</span></span>                        |
| [<span data-ttu-id="6438b-136">\_ \_ Ключевые слова объекта WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-136">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="6438b-137">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6438b-137">Optional.</span></span>                                                                      |
| [<span data-ttu-id="6438b-138">\_ \_ идентификатор синхронизации объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-138">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="6438b-139">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6438b-139">Optional.</span></span>                                                                      |
| [<span data-ttu-id="6438b-140">\_объект WPD \_ \_ защищен DRM \_</span><span class="sxs-lookup"><span data-stu-id="6438b-140">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="6438b-141">Требуется, если объект защищен с помощью технологии DRM.</span><span class="sxs-lookup"><span data-stu-id="6438b-141">Required if the object is protected by DRM technology.</span></span>                         |
| [<span data-ttu-id="6438b-142">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-142">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="6438b-143">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6438b-143">Optional.</span></span>                                                                      |
| [<span data-ttu-id="6438b-144">\_ \_ Дата изменения объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-144">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="6438b-145">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="6438b-145">Recommended.</span></span>                                                                   |
| [<span data-ttu-id="6438b-146">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-146">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="6438b-147">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6438b-147">Optional.</span></span>                                                                      |
| [<span data-ttu-id="6438b-148">\_ \_ обратные ссылки объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="6438b-148">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="6438b-149">Рекомендуется, если на объект ссылается другой объект.</span><span class="sxs-lookup"><span data-stu-id="6438b-149">Recommended if the object is referenced by another object.</span></span>                     |
| [<span data-ttu-id="6438b-150">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="6438b-150">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="6438b-151">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6438b-151">Optional.</span></span>                                                                      |
| [<span data-ttu-id="6438b-152">Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса</span><span class="sxs-lookup"><span data-stu-id="6438b-152">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="6438b-153">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6438b-153">Optional.</span></span>                                                                      |
| [<span data-ttu-id="6438b-154">\_объект WPD \_ может \_ удалить</span><span class="sxs-lookup"><span data-stu-id="6438b-154">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="6438b-155">Требуется, если объект не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="6438b-155">Required if the object cannot be deleted.</span></span>                                      |
| [<span data-ttu-id="6438b-156">\_ \_ языковой стандарт объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="6438b-156">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="6438b-157">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6438b-157">Optional.</span></span>                                                                      |



 

## <a name="typical-resources"></a><span data-ttu-id="6438b-158">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6438b-158">Typical Resources</span></span>

<span data-ttu-id="6438b-159">Эти объекты обычно включают в себя следующие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6438b-159">These objects typically include the following resources.</span></span>



| <span data-ttu-id="6438b-160">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="6438b-160">Resource Name</span></span>                                          | <span data-ttu-id="6438b-161">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="6438b-161">Required or Optional</span></span> | <span data-ttu-id="6438b-162">Описание</span><span class="sxs-lookup"><span data-stu-id="6438b-162">Description</span></span>             |
|--------------------------------------------------------|----------------------|-------------------------|
| [<span data-ttu-id="6438b-163">**\_ресурс \_ по умолчанию для WPD**</span><span class="sxs-lookup"><span data-stu-id="6438b-163">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="6438b-164">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6438b-164">Required.</span></span>            | <span data-ttu-id="6438b-165">Содержит данные файла.</span><span class="sxs-lookup"><span data-stu-id="6438b-165">Contains the file data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6438b-166">См. также</span><span class="sxs-lookup"><span data-stu-id="6438b-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6438b-167">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="6438b-167">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



