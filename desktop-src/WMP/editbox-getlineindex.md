---
title: EDITBOX. Жетлинеиндекс
description: Метод Жетлинеиндекс извлекает индекс символа первого символа в строке с указанным индексом строки.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- Жетлинеиндекс Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699274"
---
# <a name="editboxgetlineindex"></a>EDITBOX. Жетлинеиндекс

Метод **жетлинеиндекс** извлекает индекс символа первого символа в строке с указанным индексом строки.

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*номер*
</dt> <dd>

**Число** (**Long**), содержащее индекс строки, индекс которой необходимо получить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Long**).

## <a name="remarks"></a>Комментарии

Если указанный индекс строки равен 1, то используется строка, содержащая точку вставки.

Этот метод может быть вызван только после того, как элемент управления станет видимым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EDITBOX, элемент**](editbox-element.md)
</dt> <dt>

[**EDITBOX. в строке**](editbox-getline.md)
</dt> <dt>

[**EDITBOX. Жетлинефромчар**](editbox-getlinefromchar.md)
</dt> </dl>

 

 





