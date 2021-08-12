---
description: Извлекает сведения о пространстве, используемом кэшем автономные файлы.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: Функция Кскжетспацеусажев
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8dd6d12c4e0267c97b93a812a4b66d3bd14a408dff0191686d4949ccbc958723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667957"
---
# <a name="cscgetspaceusagew-function"></a>Функция Кскжетспацеусажев

\[Эта функция не поддерживается и не должна использоваться.\]

Извлекает сведения о пространстве, используемом кэшем автономные файлы.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лптзлокатион* \[ в, out\]
</dt> <dd>

Расположение каталога кэша.

</dd> <dt>

*двсизе* \[ окне\]
</dt> <dd>

Размер буфера *лптзлокатион* в символах.

</dd> <dt>

*лпдвмаксспацехигх* \[ в, out\]
</dt> <dd>

**Параметр DWORD** высокого порядка для максимального числа байтов, доступных в кэше.

</dd> <dt>

*лпдвмаксспацелов* \[ в, out\]
</dt> <dd>

**Параметр DWORD** нижнего порядка для максимального числа байтов, доступных в кэше.

</dd> <dt>

*лпдвкуррентспацехигх* \[ в, out\]
</dt> <dd>

**Параметр DWORD** высокого порядка текущего числа байтов, доступных в кэше.

</dd> <dt>

*лпдвкуррентспацелов* \[ в, out\]
</dt> <dd>

**Параметр DWORD** нижнего порядка текущего числа байтов, доступных в кэше.

</dd> <dt>

*лпкнттоталфилес* \[ в, out\]
</dt> <dd>

Общее число файлов в кэше.

</dd> <dt>

*лпкнттоталдирс* \[ в, out\]
</dt> <dd>

Общее число каталогов в кэше.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
