---
description: Умножает расширенные целые числа.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: Функция Ртлекстендединтежермултипли
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665439"
---
# <a name="rtlextendedintegermultiply-function"></a>Функция Ртлекстендединтежермултипли

\[Функция **ртлекстендединтежермултипли** экспортируется для поддержки существующих двоичных файлов драйверов и является устаревшей. Для повышения производительности используйте поддержку компилятора для 64-разрядных целочисленных операций.\]

Умножает расширенные целые числа.

## <a name="syntax"></a>Синтаксис


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Множимое* \[ окне\]
</dt> <dd>

Множимое.

</dd> <dt>

*Множитель* \[ окне\]
</dt> <dd>

Множитель.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает результат умножения.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
