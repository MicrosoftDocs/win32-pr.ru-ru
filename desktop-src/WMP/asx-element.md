---
title: Элемент ASX
description: Элемент ASX определяет файл как метафайл.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Элемент ASX, проигрыватель Windows Media
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698925"
---
# <a name="asx-element"></a><span data-ttu-id="6b8cc-104">Элемент ASX</span><span class="sxs-lookup"><span data-stu-id="6b8cc-104">ASX Element</span></span>

<span data-ttu-id="6b8cc-105">Элемент **ASX** определяет файл как метафайл.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-105">The **ASX** element defines a file as a metafile.</span></span>

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a><span data-ttu-id="6b8cc-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b8cc-106">Attributes</span></span>

<span data-ttu-id="6b8cc-107">`VERSION` (обязательный)</span><span class="sxs-lookup"><span data-stu-id="6b8cc-107">`VERSION` (required)</span></span>

<span data-ttu-id="6b8cc-108">Десятичное число, представляющее номер версии синтаксиса для метафайла.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-108">Decimal number representing the version number of the syntax for the metafile.</span></span> <span data-ttu-id="6b8cc-109">Задайте значение 3 или 3,0.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-109">Set to 3 or 3.0.</span></span>

<span data-ttu-id="6b8cc-110">**PREVIEWMODE** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="6b8cc-110">**PREVIEWMODE** (optional)</span></span>

<span data-ttu-id="6b8cc-111">Значение, указывающее, входит ли проигрыватель Windows Media в режим предварительного просмотра перед воспроизведением первого клипа.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-111">Value indicating whether Windows Media Player enters preview mode before playing the first clip.</span></span>

<span data-ttu-id="6b8cc-112">Должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-112">Must be one of the following values.</span></span>



| <span data-ttu-id="6b8cc-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6b8cc-113">Value</span></span> | <span data-ttu-id="6b8cc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6b8cc-114">Description</span></span>                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8cc-115">YES</span><span class="sxs-lookup"><span data-stu-id="6b8cc-115">YES</span></span>   | <span data-ttu-id="6b8cc-116">Проигрыватель Windows Media переходит в режим предварительного просмотра перед воспроизведением первого клипа.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-116">Windows Media Player enters preview mode before playing the first clip.</span></span>                            |
| <span data-ttu-id="6b8cc-117">NO</span><span class="sxs-lookup"><span data-stu-id="6b8cc-117">NO</span></span>    | <span data-ttu-id="6b8cc-118">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-118">The default value.</span></span> <span data-ttu-id="6b8cc-119">Проигрыватель Windows Media не перейдет в режим предварительного просмотра перед воспроизведением первого клипа.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-119">Windows Media Player does not enter preview mode before playing the first clip.</span></span> |



 

<span data-ttu-id="6b8cc-120">**Баннербар** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="6b8cc-120">**BANNERBAR** (optional)</span></span>

<span data-ttu-id="6b8cc-121">Значение, указывающее, резервирует ли проигрыватель Windows Media пространство для изображения баннера.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-121">Value indicating whether Windows Media Player reserves space for a banner graphic.</span></span>

<span data-ttu-id="6b8cc-122">Должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-122">Must be one of the following values.</span></span>



| <span data-ttu-id="6b8cc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6b8cc-123">Value</span></span> | <span data-ttu-id="6b8cc-124">Описание</span><span class="sxs-lookup"><span data-stu-id="6b8cc-124">Description</span></span>                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8cc-125">AUTO</span><span class="sxs-lookup"><span data-stu-id="6b8cc-125">AUTO</span></span>  | <span data-ttu-id="6b8cc-126">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-126">The default value.</span></span> <span data-ttu-id="6b8cc-127">Проигрыватель Windows Media резервирует место для заголовков, только если фрагмент содержимого содержит одно содержимое.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-127">Windows Media Player reserves space for the banner bar only when a piece of content includes one.</span></span>                       |
| <span data-ttu-id="6b8cc-128">FIXED</span><span class="sxs-lookup"><span data-stu-id="6b8cc-128">FIXED</span></span> | <span data-ttu-id="6b8cc-129">Проигрыватель Windows Media резервирует фиксированное пространство для рисунка баннера для каждого воспроизводимого материала, независимо от наличия баннера.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-129">Windows Media Player reserves a fixed space for a banner graphic for every piece of content played, whether there is an associated banner.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="6b8cc-130">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6b8cc-130">Parent/Child Elements</span></span>



| <span data-ttu-id="6b8cc-131">Иерархия</span><span class="sxs-lookup"><span data-stu-id="6b8cc-131">Hierarchy</span></span>       | <span data-ttu-id="6b8cc-132">Элементы</span><span class="sxs-lookup"><span data-stu-id="6b8cc-132">Elements</span></span>                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8cc-133">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6b8cc-133">Parent elements</span></span> | <span data-ttu-id="6b8cc-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-134">None.</span></span> <span data-ttu-id="6b8cc-135">Элемент **ASX** должен быть первым элементом в каждом метафайле.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-135">The **ASX** element must be the first element in every metafile.</span></span>                                                                                                 |
| <span data-ttu-id="6b8cc-136">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6b8cc-136">Child elements</span></span>  | <span data-ttu-id="6b8cc-137">**абстрактный**, **Автор**, **баннер**, **базовый**, **авторские права**, **запись**, **ентриреф**, **событие**, **мореинфо**, **превиевдуратион**, **param**, **повторение**, **заголовок**</span><span class="sxs-lookup"><span data-stu-id="6b8cc-137">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **ENTRY**, **ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6b8cc-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b8cc-138">Remarks</span></span>

<span data-ttu-id="6b8cc-139">Первые четыре символа списка воспроизведения метафайла должны иметь значение "<ASX".</span><span class="sxs-lookup"><span data-stu-id="6b8cc-139">The first four characters of a metafile playlist must be "<ASX".</span></span> <span data-ttu-id="6b8cc-140">Другие элементы, определенные в области элемента **ASX** , такие как **Title** и **Author**, связаны с отображением сведений, отображаемых проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-140">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the show information displayed by Windows Media Player.</span></span>

<span data-ttu-id="6b8cc-141">Для проигрывателя Windows Media номер версии синтаксиса равен 3,0.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-141">For Windows Media Player, the syntax version number is 3.0.</span></span> <span data-ttu-id="6b8cc-142">Проигрыватель Windows Media поддерживает все предыдущие версии синтаксиса метафайлов.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-142">Windows Media Player supports all previous versions of metafile syntax.</span></span> <span data-ttu-id="6b8cc-143">Допустимые значения для атрибута **Version** : 3,0 и 3 (без десятичной запятой).</span><span class="sxs-lookup"><span data-stu-id="6b8cc-143">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="6b8cc-144">Если атрибут **PREVIEWMODE** имеет значение Yes, проигрыватель Windows Media немедленно переходит в режим предварительного просмотра перед воспроизведением первого клипа.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-144">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player immediately enters preview mode before playing the first clip.</span></span> <span data-ttu-id="6b8cc-145">Когда проигрыватель Windows Media переходит в режим предварительного просмотра, он предварительно просматривает каждый клип, указанный в метафайле.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-145">When Windows Media Player enters preview mode, it previews each clip referenced in the metafile.</span></span> <span data-ttu-id="6b8cc-146">Элемент **превиевдуратион** определяет продолжительность каждого предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-146">The **PREVIEWDURATION** element determines the duration of each preview.</span></span>

<span data-ttu-id="6b8cc-147">Атрибут **баннербар** определяет, резервирует ли проигрыватель Windows Media пространство для изображения баннера.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-147">The **BANNERBAR** attribute defines whether Windows Media Player reserves space for a banner graphic.</span></span> <span data-ttu-id="6b8cc-148">Баннер — это изображение, отображаемое в области отображения видео во время воспроизведения мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-148">A banner is a graphic that is displayed in the video display area while media content is playing.</span></span> <span data-ttu-id="6b8cc-149">(Используйте элемент **баннера** для добавления баннера к содержимому.) Если значение **баннербар** является фиксированным, проигрыватель Windows Media резервирует место для каждого фрагмента мультимедийного содержимого, независимо от того, есть ли у него баннер.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-149">(Use the **BANNER** element to add a banner to the content.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for every piece of media content, whether the media content has a banner.</span></span> <span data-ttu-id="6b8cc-150">Если с содержимым носителя не связан баннер, то пространство, зарезервированное для одного, является черным.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-150">If a piece of media content does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="6b8cc-151">Если значение атрибута **баннербар** — Auto, проигрыватель Windows Media резервирует пространство для баннера только в том случае, если его содержимое содержит.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-151">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the media content includes one.</span></span>

<span data-ttu-id="6b8cc-152">Если вы создаете метафайл с несколькими клипами (элементы **entry** или **ентриреф** ) и устанавливаете для атрибута **Баннербар** значение Auto, проигрыватель Windows Media может изменить размер, чтобы разрешить место для изображения баннера для одного клипа, а затем снова изменить размер, если следующий клип не содержит изображение баннера.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-152">If you create a metafile with multiple clips (**ENTRY** or **ENTRYREF** elements) and set the value of the **BANNERBAR** attribute to AUTO, Windows Media Player might resize to allow space for a banner graphic for one clip, and then resize again if the next clip does not contain a banner graphic.</span></span> <span data-ttu-id="6b8cc-153">Если требуется, чтобы размер окна оставался прежним (за исключением изменения размера видео), используйте ФИКСИРОВАНное значение для атрибута **баннербар** .</span><span class="sxs-lookup"><span data-stu-id="6b8cc-153">If you want the size of the window to stay the same (except when the video size changes), use the FIXED value for the **BANNERBAR** attribute.</span></span>

<span data-ttu-id="6b8cc-154">Пространство, зарезервированное для изображения баннера, составляет 32 пикселей в ширину на 194 пикселей.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-154">The space reserved for a banner graphic is 32 pixels high by 194 pixels wide.</span></span> <span data-ttu-id="6b8cc-155">Зарезервированное пространство отображается под любым визуализированным видеоматериалом и 6 пикселями над нижней границей видеообласти, что позволяет использовать пространство для границы области в 6 пикселей.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-155">The reserved space appears below any rendered video content and 6 pixels above the lower edge of the video area, allowing space for the 6-pixel video area border.</span></span> <span data-ttu-id="6b8cc-156">Зарезервированное пространство заголовков центрируется по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-156">The reserved banner space is centered horizontally.</span></span>

<span data-ttu-id="6b8cc-157">Проигрыватель Windows Media визуализирует изображение, начиная с самого левого пикселя области баннера.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-157">Windows Media Player renders the graphic beginning in the leftmost pixel of the banner space.</span></span> <span data-ttu-id="6b8cc-158">Если рисунок заполняет все пространство, он будет отображаться по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-158">If the graphic fills the entire space, it will appear centered horizontally.</span></span> <span data-ttu-id="6b8cc-159">В противном случае будет использоваться конечный пробел.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-159">Otherwise there will be trailing space.</span></span> <span data-ttu-id="6b8cc-160">Обратите внимание, что минимальная ширина проигрывателя Windows Media всегда превышает размер видеоклипа, независимо от значения атрибута **баннербар** .</span><span class="sxs-lookup"><span data-stu-id="6b8cc-160">Note that the minimum width of Windows Media Player is always wider than the size of the video clip, regardless of the value of the **BANNERBAR** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="6b8cc-161">Примеры</span><span class="sxs-lookup"><span data-stu-id="6b8cc-161">Examples</span></span>


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="6b8cc-162">Требования</span><span class="sxs-lookup"><span data-stu-id="6b8cc-162">Requirements</span></span>



| <span data-ttu-id="6b8cc-163">Требование</span><span class="sxs-lookup"><span data-stu-id="6b8cc-163">Requirement</span></span> | <span data-ttu-id="6b8cc-164">Значение</span><span class="sxs-lookup"><span data-stu-id="6b8cc-164">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="6b8cc-165">Версия</span><span class="sxs-lookup"><span data-stu-id="6b8cc-165">Version</span></span><br/> | <span data-ttu-id="6b8cc-166">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="6b8cc-166">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b8cc-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b8cc-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8cc-168">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6b8cc-168">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6b8cc-169">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6b8cc-169">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





