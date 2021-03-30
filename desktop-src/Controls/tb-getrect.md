---
title: Сообщение TB_GETRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для указанной кнопки панели инструментов.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- Элементы управления Windows для TB_GETRECT сообщений
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892722"
---
# <a name="tb_getrect-message"></a>Сообщение о терабайте (ТБ) \_

Извлекает ограничивающий прямоугольник для указанной кнопки панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор команды для кнопки.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая будет принимать сведения об ограничивающем прямоугольнике.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="remarks"></a>Комментарии

Это сообщение не извлекает ограничивающий прямоугольник для кнопок, состояние которых равно [**\_ скрытому**](toolbar-button-states.md) значению тбстате.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

