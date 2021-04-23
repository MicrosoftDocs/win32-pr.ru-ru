---
title: Атрибут Усерсервицератинг
description: Атрибут Усерсервицератинг зарезервирован для использования в будущем.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- Усерсервицератинг атрибут Windows Media Player
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704057"
---
# <a name="userservicerating-attribute"></a><span data-ttu-id="3f305-104">Атрибут Усерсервицератинг</span><span class="sxs-lookup"><span data-stu-id="3f305-104">UserServiceRating Attribute</span></span>

<span data-ttu-id="3f305-105">Атрибут **усерсервицератинг** зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="3f305-105">The **UserServiceRating** attribute is reserved for future use.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3f305-106">Применение</span><span class="sxs-lookup"><span data-stu-id="3f305-106">Applies To</span></span>

-   [<span data-ttu-id="3f305-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="3f305-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="3f305-108">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="3f305-108">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="3f305-109">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="3f305-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="3f305-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f305-110">Remarks</span></span>

<span data-ttu-id="3f305-111">Рейтинги пользователей представлены целыми значениями, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3f305-111">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="3f305-112">При указании значения используйте одно из значений в столбце запись значения.</span><span class="sxs-lookup"><span data-stu-id="3f305-112">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="3f305-113">При извлечении значений можно использовать диапазоны в столбце значения для чтения, чтобы определить количество звезд.</span><span class="sxs-lookup"><span data-stu-id="3f305-113">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="3f305-114">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="3f305-114">Rating</span></span>  | <span data-ttu-id="3f305-115">Запись значения</span><span class="sxs-lookup"><span data-stu-id="3f305-115">Writing value</span></span> | <span data-ttu-id="3f305-116">Считывание значений</span><span class="sxs-lookup"><span data-stu-id="3f305-116">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="3f305-117">Запретить</span><span class="sxs-lookup"><span data-stu-id="3f305-117">Unrated</span></span> | <span data-ttu-id="3f305-118">0</span><span class="sxs-lookup"><span data-stu-id="3f305-118">0</span></span>             | <span data-ttu-id="3f305-119">0</span><span class="sxs-lookup"><span data-stu-id="3f305-119">0</span></span>              |
| <span data-ttu-id="3f305-120">1 звезда</span><span class="sxs-lookup"><span data-stu-id="3f305-120">1 star</span></span>  | <span data-ttu-id="3f305-121">1</span><span class="sxs-lookup"><span data-stu-id="3f305-121">1</span></span>             | <span data-ttu-id="3f305-122">От 1 до 12.</span><span class="sxs-lookup"><span data-stu-id="3f305-122">1 to 12</span></span>        |
| <span data-ttu-id="3f305-123">2 звезды</span><span class="sxs-lookup"><span data-stu-id="3f305-123">2 stars</span></span> | <span data-ttu-id="3f305-124">25</span><span class="sxs-lookup"><span data-stu-id="3f305-124">25</span></span>            | <span data-ttu-id="3f305-125">от 13 до 37</span><span class="sxs-lookup"><span data-stu-id="3f305-125">13 to 37</span></span>       |
| <span data-ttu-id="3f305-126">3 звезды</span><span class="sxs-lookup"><span data-stu-id="3f305-126">3 stars</span></span> | <span data-ttu-id="3f305-127">50</span><span class="sxs-lookup"><span data-stu-id="3f305-127">50</span></span>            | <span data-ttu-id="3f305-128">от 38 до 62</span><span class="sxs-lookup"><span data-stu-id="3f305-128">38 to 62</span></span>       |
| <span data-ttu-id="3f305-129">4 звезды</span><span class="sxs-lookup"><span data-stu-id="3f305-129">4 stars</span></span> | <span data-ttu-id="3f305-130">75</span><span class="sxs-lookup"><span data-stu-id="3f305-130">75</span></span>            | <span data-ttu-id="3f305-131">от 63 до 86</span><span class="sxs-lookup"><span data-stu-id="3f305-131">63 to 86</span></span>       |
| <span data-ttu-id="3f305-132">5 звезд</span><span class="sxs-lookup"><span data-stu-id="3f305-132">5 stars</span></span> | <span data-ttu-id="3f305-133">99</span><span class="sxs-lookup"><span data-stu-id="3f305-133">99</span></span>            | <span data-ttu-id="3f305-134">от 87 до 99</span><span class="sxs-lookup"><span data-stu-id="3f305-134">87 to 99</span></span>       |



 

<span data-ttu-id="3f305-135">Этот атрибут хранится только в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="3f305-135">This attribute is stored only in the library.</span></span>

<span data-ttu-id="3f305-136">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="3f305-136">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f305-137">Требования</span><span class="sxs-lookup"><span data-stu-id="3f305-137">Requirements</span></span>



| <span data-ttu-id="3f305-138">Требование</span><span class="sxs-lookup"><span data-stu-id="3f305-138">Requirement</span></span> | <span data-ttu-id="3f305-139">Значение</span><span class="sxs-lookup"><span data-stu-id="3f305-139">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3f305-140">Версия</span><span class="sxs-lookup"><span data-stu-id="3f305-140">Version</span></span><br/> | <span data-ttu-id="3f305-141">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3f305-141">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f305-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f305-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f305-143">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="3f305-143">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





