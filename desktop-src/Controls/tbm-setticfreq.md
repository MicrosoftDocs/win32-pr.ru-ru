---
title: Сообщение TBM_SETTICFREQ (Коммктрл. h)
description: Задает частоту интервала для делений в TrackBar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- Элементы управления Windows для TBM_SETTICFREQ сообщений
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071374"
---
# <a name="tbm_setticfreq-message"></a>\_Сообщение ТБМ сеттикфрек

Задает частоту интервала для делений в TrackBar. Например, если задана частота 2, то для каждого второго приращения в диапазоне TrackBar отображается деление. Значение по умолчанию для периодичности — единица; то есть каждый шаг приращения в диапазоне связан с делением.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Частота делений.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Для использования этого сообщения параметр TrackBar должен иметь стиль [**TBS \_**](trackbar-control-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





