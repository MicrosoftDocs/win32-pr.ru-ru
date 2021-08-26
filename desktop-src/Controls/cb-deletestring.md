---
title: Сообщение CB_DELETESTRING (Winuser. h)
description: Удаляет строку из списка в поле со списком.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- элементы управления Windows сообщений CB_DELETESTRING
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
ms.openlocfilehash: b0bed1d654b86ffeb4a02c780678822e1999847ef0e163e35ecba081af099f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063584"
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

## <a name="remarks"></a>Remarks

Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , система отправит сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) владельцу поля со списком, чтобы приложение могла освобождать любые дополнительные данные, связанные с элементом.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_РЕСЕТКОНТЕНТ CB**](cb-resetcontent.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





