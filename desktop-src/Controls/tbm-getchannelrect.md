---
title: Сообщение TBM_GETCHANNELRECT (Коммктрл. h)
description: Получает размер и расположение ограничивающего прямоугольника для канала TrackBar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- элементы управления Windows сообщений TBM_GETCHANNELRECT
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
ms.openlocfilehash: af2c9932782a150635365c1cdcb74b624f6863b27180136bc9483e8d0de3ba1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078108"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

