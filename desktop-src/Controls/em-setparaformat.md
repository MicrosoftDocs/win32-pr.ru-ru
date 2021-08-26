---
title: Сообщение EM_SETPARAFORMAT (RichEdit. h)
description: Задает форматирование абзаца для текущего выделения в элементе управления Rich Edit.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- элементы управления Windows сообщений EM_SETPARAFORMAT
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db0ba4e4bf505c5fb1b746b84cae71dcc621635a0a33b4a533ce8551486fe6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062914"
---
# <a name="em_setparaformat-message"></a>\_Сообщение СЕТПАРАФОРМАТ EM

Задает форматирование абзаца для текущего выделения в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) с указанием новых атрибутов форматирования абзаца. Изменяются только атрибуты, указанные членом **двмаск** .

Microsoft Rich Edit 2,0 и более поздние версии: этот параметр может быть указателем на структуру [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , которая является РАСШИРЕНИЕМ структуры [**формата**](/windows/desktop/api/Richedit/ns-richedit-paraformat) данных. Перед отправкой сообщения **EM \_ сетпараформат** установите элемент **кбсизе** в структуре, чтобы указать версию структуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершилась удачно, возвращаемое значение будет ненулевым.

Если операция завершается ошибкой, возвращаемое значение равно нулю.

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

[**ФОРМАТ \**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





