---
title: Сообщение PBM_SETSTATE (Коммктрл. h)
description: Задает состояние индикатора выполнения.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- элементы управления Windows сообщений PBM_SETSTATE
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
ms.openlocfilehash: 794006517eaa23789f3a25425b1213fede7f8dde9893587def02ebc9605b28f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986064"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





