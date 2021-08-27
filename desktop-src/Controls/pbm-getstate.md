---
title: Сообщение PBM_GETSTATE (Коммктрл. h)
description: Возвращает состояние индикатора выполнения.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- элементы управления Windows сообщений PBM_GETSTATE
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cd157ccb6ab8a1fe4cd4a31bf1f8a033f0e591288338e21cc322a8ac10bfc41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047014"
---
# <a name="pbm_getstate-message"></a>\_Сообщение о состоянии PBM

Возвращает состояние индикатора выполнения.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает текущее состояние индикатора выполнения. Одно из следующих значений.



| Код возврата                                                                                 | Описание             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**ПБСТ, \_ Обычная**</dt> </dl> | Выполняется.<br/> |
| <dl> <dt>**ПБСТ, \_ Ошибка**</dt> </dl>  | Ошибка.<br/>       |
| <dl> <dt>**ПБСТ \_ приостановлена**</dt> </dl> | приостановлено<br/>      |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





