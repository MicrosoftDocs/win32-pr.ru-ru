---
title: TEXT. Скроллингамаунт
description: Атрибут Скроллингамаунт указывает или получает количество пикселей, на которое текст перемещается при каждом перемещении прокрутки.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- проигрыватель Windows Media TEXT. скроллингамаунт
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a8d5b703c02c2d3049f98a934980f1dbf8b1c5beceaca4d97158ea68c13db9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466964"
---
# <a name="textscrollingamount"></a>TEXT. Скроллингамаунт

Атрибут **скроллингамаунт** указывает или получает количество пикселей, на которое текст перемещается при каждом перемещении прокрутки.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является положительным **числом** для чтения и записи (**int**) со значением по умолчанию 6.

## <a name="remarks"></a>Remarks

Для плавной прокрутки **скроллингамаунт** должны быть небольшими. Для быстрого рисования с большими промежутками **скроллингамаунт** должно быть больше. Если **Scroll** = "false", **скроллингамаунт** игнорируется.

См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TEXT, элемент**](text-element.md)
</dt> <dt>

[**TEXT. Scroll**](text-scrolling.md)
</dt> </dl>

 

 





