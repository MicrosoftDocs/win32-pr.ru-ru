---
title: Сообщение TBM_GETCHANNELRECT (Коммктрл. h)
description: Получает размер и расположение ограничивающего прямоугольника для канала TrackBar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- Элементы управления Windows для TBM_GETCHANNELRECT сообщений
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988369"
---
# <a name="tbm_getchannelrect-message"></a>\_Сообщение ТБМ жетчаннелрект

Получает размер и расположение ограничивающего прямоугольника для канала TrackBar. (Канал — это область, в которой перемещается ползунок. Он содержит выделение при выборе диапазона.)

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) . Сообщение заполняет эту структуру ограничивающим прямоугольником канала в клиентских координатах окна TrackBar.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

