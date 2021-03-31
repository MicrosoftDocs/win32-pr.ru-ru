---
description: Функция Хтмлвалуетауникоде преобразует строку HTML CP \_ UTF8 в строку Юникода.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Функция Хтмлвалуетауникоде (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808699"
---
# <a name="htmlvaluetounicode-function"></a>Функция Хтмлвалуетауникоде

Функция **хтмлвалуетауникоде** ПРЕОБРАЗУЕТ строку HTML CP \_ UTF8 в строку Юникода.

## <a name="syntax"></a>Синтаксис


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pValue* \[ в, out\]
</dt> <dd>

На входе указатель на строку HTML, предоставленную МКСВК.

В выходных данных указатель на преобразованную строку Юникода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает эквивалент строки в Юникоде.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




