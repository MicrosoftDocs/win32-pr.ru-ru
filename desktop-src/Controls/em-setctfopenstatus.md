---
title: Сообщение EM_SETCTFOPENSTATUS (RichEdit. h)
description: Открывает или закрывает клавиатуру платформы текстовых служб (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- Элементы управления Windows для EM_SETCTFOPENSTATUS сообщений
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071915"
---
# <a name="em_setctfopenstatus-message"></a>\_Сообщение СЕТКТФОПЕНСТАТУС EM

Открывает или закрывает клавиатуру платформы текстовых служб (TSF).

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Чтобы включить клавиатуру TSF, используйте **значение true**. Чтобы отключить клавиатуру TSF, используйте **значение false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха это сообщение возвращает **значение true**. В случае неудачи это сообщение возвращает **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ жетктфопенстатус**](em-getctfopenstatus.md)
</dt> </dl>

 

 





