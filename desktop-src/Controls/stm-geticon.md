---
title: Сообщение STM_GETICON (Winuser. h)
description: Приложение отправляет \_ сообщение STM-Icon, чтобы получить маркер значка, связанного со статическим элементом управления, имеющим \_ стиль значка SS.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- Элементы управления Windows для STM_GETICON сообщений
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135359"
---
# <a name="stm_geticon-message"></a>\_Сообщение STM

Приложение отправляет сообщение **STM- \_ Icon** , чтобы получить маркер значка, связанного со статическим элементом управления, имеющим \_ стиль значка SS.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является обработчиком значка или **null** , если статический элемент управления не имеет связанного значка или если произошла ошибка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**STM \_ сетикон**](stm-seticon.md)
</dt> </dl>

 

 





