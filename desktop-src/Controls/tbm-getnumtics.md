---
title: Сообщение TBM_GETNUMTICS (Коммктрл. h)
description: Возвращает количество делений в TrackBar.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- Элементы управления Windows для TBM_GETNUMTICS сообщений
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988368"
---
# <a name="tbm_getnumtics-message"></a>\_Сообщение ТБМ жетнумтикс

Возвращает количество делений в TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если [флаг деления](trackbar-control-styles.md) не установлен, он возвращает значение 2 для начального и конечного тактов. Если [**задан \_ параметр TBS**](trackbar-control-styles.md) , он возвращает ноль. В противном случае он принимает разность между минимальным и максимальным диапазоном, делит их на тактовую частоту и добавляет 2.

## <a name="remarks"></a>Комментарии

Сообщение **ТБМ \_ жетнумтикс** подсчитывает все деления, включая первый и последний деления, созданные с помощью TrackBar.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





