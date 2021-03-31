---
title: Сообщение EM_SHOWSCROLLBAR (RichEdit. h)
description: Показывает или скрывает одну из полос прокрутки в главном окне элемента управления Rich Edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- Элементы управления Windows для EM_SHOWSCROLLBAR сообщений
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988552"
---
# <a name="em_showscrollbar-message"></a>\_Сообщение ШОВСКРОЛЛБАР EM

Показывает или скрывает одну из полос прокрутки в главном окне элемента управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Определяет, какая полоса прокрутки должна отображаться: горизонтальная или вертикальная. Этот параметр должен иметь **SB \_** или **SB \_ горизонтали**.

</dd> <dt>

*lParam* 
</dt> <dd>

Указывает, показывать ли полосу прокрутки или скрывать ее. Укажите **значение true** , чтобы показать полосу прокрутки, и **false** , чтобы скрыть ее.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод допустим только в том случае, если элемент управления находится в активном месте. Вызовы, выполняемые, пока элемент управления неактивен, могут завершиться ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ жетскроллпос**](em-getscrollpos.md)
</dt> <dt>

[**EM \_ сетскроллпос**](em-setscrollpos.md)
</dt> </dl>

 

 





