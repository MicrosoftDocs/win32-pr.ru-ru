---
description: Метод Уопвалид извлекает значение, указывающее, является ли указанная пользовательская операция (УОП) в настоящее время допустимой.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Метод Уопвалид (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685343"
---
# <a name="uopvalid-method"></a><span data-ttu-id="d70cd-103">Метод Уопвалид</span><span class="sxs-lookup"><span data-stu-id="d70cd-103">UOPValid Method</span></span>

> [!Note]  
> <span data-ttu-id="d70cd-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d70cd-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d70cd-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="d70cd-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d70cd-106">`UOPValid`Метод получает значение, указывающее, допустима ли в настоящее время указанная пользовательская операция (УОП).</span><span class="sxs-lookup"><span data-stu-id="d70cd-106">The `UOPValid` method retrieves a value that indicates whether the specified user operation (UOP) is currently valid.</span></span>

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a><span data-ttu-id="d70cd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d70cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d70cd-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*иуоп*</span><span class="sxs-lookup"><span data-stu-id="d70cd-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span></span>
</dt> <dd>

<span data-ttu-id="d70cd-109">Задает пользовательскую операцию (УОП) в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="d70cd-109">Specifies the user operation (UOP) as an Integer.</span></span>



| <span data-ttu-id="d70cd-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d70cd-110">Value</span></span> | <span data-ttu-id="d70cd-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d70cd-111">Description</span></span>                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d70cd-112">0</span><span class="sxs-lookup"><span data-stu-id="d70cd-112">0</span></span>     | <span data-ttu-id="d70cd-113">[**Плайтитле**](playtitle-method.md), [**плайаттиме**](playattime-method.md)[**плайаттимеинтитле**](playattimeintitle-method.md)</span><span class="sxs-lookup"><span data-stu-id="d70cd-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span></span>                                                                                      |
| <span data-ttu-id="d70cd-114">1</span><span class="sxs-lookup"><span data-stu-id="d70cd-114">1</span></span>     | [<span data-ttu-id="d70cd-115">**плайчаптер**</span><span class="sxs-lookup"><span data-stu-id="d70cd-115">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="d70cd-116">2</span><span class="sxs-lookup"><span data-stu-id="d70cd-116">2</span></span>     | [<span data-ttu-id="d70cd-117">**плайтитле**</span><span class="sxs-lookup"><span data-stu-id="d70cd-117">**PlayTitle**</span></span>](playtitle-method.md)                                                                                                                                                                                    |
| <span data-ttu-id="d70cd-118">3</span><span class="sxs-lookup"><span data-stu-id="d70cd-118">3</span></span>     | [<span data-ttu-id="d70cd-119">**Stop**</span><span class="sxs-lookup"><span data-stu-id="d70cd-119">**Stop**</span></span>](stop-method.md)                                                                                                                                                                                              |
| <span data-ttu-id="d70cd-120">4</span><span class="sxs-lookup"><span data-stu-id="d70cd-120">4</span></span>     | [<span data-ttu-id="d70cd-121">**ретурнфромсубмену**</span><span class="sxs-lookup"><span data-stu-id="d70cd-121">**ReturnFromSubmenu**</span></span>](returnfromsubmenu-method.md)                                                                                                                                                                    |
| <span data-ttu-id="d70cd-122">5</span><span class="sxs-lookup"><span data-stu-id="d70cd-122">5</span></span>     | [<span data-ttu-id="d70cd-123">**плайчаптер**</span><span class="sxs-lookup"><span data-stu-id="d70cd-123">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="d70cd-124">6</span><span class="sxs-lookup"><span data-stu-id="d70cd-124">6</span></span>     | <span data-ttu-id="d70cd-125">[**Плайпревчаптер**](playprevchapter-method.md), [ **реплайчаптер**](replaychapter-method.md)</span><span class="sxs-lookup"><span data-stu-id="d70cd-125">[**PlayPrevChapter**](playprevchapter-method.md), [**ReplayChapter**](replaychapter-method.md)</span></span>                                                                                                                         |
| <span data-ttu-id="d70cd-126">7</span><span class="sxs-lookup"><span data-stu-id="d70cd-126">7</span></span>     | [<span data-ttu-id="d70cd-127">**плайнекстчаптер**</span><span class="sxs-lookup"><span data-stu-id="d70cd-127">**PlayNextChapter**</span></span>](playnextchapter-method.md)                                                                                                                                                                        |
| <span data-ttu-id="d70cd-128">8</span><span class="sxs-lookup"><span data-stu-id="d70cd-128">8</span></span>     | [<span data-ttu-id="d70cd-129">**плайфорвардс**</span><span class="sxs-lookup"><span data-stu-id="d70cd-129">**PlayForwards**</span></span>](playforwards-method.md)                                                                                                                                                                              |
| <span data-ttu-id="d70cd-130">9</span><span class="sxs-lookup"><span data-stu-id="d70cd-130">9</span></span>     | [<span data-ttu-id="d70cd-131">**плайбакквардс**</span><span class="sxs-lookup"><span data-stu-id="d70cd-131">**PlayBackwards**</span></span>](playbackwards-method.md)                                                                                                                                                                            |
| <span data-ttu-id="d70cd-132">10</span><span class="sxs-lookup"><span data-stu-id="d70cd-132">10</span></span>    | <span data-ttu-id="d70cd-133">[**Шовмену**](showmenu-method.md) со значением параметра 2 ( \_ Название меню DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="d70cd-133">[**ShowMenu**](showmenu-method.md) with a parameter value of 2 (DVD\_MENU\_Title)</span></span>                                                                                                                                       |
| <span data-ttu-id="d70cd-134">11</span><span class="sxs-lookup"><span data-stu-id="d70cd-134">11</span></span>    | <span data-ttu-id="d70cd-135">[**Шовмену**](showmenu-method.md) со значением параметра 3 ( \_ корень меню DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="d70cd-135">[**ShowMenu**](showmenu-method.md) with a parameter value of 3 (DVD\_MENU\_Root)</span></span>                                                                                                                                        |
| <span data-ttu-id="d70cd-136">12</span><span class="sxs-lookup"><span data-stu-id="d70cd-136">12</span></span>    | <span data-ttu-id="d70cd-137">[**Шовмену**](showmenu-method.md) со значением параметра 4 ( \_ \_ подизображением меню DVD)</span><span class="sxs-lookup"><span data-stu-id="d70cd-137">[**ShowMenu**](showmenu-method.md) with a parameter value of 4 (DVD\_MENU\_Subpicture)</span></span>                                                                                                                                  |
| <span data-ttu-id="d70cd-138">13</span><span class="sxs-lookup"><span data-stu-id="d70cd-138">13</span></span>    | <span data-ttu-id="d70cd-139">[**Шовмену**](showmenu-method.md) со значением параметра 5 ( \_ аудио меню DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="d70cd-139">[**ShowMenu**](showmenu-method.md) with a parameter value of 5 (DVD\_MENU\_Audio)</span></span>                                                                                                                                       |
| <span data-ttu-id="d70cd-140">14</span><span class="sxs-lookup"><span data-stu-id="d70cd-140">14</span></span>    | <span data-ttu-id="d70cd-141">[**Шовмену**](showmenu-method.md) со значением параметра 6 ( \_ угол меню DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="d70cd-141">[**ShowMenu**](showmenu-method.md) with a parameter value of 6 (DVD\_MENU\_Angle)</span></span>                                                                                                                                       |
| <span data-ttu-id="d70cd-142">15</span><span class="sxs-lookup"><span data-stu-id="d70cd-142">15</span></span>    | <span data-ttu-id="d70cd-143">[**Шовмену**](showmenu-method.md) со значением параметра 7 ( \_ глава меню DVD \_ )</span><span class="sxs-lookup"><span data-stu-id="d70cd-143">[**ShowMenu**](showmenu-method.md) with a parameter value of 7 (DVD\_MENU\_Chapter)</span></span>                                                                                                                                     |
| <span data-ttu-id="d70cd-144">16</span><span class="sxs-lookup"><span data-stu-id="d70cd-144">16</span></span>    | [<span data-ttu-id="d70cd-145">**Возобновить**</span><span class="sxs-lookup"><span data-stu-id="d70cd-145">**Resume**</span></span>](resume-method.md)                                                                                                                                                                                          |
| <span data-ttu-id="d70cd-146">17</span><span class="sxs-lookup"><span data-stu-id="d70cd-146">17</span></span>    | <span data-ttu-id="d70cd-147">[**Селектлефтбуттон**](selectleftbutton-method.md), [**селектригхтбуттон**](selectrightbutton-method.md), [**селектуппербуттон**](selectupperbutton-method.md), [**селектловербуттон**](selectlowerbutton-method.md)</span><span class="sxs-lookup"><span data-stu-id="d70cd-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span></span> |
| <span data-ttu-id="d70cd-148">18</span><span class="sxs-lookup"><span data-stu-id="d70cd-148">18</span></span>    | [<span data-ttu-id="d70cd-149">**стиллофф**</span><span class="sxs-lookup"><span data-stu-id="d70cd-149">**StillOff**</span></span>](stilloff-method.md)                                                                                                                                                                                      |
| <span data-ttu-id="d70cd-150">19</span><span class="sxs-lookup"><span data-stu-id="d70cd-150">19</span></span>    | [<span data-ttu-id="d70cd-151">**Пауза**</span><span class="sxs-lookup"><span data-stu-id="d70cd-151">**Pause**</span></span>](pause-method.md)                                                                                                                                                                                            |
| <span data-ttu-id="d70cd-152">20</span><span class="sxs-lookup"><span data-stu-id="d70cd-152">20</span></span>    | [<span data-ttu-id="d70cd-153">**куррентаудиостреам**</span><span class="sxs-lookup"><span data-stu-id="d70cd-153">**CurrentAudioStream**</span></span>](currentaudiostream-property.md)                                                                                                                                                                |
| <span data-ttu-id="d70cd-154">21</span><span class="sxs-lookup"><span data-stu-id="d70cd-154">21</span></span>    | [<span data-ttu-id="d70cd-155">**куррентсубпиктурестреам**</span><span class="sxs-lookup"><span data-stu-id="d70cd-155">**CurrentSubpictureStream**</span></span>](currentsubpicturestream-property.md)                                                                                                                                                      |
| <span data-ttu-id="d70cd-156">22</span><span class="sxs-lookup"><span data-stu-id="d70cd-156">22</span></span>    | <span data-ttu-id="d70cd-157">[**Куррентангле**](currentangle-property.md), [ **селектпаренталлевел**](selectparentallevel-method.md)</span><span class="sxs-lookup"><span data-stu-id="d70cd-157">[**CurrentAngle**](currentangle-property.md), [**SelectParentalLevel**](selectparentallevel-method.md)</span></span>                                                                                                                 |
| <span data-ttu-id="d70cd-158">23</span><span class="sxs-lookup"><span data-stu-id="d70cd-158">23</span></span>    | [<span data-ttu-id="d70cd-159">**караокеаудиопресентатионмоде**</span><span class="sxs-lookup"><span data-stu-id="d70cd-159">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| <span data-ttu-id="d70cd-160">24</span><span class="sxs-lookup"><span data-stu-id="d70cd-160">24</span></span>    | <span data-ttu-id="d70cd-161">Выберите параметр видеорежим.</span><span class="sxs-lookup"><span data-stu-id="d70cd-161">Select video mode preference.</span></span>                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d70cd-162">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d70cd-162">Return Value</span></span>

<span data-ttu-id="d70cd-163">Возвращает логическое значение, указывающее, разрешена ли указанная операция элементом управления УОП.</span><span class="sxs-lookup"><span data-stu-id="d70cd-163">Returns a Boolean value indicating whether the specified operation is permitted by UOP control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d70cd-164">Требования</span><span class="sxs-lookup"><span data-stu-id="d70cd-164">Requirements</span></span>



| <span data-ttu-id="d70cd-165">Требование</span><span class="sxs-lookup"><span data-stu-id="d70cd-165">Requirement</span></span> | <span data-ttu-id="d70cd-166">Значение</span><span class="sxs-lookup"><span data-stu-id="d70cd-166">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d70cd-167">Header</span><span class="sxs-lookup"><span data-stu-id="d70cd-167">Header</span></span><br/> | <dl> <span data-ttu-id="d70cd-168"><dt>Сегмент. h</dt></span><span class="sxs-lookup"><span data-stu-id="d70cd-168"><dt>Segment.h</dt></span></span> </dl> |



 

 




