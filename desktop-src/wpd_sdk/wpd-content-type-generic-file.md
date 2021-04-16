---
description: '\_ \_ \_ Общее \_ сообщение типа содержимого WPD'
ms.assetid: 8e58d15f-ee51-42c2-9d8b-6c3b9c730ff4
title: WPD_CONTENT_TYPE_GENERIC_MESSAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febde68787366dc0f84b1b187f1393017ceb9c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347395"
---
# <a name="wpd_content_type_generic_message"></a><span data-ttu-id="ab129-103">\_ \_ \_ Общее \_ сообщение типа содержимого WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-103">WPD\_CONTENT\_TYPE\_GENERIC\_MESSAGE</span></span>

<span data-ttu-id="ab129-104">Объект, описывающий его тип как \_ \_ общее сообщение типа содержимого WPD \_ \_ , представляет сообщение, например SMS, электронную почту и т. д.</span><span class="sxs-lookup"><span data-stu-id="ab129-104">An object that describes its type as WPD\_CONTENT\_TYPE\_GENERIC\_MESSAGE represents a message, for example, SMS, e-mail, and so on.</span></span>

<span data-ttu-id="ab129-105">Этот тип объекта поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ab129-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="ab129-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="ab129-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="ab129-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="ab129-107">Required or Optional</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="ab129-108">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="ab129-109">Обязательно, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ab129-109">Required, read-only.</span></span> <span data-ttu-id="ab129-110">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="ab129-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="ab129-111">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="ab129-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ab129-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="ab129-113">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="ab129-114">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="ab129-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="ab129-115">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="ab129-116">Обязательно, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ab129-116">Required, read-only.</span></span> <span data-ttu-id="ab129-117">Клиент не может задать это свойство даже во время создания.</span><span class="sxs-lookup"><span data-stu-id="ab129-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="ab129-118">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="ab129-119">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ab129-119">Required.</span></span>                                                                      |
| [<span data-ttu-id="ab129-120">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="ab129-121">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ab129-121">Required.</span></span>                                                                      |
| [<span data-ttu-id="ab129-122">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="ab129-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="ab129-123">Требуется, если объект скрыт.</span><span class="sxs-lookup"><span data-stu-id="ab129-123">Required if the object is hidden.</span></span>                                              |
| [<span data-ttu-id="ab129-124">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="ab129-125">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="ab129-125">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="ab129-126">\_размер объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="ab129-127">Требуется, если у объекта есть по крайней мере один ресурс.</span><span class="sxs-lookup"><span data-stu-id="ab129-127">Required if the object has at least one resource.</span></span>                              |
| [<span data-ttu-id="ab129-128">\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="ab129-129">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="ab129-129">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="ab129-130">\_объект WPD \_ не \_ поднимается</span><span class="sxs-lookup"><span data-stu-id="ab129-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="ab129-131">Рекомендуется, если объект не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="ab129-131">Recommended if the object is not meant for consumption by the device.</span></span>          |
| [<span data-ttu-id="ab129-132">\_ \_ ссылки на объекты WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="ab129-133">Требуется, если объект содержит ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="ab129-133">Required if the object has references to other objects.</span></span>                        |
| [<span data-ttu-id="ab129-134">\_ \_ Ключевые слова объекта WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="ab129-135">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ab129-135">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ab129-136">\_ \_ идентификатор синхронизации объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="ab129-137">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ab129-137">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ab129-138">\_объект WPD \_ \_ защищен DRM \_</span><span class="sxs-lookup"><span data-stu-id="ab129-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="ab129-139">Требуется, если объект защищен с помощью технологии DRM.</span><span class="sxs-lookup"><span data-stu-id="ab129-139">Required if the object is protected by DRM technology.</span></span>                         |
| [<span data-ttu-id="ab129-140">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="ab129-141">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ab129-141">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ab129-142">\_ \_ Дата изменения объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="ab129-143">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="ab129-143">Recommended.</span></span>                                                                   |
| [<span data-ttu-id="ab129-144">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="ab129-145">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ab129-145">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ab129-146">\_ \_ обратные ссылки объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="ab129-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="ab129-147">Рекомендуется, если на объект ссылается другой объект.</span><span class="sxs-lookup"><span data-stu-id="ab129-147">Recommended if the object is referenced by another object.</span></span>                     |
| [<span data-ttu-id="ab129-148">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="ab129-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="ab129-149">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ab129-149">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ab129-150">Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса</span><span class="sxs-lookup"><span data-stu-id="ab129-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="ab129-151">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ab129-151">Optional.</span></span>                                                                      |
| [<span data-ttu-id="ab129-152">\_объект WPD \_ может \_ удалить</span><span class="sxs-lookup"><span data-stu-id="ab129-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="ab129-153">Требуется, если объект можно удалить.</span><span class="sxs-lookup"><span data-stu-id="ab129-153">Required if the object can be deleted.</span></span>                                         |
| [<span data-ttu-id="ab129-154">\_ \_ языковой стандарт объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="ab129-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="ab129-155">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ab129-155">Optional.</span></span>                                                                      |



 

## <a name="typical-resources"></a><span data-ttu-id="ab129-156">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ab129-156">Typical Resources</span></span>

<span data-ttu-id="ab129-157">Эти объекты обычно включают в себя следующие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ab129-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="ab129-158">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="ab129-158">Resource Name</span></span>                                          | <span data-ttu-id="ab129-159">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="ab129-159">Required or Optional</span></span>                                  | <span data-ttu-id="ab129-160">Описание</span><span class="sxs-lookup"><span data-stu-id="ab129-160">Description</span></span>        |
|--------------------------------------------------------|-------------------------------------------------------|--------------------|
| [<span data-ttu-id="ab129-161">**\_ресурс \_ по умолчанию для WPD**</span><span class="sxs-lookup"><span data-stu-id="ab129-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="ab129-162">Требуется, если объект поддерживается для двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="ab129-162">Required if the object is supported with binary data.</span></span> | <span data-ttu-id="ab129-163">Содержит данные.</span><span class="sxs-lookup"><span data-stu-id="ab129-163">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ab129-164">См. также</span><span class="sxs-lookup"><span data-stu-id="ab129-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab129-165">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="ab129-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



