---
title: EDITBOX. Сетселектион
description: Метод Сетселектион выбирает текст в элементе управления "поле ввода" из указанного начального индекса в указанный конечный индекс.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- Сетселектион Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694726"
---
# <a name="editboxsetselection"></a>EDITBOX. Сетселектион

Метод **сетселектион** выбирает текст в элементе управления "поле ввода" из указанного начального индекса в указанный конечный индекс.

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="start"></span><span id="START"></span>*запустить*
</dt> <dd>

**Число** (**Long**), содержащее индекс символа начальной позиции выбранного текста.

</dd> <dt>

<span id="end"></span><span id="END"></span>*конце*
</dt> <dd>

**Число** (**Long**), содержащее индекс символа конечной позиции выбранного текста.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если значение Start равно 0, а конец равен 1, то выделяется весь текст в элементе управления "поле ввода". Если начальное значение равно 1, все выделенные элементы отменяются.

Этот метод может быть вызван только после того, как элемент управления станет видимым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EDITBOX, элемент**](editbox-element.md)
</dt> <dt>

[**EDITBOX. Жетселектионенд**](editbox-getselectionend.md)
</dt> <dt>

[**EDITBOX. Жетселектионстарт**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX. Реплацеселектион**](editbox-replaceselection.md)
</dt> </dl>

 

 





