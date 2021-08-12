---
title: Список воспроизведения. Жетнекстчеккедитем
description: Метод Жетнекстчеккедитем извлекает индекс следующего отмеченного элемента списка воспроизведения после указанного индекса.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- проигрыватель Windows Media списка воспроизведения. жетнекстчеккедитем
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54b6e598737d1aac09754b15c037c27a435deb5fff34c729aa48c51019e12982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571454"
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

## <a name="remarks"></a>Remarks

Если элементы, помеченные флажками, отсутствуют, этот метод возвращает значение 1.

Этот метод был заменен **getNextCheckedItem2**, который поддерживает вложенные списки воспроизведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





