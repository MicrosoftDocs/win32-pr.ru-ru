---
title: TEXT. Scroll
description: Атрибут прокрутки указывает или получает значение, указывающее, прокручивается ли текст.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- TEXT. прокрутка проигрывателя Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717929"
---
# <a name="textscrolling"></a>TEXT. Scroll

Атрибут **прокрутки** указывает или получает значение, указывающее, прокручивается ли текст.

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **логическим значением** для чтения и записи.



| Значение | Описание                     |
|-------|---------------------------------|
| true  | Прокрутка включена.           |
| false | По умолчанию. Прокрутка отключена. |



 

## <a name="remarks"></a>Комментарии

Функция прокрутки предоставляет буфер с двумя пробелами между концом текста и началом повторяющейся строки.

Атрибут « **обоснование** » определяет место первого отображения текста перед началом прокрутки.

См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TEXT, элемент**](text-element.md)
</dt> <dt>

[**TEXT. обоснование**](text-justification.md)
</dt> <dt>

[**TEXT. Скроллингамаунт**](text-scrollingamount.md)
</dt> <dt>

[**TEXT. Скроллингделай**](text-scrollingdelay.md)
</dt> <dt>

[**TEXT. Скроллингдиректион**](text-scrollingdirection.md)
</dt> </dl>

 

 





