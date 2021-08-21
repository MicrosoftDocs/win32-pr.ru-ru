---
title: Метод Ивмдрмнеттрансмиттер Сетлиценсечалленже (Вмдрмсдк. h)
description: метод сетлиценсечалленже обрабатывает запрос лицензии, отправленный Windows Media DRM для приемника сетевых устройств.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Формат Windows Media, Сетлиценсечалленже метод
- Сетлиценсечалленже метод Windows Media Format, интерфейс Ивмдрмнеттрансмиттер
- Интерфейс Ивмдрмнеттрансмиттер Windows Media Format, метод Сетлиценсечалленже
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 211f8de60cddb153e157af64ee300a4bbaf327d70a1564fbd9e622008c055cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027572"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>Метод Ивмдрмнеттрансмиттер:: Сетлиценсечалленже

метод **сетлиценсечалленже** обрабатывает запрос лицензии, отправленный Windows Media DRM для приемника сетевых устройств.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пблиценсечалленже* \[ окне\]
</dt> <dd>

Указатель на данные запроса лицензии, отправленные получателем.

</dd> <dt>

*кблиценсечалленже* \[ окне\]
</dt> <dd>

Размер запроса лицензии в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Если этот метод завершится с ошибкой, последующие вызовы других методов **ивмдрмнеттрансмиттер** будут использовать информацию в обработанном вызове.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмнеттрансмиттер**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





