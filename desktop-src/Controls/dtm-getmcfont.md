---
title: Сообщение DTM_GETMCFONT (Коммктрл. h)
description: Возвращает шрифт, который в настоящее время используется элементом управления "Календарь" элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать \_ макрос Жетмонскалфонт DateTime.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- Элементы управления Windows для DTM_GETMCFONT сообщений
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892493"
---
# <a name="dtm_getmcfont-message"></a>\_Сообщение DTM жетмкфонт

Возвращает шрифт, который в настоящее время используется элементом управления "Календарь" элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать макрос [**\_ жетмонскалфонт DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение ХФОНТ, которое является маркером текущего шрифта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





