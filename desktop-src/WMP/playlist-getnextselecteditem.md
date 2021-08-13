---
title: Список воспроизведения. Жетнекстселектедитем
description: Метод Жетнекстселектедитем извлекает индекс следующего выбранного элемента списка воспроизведения после указанного индекса.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- проигрыватель Windows Media списка воспроизведения. жетнекстселектедитем
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 872dd31694384dfa35d7ce98c2f26756ede14539f4e788cbb6f699d17ca78a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467754"
---
# <a name="playlistgetnextselecteditem"></a>Список воспроизведения. Жетнекстселектедитем

Метод **жетнекстселектедитем** извлекает индекс следующего выбранного элемента списка воспроизведения после указанного индекса.

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*детализирован*
</dt> <dd>

**Число** (**Long**), указывающее индекс элемента для поиска после.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Long**).

## <a name="remarks"></a>Remarks

Если другие элементы не выбраны, этот метод возвращает значение 1.

Этот метод был заменен **getNextSelectedItem2**, который поддерживает вложенные списки воспроизведения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





