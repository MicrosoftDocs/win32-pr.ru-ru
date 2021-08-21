---
title: Сообщение MCM_SETCALID (Коммктрл. h)
description: Задает идентификатор календаря для данного элемента управления Calendar. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткалид.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- элементы управления Windows сообщений MCM_SETCALID
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40e7f4577382aa0e003165e38e4557b8dc234592f747a579e5a071ce2440a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575584"
---
# <a name="mcm_setcalid-message"></a>\_Сообщение MCM сеткалид

Задает идентификатор календаря для данного элемента управления Calendar. Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сеткалид**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

ИДЕНТИФИКАТОР календаря. Одна из констант [идентификаторов календаря](/windows/desktop/Intl/calendar-identifiers) .

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Не используется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

