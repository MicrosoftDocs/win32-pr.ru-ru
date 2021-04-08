---
title: Сообщение EM_GETCTFOPENSTATUS (RichEdit. h)
description: Определяет, открыта или закрыта клавиатура платформы текстовых служб (TSF).
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- Элементы управления Windows для EM_GETCTFOPENSTATUS сообщений
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988768"
---
# <a name="em_getctfopenstatus-message"></a>\_Сообщение ЖЕТКТФОПЕНСТАТУС EM

Определяет, открыта или закрыта клавиатура платформы текстовых служб (TSF).

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

Если клавиатура TSF открыта, возвращается значение **true**. В противном случае — **false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сетктфопенстатус**](em-setctfopenstatus.md)
</dt> </dl>

 

 





