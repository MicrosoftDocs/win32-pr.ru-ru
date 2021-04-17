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
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721029"
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

## <a name="requirements"></a>Требования

| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| Header | патчапи. h |
| DLL | mspatchc.dll |
| Юникод | Реализовано как Екстрактпатчхеадертофилев (Юникод) и Екстрактпатчхеадертофилеа (ANSI) |

## <a name="see-also"></a>См. также раздел

[патчапи](patchapi.md)
