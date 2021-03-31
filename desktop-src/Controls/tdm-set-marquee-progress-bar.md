---
title: Сообщение TDM_SET_MARQUEE_PROGRESS_BAR (Коммктрл. h)
description: Указывает, должен ли размещенный индикатор выполнения диалогового окна задачи отображаться в режиме бегущей строки.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- Элементы управления Windows для TDM_SET_MARQUEE_PROGRESS_BAR сообщений
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
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137426"
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

## <a name="remarks"></a>Комментарии

Сведения о режиме бегущей строки см. в разделе [элемент управления](progress-bar-control.md)"индикатор выполнения".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





