---
title: Свойство Image. Source
description: Представляет путь к каталогу образа.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- свойство Image. Source Windows лента
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20612f0d25f914cb4c80ae77bb001a678af79e4605c3e1358ed7e33f6b19d805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202409"
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
| [**Изображение**](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a>Remarks

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



 

 





