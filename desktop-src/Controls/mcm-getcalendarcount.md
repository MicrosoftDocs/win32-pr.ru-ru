---
title: Сообщение MCM_GETCALENDARCOUNT (Коммктрл. h)
description: Возвращает число календарей, отображаемых в данный момент в элементе управления Calendar. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жеткалендаркаунт.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- элементы управления Windows сообщений MCM_GETCALENDARCOUNT
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
ms.openlocfilehash: 9379aa8c273451ba53c2a13d6190712212765b46dc1052a08b6d03ae4ae32e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019052"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





