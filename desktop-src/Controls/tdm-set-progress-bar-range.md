---
title: Сообщение TDM_SET_PROGRESS_BAR_RANGE (Коммктрл. h)
description: Задает минимальное и максимальное значения индикатора выполнения в диалоговом окне задачи.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- элементы управления Windows сообщений TDM_SET_PROGRESS_BAR_RANGE
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
ms.openlocfilehash: 54d94da64bd01b17addeb8f65def177e7e7e5d7daccbafb1629d1158f8c6636d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875914"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

