---
title: Сообщение TVM_GETLINECOLOR (Коммктрл. h)
description: Сообщение TVM \_ жетлинеколор получает текущий цвет линии.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- Элементы управления Windows для TVM_GETLINECOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071773"
---
# <a name="tvm_getlinecolor-message"></a>\_Сообщение TVM жетлинеколор

Сообщение **TVM \_ жетлинеколор** получает текущий цвет линии.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает текущий цвет строки или \_ значение CLR по умолчанию, если ничего не указано.

## <a name="remarks"></a>Комментарии

Это сообщение получает только цвета линий. Чтобы получить цвета "+" и "-" внутри кнопок, используйте сообщение [**TVM \_ жеттекстколор**](tvm-gettextcolor.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ сетлинеколор**](tvm-setlinecolor.md)
</dt> </dl>

 

 





