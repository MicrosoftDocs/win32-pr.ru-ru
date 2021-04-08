---
title: Сообщение EM_GETSELTEXT (RichEdit. h)
description: Извлекает текущий выделенный текст в элементе управления Rich Edit.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- Элементы управления Windows для EM_GETSELTEXT сообщений
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
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891838"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





