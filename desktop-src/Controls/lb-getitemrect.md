---
title: Сообщение LB_GETITEMRECT (Winuser. h)
description: Возвращает размеры прямоугольника, который привязывает элемент списка в том виде, в каком он в данный момент отображается в списке.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- Элементы управления Windows для LB_GETITEMRECT сообщений
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b66c7c1a3e9f93e90beea40869cecb2081cb20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490206"
---
# <a name="lb_getitemrect-message"></a>Сообщение жетитемрект балансировки нагрузки \_

Возвращает размеры прямоугольника, который привязывает элемент списка в том виде, в каком он в данный момент отображается в списке.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Основанный на нуле индекс элемента.

Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями. Это означает, что списки не могут содержать более 32 767 элементов. Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая будет принимать клиентские координаты элемента в списке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если возникает ошибка, возвращается значение фунтов \_ Err.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ПЕРЕТАСКИВАЕМЫЕ**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

