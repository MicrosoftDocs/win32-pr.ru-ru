---
description: Освобождает указанный блок памяти.
title: Функция DeltaFree
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721033"
---
# <a name="deltafree-function"></a>Функция DeltaFree

Освобождает указанный блок памяти. Эту функцию необходимо вызвать после успешного вызова [креатеделтаб](msdelta-createdeltab.md) и [апплиделтаб](msdelta-applydeltab.md) , чтобы освободить буфер памяти, выделенный мсделта.

## <a name="syntax"></a>Синтаксис

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>Параметры

*лпмемори*

окне Блок памяти, который должен быть освобожден.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**. Если функция возвращает **значение false**, можно вызвать [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить соответствующий код системной ошибки Win32.

## <a name="requirements"></a>Требования

| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| Header | мсделта. h |
| DLL | msdelta.dll |
| Юникод | Неприменимо |

## <a name="see-also"></a>См. также раздел

[мсделта](msdelta.md)

[креатеделтаб](msdelta-createdeltab.md)

[апплиделтаб](msdelta-applydeltab.md)
