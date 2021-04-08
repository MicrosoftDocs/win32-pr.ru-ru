---
title: Сообщение CB_RESETCONTENT (Winuser. h)
description: Удаляет все элементы из списка и элементы управления поля со списком.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- Элементы управления Windows для CB_RESETCONTENT сообщений
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891917"
---
# <a name="cb_resetcontent-message"></a>\_Сообщение РЕСЕТКОНТЕНТ CB

Удаляет все элементы из списка и элементы управления поля со списком.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение всегда возвращает значение CB \_ .

## <a name="remarks"></a>Комментарии

Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , владелец поля со списком получает сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) для каждого элемента в поле со списком.

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

[**\_ДЕЛЕТЕСТРИНГ CB**](cb-deletestring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





