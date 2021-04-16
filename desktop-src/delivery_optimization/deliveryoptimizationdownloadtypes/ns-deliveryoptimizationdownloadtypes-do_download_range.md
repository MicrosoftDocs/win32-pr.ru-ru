---
title: Структура DO_DOWNLOAD_RANGE
description: Определяет один диапазон байтов для скачивания из файла.
keywords:
- Структура DO_DOWNLOAD_RANGE
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105719089"
---
# <a name="do_download_range-structure"></a>Структура DO_DOWNLOAD_RANGE

Структура **DO_DOWNLOAD_RANGE** определяет один диапазон байтов для загрузки из файла. Структура **DO_DOWNLOAD_RANGE** включается в структуру **DO_DOWNLOAD_RANGES_INFO** , чтобы предоставить массив диапазонов для загрузки.

## <a name="syntax"></a>Синтаксис
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a>Члены

`Offset`

Смещение от нуля до начала диапазона байтов для скачивания из файла.

`Length`

Длина диапазона в байтах. Не указывайте нулевую длину в байтах. Чтобы указать, что диапазон расширяется до конца файла, укажите **DO_LENGTH_TO_EOF**.

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Деливерйоптимизатиондовнлоадтипес. h |
