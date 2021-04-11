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
ms.openlocfilehash: 1d33f6710da2261a359aa7fd0a3b493871155cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "104133282"
---
# <a name="image-element"></a>Элемент Image

Представляет изображение.

## <a name="usage"></a>Использование

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Тип</th>
<th>Обязательно</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Id</strong><br/></td>
<td>xs: Поситивеинтежер Union xs: String<br/></td>
<td>Нет<br/></td>
<td>Уникальный идентификатор ресурса. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Объединение xs: Поситивеинтежер и xs: String)<br/> </dt> <dd> Целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем. <br/> Максимальная длина — 10 символов, включая необязательные нули в начале. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>миндпи</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)<br/> </dt> <dd> Любая последовательность цифр с минимальным значением 96. <br/> Если Миндпи опущен, значение по умолчанию — 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Источник</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>Нет<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: anyURI)<br/> </dt> <dd> Любая последовательность символов, представляющая URI. Значение URI является абсолютным или относительным (для файла разметки ленты) путем к ресурсу изображения типа BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Символ</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Символ ресурса для изображения.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Строка, состоящая из буквы или символа подчеркивания, за которой следует любая последовательность букв, цифр или знаков подчеркивания, не более 100 символов. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Описание                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Image. Source**](windowsribbon-element-image-source.md)<br/> | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Command. Ларжехигхконтрастимажес**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Command. Ларжеимажес**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Command. Смаллхигхконтрастимажес**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Command. Смаллимажес**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может возникнуть один или несколько раз для каждого [**элемента Command. смаллимажес**](windowsribbon-element-command-smallimages.md), [**Command. смаллхигхконтрастимажес**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. ларжеимажес**](windowsribbon-element-command-largeimages.md)или [**Command. ларжехигхконтрастимажес**](windowsribbon-element-command-largehighcontrastimages.md) .

Когда коллекция графических ресурсов, предназначенная для поддержки конкретных точек экрана на дюйм, передается в платформу Ribbon через набор элементов **Image** , платформа использует **изображение** со значением атрибута *миндпи* , которое соответствует текущему значению dpi на экране.

Если элемент **Image** не объявлен со значением *миндпи* , совпадающим с текущим параметром dpi на экране, платформа выбирает **изображение** с ближайшим значением *миндпи* , которое меньше текущего значения DPI на экране, и масштабирует ресурс изображения. В противном случае, если ни один из элементов **изображения** не объявлен с атрибутом *миндпи* , значение которого меньше текущего значения DPI экрана, платформа выбирает ближайшее значение *миндпи* , превышающее текущий параметр dpi на экране, и масштабирует ресурс изображения вниз.

## <a name="examples"></a>Примеры

В следующем примере кода показана разметка, необходимая для объявления, с помощью набора элементов **Image** — коллекция ресурсов изображений, предназначенных для поддержки четырех параметров dpi на экране.


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



## <a name="element-information"></a>Сведения об элементе



|                                     |           |
|-------------------------------------|-----------|
| Минимальная поддерживаемая система<br/> | Windows 7 |
| Может быть пустым                        | Нет        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Указание ресурсов изображения ленты](windowsribbon-imageformats.md)
</dt> </dl>

 

 





