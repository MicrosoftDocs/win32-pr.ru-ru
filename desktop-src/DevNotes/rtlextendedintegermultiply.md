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
ms.openlocfilehash: 0048da80026029274a89d089f5c232311a481a6010c0aad32d8b1a6ae6cc6786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571474"
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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
