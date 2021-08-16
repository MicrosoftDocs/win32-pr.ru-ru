---
title: Сообщение EM_SETPALETTE (RichEdit. h)
description: Изменяет палитру, которую элемент управления Rich Edit использует для окна его просмотра.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- элементы управления Windows сообщений EM_SETPALETTE
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93225a7a550f86bb8b32bf5939a8c7b7aa862ac96c8459bd6bcceb4c6b76e516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831155"
---
# <a name="em_setpalette-message"></a>\_Сообщение СЕТПАЛЕТТЕ EM

Изменяет палитру, которую элемент управления Rich Edit использует для окна его просмотра.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик для новой палитры, используемой элементом управления Rich Edit.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Элемент управления Rich Edit не проверяет, является ли новая палитра допустимой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





