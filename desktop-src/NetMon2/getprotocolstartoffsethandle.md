---
description: Функция Жетпротоколстартоффсесандле возвращает смещение кадра для данного протокола.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Функция Жетпротоколстартоффсесандле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662181"
---
# <a name="getprotocolstartoffsethandle-function"></a>Функция Жетпротоколстартоффсесандле

Функция **жетпротоколстартоффсесандле** возвращает смещение кадра для данного протокола.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфраме* \[ окне\]
</dt> <dd>

Обработчик для фрейма.

</dd> <dt>

*хпротокол* \[ окне\]
</dt> <dd>

Обработчик для протокола.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является смещением кадра, измеряемого в байтах.

Если функция завершилась неудачно, возвращаемое значение равно единице (1).

## <a name="remarks"></a>Комментарии

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетпротоколстартоффсесандле** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




