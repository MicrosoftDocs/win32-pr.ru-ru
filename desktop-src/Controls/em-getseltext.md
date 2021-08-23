---
title: Сообщение EM_GETSELTEXT (RichEdit. h)
description: Извлекает текущий выделенный текст в элементе управления Rich Edit.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- элементы управления Windows сообщений EM_GETSELTEXT
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540567f1b52c936ad085acac8e0374fdb0a912bae06480632263f9676f2948e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019502"
---
# <a name="em_getseltext-message"></a>\_Сообщение ЖЕТСЕЛТЕКСТ EM

Извлекает текущий выделенный текст в элементе управления Rich Edit.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на буфер, который получает выделенный текст. Вызывающее приложение должно гарантировать, что буфер достаточно велик, чтобы вместить выделенный текст.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение возвращает число скопированных символов, не включая завершающий символ null.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





