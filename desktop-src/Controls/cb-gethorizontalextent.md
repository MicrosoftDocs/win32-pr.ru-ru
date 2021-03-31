---
title: Сообщение CB_GETHORIZONTALEXTENT (Winuser. h)
description: Возвращает ширину (в пикселях), в которой окно списка можно прокручивать горизонтально (прокручиваемая ширина). Это применимо только в том случае, если в списке есть горизонтальная полоса прокрутки.
ms.assetid: 7c9fff88-2750-4c94-b7f6-6bdd81c224e9
keywords:
- Элементы управления Windows для CB_GETHORIZONTALEXTENT сообщений
topic_type:
- apiref
api_name:
- CB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a2b1fb7c8fe7549360801516364528c9a2ef1f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071619"
---
# <a name="cb_gethorizontalextent-message"></a>\_Сообщение ЖЕСОРИЗОНТАЛЕКСТЕНТ CB

Возвращает ширину (в пикселях), в которой окно списка можно прокручивать горизонтально (прокручиваемая ширина). Это применимо только в том случае, если в списке есть горизонтальная полоса прокрутки.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является прокручиваемой шириной в пикселях.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕСОРИЗОНТАЛЕКСТЕНТ CB**](cb-sethorizontalextent.md)
</dt> </dl>

 

 





