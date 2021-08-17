---
title: 'Идодовнлоад:: метод Property'
description: Извлекает указатель на **вариант** , содержащий определенное свойство загрузки.
keywords:
- 'Идодовнлоад:: метод Property'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: f498900e8dd2e87460a5fe4e75ea1269272788488159379d64f5332f2006f97a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736251"
---
# <a name="idodownloadgetproperty-method"></a>Идодовнлоад:: метод Property

Извлекает указатель на **вариант** , содержащий определенное свойство загрузки.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Параметры

`propId`

Обязательный идентификатор свойства для получения (типа **додовнлоадпроперти**).

`propVal`

Результирующее значение свойства, хранящееся в **варианте**.

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* неизвестен.|
|DO_E_WRITE_ONLY_PROPERTY|Свойство доступно только для записи и не может быть прочитано.|
|E_NOT_SET|Такое свойство не было задано с помощью **SetProperty**.|

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
