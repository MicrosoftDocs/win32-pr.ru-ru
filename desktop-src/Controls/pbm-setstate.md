---
title: Сообщение PBM_SETSTATE (Коммктрл. h)
description: Задает состояние индикатора выполнения.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- Элементы управления Windows для PBM_SETSTATE сообщений
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491799"
---
# <a name="pbm_setstate-message"></a>\_Сообщение SETSTATE PBM

Задает состояние индикатора выполнения.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Состояние установленного индикатора выполнения. Одно из следующих значений.



| Значение                                                                                                                                                   | Значение                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**ПБСТ, \_ Обычная**</dt> </dl> | Выполняется.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**ПБСТ, \_ Ошибка**</dt> </dl>    | Ошибка.<br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**ПБСТ \_ приостановлена**</dt> </dl> | приостановлено<br/>      |



 

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущее состояние.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





