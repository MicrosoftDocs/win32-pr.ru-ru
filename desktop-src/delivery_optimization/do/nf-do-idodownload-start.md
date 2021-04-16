---
title: 'Метод Идодовнлоад:: Start'
description: Запускает или возобновляет загрузку.
keywords:
- 'Метод Идодовнлоад:: Start'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105720837"
---
# <a name="idodownloadstart-method"></a>Метод Идодовнлоад:: Start

Запускает или возобновляет загрузку, передавая необязательные диапазоны в виде указателя на структуру [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) .

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>Параметры

`ranges`

Необязательный параметр. Указатель на структуру [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (чтобы скачать только определенные диапазоны файла). Передайте `nullptr` скачивание всего файла.

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
