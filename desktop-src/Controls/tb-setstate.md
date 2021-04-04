---
title: Сообщение TB_SETSTATE (Коммктрл. h)
description: Задает состояние указанной кнопки на панели инструментов.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- Элементы управления Windows для TB_SETSTATE сообщений
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aa46dc68d9af5559e580e697bf6893b15051cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137838"
---
# <a name="tb_setstate-message"></a>\_Сообщение SETSTATE ТБ

Задает состояние указанной кнопки на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор команды для кнопки.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) представляет собой сочетание значений, перечисленных в поле [состояния кнопки на панели инструментов](toolbar-button-states.md). [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

