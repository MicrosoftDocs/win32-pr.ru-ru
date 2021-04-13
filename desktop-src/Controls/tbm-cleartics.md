---
title: Сообщение TBM_CLEARTICS (Коммктрл. h)
description: Удаляет текущие деления из TrackBar. Это сообщение не удаляет первый и последний деления, которые создаются автоматически с помощью TrackBar.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- Элементы управления Windows для TBM_CLEARTICS сообщений
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489813"
---
# <a name="tbm_cleartics-message"></a>\_Сообщение ТБМ клеартикс

Удаляет текущие деления из TrackBar. Это сообщение не удаляет первый и последний деления, которые создаются автоматически с помощью TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг перерисовки. Если этот параметр имеет **значение true**, линейка перерисовывается после очистки делений. Если этот параметр имеет **значение false**, сообщение очищает деления, но не перерисовывает TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





