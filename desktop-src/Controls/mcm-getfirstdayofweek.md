---
title: Сообщение MCM_GETFIRSTDAYOFWEEK (Коммктрл. h)
description: Извлекает первый день недели для элемента управления "месячный календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетфирстдайофвик.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- элементы управления Windows сообщений MCM_GETFIRSTDAYOFWEEK
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
ms.openlocfilehash: 1bc0ddcd36da0b993f3a05092c878319a6749d9eb5a3043ce910eba1462beef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319654"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





