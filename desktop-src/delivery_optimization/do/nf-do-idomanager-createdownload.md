---
title: 'Метод Идоманажер:: Креатедовнлоад'
description: Создает новую загрузку.
keywords:
- 'Метод Идоманажер:: Креатедовнлоад'
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412291"
---
# <a name="idomanagercreatedownload-method"></a>Метод Идоманажер:: Креатедовнлоад

Создает новую загрузку.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a>Параметры

`download`

Адрес указателя интерфейса **идодовнлоад** .

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
