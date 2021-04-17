---
title: Список воспроизведения. Жетнекстселектедитем
description: Метод Жетнекстселектедитем извлекает индекс следующего выбранного элемента списка воспроизведения после указанного индекса.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- Проигрыватель Windows Media Player. Жетнекстселектедитем
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704136"
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

## <a name="remarks"></a>Комментарии

Если другие элементы не выбраны, этот метод возвращает значение 1.

Этот метод был заменен **getNextSelectedItem2**, который поддерживает вложенные списки воспроизведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





