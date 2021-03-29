---
title: Сообщение EM_SETWORDBREAKPROCEX (RichEdit. h)
description: Задает расширенную процедуру разбиения по словам для элемента управления расширенного редактирования.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- Элементы управления Windows для EM_SETWORDBREAKPROCEX сообщений
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988485"
---
# <a name="em_setwordbreakprocex-message"></a>\_Сообщение СЕТВОРДБРЕАКПРОЦЕКС EM

Задает расширенную процедуру разбиения по словам для элемента управления расширенного редактирования.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на функцию [*едитвордбреакпроцекс*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) или **значение NULL** для использования процедуры по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение возвращает адрес предыдущей расширенной процедуры разбиения по словам.

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

[**едитвордбреакпроцекс**](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[**EM \_ жетвордбреакпроцекс**](em-getwordbreakprocex.md)
</dt> </dl>

 

 





