---
title: Ивмдрмдевице Сетлиценсереспонсе, метод
description: Метод Сетлиценсереспонсе задает ответ лицензии.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Метод Сетлиценсереспонсе Windows Media диспетчер устройств
- Метод Сетлиценсереспонсе Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Сетлиценсереспонсе
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4161732002378449f196fdf83c4b880fcc2c02d345a0b08c6e6a464b81acb1dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055722"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a>Метод Ивмдрмдевице:: Сетлиценсереспонсе

Метод **сетлиценсереспонсе** задает ответ лицензии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбреспонсе* \[ окне\]
</dt> <dd>

Задает ответ, который необходимо задать.

</dd> <dt>

*кбреспонсе* \[ окне\]
</dt> <dd>

Размер ответа в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ВМДДРМСП. idl</dt> </dl> |
| Библиотека<br/> | <dl> <dt>Мссачлп. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмдрмдевице**](iwmdrmdevice.md)
</dt> </dl>

 

 





