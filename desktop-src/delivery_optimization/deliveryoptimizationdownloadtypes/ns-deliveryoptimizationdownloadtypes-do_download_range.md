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
ms.openlocfilehash: 39672bff2e3a7194f7d674b2184d5de8c9c3c601e4a7777ef31ace80f5f9f327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047122"
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

## <a name="requirements"></a>Requirements (Требования)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Деливерйоптимизатиондовнлоадтипес. h |
