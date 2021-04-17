---
description: Функция Жетфрамедстаддрессоффсет возвращает смещение к адресу назначения данного кадра.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Функция Жетфрамедстаддрессоффсет (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673187"
---
# <a name="getframedstaddressoffset-function"></a>Функция Жетфрамедстаддрессоффсет

Функция **жетфрамедстаддрессоффсет** возвращает смещение к адресу назначения данного кадра.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфраме* \[ окне\]
</dt> <dd>

Обработчик для фрейма.

</dd> <dt>

*AddressType* \[ окне\]
</dt> <dd>

Тип адреса назначения. Укажите одно из следующих значений.

\_тип адреса \_ Ethernet адрес \_ тип \_ IP-адреса тип \_ \_ IPX адрес тип \_ \_ токенринг адрес тип \_ \_ FDDI адрес \_ тип \_ КСНС адрес тип адреса \_ \_ Vine \_ IP address \_ Type \_ ATM.

</dd> <dt>

*Аддрессленгс* \[ окне\]
</dt> <dd>

Длина адреса назначения в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение смещения (измеряется в байтах) с запрошенным типом адреса.

Если функция завершилась неудачно, возвращаемое значение равно минус единице (-1).

## <a name="remarks"></a>Комментарии

Если параметру *addressType* присвоено \_ \_ значение Ethernet, возвращаемое функция **жетфрамедстаддрессоффсет** всегда равно нулю. Смещение адреса Ethernet всегда равно нулю.

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамедстаддрессоффсет** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




