---
title: Атрибут Усереффективератинг
description: Атрибут Усереффективератинг — это оценка, вычисленная проигрывателем Windows Media в зависимости от частоты воспроизведения элемента.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- Усереффективератинг атрибут Windows Media Player
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717851"
---
# <a name="usereffectiverating-attribute"></a><span data-ttu-id="4e8b5-104">Атрибут Усереффективератинг</span><span class="sxs-lookup"><span data-stu-id="4e8b5-104">UserEffectiveRating Attribute</span></span>

<span data-ttu-id="4e8b5-105">Атрибут **усереффективератинг** — это оценка, вычисленная проигрывателем Windows Media в зависимости от частоты воспроизведения элемента.</span><span class="sxs-lookup"><span data-stu-id="4e8b5-105">The **UserEffectiveRating** attribute is the rating computed by Windows Media Player based on how often the item has been played.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4e8b5-106">Применение</span><span class="sxs-lookup"><span data-stu-id="4e8b5-106">Applies To</span></span>

-   [<span data-ttu-id="4e8b5-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="4e8b5-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="4e8b5-108">Другие элементы</span><span class="sxs-lookup"><span data-stu-id="4e8b5-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="4e8b5-109">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="4e8b5-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="4e8b5-110">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="4e8b5-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4e8b5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e8b5-111">Remarks</span></span>

<span data-ttu-id="4e8b5-112">Рейтинги пользователей представлены целыми значениями, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4e8b5-112">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="4e8b5-113">При указании значения используйте одно из значений в столбце запись значения.</span><span class="sxs-lookup"><span data-stu-id="4e8b5-113">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="4e8b5-114">При извлечении значений можно использовать диапазоны в столбце значения для чтения, чтобы определить количество звезд.</span><span class="sxs-lookup"><span data-stu-id="4e8b5-114">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="4e8b5-115">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="4e8b5-115">Rating</span></span>  | <span data-ttu-id="4e8b5-116">Запись значения</span><span class="sxs-lookup"><span data-stu-id="4e8b5-116">Writing value</span></span> | <span data-ttu-id="4e8b5-117">Считывание значений</span><span class="sxs-lookup"><span data-stu-id="4e8b5-117">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="4e8b5-118">Запретить</span><span class="sxs-lookup"><span data-stu-id="4e8b5-118">Unrated</span></span> | <span data-ttu-id="4e8b5-119">0</span><span class="sxs-lookup"><span data-stu-id="4e8b5-119">0</span></span>             | <span data-ttu-id="4e8b5-120">0</span><span class="sxs-lookup"><span data-stu-id="4e8b5-120">0</span></span>              |
| <span data-ttu-id="4e8b5-121">1 звезда</span><span class="sxs-lookup"><span data-stu-id="4e8b5-121">1 star</span></span>  | <span data-ttu-id="4e8b5-122">1</span><span class="sxs-lookup"><span data-stu-id="4e8b5-122">1</span></span>             | <span data-ttu-id="4e8b5-123">От 1 до 12.</span><span class="sxs-lookup"><span data-stu-id="4e8b5-123">1 to 12</span></span>        |
| <span data-ttu-id="4e8b5-124">2 звезды</span><span class="sxs-lookup"><span data-stu-id="4e8b5-124">2 stars</span></span> | <span data-ttu-id="4e8b5-125">25</span><span class="sxs-lookup"><span data-stu-id="4e8b5-125">25</span></span>            | <span data-ttu-id="4e8b5-126">от 13 до 37</span><span class="sxs-lookup"><span data-stu-id="4e8b5-126">13 to 37</span></span>       |
| <span data-ttu-id="4e8b5-127">3 звезды</span><span class="sxs-lookup"><span data-stu-id="4e8b5-127">3 stars</span></span> | <span data-ttu-id="4e8b5-128">50</span><span class="sxs-lookup"><span data-stu-id="4e8b5-128">50</span></span>            | <span data-ttu-id="4e8b5-129">от 38 до 62</span><span class="sxs-lookup"><span data-stu-id="4e8b5-129">38 to 62</span></span>       |
| <span data-ttu-id="4e8b5-130">4 звезды</span><span class="sxs-lookup"><span data-stu-id="4e8b5-130">4 stars</span></span> | <span data-ttu-id="4e8b5-131">75</span><span class="sxs-lookup"><span data-stu-id="4e8b5-131">75</span></span>            | <span data-ttu-id="4e8b5-132">от 63 до 86</span><span class="sxs-lookup"><span data-stu-id="4e8b5-132">63 to 86</span></span>       |
| <span data-ttu-id="4e8b5-133">5 звезд</span><span class="sxs-lookup"><span data-stu-id="4e8b5-133">5 stars</span></span> | <span data-ttu-id="4e8b5-134">99</span><span class="sxs-lookup"><span data-stu-id="4e8b5-134">99</span></span>            | <span data-ttu-id="4e8b5-135">от 87 до 99</span><span class="sxs-lookup"><span data-stu-id="4e8b5-135">87 to 99</span></span>       |



 

<span data-ttu-id="4e8b5-136">Этот атрибут хранится только в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="4e8b5-136">This attribute is stored only in the library.</span></span>

<span data-ttu-id="4e8b5-137">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4e8b5-137">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e8b5-138">Требования</span><span class="sxs-lookup"><span data-stu-id="4e8b5-138">Requirements</span></span>



| <span data-ttu-id="4e8b5-139">Требование</span><span class="sxs-lookup"><span data-stu-id="4e8b5-139">Requirement</span></span> | <span data-ttu-id="4e8b5-140">Значение</span><span class="sxs-lookup"><span data-stu-id="4e8b5-140">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="4e8b5-141">Версия</span><span class="sxs-lookup"><span data-stu-id="4e8b5-141">Version</span></span><br/> | <span data-ttu-id="4e8b5-142">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4e8b5-142">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e8b5-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e8b5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e8b5-144">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="4e8b5-144">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





