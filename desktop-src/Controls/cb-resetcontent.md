---
title: Сообщение CB_RESETCONTENT (Winuser. h)
description: Удаляет все элементы из списка и элементы управления поля со списком.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- элементы управления Windows сообщений CB_RESETCONTENT
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
ms.openlocfilehash: 4918437d7b0d347e071386486b31e5f4b9d948b4ff55b4c6eea6e3afe93fb1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832252"
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

## <a name="remarks"></a>Remarks

Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , владелец поля со списком получает сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) для каждого элемента в поле со списком.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_ДЕЛЕТЕСТРИНГ CB**](cb-deletestring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





