---
title: Сообщение UDM_GETRANGE (Коммктрл. h)
description: Извлекает минимальные и максимальные позиции (диапазон) для элемента управления "вверх/вниз".
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- элементы управления Windows сообщений UDM_GETRANGE
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
ms.openlocfilehash: d13811f383886e0e4985eb3f2f5093eec53cb0745349a36ca133fa3de9656773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408104"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

