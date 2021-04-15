---
title: Сообщение TBM_GETSELSTART (Коммктрл. h)
description: Получает начальную точку текущего диапазона выбора в TrackBar.
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- Элементы управления Windows для TBM_GETSELSTART сообщений
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af796c57adb3615241a8f5b702ff58062468509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654514"
---
# <a name="tbm_getselstart-message"></a>\_Сообщение ТБМ жетселстарт

Получает начальную точку текущего диапазона выбора в TrackBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 32-разрядное значение, указывающее начальную точку диапазона текущего выбора.

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

[**ТБМ \_ жетселенд**](tbm-getselend.md)
</dt> <dt>

[**ТБМ \_ сетсел**](tbm-setsel.md)
</dt> <dt>

[**ТБМ \_ сетселенд**](tbm-setselend.md)
</dt> <dt>

[**ТБМ \_ сетселстарт**](tbm-setselstart.md)
</dt> </dl>

 

 





