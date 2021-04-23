---
description: Система оценок, использующая целочисленные значения от 1 до 99. Это система оценки, используемая оболочкой Windows Vista.
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: System. Оценка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e411e313f0fa6042a8cbe3a076a7166928020af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692948"
---
# <a name="systemrating"></a><span data-ttu-id="a5477-104">System. Оценка</span><span class="sxs-lookup"><span data-stu-id="a5477-104">System.Rating</span></span>

<span data-ttu-id="a5477-105">Система оценок, использующая целочисленные значения от 1 до 99.</span><span class="sxs-lookup"><span data-stu-id="a5477-105">A rating system that uses integer values between 1 and 99.</span></span> <span data-ttu-id="a5477-106">Это система оценки, используемая оболочкой Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a5477-106">This is the rating system used by the Windows Vista Shell.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a5477-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5477-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a><span data-ttu-id="a5477-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5477-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a><span data-ttu-id="a5477-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5477-109">Remarks</span></span>

<span data-ttu-id="a5477-110">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="a5477-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="a5477-111">Сведения о совместимости с системами оценок, которые используют значения от 1 до 5, см. в свойстве [System. симплератинг](./props-system-simplerating.md).</span><span class="sxs-lookup"><span data-stu-id="a5477-111">For compatibility with ratings systems that use values between 1 and 5, see the property [System.SimpleRating](./props-system-simplerating.md).</span></span> <span data-ttu-id="a5477-112">Однако обратите внимание, что System. Симплератинг не используется в оболочке Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a5477-112">Note, however, that System.SimpleRating is not used in the Windows Vista Shell.</span></span>

<span data-ttu-id="a5477-113">В следующей таблице описывается, что означает система оценки, используемая в пользовательском интерфейсе оболочки, в терминах значения [System. рейтингов]() .</span><span class="sxs-lookup"><span data-stu-id="a5477-113">The following table describes what the star rating system used in the Shell UI means in terms of the [System.Rating]() value.</span></span>



| <span data-ttu-id="a5477-114">System. Оценка</span><span class="sxs-lookup"><span data-stu-id="a5477-114">System.Rating</span></span> | <span data-ttu-id="a5477-115">Оценка</span><span class="sxs-lookup"><span data-stu-id="a5477-115">Star Rating</span></span> |
|---------------|-------------|
| <span data-ttu-id="a5477-116">1–12</span><span class="sxs-lookup"><span data-stu-id="a5477-116">1-12</span></span>          | <span data-ttu-id="a5477-117">1 звезда</span><span class="sxs-lookup"><span data-stu-id="a5477-117">1 Star</span></span>      |
| <span data-ttu-id="a5477-118">13-37</span><span class="sxs-lookup"><span data-stu-id="a5477-118">13-37</span></span>         | <span data-ttu-id="a5477-119">2 звезды</span><span class="sxs-lookup"><span data-stu-id="a5477-119">2 Stars</span></span>     |
| <span data-ttu-id="a5477-120">38-62</span><span class="sxs-lookup"><span data-stu-id="a5477-120">38-62</span></span>         | <span data-ttu-id="a5477-121">3 звезды</span><span class="sxs-lookup"><span data-stu-id="a5477-121">3 Stars</span></span>     |
| <span data-ttu-id="a5477-122">63-87</span><span class="sxs-lookup"><span data-stu-id="a5477-122">63-87</span></span>         | <span data-ttu-id="a5477-123">4 звезды</span><span class="sxs-lookup"><span data-stu-id="a5477-123">4 Stars</span></span>     |
| <span data-ttu-id="a5477-124">88-99</span><span class="sxs-lookup"><span data-stu-id="a5477-124">88-99</span></span>         | <span data-ttu-id="a5477-125">5 звезд</span><span class="sxs-lookup"><span data-stu-id="a5477-125">5 Stars</span></span>     |



 

<span data-ttu-id="a5477-126">Когда пользователь рассчитывает элемент, выбрав значение рейтинга "звезда" в пользовательском интерфейсе, фактические значения [System. рейтинга]() присваиваются, как показано в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="a5477-126">When a user rates an item by choosing a star rating value in the UI, actual [System.Rating]() values are assigned as shown in this table:</span></span>



| <span data-ttu-id="a5477-127">Оценка</span><span class="sxs-lookup"><span data-stu-id="a5477-127">Star Rating</span></span> | <span data-ttu-id="a5477-128">Значение, назначенное через пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="a5477-128">Value Assigned Through UI</span></span> |
|-------------|---------------------------|
| <span data-ttu-id="a5477-129">1 звезда</span><span class="sxs-lookup"><span data-stu-id="a5477-129">1 Star</span></span>      | <span data-ttu-id="a5477-130">1</span><span class="sxs-lookup"><span data-stu-id="a5477-130">1</span></span>                         |
| <span data-ttu-id="a5477-131">2 звезды</span><span class="sxs-lookup"><span data-stu-id="a5477-131">2 Stars</span></span>     | <span data-ttu-id="a5477-132">25</span><span class="sxs-lookup"><span data-stu-id="a5477-132">25</span></span>                        |
| <span data-ttu-id="a5477-133">3 звезды</span><span class="sxs-lookup"><span data-stu-id="a5477-133">3 Stars</span></span>     | <span data-ttu-id="a5477-134">50</span><span class="sxs-lookup"><span data-stu-id="a5477-134">50</span></span>                        |
| <span data-ttu-id="a5477-135">4 звезды</span><span class="sxs-lookup"><span data-stu-id="a5477-135">4 Stars</span></span>     | <span data-ttu-id="a5477-136">75</span><span class="sxs-lookup"><span data-stu-id="a5477-136">75</span></span>                        |
| <span data-ttu-id="a5477-137">5 звезд</span><span class="sxs-lookup"><span data-stu-id="a5477-137">5 Stars</span></span>     | <span data-ttu-id="a5477-138">99</span><span class="sxs-lookup"><span data-stu-id="a5477-138">99</span></span>                        |



 

<span data-ttu-id="a5477-139">Если файл имеет значение [System. симплератинг](./props-system-simplerating.md) , а не значение [System. рейтингов]() , используйте приведенную ниже таблицу для преобразования и указания значений для System. рейтингов.</span><span class="sxs-lookup"><span data-stu-id="a5477-139">If your file has a [System.SimpleRating](./props-system-simplerating.md) value rather than a [System.Rating]() value, use the table below to convert and specify values for System.Rating.</span></span>



| <span data-ttu-id="a5477-140">System. Симплератинг</span><span class="sxs-lookup"><span data-stu-id="a5477-140">System.SimpleRating</span></span> | <span data-ttu-id="a5477-141">System. Оценка</span><span class="sxs-lookup"><span data-stu-id="a5477-141">System.Rating</span></span> |
|---------------------|---------------|
| <span data-ttu-id="a5477-142">1</span><span class="sxs-lookup"><span data-stu-id="a5477-142">1</span></span>                   | <span data-ttu-id="a5477-143">1</span><span class="sxs-lookup"><span data-stu-id="a5477-143">1</span></span>             |
| <span data-ttu-id="a5477-144">2</span><span class="sxs-lookup"><span data-stu-id="a5477-144">2</span></span>                   | <span data-ttu-id="a5477-145">25</span><span class="sxs-lookup"><span data-stu-id="a5477-145">25</span></span>            |
| <span data-ttu-id="a5477-146">3</span><span class="sxs-lookup"><span data-stu-id="a5477-146">3</span></span>                   | <span data-ttu-id="a5477-147">50</span><span class="sxs-lookup"><span data-stu-id="a5477-147">50</span></span>            |
| <span data-ttu-id="a5477-148">4</span><span class="sxs-lookup"><span data-stu-id="a5477-148">4</span></span>                   | <span data-ttu-id="a5477-149">75</span><span class="sxs-lookup"><span data-stu-id="a5477-149">75</span></span>            |
| <span data-ttu-id="a5477-150">5</span><span class="sxs-lookup"><span data-stu-id="a5477-150">5</span></span>                   | <span data-ttu-id="a5477-151">99</span><span class="sxs-lookup"><span data-stu-id="a5477-151">99</span></span>            |



 

<span data-ttu-id="a5477-152">Если в файле имеются сохраненные значения [System. Оценка]() и [System. симплератинг](./props-system-simplerating.md) , всегда используйте значение System. рейтингов при запросе непосредственно, без ссылки на System. симплератинг.</span><span class="sxs-lookup"><span data-stu-id="a5477-152">If your file has both [System.Rating]() and [System.SimpleRating](./props-system-simplerating.md) persisted values, always use the System.Rating value when it is directly requested, without reference to System.SimpleRating.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5477-153">См. также</span><span class="sxs-lookup"><span data-stu-id="a5477-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5477-154">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="a5477-154">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a5477-155">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="a5477-155">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a5477-156">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="a5477-156">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a5477-157">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a5477-157">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a5477-158">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a5477-158">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a5477-159">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a5477-159">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a5477-160">булеанформат</span><span class="sxs-lookup"><span data-stu-id="a5477-160">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a5477-161">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a5477-161">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a5477-162">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a5477-162">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a5477-163">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="a5477-163">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a5477-164">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="a5477-164">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a5477-165">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="a5477-165">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a5477-166">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="a5477-166">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a5477-167">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="a5477-167">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
