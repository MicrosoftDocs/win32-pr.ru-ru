---
title: Сообщение LB_ITEMFROMPOINT (Winuser. h)
description: Возвращает отсчитываемый от нуля индекс элемента, ближайшего к заданной точке в списке.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- элементы управления Windows сообщений LB_ITEMFROMPOINT
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
ms.openlocfilehash: ddddd58780cb4b140501c567d699373cb1fa03cbf212332bea71611a4add3788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575934"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**макелпарам**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

