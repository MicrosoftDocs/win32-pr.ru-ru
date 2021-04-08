---
title: Сообщение LB_DELETESTRING (Winuser. h)
description: Удаляет строку из списка.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- Элементы управления Windows для LB_DELETESTRING сообщений
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892389"
---
# <a name="lb_deletestring-message"></a>Сообщение делетестринг балансировки нагрузки \_

Удаляет строку из списка.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс удаляемой строки.

Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями. Это означает, что списки не могут содержать более 32 767 элементов. Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение — это количество строк, остающихся в списке. Возвращаемое значение — это ошибка балансировки нагрузки, \_ Если параметр *wParam* задает индекс, превышающий число элементов в списке.

## <a name="remarks"></a>Комментарии

Если приложение создает список с помощью стиля, рисуемого владельцем, но без стиля [**фунта \_ хасстрингс**](list-box-styles.md) , система отправляет владельцу списка сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) , чтобы приложение могла освобождать любые дополнительные данные, связанные с элементом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ADDSTRING балансировки нагрузки \_**](lb-addstring.md)
</dt> <dt>

[**инсертстринг балансировки нагрузки \_**](lb-insertstring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





