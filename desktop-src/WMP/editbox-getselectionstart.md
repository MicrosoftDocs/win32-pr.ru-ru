---
title: EDITBOX. Жетселектионстарт
description: Метод Жетселектионстарт извлекает начальную точку выделенного текста в элементе управления EditBox.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- EDITBOX. жетселектионстарт проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c555cc7231440e15275dcd44a2508f1d8cc5ba53a8137db861cc71b61528ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340035"
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

## <a name="remarks"></a>Remarks

Если текст не выбран, этот метод возвращает позицию точки вставки.

Если элемент управления является многострочным, этот метод возвращает индекс символа в элементе управления, а не индекс строки.

Этот метод может быть вызван только после того, как элемент управления станет видимым.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



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

 

 





