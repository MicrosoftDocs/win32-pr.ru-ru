---
title: Сообщение TB_GETRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для указанной кнопки панели инструментов.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- элементы управления Windows сообщений TB_GETRECT
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
ms.openlocfilehash: bc9a2b12fd2331a8346addbb5702a7837c9c0b28108850d3a4fd0d8e35432fa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078308"
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

## <a name="remarks"></a>Remarks

Это сообщение не извлекает ограничивающий прямоугольник для кнопок, состояние которых равно [**\_ скрытому**](toolbar-button-states.md) значению тбстате.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

