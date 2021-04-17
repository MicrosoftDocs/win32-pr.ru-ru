---
title: LISTBOX. Жетнекстселектедитем
description: Метод Жетнекстселектедитем извлекает следующий выбранный элемент в элементе управления "список", начиная с элемента с указанным индексом.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- Проигрыватель Windows Media LISTBOX. Жетнекстселектедитем
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694968"
---
# <a name="listboxgetnextselecteditem"></a>LISTBOX. Жетнекстселектедитем

Метод **жетнекстселектедитем** извлекает следующий выбранный элемент в элементе управления "список", начиная с элемента с указанным индексом.

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Число** (**Long**), содержащее индекс элемента, предшествующего получаемому элементу.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Long**), содержащее индекс следующего выбранного элемента.

## <a name="remarks"></a>Комментарии

Чтобы начать поиск с начала, используйте значение 1 для начального индекса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





