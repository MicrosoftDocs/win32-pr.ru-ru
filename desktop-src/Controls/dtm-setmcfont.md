---
title: Сообщение DTM_SETMCFONT (Коммктрл. h)
description: Задает шрифт, используемый элементом управления "Календарь" элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать \_ макрос Сетмонскалфонт DateTime.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- элементы управления Windows сообщений DTM_SETMCFONT
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa1b34c1a51e365868cbdae30e46cd299937d3d6fe33bad6c57d630a0b226fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877814"
---
# <a name="dtm_setmcfont-message"></a>\_Сообщение DTM сетмкфонт

Задает шрифт, используемый элементом управления "Календарь" элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать макрос [**\_ сетмонскалфонт DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Описатель для шрифта, который будет задан.

</dd> <dt>

*lParam* 
</dt> <dd>

Указывает, должен ли элемент управления перерисоваться сразу после установки шрифта. Если задать для этого параметра **значение true** , элемент управления будет перерисовываться самим собой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





