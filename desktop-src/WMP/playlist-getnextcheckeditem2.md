---
title: Список воспроизведения. getNextCheckedItem2
description: Метод getNextCheckedItem2 извлекает индекс следующего отмеченного элемента списка воспроизведения после указанного индекса.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- Проигрыватель Windows Media Player. getNextCheckedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704138"
---
# <a name="playlistgetnextcheckeditem2"></a>Список воспроизведения. getNextCheckedItem2

Метод **getNextCheckedItem2** извлекает индекс следующего отмеченного элемента списка воспроизведения после указанного индекса.

``` syntax
        elementID.getNextCheckedItem2(item)
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

Этот метод может работать с вложенными списками воспроизведения и заменять метод **жетнекстчеккедитем** , который не может. Передайте 1 в параметре *Item* , чтобы найти первый отмеченный элемент. Если элементы, помеченные флажками, отсутствуют, этот метод возвращает значение 1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. Жетнекстчеккедитем**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





