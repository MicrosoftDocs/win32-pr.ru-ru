---
title: Список воспроизведения. setCheckedState2
description: Метод setCheckedState2 устанавливает состояние Checked элемента с указанным индексом в элементе списка воспроизведения.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- Проигрыватель Windows Media Player. setCheckedState2
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704119"
---
# <a name="playlistsetcheckedstate2"></a>Список воспроизведения. setCheckedState2

Метод **setCheckedState2** устанавливает состояние Checked элемента с указанным индексом в элементе **списка воспроизведения** .

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*детализирован*
</dt> <dd>

**Число** (**длинное**), указывающее индекс элемента списка воспроизведения, который должен быть установлен или снят.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*отмечен*
</dt> <dd>

**Логическое значение** , указывающее, должен ли заданный элемент проверяться (true) или неустановленным (false).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **логическое значение**.

## <a name="remarks"></a>Комментарии

Этот метод может работать с вложенными списками воспроизведения и заменять метод **сетчеккедстате** , который не может. Вы можете задать для всех элементов запрошенное состояние, указав значение 1 в параметре *Item* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. Сетчеккедстате**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





