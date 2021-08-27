---
title: Сообщение LB_GETSEL (Winuser. h)
description: Возвращает состояние выбора элемента.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- элементы управления Windows сообщений LB_GETSEL
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
ms.openlocfilehash: 43e27a1bcec021d7416e32d1bae4047f7b2705e347cc396a07dcf6c377ccb48f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085514"
---
# <a name="lb_getsel-message"></a>Сообщение жетсел балансировки нагрузки \_

Возвращает состояние выбора элемента.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Основанный на нуле индекс элемента.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями. Это означает, что списки не могут содержать более 32 767 элементов. Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если выбран элемент, возвращаемое значение больше нуля; в противном случае он равен нулю. Если возникает ошибка, возвращается значение фунтов \_ Err.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сетсел балансировки нагрузки \_**](lb-setsel.md)
</dt> </dl>

 

 





