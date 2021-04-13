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
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412289"
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
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
