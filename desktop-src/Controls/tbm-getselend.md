---
title: Сообщение TBM_GETSELEND (Коммктрл. h)
description: Извлекает конечное расположение текущего диапазона выбора в TrackBar.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- Элементы управления Windows для TBM_GETSELEND сообщений
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 486d66d3e7fc2dd4d23b89cb5e9406fa81b34638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490695"
---
# <a name="tbm_getselend-message"></a>\_Сообщение ТБМ жетселенд

Извлекает конечное расположение текущего диапазона выбора в TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 32-разрядное значение, указывающее конечную точку текущего диапазона выбора.

## <a name="remarks"></a>Комментарии

Параметр TrackBar может иметь диапазон выбора, только если вы указали стиль [**TBS \_ енаблеселранже**](trackbar-control-styles.md) при его создании.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТБМ \_ жетселстарт**](tbm-getselstart.md)
</dt> <dt>

[**ТБМ \_ сетсел**](tbm-setsel.md)
</dt> <dt>

[**ТБМ \_ сетселенд**](tbm-setselend.md)
</dt> <dt>

[**ТБМ \_ сетселстарт**](tbm-setselstart.md)
</dt> </dl>

 

 





