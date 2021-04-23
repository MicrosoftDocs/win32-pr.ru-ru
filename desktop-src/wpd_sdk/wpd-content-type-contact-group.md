---
description: '\_тип содержимого \_ WPD \_ \_ Группа контактов'
ms.assetid: ddebb789-7e60-4728-a0a4-94c06d8a98f9
title: WPD_CONTENT_TYPE_CONTACT_GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b9db8d82807f854ee6cf04e4654228631eb1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265975"
---
# <a name="wpd_content_type_contact_group"></a><span data-ttu-id="d5175-103">\_тип содержимого \_ WPD \_ \_ Группа контактов</span><span class="sxs-lookup"><span data-stu-id="d5175-103">WPD\_CONTENT\_TYPE\_CONTACT\_GROUP</span></span>

<span data-ttu-id="d5175-104">Объект, описывающий его тип как \_ тип содержимого \_ WPD \_ Группа контактов, \_ представляет группу контактов.</span><span class="sxs-lookup"><span data-stu-id="d5175-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CONTACT\_GROUP represents a group of contacts.</span></span> <span data-ttu-id="d5175-105">Ссылки на объекты WPD этого объекта \_ \_ содержат список идентификаторов объектов для различных \_ \_ \_ контактных объектов типа содержимого WPD.</span><span class="sxs-lookup"><span data-stu-id="d5175-105">This object's WPD\_OBJECT\_REFERENCES contains a list of object IDs for various WPD\_CONTENT\_TYPE\_CONTACT objects.</span></span>

<span data-ttu-id="d5175-106">Этот тип объекта поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d5175-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="d5175-107">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="d5175-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="d5175-108">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="d5175-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="d5175-109">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="d5175-110">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d5175-110">Required.</span></span>                                                             |
| [<span data-ttu-id="d5175-111">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="d5175-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d5175-112">Required.</span></span>                                                             |
| [<span data-ttu-id="d5175-113">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="d5175-114">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="d5175-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="d5175-115">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="d5175-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d5175-116">Required.</span></span>                                                             |
| [<span data-ttu-id="d5175-117">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="d5175-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d5175-118">Required.</span></span>                                                             |
| [<span data-ttu-id="d5175-119">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="d5175-120">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d5175-120">Required.</span></span>                                                             |
| [<span data-ttu-id="d5175-121">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="d5175-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="d5175-122">Требуется, если объект скрыт.</span><span class="sxs-lookup"><span data-stu-id="d5175-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="d5175-123">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="d5175-124">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="d5175-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="d5175-125">\_размер объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="d5175-126">Требуется, если у объекта есть по крайней мере один ресурс.</span><span class="sxs-lookup"><span data-stu-id="d5175-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="d5175-127">\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="d5175-128">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="d5175-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="d5175-129">\_объект WPD \_ не \_ поднимается</span><span class="sxs-lookup"><span data-stu-id="d5175-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="d5175-130">Рекомендуется, если объект не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="d5175-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="d5175-131">\_ \_ ссылки на объекты WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="d5175-132">Требуется, если объект содержит ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="d5175-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="d5175-133">\_ \_ Ключевые слова объекта WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="d5175-134">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d5175-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="d5175-135">\_ \_ идентификатор синхронизации объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="d5175-136">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d5175-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="d5175-137">\_объект WPD \_ \_ защищен DRM \_</span><span class="sxs-lookup"><span data-stu-id="d5175-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="d5175-138">Требуется, если объект защищен с помощью технологии DRM.</span><span class="sxs-lookup"><span data-stu-id="d5175-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="d5175-139">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="d5175-140">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d5175-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="d5175-141">\_ \_ Дата изменения объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="d5175-142">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="d5175-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="d5175-143">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="d5175-144">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d5175-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="d5175-145">\_ \_ обратные ссылки объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="d5175-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="d5175-146">Рекомендуется, если на объект ссылается другой объект.</span><span class="sxs-lookup"><span data-stu-id="d5175-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="d5175-147">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d5175-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="d5175-148">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d5175-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="d5175-149">Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса</span><span class="sxs-lookup"><span data-stu-id="d5175-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="d5175-150">Необязательно</span><span class="sxs-lookup"><span data-stu-id="d5175-150">Optional</span></span>                                                              |
| [<span data-ttu-id="d5175-151">\_объект WPD \_ может \_ удалить</span><span class="sxs-lookup"><span data-stu-id="d5175-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="d5175-152">Требуется, если объект можно удалить.</span><span class="sxs-lookup"><span data-stu-id="d5175-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="d5175-153">\_ \_ языковой стандарт объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="d5175-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="d5175-154">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d5175-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="d5175-155">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d5175-155">Typical Resources</span></span>

<span data-ttu-id="d5175-156">Нет.</span><span class="sxs-lookup"><span data-stu-id="d5175-156">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5175-157">См. также</span><span class="sxs-lookup"><span data-stu-id="d5175-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5175-158">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="d5175-158">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



