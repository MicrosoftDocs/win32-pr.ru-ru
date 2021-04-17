---
title: Метод Ивмдрмнетрецеивер Жетлиценсечалленже (Вмдрмсдк. h)
description: Метод Жетлиценсечалленже создает запрос на лицензию Windows Media DRM для сетевых устройств, который может быть отправлен передатчику при запросе защищенного содержимого.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Формат Windows Media, Жетлиценсечалленже метод
- Жетлиценсечалленже метод Windows Media Format, интерфейс Ивмдрмнетрецеивер
- Интерфейс Ивмдрмнетрецеивер Windows Media Format, метод Жетлиценсечалленже
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675050"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a>Метод Ивмдрмнетрецеивер:: Жетлиценсечалленже

Метод **жетлиценсечалленже** создает запрос на лицензию Windows Media DRM для сетевых устройств, который может быть отправлен передатчику при запросе защищенного содержимого.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрактион* \[ окне\]
</dt> <dd>

Действие, для которого создается запрос.

</dd> <dt>

*ппблиценсечалленже* \[ заполняет\]
</dt> <dd>

Адрес указателя, которому присваивается адрес созданного запроса. После завершения работы с этими данными необходимо освободить память, вызвав **CoTaskMemFree**.

</dd> <dt>

*пкблиценсечалленже* \[ заполняет\]
</dt> <dd>

Адрес переменной, которая получает размер запроса лицензии в байтах.

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
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмнетрецеивер**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Ивмдрмнетрецеивер::P Роцесслиценсереспонсе**](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





