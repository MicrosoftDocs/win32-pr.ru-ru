---
title: Сообщение STM_GETICON (Winuser. h)
description: Приложение отправляет \_ сообщение STM-Icon, чтобы получить маркер значка, связанного со статическим элементом управления, имеющим \_ стиль значка SS.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- элементы управления Windows сообщений STM_GETICON
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
ms.openlocfilehash: d33aab01e668f4b77e36a0a62b8eab75f3ee5db82188416c295c04cdf9bcb078
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084954"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**STM \_ сетикон**](stm-seticon.md)
</dt> </dl>

 

 





