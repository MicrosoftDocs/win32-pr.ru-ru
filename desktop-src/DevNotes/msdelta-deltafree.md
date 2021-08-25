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
ms.openlocfilehash: 606b8d91d20c74f7dd56ff4e09986abec3eef547989990a38bd8b4e3a27382c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079734"
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

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| Заголовок | мсделта. h |
| DLL | msdelta.dll |
| Юникод | Неприменимо |

## <a name="see-also"></a>См. также

[мсделта](msdelta.md)

[креатеделтаб](msdelta-createdeltab.md)

[апплиделтаб](msdelta-applydeltab.md)
