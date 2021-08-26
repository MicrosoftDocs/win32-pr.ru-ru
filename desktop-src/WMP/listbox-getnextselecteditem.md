---
title: LISTBOX. Жетнекстселектедитем
description: Метод Жетнекстселектедитем извлекает следующий выбранный элемент в элементе управления "список", начиная с элемента с указанным индексом.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- проигрыватель Windows Media LISTBOX. жетнекстселектедитем
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4a5d95880b1300ebfb7f1732e7c20b6975ad82cf2d15514c58e68b9f9c42cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003404"
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

## <a name="remarks"></a>Remarks

Чтобы начать поиск с начала, используйте значение 1 для начального индекса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





