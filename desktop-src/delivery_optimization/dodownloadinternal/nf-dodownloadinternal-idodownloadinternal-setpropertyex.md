---
title: 'Метод Идодовнлоадинтернал:: Сетпропертекс'
description: Задает свойство расширенной загрузки. Метод принимает указатель на **вариант** , который содержит определенное значение свойства, применяемое к скачиванию.
keywords:
- 'Метод Идодовнлоадинтернал:: Сетпропертекс'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987559"
---
# <a name="idodownloadinternalsetpropertyex-method"></a>Метод Идодовнлоадинтернал:: Сетпропертекс

> [!IMPORTANT]
> Интерфейс **идодовнлоадинтернал** является устаревшим. Вместо этого используйте интерфейс [идодовнлоад](../do/nn-do-idodownload.md) .

Задает свойство расширенной загрузки. Метод принимает указатель на **вариант** , который содержит определенное значение свойства, применяемое к скачиванию.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Параметры

`propId`

Обязательный идентификатор свойства для задания (типа **додовнлоадпропертекс**).

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
| **Header** | Додовнлоадинтернал. h |