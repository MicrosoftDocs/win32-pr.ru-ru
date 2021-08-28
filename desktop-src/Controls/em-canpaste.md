---
title: Сообщение EM_CANPASTE (RichEdit. h)
description: Определяет, может ли элемент управления Rich-Edit вставлять указанный формат буфера обмена.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- элементы управления Windows сообщений EM_CANPASTE
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f2d831cd3b3d04fcb7859d2b5936b7354fbb6b638558d605c9f8c5a6ee6333
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916064"
---
# <a name="em_canpaste-message"></a>\_Сообщение КАНПАСТЕ EM

Определяет, может ли элемент управления Rich-Edit вставлять указанный формат буфера обмена.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает [форматы буфера обмена](/windows/desktop/dataxchg/clipboard-formats) для попыток. Чтобы использовать любой формат в буфере обмена, присвойте этому параметру значение 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если формат буфера обмена может быть вставлен, возвращаемое значение будет ненулевым.

Если формат буфера обмена не может быть вставлен, возвращаемое значение равно нулю.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

