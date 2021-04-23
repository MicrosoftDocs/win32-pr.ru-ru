---
title: Атрибут Усерратинг
description: Атрибут Усерратинг — это оценка, заданная пользователем в библиотеке.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Усерратинг атрибут Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704058"
---
# <a name="userrating-attribute"></a><span data-ttu-id="6e7fa-104">Атрибут Усерратинг</span><span class="sxs-lookup"><span data-stu-id="6e7fa-104">UserRating Attribute</span></span>

<span data-ttu-id="6e7fa-105">Атрибут **усерратинг** — это оценка, заданная пользователем в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-105">The **UserRating** attribute is the rating specified by the user in the library.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6e7fa-106">Применение</span><span class="sxs-lookup"><span data-stu-id="6e7fa-106">Applies To</span></span>

-   [<span data-ttu-id="6e7fa-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="6e7fa-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6e7fa-108">Другие элементы</span><span class="sxs-lookup"><span data-stu-id="6e7fa-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="6e7fa-109">Элементы фото</span><span class="sxs-lookup"><span data-stu-id="6e7fa-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="6e7fa-110">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="6e7fa-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="6e7fa-111">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="6e7fa-111">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6e7fa-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e7fa-112">Remarks</span></span>

<span data-ttu-id="6e7fa-113">Рейтинги пользователей представлены целыми значениями, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-113">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="6e7fa-114">При указании значения используйте одно из значений в столбце запись значения.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-114">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="6e7fa-115">При извлечении значений можно использовать диапазоны в столбце значения для чтения, чтобы определить количество звезд.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-115">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="6e7fa-116">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="6e7fa-116">Rating</span></span>  | <span data-ttu-id="6e7fa-117">Запись значения</span><span class="sxs-lookup"><span data-stu-id="6e7fa-117">Writing value</span></span> | <span data-ttu-id="6e7fa-118">Считывание значений</span><span class="sxs-lookup"><span data-stu-id="6e7fa-118">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="6e7fa-119">Запретить</span><span class="sxs-lookup"><span data-stu-id="6e7fa-119">Unrated</span></span> | <span data-ttu-id="6e7fa-120">0</span><span class="sxs-lookup"><span data-stu-id="6e7fa-120">0</span></span>             | <span data-ttu-id="6e7fa-121">0</span><span class="sxs-lookup"><span data-stu-id="6e7fa-121">0</span></span>              |
| <span data-ttu-id="6e7fa-122">1 звезда</span><span class="sxs-lookup"><span data-stu-id="6e7fa-122">1 star</span></span>  | <span data-ttu-id="6e7fa-123">1</span><span class="sxs-lookup"><span data-stu-id="6e7fa-123">1</span></span>             | <span data-ttu-id="6e7fa-124">От 1 до 12.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-124">1 to 12</span></span>        |
| <span data-ttu-id="6e7fa-125">2 звезды</span><span class="sxs-lookup"><span data-stu-id="6e7fa-125">2 stars</span></span> | <span data-ttu-id="6e7fa-126">25</span><span class="sxs-lookup"><span data-stu-id="6e7fa-126">25</span></span>            | <span data-ttu-id="6e7fa-127">от 13 до 37</span><span class="sxs-lookup"><span data-stu-id="6e7fa-127">13 to 37</span></span>       |
| <span data-ttu-id="6e7fa-128">3 звезды</span><span class="sxs-lookup"><span data-stu-id="6e7fa-128">3 stars</span></span> | <span data-ttu-id="6e7fa-129">50</span><span class="sxs-lookup"><span data-stu-id="6e7fa-129">50</span></span>            | <span data-ttu-id="6e7fa-130">от 38 до 62</span><span class="sxs-lookup"><span data-stu-id="6e7fa-130">38 to 62</span></span>       |
| <span data-ttu-id="6e7fa-131">4 звезды</span><span class="sxs-lookup"><span data-stu-id="6e7fa-131">4 stars</span></span> | <span data-ttu-id="6e7fa-132">75</span><span class="sxs-lookup"><span data-stu-id="6e7fa-132">75</span></span>            | <span data-ttu-id="6e7fa-133">от 63 до 86</span><span class="sxs-lookup"><span data-stu-id="6e7fa-133">63 to 86</span></span>       |
| <span data-ttu-id="6e7fa-134">5 звезд</span><span class="sxs-lookup"><span data-stu-id="6e7fa-134">5 stars</span></span> | <span data-ttu-id="6e7fa-135">99</span><span class="sxs-lookup"><span data-stu-id="6e7fa-135">99</span></span>            | <span data-ttu-id="6e7fa-136">от 87 до 99</span><span class="sxs-lookup"><span data-stu-id="6e7fa-136">87 to 99</span></span>       |



 

<span data-ttu-id="6e7fa-137">Этот атрибут хранится только в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-137">This attribute is stored only in the library.</span></span>

<span data-ttu-id="6e7fa-138">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6e7fa-138">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e7fa-139">Требования</span><span class="sxs-lookup"><span data-stu-id="6e7fa-139">Requirements</span></span>



| <span data-ttu-id="6e7fa-140">Требование</span><span class="sxs-lookup"><span data-stu-id="6e7fa-140">Requirement</span></span> | <span data-ttu-id="6e7fa-141">Значение</span><span class="sxs-lookup"><span data-stu-id="6e7fa-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7fa-142">Версия</span><span class="sxs-lookup"><span data-stu-id="6e7fa-142">Version</span></span><br/> | <span data-ttu-id="6e7fa-143">Проигрыватель Windows Media 9 Series или более поздней версии (элемент Photo поддерживается только в проигрывателе Windows Media 10 или более поздней версии)</span><span class="sxs-lookup"><span data-stu-id="6e7fa-143">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e7fa-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e7fa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e7fa-145">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="6e7fa-145">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





