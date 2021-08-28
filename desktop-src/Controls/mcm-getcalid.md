---
title: Сообщение MCM_GETCALID (Коммктрл. h)
description: Возвращает идентификатор календаря для данного элемента управления "Календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жеткалид.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- элементы управления Windows сообщений MCM_GETCALID
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148db880fe941c3b7df045c0ecdd4fbc9303203eace2b3be3ab38831aa4e3644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170191"
---
# <a name="mcm_getcalid-message"></a>\_Сообщение MCM жеткалид

Возвращает идентификатор календаря для данного элемента управления "Календарь". Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жеткалид**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Идентификатор текущего календаря. Одна из констант [идентификаторов календаря](/windows/desktop/Intl/calendar-identifiers) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

