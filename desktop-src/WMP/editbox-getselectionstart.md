---
title: EDITBOX. Жетселектионстарт
description: Метод Жетселектионстарт извлекает начальную точку выделенного текста в элементе управления EditBox.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- Жетселектионстарт Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2508119e5b1d46d09b3531582e86caad7e7facbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699271"
---
# <a name="editboxgetselectionstart"></a>EDITBOX. Жетселектионстарт

Метод **жетселектионстарт** извлекает начальную точку выделенного текста в элементе управления EditBox.

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Long**).

## <a name="remarks"></a>Комментарии

Если текст не выбран, этот метод возвращает позицию точки вставки.

Если элемент управления является многострочным, этот метод возвращает индекс символа в элементе управления, а не индекс строки.

Этот метод может быть вызван только после того, как элемент управления станет видимым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EDITBOX, элемент**](editbox-element.md)
</dt> <dt>

[**EDITBOX. Жетселектионенд**](editbox-getselectionend.md)
</dt> <dt>

[**EDITBOX. Реплацеселектион**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX. Сетселектион**](editbox-setselection.md)
</dt> </dl>

 

 





