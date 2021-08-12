---
title: EDITBOX. в строке
description: Метод GetText извлекает текст для строки с указанным индексом.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- проигрыватель Windows Media EDITBOX./line
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28d555cb684fa849b5fc7cdb42ebaf0ab4fb278b4ef126845add2f12ddf59948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578840"
---
# <a name="editboxgetline"></a>EDITBOX. в строке

Метод **gettext** извлекает текст для строки с указанным индексом.

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*номер*
</dt> <dd>

**Число** (**Long**), содержащее индекс строки для извлечения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку**.

## <a name="remarks"></a>Remarks

Если индекс является недопустимым, возвращается пустая строка. Этот метод может быть вызван только после того, как элемент управления станет видимым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EDITBOX, элемент**](editbox-element.md)
</dt> <dt>

[**EDITBOX. Жетлинефромчар**](editbox-getlinefromchar.md)
</dt> <dt>

[**EDITBOX. Жетлинеиндекс**](editbox-getlineindex.md)
</dt> </dl>

 

 





