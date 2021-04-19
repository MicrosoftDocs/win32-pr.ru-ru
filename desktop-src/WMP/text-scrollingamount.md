---
title: TEXT. Скроллингамаунт
description: Атрибут Скроллингамаунт указывает или получает количество пикселей, на которое текст перемещается при каждом перемещении прокрутки.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- Проигрыватель Windows Media TEXT. Скроллингамаунт
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675608"
---
# <a name="textscrollingamount"></a>TEXT. Скроллингамаунт

Атрибут **скроллингамаунт** указывает или получает количество пикселей, на которое текст перемещается при каждом перемещении прокрутки.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является положительным **числом** для чтения и записи (**int**) со значением по умолчанию 6.

## <a name="remarks"></a>Комментарии

Для плавной прокрутки **скроллингамаунт** должны быть небольшими. Для быстрого рисования с большими промежутками **скроллингамаунт** должно быть больше. Если **Scroll** = "false", **скроллингамаунт** игнорируется.

См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TEXT, элемент**](text-element.md)
</dt> <dt>

[**TEXT. Scroll**](text-scrolling.md)
</dt> </dl>

 

 





