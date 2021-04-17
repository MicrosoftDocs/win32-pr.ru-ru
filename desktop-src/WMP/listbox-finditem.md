---
title: LISTBOX. findItem
description: Метод findItem выполняет поиск заданной строки, начиная с элемента, следующего за указанным индексом элемента.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- Проигрыватель Windows Media LISTBOX. findItem
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694982"
---
# <a name="listboxfinditem"></a>LISTBOX. findItem

Метод **findItem** выполняет поиск заданной строки, начиная с элемента, следующего за указанным индексом элемента.

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Число** (**Long**), содержащее индекс элемента, с которого начинается поиск.

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*
</dt> <dd>

**Строка** , содержащая искомый текст.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Long**), содержащее индекс элемента, содержащего строку.

## <a name="remarks"></a>Комментарии

Чтобы начать поиск с первой строки элемента управления "список", используйте 1 в качестве *startIndex*. Чтобы продолжить поиск текста после того, как будет найдена первая строка, используйте возвращенный индекс строки в качестве *startIndex*, и поиск начнется со следующей строки. Этот метод будет искать подстроки и не учитывает регистр.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





