---
description: Функция Компарефрамесаурцеаддресс сравнивает адрес с исходным адресом кадра.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Функция Компарефрамесаурцеаддресс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265818"
---
# <a name="compareframesourceaddress-function"></a>Функция Компарефрамесаурцеаддресс

Функция **компарефрамесаурцеаддресс** сравнивает адрес с исходным адресом кадра.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфраме* \[ окне\]
</dt> <dd>

Обработчик для фрейма.

</dd> <dt>

*лпаддресс* \[ окне\]
</dt> <dd>

Указатель на адрес.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если адреса совпадают, возвращается значение **true**.

Если адреса не совпадают, возвращается значение **false**.

## <a name="remarks"></a>Комментарии

Чтобы функция **компарефрамесаурцеаддресс** была выполнена, тип адреса источника должен совпадать с типом адреса, указанным в параметре *лпаддресс* .

Сетевой монитор предоставляет две другие функции для сравнения адресов: [компарефрамедестаддресс](compareframedestaddress.md) и [компареаддрессес](compareaddresses.md). Функция **компарефрамедестаддресс** сравнивает заданный адрес с адресом назначения кадра, а функция **компареаддресс** сравнивает два заданных адреса.

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **компарефрамесаурцеаддресс** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[компареаддрессес](compareaddresses.md)
</dt> <dt>

[компарефрамедестаддресс](compareframedestaddress.md)
</dt> </dl>

 

 




