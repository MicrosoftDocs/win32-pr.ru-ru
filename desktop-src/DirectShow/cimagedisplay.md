---
description: Класс Цимажедисплай является вспомогательным классом для модулей подготовки видео GDI для управления форматом отображения.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Класс Цимажедисплай (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679824"
---
# <a name="cimagedisplay-class"></a><span data-ttu-id="b6adc-103">Класс Цимажедисплай</span><span class="sxs-lookup"><span data-stu-id="b6adc-103">CImageDisplay class</span></span>

![Цимажедисплайкласшиерарчи](images/wutil06.png)

<span data-ttu-id="b6adc-105">`CImageDisplay`Класс является вспомогательным классом для модулей подготовки видео GDI для управления форматом отображения.</span><span class="sxs-lookup"><span data-stu-id="b6adc-105">The `CImageDisplay` class is a helper class for GDI video renderers to manage the display format.</span></span> <span data-ttu-id="b6adc-106">Объект хранит структуру [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , описывающую текущий режим просмотра, который инициализируется в методе конструктора объекта.</span><span class="sxs-lookup"><span data-stu-id="b6adc-106">The object stores a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that describes the current display mode, which is initialized in the object's constructor method.</span></span> <span data-ttu-id="b6adc-107">Метод **чеккмедиатипе** объекта проверяет, можно ли эффективно визуализировать предложенный тип мультимедиа с помощью GDI.</span><span class="sxs-lookup"><span data-stu-id="b6adc-107">The object's **CheckMediaType** method checks whether a proposed media type can be rendered efficiently using GDI.</span></span>



| <span data-ttu-id="b6adc-108">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="b6adc-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="b6adc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b6adc-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6adc-110">**\_вывод m**</span><span class="sxs-lookup"><span data-stu-id="b6adc-110">**m\_Display**</span></span>](cimagedisplay-m-display.md)                    | <span data-ttu-id="b6adc-111">Структура **видеоинфо** , описывающая текущий формат представления.</span><span class="sxs-lookup"><span data-stu-id="b6adc-111">**VIDEOINFO** structure that describes the current display format.</span></span>                     |
| <span data-ttu-id="b6adc-112">Защищенные методы</span><span class="sxs-lookup"><span data-stu-id="b6adc-112">Protected Methods</span></span>                                                | <span data-ttu-id="b6adc-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b6adc-113">Description</span></span>                                                                            |
| [<span data-ttu-id="b6adc-114">**чеккбитфиелдс**</span><span class="sxs-lookup"><span data-stu-id="b6adc-114">**CheckBitFields**</span></span>](cimagedisplay-checkbitfields.md)           | <span data-ttu-id="b6adc-115">Проверяет цветовую маску в структуре **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="b6adc-115">Validates the color masks in a **VIDEOINFO** structure.</span></span>                                |
| [<span data-ttu-id="b6adc-116">**каунтпрефиксбитс**</span><span class="sxs-lookup"><span data-stu-id="b6adc-116">**CountPrefixBits**</span></span>](cimagedisplay-countprefixbits.md)         | <span data-ttu-id="b6adc-117">Вычисляет количество нулевых битов в начале указанного битового поля.</span><span class="sxs-lookup"><span data-stu-id="b6adc-117">Calculates the number of zero bits at the start of a specified bit field.</span></span>              |
| [<span data-ttu-id="b6adc-118">**каунтсетбитс**</span><span class="sxs-lookup"><span data-stu-id="b6adc-118">**CountSetBits**</span></span>](cimagedisplay-countsetbits.md)               | <span data-ttu-id="b6adc-119">Возвращает число битов, равное 1, в указанном битовом поле.</span><span class="sxs-lookup"><span data-stu-id="b6adc-119">Returns the number of bits set to 1 in a specified bit field.</span></span>                          |
| <span data-ttu-id="b6adc-120">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="b6adc-120">Public Methods</span></span>                                                   | <span data-ttu-id="b6adc-121">Описание</span><span class="sxs-lookup"><span data-stu-id="b6adc-121">Description</span></span>                                                                            |
| [<span data-ttu-id="b6adc-122">**чеккхеадервалидити**</span><span class="sxs-lookup"><span data-stu-id="b6adc-122">**CheckHeaderValidity**</span></span>](cimagedisplay-checkheadervalidity.md) | <span data-ttu-id="b6adc-123">Проверяет структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="b6adc-123">Validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>                    |
| [<span data-ttu-id="b6adc-124">**чеккмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="b6adc-124">**CheckMediaType**</span></span>](cimagedisplay-checkmediatype.md)           | <span data-ttu-id="b6adc-125">Определяет, совместим ли предложенный тип мультимедиа с форматом вывода.</span><span class="sxs-lookup"><span data-stu-id="b6adc-125">Determines whether a proposed media type is compatible with the display format.</span></span>        |
| [<span data-ttu-id="b6adc-126">**чеккпалеттехеадер**</span><span class="sxs-lookup"><span data-stu-id="b6adc-126">**CheckPaletteHeader**</span></span>](cimagedisplay-checkpaletteheader.md)   | <span data-ttu-id="b6adc-127">Проверяет записи палитры в структуре **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="b6adc-127">Validates the palette entries in a **VIDEOINFO** structure.</span></span>                            |
| [<span data-ttu-id="b6adc-128">**чекквидеотипе**</span><span class="sxs-lookup"><span data-stu-id="b6adc-128">**CheckVideoType**</span></span>](cimagedisplay-checkvideotype.md)           | <span data-ttu-id="b6adc-129">Проверяет, совместим ли указанный формат **видеоинфо** с форматом вывода.</span><span class="sxs-lookup"><span data-stu-id="b6adc-129">Checks whether a specified **VIDEOINFO** format is compatible with the display format.</span></span> |
| [<span data-ttu-id="b6adc-130">**Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="b6adc-130">**CImageDisplay**</span></span>](cimagedisplay-cimagedisplay.md)             | <span data-ttu-id="b6adc-131">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="b6adc-131">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="b6adc-132">**Битовые маски**</span><span class="sxs-lookup"><span data-stu-id="b6adc-132">**GetBitMasks**</span></span>](cimagedisplay-getbitmasks.md)                 | <span data-ttu-id="b6adc-133">Извлекает цветовую маску для указанного формата **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="b6adc-133">Retrieves the color masks for a specified **VIDEOINFO** format.</span></span>                        |
| [<span data-ttu-id="b6adc-134">**жетколаурмаск**</span><span class="sxs-lookup"><span data-stu-id="b6adc-134">**GetColourMask**</span></span>](cimagedisplay-getcolourmask.md)             | <span data-ttu-id="b6adc-135">Получает цветовую маску для текущего формата изображения.</span><span class="sxs-lookup"><span data-stu-id="b6adc-135">Retrieves the color masks for the current display format.</span></span>                              |
| [<span data-ttu-id="b6adc-136">**жетдисплайдепс**</span><span class="sxs-lookup"><span data-stu-id="b6adc-136">**GetDisplayDepth**</span></span>](cimagedisplay-getdisplaydepth.md)         | <span data-ttu-id="b6adc-137">Возвращает битовую глубину текущего режима экрана.</span><span class="sxs-lookup"><span data-stu-id="b6adc-137">Retrieves the bit depth of the current display mode.</span></span>                                   |
| [<span data-ttu-id="b6adc-138">**жетдисплайформат**</span><span class="sxs-lookup"><span data-stu-id="b6adc-138">**GetDisplayFormat**</span></span>](cimagedisplay-getdisplayformat.md)       | <span data-ttu-id="b6adc-139">Возвращает видеоформат, описывающий текущий режим экрана.</span><span class="sxs-lookup"><span data-stu-id="b6adc-139">Retrieves a video format that describes the current display mode.</span></span>                      |
| [<span data-ttu-id="b6adc-140">**испалеттисед**</span><span class="sxs-lookup"><span data-stu-id="b6adc-140">**IsPalettised**</span></span>](cimagedisplay-ispalettised.md)               | <span data-ttu-id="b6adc-141">Ретерминес, является ли текущий формат просмотра палеттизед.</span><span class="sxs-lookup"><span data-stu-id="b6adc-141">Retermines whether the current display format is palettized.</span></span>                           |
| [<span data-ttu-id="b6adc-142">**рефрешдисплайтипе**</span><span class="sxs-lookup"><span data-stu-id="b6adc-142">**RefreshDisplayType**</span></span>](cimagedisplay-refreshdisplaytype.md)   | <span data-ttu-id="b6adc-143">Обновляет формат видео объекта в соответствии с указанным отображением</span><span class="sxs-lookup"><span data-stu-id="b6adc-143">Updates the object's video format to match the specified display</span></span>                       |



 

## <a name="requirements"></a><span data-ttu-id="b6adc-144">Требования</span><span class="sxs-lookup"><span data-stu-id="b6adc-144">Requirements</span></span>



| <span data-ttu-id="b6adc-145">Требование</span><span class="sxs-lookup"><span data-stu-id="b6adc-145">Requirement</span></span> | <span data-ttu-id="b6adc-146">Значение</span><span class="sxs-lookup"><span data-stu-id="b6adc-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6adc-147">Header</span><span class="sxs-lookup"><span data-stu-id="b6adc-147">Header</span></span><br/>  | <dl> <span data-ttu-id="b6adc-148"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6adc-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6adc-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6adc-149">Library</span></span><br/> | <dl> <span data-ttu-id="b6adc-150"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b6adc-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




