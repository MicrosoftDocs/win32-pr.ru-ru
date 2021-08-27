---
title: Сообщение TDM_SET_MARQUEE_PROGRESS_BAR (Коммктрл. h)
description: Указывает, должен ли размещенный индикатор выполнения диалогового окна задачи отображаться в режиме бегущей строки.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- элементы управления Windows сообщений TDM_SET_MARQUEE_PROGRESS_BAR
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13262339f7d87ea68755a38a49cc8c327706939d6b18025f350334dfdbe3dd4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104614"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>Сообщение с индикатором \_ выполнения TDM Set \_ Marquee \_ \_

Указывает, должен ли размещенный индикатор выполнения диалогового окна задачи отображаться в режиме бегущей строки.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

**Логическое** значение, указывающее, должен ли индикатор выполнения отображаться в режиме бегущей строки. Значение **true** включает режим бегущей строки, а значение **false** отключает режим бегущей строки.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Remarks

Сведения о режиме бегущей строки см. в разделе [элемент управления](progress-bar-control.md)"индикатор выполнения".

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





