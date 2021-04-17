---
title: Метод GetURL Ивмдрмнонсилентлиценсеакуиситион (Вмдрмсдк. h)
description: Метод GetURL извлекает URL-адрес, на который должен быть опубликован запрос лицензии.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Формат Windows Media для метода GetURL
- Метод GetURL Windows Media Format, интерфейс Ивмдрмнонсилентлиценсеакуиситион
- Интерфейс Ивмдрмнонсилентлиценсеакуиситион Windows Media Format, метод GetURL
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675045"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>Метод Ивмдрмнонсилентлиценсеакуиситион:: GetURL

Метод **getURL** извлекает URL-адрес, на который должен быть опубликован запрос лицензии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбструрл* \[ заполняет\]
</dt> <dd>

Адрес переменной, которая получает URL-адрес.

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

 

 





