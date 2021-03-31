---
title: Сообщение MCM_GETCALENDARCOUNT (Коммктрл. h)
description: Возвращает число календарей, отображаемых в данный момент в элементе управления Calendar. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жеткалендаркаунт.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- Элементы управления Windows для MCM_GETCALENDARCOUNT сообщений
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136650"
---
# <a name="mcm_getcalendarcount-message"></a>\_Сообщение MCM жеткалендаркаунт

Возвращает число календарей, отображаемых в данный момент в элементе управления Calendar. Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жеткалендаркаунт**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .

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

Число календарей, отображаемых в данный момент в элементе управления Calendar. Максимальное число разрешенных календарей — 12.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





