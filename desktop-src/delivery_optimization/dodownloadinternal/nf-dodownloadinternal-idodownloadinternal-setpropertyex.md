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
ms.openlocfilehash: d6156f4309c0eac9d2d250c85f7e9ab365e4a3b1e4072aabec7f6aa7e17c437f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858804"
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

## <a name="requirements"></a>Requirements (Требования)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Додовнлоадинтернал. h |