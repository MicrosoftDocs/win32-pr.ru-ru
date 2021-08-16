---
description: Функция Жетфрамесркаддрессоффсет возвращает смещение исходного адреса кадров.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Функция Жетфрамесркаддрессоффсет (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5c8c2315b53d336a06a73e63019daee842439f65aa53e3fb7d34d4944dcab9cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366098"
---
# <a name="getframesrcaddressoffset-function"></a>Функция Жетфрамесркаддрессоффсет

Функция **жетфрамесркаддрессоффсет** возвращает смещение исходного адреса кадра.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфраме* 
</dt> <dd>

Обработчик для фрейма.

</dd> <dt>

*AddressType* 
</dt> <dd>

Тип исходного адреса. Значение параметра может быть одним из следующих:

-   \_тип адреса \_ Ethernet
-   \_IP-адрес типа адреса \_
-   \_тип адреса \_ IPX
-   \_тип адреса \_ токенринг
-   \_тип адреса \_ FDDI
-   \_тип адреса \_ КСНС
-   тип адреса " \_ \_ IP-адрес Vines" \_
-   \_тип адреса \_ ATM

</dd> <dt>

*аддрессленгс* 
</dt> <dd>

Указатель на возвращаемый **параметр типа DWORD** содержит длину адреса в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является смещением к исходному адресу.

Если функция завершилась неудачно, возвращаемое значение равно минус единице (-1).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




