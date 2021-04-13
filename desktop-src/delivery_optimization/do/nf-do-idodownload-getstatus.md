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
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412293"
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

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
