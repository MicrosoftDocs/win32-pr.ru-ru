---
title: Структура DO_DOWNLOAD_STATUS
description: Используется для получения состояния определенного скачивания.
keywords:
- Структура DO_DOWNLOAD_STATUS
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8775b7daf55d58698d00bcaa2820b909e302933c9f407d1cb6416d6b095a872b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543738"
---
# <a name="do_download_status-structure"></a>Структура DO_DOWNLOAD_STATUS

Структура **DO_DOWNLOAD_STATUS** используется для получения состояния определенного скачивания. Он получается путем вызова функции **идодовнлоад::-Status** .

## <a name="syntax"></a>Синтаксис
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a>Члены

`BytesTotal`

Общее число байтов для скачивания.

`BytesTransferred`

Число уже скачанных байтов.

`State`

Текущее состояние загрузки в соответствии с определением перечисления **додовнлоадстате** .

`Error`

Сведения об ошибке (если они существуют), связанные с текущей загрузкой.

`ExtendedError`

Расширенные сведения об ошибке (если они существуют), связанные с текущей загрузкой.

## <a name="requirements"></a>Requirements (Требования)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
