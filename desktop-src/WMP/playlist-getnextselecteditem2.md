---
title: Список воспроизведения. getNextSelectedItem2
description: Метод getNextSelectedItem2 извлекает индекс следующего выбранного элемента списка воспроизведения после указанного индекса.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- проигрыватель Windows Media списка воспроизведения. getNextSelectedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6d1f98a418da1d8b21345598999f847cbf2142e9ca575bcfdc7047e2f9fd524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415284"
---
# <a name="playlistgetnextselecteditem2"></a>Список воспроизведения. getNextSelectedItem2

Метод **getNextSelectedItem2** извлекает индекс следующего выбранного элемента списка воспроизведения после указанного индекса.

``` syntax
        elementID.getNextSelectedItem2(item)
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

Этот метод может работать с вложенными списками воспроизведения и заменять метод **жетнекстселектедитем** , который не может. Передайте 1 в параметре *Item* , чтобы найти первый выбранный элемент. Если другие элементы не выбраны, возвращается-1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. Жетнекстселектедитем**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





