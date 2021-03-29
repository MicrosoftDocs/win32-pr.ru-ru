---
title: Метод Ивмдрмпровидер CreateObject (Вмдрмсдк. h)
description: Метод CreateObject извлекает указатель на указанный интерфейс, создавая реализующий объект при необходимости.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Формат метода CreateObject Windows Media Format
- Метод CreateObject формат Windows Media Format, интерфейс Ивмдрмпровидер
- Интерфейс Ивмдрмпровидер интерфейса Windows Media Format, метод CreateObject
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648013"
---
# <a name="iwmdrmprovidercreateobject-method"></a>Метод Ивмдрмпровидер:: CreateObject

Метод **CreateObject** извлекает указатель на указанный интерфейс, создавая реализующий объект при необходимости.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*riid* \[ окне\]
</dt> <dd>

Идентификатор создаваемого интерфейса. Задайте одно из следующих значений.

-   IID \_ ивмдрмлиценсеманажемент
-   IID \_ ивмдрмлиценсекуери
-   IID \_ ивмдрмнетрецеивер
-   IID \_ ивмдрмнеттрансмиттер
-   IID \_ ивмдрмсекурити

</dd> <dt>

*ппвобжект* \[ заполняет\]
</dt> <dd>

Адрес указателя, получающего адрес запрошенного интерфейса.

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

[**Интерфейс Ивмдрмпровидер**](iwmdrmprovider.md)
</dt> <dt>

[**Интерфейс Ивмдрмлиценсеманажемент**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Интерфейс Ивмдрмлиценсекуери**](iwmdrmlicensequery.md)
</dt> <dt>

[**Интерфейс Ивмдрмнетрецеивер**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Интерфейс Ивмдрмнеттрансмиттер**](iwmdrmnettransmitter.md)
</dt> <dt>

[**Интерфейс Ивмдрмсекурити**](iwmdrmsecurity.md)
</dt> </dl>

 

 





