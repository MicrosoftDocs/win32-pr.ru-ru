---
title: Сообщение LB_SETTOPINDEX (Winuser. h)
description: Гарантирует, что указанный элемент в окне списка будет видимым.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- элементы управления Windows сообщений LB_SETTOPINDEX
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b640b55ed2c6e3e38eea0b8bd23eb4f99d770dd49b4499f054f5ec38b71873
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435464"
---
# <a name="lb_settopindex-message"></a>Сообщение сеттопиндекс балансировки нагрузки \_

Гарантирует, что указанный элемент в окне списка будет видимым.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс элемента в списке.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями. Это означает, что списки не могут содержать более 32 767 элементов. Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если возникает ошибка, возвращается значение фунтов \_ Err.

## <a name="remarks"></a>Remarks

Система прокручивает содержимое списка таким образом, чтобы указанный элемент появился в верхней части окна списка или был достигнут максимальный диапазон прокрутки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жеттопиндекс балансировки нагрузки \_**](lb-gettopindex.md)
</dt> </dl>

 

 





