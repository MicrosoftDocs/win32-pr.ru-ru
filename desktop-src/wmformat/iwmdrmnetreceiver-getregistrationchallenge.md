---
title: Метод Ивмдрмнетрецеивер Жетрегистратиончалленже (Вмдрмсдк. h)
description: метод жетрегистратиончалленже создает Windows Media DRM для сообщения с запросом регистрации сетевых устройств.
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
ms.openlocfilehash: 7f6c066de9c455006bfa7e500a30ac290299956ba03a6b4d8df6652a60a75a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701039"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>Метод Ивмдрмнетрецеивер:: Жетрегистратиончалленже

метод **жетрегистратиончалленже** создает Windows Media DRM для сообщения с запросом регистрации сетевых устройств.

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



 

## <a name="remarks"></a>Remarks

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмнетрецеивер**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Ивмдрмнетрецеивер::P Роцессрегистратионреспонсе**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





