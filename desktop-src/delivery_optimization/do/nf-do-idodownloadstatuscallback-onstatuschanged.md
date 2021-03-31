---
title: 'Метод Идодовнлоадстатускаллбакк:: Онстатусчанже'
description: Вызывает реализацию этого метода при каждом изменении состояния загрузки.
keywords:
- 'Метод Идодовнлоадстатускаллбакк:: Онстатусчанже'
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104069406"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>Метод Идодовнлоадстатускаллбакк:: Онстатусчанже

Вызывает реализацию этого метода при каждом изменении состояния загрузки.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Параметры

`download`

Указатель на интерфейс **идодовнлоад** , состояние которого изменилось.

`status`

Указатель на структуру **DO_DOWNLOAD_STATUS** , содержащую состояние загрузки.

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
