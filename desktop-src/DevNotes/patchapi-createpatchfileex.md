---
description: Создает разницу между указанным исходным файлом и указанным целевым файлом.
title: Функция Креатепатчфиликса/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 7d73b6f4d10c52e9eca147227fdbfece31cba157af84fdf56dbef5cacda516b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690874"
---
# <a name="createpatchfileexaw-function"></a>Функция Креатепатчфиликса/W

Функции **креатепатчфиликса** и **креатепатчфиликсв** создают разницу между указанным исходным файлом и указанным целевым файлом. Исходные и целевые файлы предоставляются в виде путей. Выходная Дельта также записывается в указанный путь. Эти функции предоставляют отчеты о ходе выполнения в процессе создания.

## <a name="syntax"></a>Синтаксис

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a>Параметры

*олдфилекаунт*

Общее число исходных файлов. Используется для создания разностей к нескольким исходным файлам (максимум 255).

*олдфилеинфоаррай*

Указатель на массив сведений о исходном файле.

*невфиленаме*

Имя конечного файла.

*патчфиленаме*

Имя создаваемой разностной копии.

*оптионфлагс*

Флаги создания.

*прогресскаллбакк*

Указатель на обратный вызов, определяемый приложением.

*CallbackContext*

Указатель на определяемый приложением контекст.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| Заголовок | патчапи. h |
| DLL | mspatchc.dll |
| Юникод | Реализовано как Креатепатчфиликсв (Юникод) и Креатепатчфиликса (ANSI) |

## <a name="see-also"></a>См. также

[патчапи](patchapi.md)
