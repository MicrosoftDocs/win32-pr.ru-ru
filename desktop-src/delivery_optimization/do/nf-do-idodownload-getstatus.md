---
title: 'Метод Идодовнлоад:: with Status'
description: Получает указатель на структуру **DO_DOWNLOAD_STATUS** , отражающую текущее состояние загрузки.
keywords:
- 'Метод Идодовнлоад:: with Status'
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e3a5aec5e35187a51865e074dae26ff012b75dfa3a41ffd13a8bed7371515fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047112"
---
# <a name="idodownloadgetstatus-method"></a>Метод Идодовнлоад:: with Status

Получает указатель на структуру **DO_DOWNLOAD_STATUS** , отражающую текущее состояние загрузки.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Параметры

`status`

Указатель на структуру **DO_DOWNLOAD_STATUS** .

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Requirements (Требования)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
