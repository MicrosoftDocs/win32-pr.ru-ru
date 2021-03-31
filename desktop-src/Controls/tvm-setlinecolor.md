---
title: Сообщение TVM_SETLINECOLOR (Коммктрл. h)
description: В \_ сообщении TVM сетлинеколор устанавливается текущий цвет линии.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- Элементы управления Windows для TVM_SETLINECOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071735"
---
# <a name="tvm_setlinecolor-message"></a>\_Сообщение TVM сетлинеколор

В сообщении **TVM \_ сетлинеколор** устанавливается текущий цвет линии.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Цвет новой линии. Используйте \_ значение по умолчанию CLR для восстановления системных цветов по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает цвет предыдущей строки.

## <a name="remarks"></a>Комментарии

Это сообщение изменяет только цвета линий. Чтобы изменить цвета "+" и "-" внутри кнопок, используйте сообщение [**TVM \_ сеттекстколор**](tvm-settextcolor.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ жетлинеколор**](tvm-getlinecolor.md)
</dt> </dl>

 

 





