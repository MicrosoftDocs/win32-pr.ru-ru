---
title: Сообщение TDM_SET_PROGRESS_BAR_RANGE (Коммктрл. h)
description: Задает минимальное и максимальное значения индикатора выполнения в диалоговом окне задачи.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- Элементы управления Windows для TDM_SET_PROGRESS_BAR_RANGE сообщений
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892717"
---
# <a name="tdm_set_progress_bar_range-message"></a>TDM \_ задать \_ \_ \_ сообщение диапазона индикатора выполнения

Задает минимальное и максимальное значения индикатора выполнения в диалоговом окне задачи.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает минимальное значение. По умолчанию минимальное значение равно нулю. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает максимальное значение. По умолчанию максимальное значение равно 100.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущие минимальные и максимальные значения, если они успешно, или ноль в противном случае. [**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит минимальное значение, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) содержит максимальное значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

