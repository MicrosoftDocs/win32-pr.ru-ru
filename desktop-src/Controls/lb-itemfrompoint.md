---
title: Сообщение LB_ITEMFROMPOINT (Winuser. h)
description: Возвращает отсчитываемый от нуля индекс элемента, ближайшего к заданной точке в списке.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- Элементы управления Windows для LB_ITEMFROMPOINT сообщений
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803418"
---
# <a name="lb_itemfrompoint-message"></a>Сообщение итемфромпоинт балансировки нагрузки \_

Возвращает отсчитываемый от нуля индекс элемента, ближайшего к заданной точке в списке.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает координату x точки относительно левого верхнего угла клиентской области окна списка.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Указывает координату y точки относительно левого верхнего угла клиентской области окна списка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение содержит индекс ближайшего элемента в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)). [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) равен нулю, если указанная точка находится в клиентской области списка или если она находится за пределами клиентской области.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**макелпарам**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

