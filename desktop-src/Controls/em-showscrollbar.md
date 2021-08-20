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
ms.openlocfilehash: dc3988ced825fed457549fc9f662a418295de7df6085f04c3e71255ca4ad54c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831145"
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

## <a name="remarks"></a>Remarks

Этот метод допустим только в том случае, если элемент управления находится в активном месте. Вызовы, выполняемые, пока элемент управления неактивен, могут завершиться ошибкой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ жетскроллпос**](em-getscrollpos.md)
</dt> <dt>

[**EM \_ сетскроллпос**](em-setscrollpos.md)
</dt> </dl>

 

 





