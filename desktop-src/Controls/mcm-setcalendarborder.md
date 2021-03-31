---
title: Сообщение MCM_SETCALENDARBORDER (Коммктрл. h)
description: Задает размер границы (в пикселях). Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткалендарбордер.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- Элементы управления Windows для MCM_SETCALENDARBORDER сообщений
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490518"
---
# <a name="mcm_setcalendarborder-message"></a>\_Сообщение MCM сеткалендарбордер

Задает размер границы (в пикселях). Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сеткалендарбордер**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Если **значение равно true**, то размер границы устанавливается равным количеству пикселей, заданному параметром *lParam* . Если **значение равно false**, то размер границы сбрасывается до значения по умолчанию, указанного в теме, или нуль, если темы не используются.

</dd> <dt>

*lParam* 
</dt> <dd>

Число пикселей размера границы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





