---
title: Сообщение EM_SETPARAFORMAT (RichEdit. h)
description: Задает форматирование абзаца для текущего выделения в элементе управления Rich Edit.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- Элементы управления Windows для EM_SETPARAFORMAT сообщений
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
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490230"
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

[**ФОРМАТ \**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





