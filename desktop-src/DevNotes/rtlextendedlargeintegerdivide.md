---
description: Делит расширенные целые числа.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: Функция Ртлекстендедларжеинтежердивиде
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668942"
---
# <a name="rtlextendedlargeintegerdivide-function"></a>Функция Ртлекстендедларжеинтежердивиде

\[Функция **ртлекстендедларжеинтежердивиде** экспортируется для поддержки существующих двоичных файлов драйверов и является устаревшей. Для повышения производительности используйте поддержку компилятора для 64-разрядных целочисленных операций.\]

Делит расширенные целые числа.

## <a name="syntax"></a>Синтаксис


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Делимое* \[ окне\]
</dt> <dd>

Дивиденд.

</dd> <dt>

*Делитель* \[ окне\]
</dt> <dd>

Равн.

</dd> <dt>

*Остаток от деления* \[ в, out\]
</dt> <dd>

Указатель на остаток от деления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает результат операции деления.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
