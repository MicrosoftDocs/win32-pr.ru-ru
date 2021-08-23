---
title: Сообщение MCM_SETCALENDARBORDER (Коммктрл. h)
description: Задает размер границы (в пикселях). Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткалендарбордер.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- элементы управления Windows сообщений MCM_SETCALENDARBORDER
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
ms.openlocfilehash: 08e020ad282ce21555e6c3a74198a0034013ac1d7cfac8f4eb68e52137e5f684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697204"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





