---
title: Список воспроизведения. Жетнекстчеккедитем
description: Метод Жетнекстчеккедитем извлекает индекс следующего отмеченного элемента списка воспроизведения после указанного индекса.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- Проигрыватель Windows Media Player. Жетнекстчеккедитем
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704139"
---
# <a name="playlistgetnextcheckeditem"></a>Список воспроизведения. Жетнекстчеккедитем

Метод **жетнекстчеккедитем** извлекает индекс следующего отмеченного элемента списка воспроизведения после указанного индекса.

``` syntax
        elementID.getNextCheckedItem(item)
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

Если элементы, помеченные флажками, отсутствуют, этот метод возвращает значение 1.

Этот метод был заменен **getNextCheckedItem2**, который поддерживает вложенные списки воспроизведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





