---
title: Сообщение EM_GETUNDONAME (RichEdit. h)
description: Microsoft Rich Edit 2,0 и более поздних версий Извлекает тип следующего действия отмены, если оно есть. Microsoft Rich Edit 1,0 это сообщение не поддерживается.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- Элементы управления Windows для EM_GETUNDONAME сообщений
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989087"
---
# <a name="em_getundoname-message"></a>\_Сообщение ЖЕТУНДОНАМЕ EM

Microsoft Rich Edit 2,0 и более поздние версии: Извлекает тип следующего действия отмены, если оно есть.

Microsoft Rich Edit 1,0: это сообщение не поддерживается.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если имеется действие отмены, возвращается значение перечисления [**ундонамеид**](/windows/desktop/api/Richedit/ne-richedit-undonameid) , указывающее тип следующего действия в очереди отмены элемента управления.

Если нет действий, которые можно отменить, или тип следующего действия отмены неизвестен, возвращаемое значение равно нулю.

## <a name="remarks"></a>Комментарии

Типы действий, которые могут быть отменены или повторно выполнены, включают операции ввода, удаления, перетаскивания, удаления, вырезания и вставки. Эти сведения могут быть полезны для приложений, которые предоставляют расширенный пользовательский интерфейс для операций отмены и повтора, например раскрывающийся список действий, которые могут быть отменены.

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

[**EM \_ жетредонаме**](em-getredoname.md)
</dt> <dt>

[**\_Повтор EM**](em-redo.md)
</dt> <dt>

[**\_Отмена EM**](em-undo.md)
</dt> <dt>

[**ундонамеид**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





