---
description: '\_тип содержимого \_ WPD \_ профиль беспроводной сети \_'
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999c8aec77c6ff046690e4c3450c0643d685e1db
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423704"
---
# <a name="wpd_content_type_wireless_profile"></a><span data-ttu-id="44711-103">\_тип содержимого \_ WPD \_ профиль беспроводной сети \_</span><span class="sxs-lookup"><span data-stu-id="44711-103">WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE</span></span>

<span data-ttu-id="44711-104">Объект, описывающий его тип как \_ тип содержимого \_ WPD \_ Wireless \_ Profile, представляет сведения, используемые для доступа к беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="44711-104">An object that describes its type as WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE represents information used to access a wireless network.</span></span>

<span data-ttu-id="44711-105">Этот тип объекта поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="44711-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="44711-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="44711-106">Property Name</span></span>             | <span data-ttu-id="44711-107">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="44711-107">Required or Optional</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="44711-108">\_идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="44711-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="44711-109">Required.</span></span>                                                             |
| [<span data-ttu-id="44711-110">\_ \_ идентификатор родительского объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="44711-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="44711-111">Required.</span></span>                                                             |
| [<span data-ttu-id="44711-112">\_имя объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="44711-113">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="44711-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="44711-114">\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="44711-115">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="44711-115">Required.</span></span>                                                             |
| [<span data-ttu-id="44711-116">\_Формат объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="44711-117">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="44711-117">Required.</span></span>                                                             |
| [<span data-ttu-id="44711-118">\_ \_ тип содержимого объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="44711-119">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="44711-119">Required.</span></span>                                                             |
| [<span data-ttu-id="44711-120">\_объект WPD \_</span><span class="sxs-lookup"><span data-stu-id="44711-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="44711-121">Требуется, если объект скрыт.</span><span class="sxs-lookup"><span data-stu-id="44711-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="44711-122">\_система объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="44711-123">Требуется, если объект является системным объектом (представляет системный файл).</span><span class="sxs-lookup"><span data-stu-id="44711-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="44711-124">\_размер объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="44711-125">Требуется, если у объекта есть по крайней мере один ресурс.</span><span class="sxs-lookup"><span data-stu-id="44711-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="44711-126">\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD</span><span class="sxs-lookup"><span data-stu-id="44711-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="44711-127">Требуется, если объект представляет файл.</span><span class="sxs-lookup"><span data-stu-id="44711-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="44711-128">\_объект WPD \_ не \_ поднимается</span><span class="sxs-lookup"><span data-stu-id="44711-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="44711-129">Рекомендуется, если объект не предназначен для использования устройством.</span><span class="sxs-lookup"><span data-stu-id="44711-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="44711-130">\_ \_ ссылки на объекты WPD</span><span class="sxs-lookup"><span data-stu-id="44711-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="44711-131">Требуется, если объект содержит ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="44711-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="44711-132">\_ \_ Ключевые слова объекта WPD</span><span class="sxs-lookup"><span data-stu-id="44711-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="44711-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="44711-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="44711-134">\_ \_ идентификатор синхронизации объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="44711-135">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="44711-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="44711-136">\_объект WPD \_ \_ защищен DRM \_</span><span class="sxs-lookup"><span data-stu-id="44711-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="44711-137">Требуется, если объект защищен с помощью технологии DRM.</span><span class="sxs-lookup"><span data-stu-id="44711-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="44711-138">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="44711-139">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="44711-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="44711-140">\_ \_ Дата изменения объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="44711-141">(рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="44711-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="44711-142">\_ \_ Дата создания объекта \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="44711-143">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="44711-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="44711-144">\_ \_ обратные ссылки объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="44711-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="44711-145">Рекомендуется, если на объект ссылается другой объект.</span><span class="sxs-lookup"><span data-stu-id="44711-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="44711-146">\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD</span><span class="sxs-lookup"><span data-stu-id="44711-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="44711-147">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="44711-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="44711-148">Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса</span><span class="sxs-lookup"><span data-stu-id="44711-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="44711-149">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="44711-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="44711-150">\_объект WPD \_ может \_ удалить</span><span class="sxs-lookup"><span data-stu-id="44711-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="44711-151">Требуется, если объект не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="44711-151">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="44711-152">\_ \_ языковой стандарт объекта WPD \_</span><span class="sxs-lookup"><span data-stu-id="44711-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="44711-153">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="44711-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="44711-154">Типичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="44711-154">Typical Resources</span></span>

<span data-ttu-id="44711-155">Эти объекты обычно включают в себя следующие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="44711-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="44711-156">Имя ресурса</span><span class="sxs-lookup"><span data-stu-id="44711-156">Resource Name</span></span>                                          | <span data-ttu-id="44711-157">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="44711-157">Required or Optional</span></span>                                  | <span data-ttu-id="44711-158">Описание</span><span class="sxs-lookup"><span data-stu-id="44711-158">Description</span></span>               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [<span data-ttu-id="44711-159">**\_ресурс \_ по умолчанию для WPD**</span><span class="sxs-lookup"><span data-stu-id="44711-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="44711-160">Требуется, если объект представлен двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="44711-160">Required if the object is represented by binary data.</span></span> | <span data-ttu-id="44711-161">Содержит двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="44711-161">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="44711-162">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="44711-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44711-163">**Требования к объектам**</span><span class="sxs-lookup"><span data-stu-id="44711-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



