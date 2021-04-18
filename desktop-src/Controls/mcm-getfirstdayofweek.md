---
title: Сообщение MCM_GETFIRSTDAYOFWEEK (Коммктрл. h)
description: Извлекает первый день недели для элемента управления "месячный календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетфирстдайофвик.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- Элементы управления Windows для MCM_GETFIRSTDAYOFWEEK сообщений
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654551"
---
# <a name="mcm_getfirstdayofweek-message"></a>\_Сообщение MCM жетфирстдайофвик

Извлекает первый день недели для элемента управления "месячный календарь". Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жетфирстдайофвик**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа DWORD** , содержащее два значения. Верхнее слово является **логическим** значением, которое не равно нулю, если первый день недели имеет значение, отличное от locale \_ ифирстдайофвик, или ноль в противном случае. Младшее слово — это значение типа INT, представляющее первый день недели, где 0 — понедельник, 1 — вторник и т. д.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





