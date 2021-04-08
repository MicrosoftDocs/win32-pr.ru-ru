---
title: Сообщение LB_GETSEL (Winuser. h)
description: Возвращает состояние выбора элемента.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- Элементы управления Windows для LB_GETSEL сообщений
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d808935e65a1ea748c59d606aa2cf483748fb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892149"
---
# <a name="lb_getsel-message"></a>Сообщение жетсел балансировки нагрузки \_

Возвращает состояние выбора элемента.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Основанный на нуле индекс элемента.

Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями. Это означает, что списки не могут содержать более 32 767 элементов. Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если выбран элемент, возвращаемое значение больше нуля; в противном случае он равен нулю. Если возникает ошибка, возвращается значение фунтов \_ Err.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сетсел балансировки нагрузки \_**](lb-setsel.md)
</dt> </dl>

 

 





