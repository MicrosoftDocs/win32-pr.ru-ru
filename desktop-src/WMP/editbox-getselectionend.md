---
title: EDITBOX. Жетселектионенд
description: Метод Жетселектионенд извлекает конечное расположение выделенного текста в элементе управления EditBox.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- EDITBOX. жетселектионенд проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8dff56bda802286ed76ba3b448478dfa57d005c13baf229612e190bbf163b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838848"
---
# <a name="editboxgetselectionend"></a>EDITBOX. Жетселектионенд

Метод **жетселектионенд** извлекает конечное расположение выделенного текста в элементе управления EditBox.

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Long**).

## <a name="remarks"></a>Remarks

Если текст не выбран, этот метод возвращает позицию точки вставки.

Если элемент управления является многострочным, этот метод возвращает индекс символа в элементе управления, а не индекс строки.

Этот метод может быть вызван только после того, как элемент управления станет видимым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EDITBOX, элемент**](editbox-element.md)
</dt> <dt>

[**EDITBOX. Жетселектионстарт**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX. Реплацеселектион**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX. Сетселектион**](editbox-setselection.md)
</dt> </dl>

 

 





