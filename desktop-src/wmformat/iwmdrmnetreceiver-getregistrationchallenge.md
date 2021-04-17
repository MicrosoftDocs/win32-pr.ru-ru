---
title: Метод Ивмдрмнетрецеивер Жетрегистратиончалленже (Вмдрмсдк. h)
description: Метод Жетрегистратиончалленже создает сообщение с запросом на регистрацию DRM Windows Media для сетевых устройств.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Формат Windows Media, Жетрегистратиончалленже метод
- Жетрегистратиончалленже метод Windows Media Format, интерфейс Ивмдрмнетрецеивер
- Интерфейс Ивмдрмнетрецеивер Windows Media Format, метод Жетрегистратиончалленже
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679724"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>Метод Ивмдрмнетрецеивер:: Жетрегистратиончалленже

Метод **жетрегистратиончалленже** создает сообщение с запросом на регистрацию DRM Windows Media для сетевых устройств.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппбрегистратиончалленже* \[ заполняет\]
</dt> <dd>

Адрес указателя, получающего адрес созданного запроса. После завершения работы с этими данными необходимо освободить память, вызвав **CoTaskMemFree**.

</dd> <dt>

*пкбрегистратиончалленже* \[ заполняет\]
</dt> <dd>

Адрес переменной, которая получает размер запроса на регистрацию в байтах.

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

[**Ивмдрмнетрецеивер::P Роцессрегистратионреспонсе**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





