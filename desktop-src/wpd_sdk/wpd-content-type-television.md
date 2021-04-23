---
description: Объект, описывающий его тип как \_ тип содержимого \_ WPD \_ телевидение, представляет запись телевизионных передач.
ms.assetid: b8e8da1a-94a9-4540-a4eb-fe0c0cd383f9
title: WPD_CONTENT_TYPE_TELEVISION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5141be847c0701f8828af0de8df41b8be21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347382"
---
# <a name="wpd_content_type_television"></a><span data-ttu-id="a363e-103">\_ \_ телевидение типа содержимого \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-103">WPD\_CONTENT\_TYPE\_TELEVISION</span></span>

<span data-ttu-id="a363e-104">Объект, описывающий его тип как \_ тип содержимого \_ WPD \_ телевидение, представляет запись телевизионных передач.</span><span class="sxs-lookup"><span data-stu-id="a363e-104">An object that describes its type as WPD\_CONTENT\_TYPE\_TELEVISION represents a television recording.</span></span>

<span data-ttu-id="a363e-105">Этот тип объекта должен содержать следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a363e-105">This type of object should host the following properties.</span></span>



| <span data-ttu-id="a363e-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="a363e-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="a363e-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="a363e-107">Required or Optional</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="a363e-108">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="a363e-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a363e-109">Required.</span></span>                                                                    |
| [<span data-ttu-id="a363e-110">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="a363e-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a363e-111">Required.</span></span>                                                                    |
| [<span data-ttu-id="a363e-112">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="a363e-113">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="a363e-113">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="a363e-114">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="a363e-115">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a363e-115">Required.</span></span>                                                                    |
| [<span data-ttu-id="a363e-116">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="a363e-117">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a363e-117">Required.</span></span>                                                                    |
| [<span data-ttu-id="a363e-118">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="a363e-119">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a363e-119">Required.</span></span>                                                                    |
| [<span data-ttu-id="a363e-120">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="a363e-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="a363e-121">Требуется, если объект скрыт.</span><span class="sxs-lookup"><span data-stu-id="a363e-121">Required if the object is hidden.</span></span>                                            |
| [<span data-ttu-id="a363e-122">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="a363e-123">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="a363e-123">Required if the object is a system object (represents a system file).</span></span>        |
| [<span data-ttu-id="a363e-124">\_размер объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="a363e-125">Требуется, если у объекта есть по крайней мере один ресурс.</span><span class="sxs-lookup"><span data-stu-id="a363e-125">Required if the object has at least one resource.</span></span>                            |
| [<span data-ttu-id="a363e-126">\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="a363e-127">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="a363e-127">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="a363e-128">\_объект WPD \_ не \_ поднимается</span><span class="sxs-lookup"><span data-stu-id="a363e-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="a363e-129">Рекомендуется, если объект не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="a363e-129">Recommended if the object is not meant for consumption by the device.</span></span>        |
| [<span data-ttu-id="a363e-130">\_ \_ ссылки на объекты WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="a363e-131">Требуется, если объект содержит ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="a363e-131">Required if the object has references to other objects.</span></span>                      |
| [<span data-ttu-id="a363e-132">\_ \_ Ключевые слова объекта WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="a363e-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a363e-133">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a363e-134">\_ \_ идентификатор синхронизации объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="a363e-135">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a363e-135">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a363e-136">\_объект WPD \_ \_ защищен DRM \_</span><span class="sxs-lookup"><span data-stu-id="a363e-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="a363e-137">Требуется, если объект защищен с помощью технологии Digital Rights Management.</span><span class="sxs-lookup"><span data-stu-id="a363e-137">Required if the object is protected by Digital Rights Management technology.</span></span> |
| [<span data-ttu-id="a363e-138">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="a363e-139">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a363e-139">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a363e-140">\_ \_ Дата изменения объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="a363e-141">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="a363e-141">Recommended.</span></span>                                                                 |
| [<span data-ttu-id="a363e-142">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="a363e-143">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a363e-143">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a363e-144">\_ \_ обратные ссылки объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="a363e-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="a363e-145">Рекомендуется, если на объект ссылается другой объект.</span><span class="sxs-lookup"><span data-stu-id="a363e-145">Recommended if the object is referenced by another object.</span></span>                   |
| [<span data-ttu-id="a363e-146">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="a363e-147">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a363e-147">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a363e-148">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="a363e-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="a363e-149">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a363e-149">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a363e-150">Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса</span><span class="sxs-lookup"><span data-stu-id="a363e-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="a363e-151">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a363e-151">Optional.</span></span>                                                                    |
| [<span data-ttu-id="a363e-152">\_объект WPD \_ может \_ удалить</span><span class="sxs-lookup"><span data-stu-id="a363e-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="a363e-153">Требуется, если объект не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="a363e-153">Required if the object cannot be deleted.</span></span>                                    |



 

## <a name="typical-resources"></a><span data-ttu-id="a363e-154">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a363e-154">Typical Resources</span></span>

<span data-ttu-id="a363e-155">Нет.</span><span class="sxs-lookup"><span data-stu-id="a363e-155">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="a363e-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a363e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a363e-157">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="a363e-157">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



