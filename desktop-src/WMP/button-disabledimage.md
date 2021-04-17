---
title: КНОПКА. Дисабледимаже
description: Атрибут Дисабледимаже указывает или получает изображение, отображаемое при отключенной КНОПКе.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- КНОПКА. Дисабледимаже Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eac407f6e7fbdd155f4bcabe98cecc0546f7d97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694522"
---
# <a name="buttondisabledimage"></a>КНОПКА. Дисабледимаже

Атрибут **дисабледимаже** указывает или получает изображение, отображаемое при отключенной **кнопке** .

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.

## <a name="remarks"></a>Комментарии

Поддерживаются форматы изображений BMP, JPG, PNG и GIF.

Это изображение будет отображаться каждый раз, когда **отключенный** атрибут элемента управления имеет значение true. Если отключенный образ больше, чем заданный регион, отключенный образ будет обрезан.

Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BUTTON, элемент**](button-element.md)
</dt> </dl>

 

 





