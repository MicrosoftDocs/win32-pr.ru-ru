---
title: Сообщение ACM_ISPLAYING (Коммктрл. h)
description: Проверяет, воспроизводится ли ролик с чередованием Audio-Video (AVI). Это сообщение можно отправить явно или использовать \_ макрос анимации.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- Элементы управления Windows для ACM_ISPLAYING сообщений
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071333"
---
# <a name="acm_isplaying-message"></a>ACM \_ воспроизведение сообщения

Проверяет, воспроизводится ли ролик с чередованием Audio-Video (AVI). Это сообщение можно отправить явно или использовать макрос [**анимации. \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying)

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

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





