---
title: Ивмдрмдевице Жетдевицецертификате, метод
description: Метод Жетдевицецертификате извлекает сертификат устройства.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- Метод Жетдевицецертификате Windows Media диспетчер устройств
- Метод Жетдевицецертификате Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Жетдевицецертификате
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299233ff4344f44535933221141534ab2b0173ba54e47c9cc340020a2f462eb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619824"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a>Метод Ивмдрмдевице:: Жетдевицецертификате

Метод **жетдевицецертификате** извлекает сертификат устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбстрдевцерт* \[ заполняет\]
</dt> <dd>

Указатель на **строку BSTR** , содержащую полученный сертификат устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ВМДДРМСП. idl</dt> </dl> |
| Библиотека<br/> | <dl> <dt>Мссачлп. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрмдевице**](iwmdrmdevice.md)
</dt> </dl>

 

 





