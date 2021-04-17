---
title: EDITBOX. Реплацеселектион
description: Метод Реплацеселектион заменяет текущее выделение на указанный текст.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- Реплацеселектион Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694727"
---
# <a name="editboxreplaceselection"></a>EDITBOX. Реплацеселектион

Метод **реплацеселектион** заменяет текущее выделение на указанный текст.

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*
</dt> <dd>

**Строка** , содержащая текст для замены выделенного текста.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если текст не выбран, замещающий текст вставляется в текущую позицию курсора.

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

[**EDITBOX. Жетселектионстарт**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX. Сетселектион**](editbox-setselection.md)
</dt> </dl>

 

 





