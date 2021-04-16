---
description: '\_ \_ сертификат типа содержимого \_ WPD'
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde0ff631cd8eed28226d1e374d84e65d9756b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702768"
---
# <a name="wpd_content_type_certificate"></a><span data-ttu-id="5d00c-103">\_ \_ сертификат типа содержимого \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-103">WPD\_CONTENT\_TYPE\_CERTIFICATE</span></span>

<span data-ttu-id="5d00c-104">Объект, описывающий его тип как \_ сертификат типа содержимого WPD, \_ \_ представляет сертификат, используемый для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5d00c-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CERTIFICATE represents a certificate used for authentication.</span></span>

<span data-ttu-id="5d00c-105">Этот тип объекта поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5d00c-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="5d00c-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="5d00c-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="5d00c-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="5d00c-107">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="5d00c-108">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="5d00c-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5d00c-109">Required.</span></span>                                                             |
| [<span data-ttu-id="5d00c-110">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="5d00c-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5d00c-111">Required.</span></span>                                                             |
| [<span data-ttu-id="5d00c-112">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="5d00c-113">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="5d00c-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="5d00c-114">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="5d00c-115">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5d00c-115">Required.</span></span>                                                             |
| [<span data-ttu-id="5d00c-116">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="5d00c-117">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5d00c-117">Required.</span></span>                                                             |
| [<span data-ttu-id="5d00c-118">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="5d00c-119">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5d00c-119">Required.</span></span>                                                             |
| [<span data-ttu-id="5d00c-120">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="5d00c-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="5d00c-121">Требуется, если объект скрыт.</span><span class="sxs-lookup"><span data-stu-id="5d00c-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="5d00c-122">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="5d00c-123">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="5d00c-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="5d00c-124">\_размер объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="5d00c-125">Требуется, если у объекта есть по крайней мере один ресурс.</span><span class="sxs-lookup"><span data-stu-id="5d00c-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="5d00c-126">\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="5d00c-127">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="5d00c-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="5d00c-128">\_объект WPD \_ не \_ поднимается</span><span class="sxs-lookup"><span data-stu-id="5d00c-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="5d00c-129">Рекомендуется, если объект не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="5d00c-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="5d00c-130">\_ \_ ссылки на объекты WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="5d00c-131">Требуется, если объект содержит ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="5d00c-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="5d00c-132">\_ \_ Ключевые слова объекта WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="5d00c-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5d00c-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="5d00c-134">\_ \_ идентификатор синхронизации объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="5d00c-135">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5d00c-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="5d00c-136">\_объект WPD \_ \_ защищен DRM \_</span><span class="sxs-lookup"><span data-stu-id="5d00c-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="5d00c-137">Требуется, если объект защищен с помощью технологии DRM.</span><span class="sxs-lookup"><span data-stu-id="5d00c-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="5d00c-138">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="5d00c-139">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5d00c-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="5d00c-140">\_ \_ Дата изменения объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="5d00c-141">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="5d00c-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="5d00c-142">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="5d00c-143">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5d00c-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="5d00c-144">\_ \_ обратные ссылки объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="5d00c-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="5d00c-145">Рекомендуется, если на объект ссылается другой объект.</span><span class="sxs-lookup"><span data-stu-id="5d00c-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="5d00c-146">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="5d00c-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="5d00c-147">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5d00c-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="5d00c-148">Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса</span><span class="sxs-lookup"><span data-stu-id="5d00c-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="5d00c-149">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5d00c-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="5d00c-150">\_объект WPD \_ может \_ удалить</span><span class="sxs-lookup"><span data-stu-id="5d00c-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="5d00c-151">Требуется, если объект можно удалить.</span><span class="sxs-lookup"><span data-stu-id="5d00c-151">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="5d00c-152">\_ \_ языковой стандарт объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="5d00c-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="5d00c-153">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5d00c-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="5d00c-154">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5d00c-154">Typical Resources</span></span>

<span data-ttu-id="5d00c-155">Эти объекты обычно включают в себя следующие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5d00c-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="5d00c-156">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="5d00c-156">Resource Name</span></span>                                          | <span data-ttu-id="5d00c-157">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="5d00c-157">Required or Optional</span></span> | <span data-ttu-id="5d00c-158">Описание</span><span class="sxs-lookup"><span data-stu-id="5d00c-158">Description</span></span>        |
|--------------------------------------------------------|----------------------|--------------------|
| [<span data-ttu-id="5d00c-159">**\_ресурс \_ по умолчанию для WPD**</span><span class="sxs-lookup"><span data-stu-id="5d00c-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="5d00c-160">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5d00c-160">Required.</span></span>            | <span data-ttu-id="5d00c-161">Содержит данные.</span><span class="sxs-lookup"><span data-stu-id="5d00c-161">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5d00c-162">См. также</span><span class="sxs-lookup"><span data-stu-id="5d00c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d00c-163">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="5d00c-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



