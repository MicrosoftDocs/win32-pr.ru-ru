---
title: Сообщение MCM_SETCALID (Коммктрл. h)
description: Задает идентификатор календаря для данного элемента управления Calendar. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткалид.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- Элементы управления Windows для MCM_SETCALID сообщений
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
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071257"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

