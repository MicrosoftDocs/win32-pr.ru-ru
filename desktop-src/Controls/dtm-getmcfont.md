---
title: Сообщение DTM_GETMCFONT (Коммктрл. h)
description: Возвращает шрифт, который в настоящее время используется элементом управления "Календарь" элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать \_ макрос Жетмонскалфонт DateTime.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- элементы управления Windows сообщений DTM_GETMCFONT
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
ms.openlocfilehash: b2bf60f226e7fe5d309324bc517a7fd215abe4591fd5141ff149b14e162ac9be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878134"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





