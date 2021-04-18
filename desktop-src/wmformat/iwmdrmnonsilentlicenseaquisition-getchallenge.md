---
title: Метод Ивмдрмнонсилентлиценсеакуиситион (Вмдрмсдк. h)
description: Метод метода WebMethod извлекает запрос лицензии, который должен быть опубликован на сервере лицензирования.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Метод вызова Windows Media Format
- Метод Ивмдрмнонсилентлиценсеакуиситион формат Windows Media, интерфейс
- Интерфейс Ивмдрмнонсилентлиценсеакуиситион интерфейса Windows Media Format, метод Challenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675389"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a>Метод Ивмдрмнонсилентлиценсеакуиситион:: Challenge

Метод **метода WebMethod** извлекает запрос лицензии, который должен быть опубликован на сервере лицензирования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбстрчалленже* \[ заполняет\]
</dt> <dd>

Адрес переменной, которая получает запрос лицензии.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вмдрмсдк. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Вмдрмсдк. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмнонсилентлиценсеакуиситион**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





