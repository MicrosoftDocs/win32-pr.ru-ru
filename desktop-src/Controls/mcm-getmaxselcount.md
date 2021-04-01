---
title: Сообщение MCM_GETMAXSELCOUNT (Коммктрл. h)
description: Возвращает максимальный диапазон дат, который можно выбрать в элементе управления ' календарь на месяц '. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетмаксселкаунт.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- Элементы управления Windows для MCM_GETMAXSELCOUNT сообщений
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071778"
---
# <a name="mcm_getmaxselcount-message"></a>\_Сообщение MCM жетмаксселкаунт

Возвращает максимальный диапазон дат, который можно выбрать в элементе управления ' календарь на месяц '. Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жетмаксселкаунт**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа INT, представляющее общее количество дней, которое может быть выбрано для элемента управления.

## <a name="remarks"></a>Комментарии

Можно изменить максимальный диапазон дат, который можно выбрать, с помощью сообщения [**MCM \_ сетмаксселкаунт**](mcm-setmaxselcount.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





