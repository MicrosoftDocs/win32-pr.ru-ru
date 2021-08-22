---
title: Структура DO_DOWNLOAD_RANGE_INFO
description: Определяет массив диапазонов байтов для скачивания из файла.
keywords:
- Структура DO_DOWNLOAD_RANGE_INFO
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 30df22c7232ad1d28315e8152396ddd92bdab9a7cbf67d748af134c0f0760c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543748"
---
# <a name="do_download_range_info-structure"></a>Структура DO_DOWNLOAD_RANGE_INFO

Структура **DO_DOWNLOAD_RANGE_INFO** определяет массив диапазонов байтов для скачивания из файла. Обычно он передается как необязательный аргумент функции **идодовнлоад:: Start** .

## <a name="syntax"></a>Синтаксис
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a>Члены

`RangeCount`

Число элементов в диапазонах.

`Ranges`

Массив из одной или нескольких структур **DO_DOWNLOAD_RANGE** , указывающих диапазоны для загрузки.

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
