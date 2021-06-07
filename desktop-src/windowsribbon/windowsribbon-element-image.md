---
title: Элемент Image (платформа ленты Windows)
description: Представляет изображение.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Лента Windows, элемент изображения
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe0b9afb51697d50de9cb80886cf829b90c81262
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442895"
---
# <a name="image-element"></a><span data-ttu-id="98837-104">Элемент Image</span><span class="sxs-lookup"><span data-stu-id="98837-104">Image element</span></span>

<span data-ttu-id="98837-105">Представляет изображение.</span><span class="sxs-lookup"><span data-stu-id="98837-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="98837-106">Использование</span><span class="sxs-lookup"><span data-stu-id="98837-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="98837-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="98837-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98837-108">attribute</span><span class="sxs-lookup"><span data-stu-id="98837-108">Attribute</span></span></th>
<th><span data-ttu-id="98837-109">Тип</span><span class="sxs-lookup"><span data-stu-id="98837-109">Type</span></span></th>
<th><span data-ttu-id="98837-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="98837-110">Required</span></span></th>
<th><span data-ttu-id="98837-111">Описание</span><span class="sxs-lookup"><span data-stu-id="98837-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98837-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="98837-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="98837-113">xs: Поситивеинтежер Union xs: String</span><span class="sxs-lookup"><span data-stu-id="98837-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="98837-114">Нет</span><span class="sxs-lookup"><span data-stu-id="98837-114">No</span></span><br/></td>
<td><span data-ttu-id="98837-115">Уникальный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="98837-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="98837-116">
<dt><span></span><span></span><strong></strong> (Объединение xs: Поситивеинтежер и xs: String)</span><span class="sxs-lookup"><span data-stu-id="98837-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="98837-117">Целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем.</span><span class="sxs-lookup"><span data-stu-id="98837-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="98837-118">Максимальная длина — 10 символов, включая необязательные нули в начале.</span><span class="sxs-lookup"><span data-stu-id="98837-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98837-119"><strong>миндпи</strong></span><span class="sxs-lookup"><span data-stu-id="98837-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="98837-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="98837-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="98837-121">Нет</span><span class="sxs-lookup"><span data-stu-id="98837-121">No</span></span><br/></td>
<td><span data-ttu-id="98837-122"><dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)</span><span class="sxs-lookup"><span data-stu-id="98837-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="98837-123">Любая последовательность цифр с минимальным значением 96.</span><span class="sxs-lookup"><span data-stu-id="98837-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="98837-124">Если Миндпи опущен, значение по умолчанию — 96.</span><span class="sxs-lookup"><span data-stu-id="98837-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98837-125"><strong>Источник</strong></span><span class="sxs-lookup"><span data-stu-id="98837-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="98837-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="98837-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="98837-127">Нет</span><span class="sxs-lookup"><span data-stu-id="98837-127">No</span></span><br/></td>
<td><span data-ttu-id="98837-128"><dt><span></span><span></span><strong></strong> (xs: anyURI)</span><span class="sxs-lookup"><span data-stu-id="98837-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="98837-129">Любая последовательность символов, представляющая URI.</span><span class="sxs-lookup"><span data-stu-id="98837-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="98837-130">Значение URI является абсолютным или относительным (для файла разметки ленты) путем к ресурсу изображения типа BMP.</span><span class="sxs-lookup"><span data-stu-id="98837-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98837-131"><strong>Символ</strong></span><span class="sxs-lookup"><span data-stu-id="98837-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="98837-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="98837-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="98837-133">Нет</span><span class="sxs-lookup"><span data-stu-id="98837-133">No</span></span><br/></td>
<td><span data-ttu-id="98837-134">Символ ресурса для изображения.</span><span class="sxs-lookup"><span data-stu-id="98837-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="98837-135">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="98837-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="98837-136">Строка, состоящая из буквы или символа подчеркивания, за которой следует любая последовательность букв, цифр или знаков подчеркивания, не более 100 символов.</span><span class="sxs-lookup"><span data-stu-id="98837-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="98837-137">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="98837-137">Child elements</span></span>



| <span data-ttu-id="98837-138">Элемент</span><span class="sxs-lookup"><span data-stu-id="98837-138">Element</span></span>                                                               | <span data-ttu-id="98837-139">Описание</span><span class="sxs-lookup"><span data-stu-id="98837-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="98837-140">**Image. Source**</span><span class="sxs-lookup"><span data-stu-id="98837-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="98837-141">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="98837-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="98837-142">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="98837-142">Parent elements</span></span>



| <span data-ttu-id="98837-143">Элемент</span><span class="sxs-lookup"><span data-stu-id="98837-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98837-144">**Command. Ларжехигхконтрастимажес**</span><span class="sxs-lookup"><span data-stu-id="98837-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="98837-145">**Command. Ларжеимажес**</span><span class="sxs-lookup"><span data-stu-id="98837-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="98837-146">**Command. Смаллхигхконтрастимажес**</span><span class="sxs-lookup"><span data-stu-id="98837-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="98837-147">**Command. Смаллимажес**</span><span class="sxs-lookup"><span data-stu-id="98837-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="98837-148">Remarks</span><span class="sxs-lookup"><span data-stu-id="98837-148">Remarks</span></span>

<span data-ttu-id="98837-149">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="98837-149">Optional.</span></span>

<span data-ttu-id="98837-150">Может возникнуть один или несколько раз для каждого [**элемента Command. смаллимажес**](windowsribbon-element-command-smallimages.md), [**Command. смаллхигхконтрастимажес**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. ларжеимажес**](windowsribbon-element-command-largeimages.md)или [**Command. ларжехигхконтрастимажес**](windowsribbon-element-command-largehighcontrastimages.md) .</span><span class="sxs-lookup"><span data-stu-id="98837-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="98837-151">Когда коллекция графических ресурсов, предназначенная для поддержки конкретных точек экрана на дюйм, передается в платформу Ribbon через набор элементов **Image** , платформа использует **изображение** со значением атрибута *миндпи* , которое соответствует текущему значению dpi на экране.</span><span class="sxs-lookup"><span data-stu-id="98837-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="98837-152">Если элемент **Image** не объявлен со значением *миндпи* , совпадающим с текущим параметром dpi на экране, платформа выбирает **изображение** с ближайшим значением *миндпи* , которое меньше текущего значения DPI на экране, и масштабирует ресурс изображения.</span><span class="sxs-lookup"><span data-stu-id="98837-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="98837-153">В противном случае, если ни один из элементов **изображения** не объявлен с атрибутом *миндпи* , значение которого меньше текущего значения DPI экрана, платформа выбирает ближайшее значение *миндпи* , превышающее текущий параметр dpi на экране, и масштабирует ресурс изображения вниз.</span><span class="sxs-lookup"><span data-stu-id="98837-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="98837-154">Примеры</span><span class="sxs-lookup"><span data-stu-id="98837-154">Examples</span></span>

<span data-ttu-id="98837-155">В следующем примере кода показана разметка, необходимая для объявления, с помощью набора элементов **Image** — коллекция ресурсов изображений, предназначенных для поддержки четырех параметров dpi на экране.</span><span class="sxs-lookup"><span data-stu-id="98837-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a><span data-ttu-id="98837-156">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="98837-156">Element information</span></span>

* <span data-ttu-id="98837-157">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="98837-157">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="98837-158">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="98837-158">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="98837-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98837-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98837-160">Указание ресурсов изображения ленты</span><span class="sxs-lookup"><span data-stu-id="98837-160">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





