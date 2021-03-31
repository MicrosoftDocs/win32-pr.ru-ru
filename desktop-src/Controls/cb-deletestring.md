---
title: Сообщение CB_DELETESTRING (Winuser. h)
description: Удаляет строку из списка в поле со списком.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- Элементы управления Windows для CB_DELETESTRING сообщений
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137447"
---
# <a name="cb_deletestring-message"></a>\_Сообщение ДЕЛЕТЕСТРИНГ CB

Удаляет строку из списка в поле со списком.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс удаляемой строки.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение — это количество строк, остающихся в списке. Если параметр *wParam* задает индекс, превышающий число элементов в списке, возвращается значение CB \_ Err.

## <a name="remarks"></a>Комментарии

Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , система отправит сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) владельцу поля со списком, чтобы приложение могла освобождать любые дополнительные данные, связанные с элементом.

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

[**\_РЕСЕТКОНТЕНТ CB**](cb-resetcontent.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





