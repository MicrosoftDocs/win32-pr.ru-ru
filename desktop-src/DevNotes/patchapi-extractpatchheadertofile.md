---
description: Извлекает сведения о заголовке из разностной области.
title: Функция Екстрактпатчхеадертофилеа/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 626bd53e3361f4d29cc76e17ae2788ddea3bc8b99b580196bcbf77c27a6983d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571804"
---
# <a name="extractpatchheadertofileaw-function"></a>Функция Екстрактпатчхеадертофилеа/W

Функции **екстрактпатчхеадертофилеа** и **екстрактпатчхеадертофилев** извлекают данные заголовка из разностной области. Дельта предоставляется в виде пути к файлу. Выходной заголовок также записывается в указанный путь.

## <a name="syntax"></a>Синтаксис

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a>Параметры

*патчфиленаме*

Имя разностного файла, содержащего заголовок.

*патчхеадерфиленаме*

Имя создаваемого файла заголовка.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| Заголовок | патчапи. h |
| DLL | mspatchc.dll |
| Юникод | Реализовано как Екстрактпатчхеадертофилев (Юникод) и Екстрактпатчхеадертофилеа (ANSI) |

## <a name="see-also"></a>См. также

[патчапи](patchapi.md)
