---
title: Сообщение MCM_GETCALID (Коммктрл. h)
description: Возвращает идентификатор календаря для данного элемента управления "Календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жеткалид.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- Элементы управления Windows для MCM_GETCALID сообщений
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
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136138"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

