---
title: Свойство Image. Source
description: Представляет путь к каталогу образа.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Свойство Image. Source ленты Windows
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801900"
---
# <a name="imagesource-property"></a>Свойство Image. Source

Представляет путь к каталогу образа.

## <a name="usage"></a>Использование

``` syntax
<Image.Source/>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                 |
|---------------------------------------------------------|
| [**Образ**](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Для каждого [**образа**](windowsribbon-element-image.md)может использоваться не более одного раза.

Этот элемент содержит значение типа *xs: anyURI* или любую последовательность символов, представляющих универсальный код ресурса (URI). Значение URI является абсолютным или относительным (для файла разметки ленты) путем к каталогу ресурса изображения типа Bitmap (BMP).

## <a name="examples"></a>Примеры

В следующем примере кода показана разметка, необходимая для объявления, с помощью набора элементов [**Image**](windowsribbon-element-image.md) — коллекция ресурсов изображений, предназначенных для поддержки четырех параметров dpi на экране. Свойство **Image. Source** используется для указания пути к ресурсу изображения.


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

 





