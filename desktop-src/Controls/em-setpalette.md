---
title: Сообщение EM_SETPALETTE (RichEdit. h)
description: Изменяет палитру, которую элемент управления Rich Edit использует для окна его просмотра.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- Элементы управления Windows для EM_SETPALETTE сообщений
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
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071524"
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

## <a name="remarks"></a>Комментарии

Элемент управления Rich Edit не проверяет, является ли новая палитра допустимой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





