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
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "103785100"
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
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
