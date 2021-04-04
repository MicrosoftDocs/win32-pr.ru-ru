---
title: Сообщение LB_SETANCHORINDEX (Winuser. h)
description: Задает элемент привязки \ 8212;, т. е. элемент, из которого начинается выбор нескольких элементов. Множественный выбор охватывает все элементы из привязанного элемента в элемент курсора.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- Элементы управления Windows для LB_SETANCHORINDEX сообщений
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137138"
---
# <a name="lb_setanchorindex-message"></a>Сообщение сетанчориндекс балансировки нагрузки \_

Задает элемент привязки, т. е. элемент, из которого начинается выбор нескольких элементов. Множественный выбор охватывает все элементы из привязанного элемента в элемент курсора.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Задает индекс нового элемента привязки.

Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями. Это означает, что списки не могут содержать более 32 767 элементов. Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение прошло удачно, возвращаемое значение равно нулю.

Если сообщение не выполняется, возвращается значение фунтов \_ Err.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетанчориндекс балансировки нагрузки \_**](lb-getanchorindex.md)
</dt> </dl>

 

 





