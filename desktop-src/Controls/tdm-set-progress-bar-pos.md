---
title: Сообщение TDM_SET_PROGRESS_BAR_POS (Коммктрл. h)
description: Задает расположение индикатора выполнения в диалоговом окне задачи.
ms.assetid: 82247d70-8527-4195-87af-5c4e5fd1d1a2
keywords:
- Элементы управления Windows для TDM_SET_PROGRESS_BAR_POS сообщений
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_POS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58e12b67c218f21c72f28089a3246d52c6165740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489012"
---
# <a name="tdm_set_progress_bar_pos-message"></a>TDM \_ Задание \_ индикатора \_ выполнения \_ сообщение POS

Задает расположение индикатора выполнения в диалоговом окне задачи.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Значение **типа int** , указывающее новую точку.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущее расположение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





