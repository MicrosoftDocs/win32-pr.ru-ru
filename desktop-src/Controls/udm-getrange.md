---
title: Сообщение UDM_GETRANGE (Коммктрл. h)
description: Извлекает минимальные и максимальные позиции (диапазон) для элемента управления "вверх/вниз".
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- Элементы управления Windows для UDM_GETRANGE сообщений
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262229"
---
# <a name="udm_getrange-message"></a>\_Сообщение о ВЫДИАПАЗОНЕ UDM

Извлекает минимальные и максимальные позиции (диапазон) для элемента управления "вверх/вниз".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение — это 32-разрядное значение, которое содержит минимальное и максимальное позиции. [**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) является максимальным положением для элемента управления, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — минимальным положением.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

