---
title: Сообщение ACM_STOP (Коммктрл. h)
description: Останавливает воспроизведение фрагмента AVI в элементе управления Animation. Это сообщение можно отправить явным образом или с помощью \_ макроса анимации.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- Элементы управления Windows для ACM_STOP сообщений
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135371"
---
# <a name="acm_stop-message"></a>Сообщение о фатальной ошибке ACM \_

Останавливает воспроизведение фрагмента AVI в элементе управления Animation. Это сообщение можно отправить явным образом или с помощью макроса [**анимации \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





