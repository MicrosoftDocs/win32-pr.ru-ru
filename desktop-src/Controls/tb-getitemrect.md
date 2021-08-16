---
title: Сообщение TB_GETITEMRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник кнопки на панели инструментов.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- элементы управления Windows сообщений TB_GETITEMRECT
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6dbfa4c7e305c4e2dfe53b45edaac1d6601631c920fa266c64292fd7e6d97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829709"
---
# <a name="tb_getitemrect-message"></a>\_Сообщение ЖЕТИТЕМРЕКТ ТБ

Извлекает ограничивающий прямоугольник кнопки на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс кнопки, для которой требуется получить сведения.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает клиентские координаты ограничивающего прямоугольника.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Это сообщение не извлекает ограничивающий прямоугольник для кнопок, состояние которых равно [**\_ скрытому**](toolbar-button-states.md) значению тбстате.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

