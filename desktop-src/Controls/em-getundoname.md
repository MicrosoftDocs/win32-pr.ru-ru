---
title: Сообщение EM_GETUNDONAME (RichEdit. h)
description: Microsoft Rich Edit 2,0 и более поздних версий Извлекает тип следующего действия отмены, если оно есть. Microsoft Rich Edit 1,0 это сообщение не поддерживается.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- элементы управления Windows сообщений EM_GETUNDONAME
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
ms.openlocfilehash: d133038c0adad2fe7eaa1ae98cf638fe6bd13fad82df3b3d2d1ac384a30e1a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576644"
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

## <a name="remarks"></a>Remarks

Типы действий, которые могут быть отменены или повторно выполнены, включают операции ввода, удаления, перетаскивания, удаления, вырезания и вставки. Эти сведения могут быть полезны для приложений, которые предоставляют расширенный пользовательский интерфейс для операций отмены и повтора, например раскрывающийся список действий, которые могут быть отменены.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 





