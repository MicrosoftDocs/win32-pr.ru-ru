---
title: Сообщение EM_GETTEXTMODE (RichEdit. h)
description: Возвращает текущий текстовый режим и уровень отменяемого элемента управления расширенного редактирования.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- Элементы управления Windows для EM_GETTEXTMODE сообщений
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492006"
---
# <a name="em_gettextmode-message"></a>\_Сообщение ЖЕТТЕКСТМОДЕ EM

Возвращает текущий текстовый режим и уровень отменяемого элемента управления расширенного редактирования.

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

Возвращаемое значение — это одно или несколько значений из типа перечисления [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) . Значения указывают текущий текстовый режим и уровень отмены элемента управления.

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

[**EM \_ сеттекстмоде**](em-settextmode.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





