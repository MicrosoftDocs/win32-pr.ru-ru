---
description: Функция Мактипетоаддресстипе преобразует данный тип MAC в тип адреса.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Функция Мактипетоаддресстипе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897626"
---
# <a name="mactypetoaddresstype-function"></a>Функция Мактипетоаддресстипе

Функция **мактипетоаддресстипе** преобразует данный тип Mac в тип адреса.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*MacType* \[ окне\]
</dt> <dd>

Преобразуемый тип MAC. Укажите одно из следующих значений.

\_тип Mac \_ Ethernet Mac \_ Type \_ токенринг Mac \_ Type \_ FDDI

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является одним из следующих типов адресов.

\_тип адреса \_ Ethernet адрес \_ тип \_ токенринг адрес \_ тип \_ FDDI

Если функция не выполнена, тип MAC неизвестен, возвращается значение-1.

## <a name="remarks"></a>Комментарии

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **мактипетоаддресстипе** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




