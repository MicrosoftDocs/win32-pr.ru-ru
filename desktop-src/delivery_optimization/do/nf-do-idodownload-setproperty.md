---
title: 'Метод Идодовнлоад:: SetProperty'
description: Задает свойство загрузки.
keywords:
- 'Метод Идодовнлоад:: SetProperty'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7d966edb083107b80f0723bce195bfc588797efb8ad1931e0e75a468bec5a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543903"
---
# <a name="idodownloadsetproperty-method"></a>Метод Идодовнлоад:: SetProperty

Задает свойство загрузки. Метод принимает указатель на **вариант** , который содержит определенное свойство, применяемое к скачиванию.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a>Параметры

`propId`

Обязательный идентификатор свойства для задания (типа **додовнлоадпроперти**).

`propVal`

Заданное значение свойства, хранящееся в **варианте**.

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* неизвестен.|
|DO_E_INVALID_STATE|Скачивание сейчас не находится в состоянии, допускающем установку свойств.|

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
