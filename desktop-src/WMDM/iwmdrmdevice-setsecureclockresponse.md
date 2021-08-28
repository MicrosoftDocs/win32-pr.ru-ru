---
title: Ивмдрмдевице Сетсекуреклоккреспонсе, метод
description: Метод Сетсекуреклоккреспонсе задает ответ на безопасных синхронизирующих импульсов.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Метод Сетсекуреклоккреспонсе Windows Media диспетчер устройств
- Метод Сетсекуреклоккреспонсе Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Сетсекуреклоккреспонсе
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1af9dae5e49240ef0095f499cf8abe34d6931caf7c36cf0ec7fc6908c9821a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031864"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a>Метод Ивмдрмдевице:: Сетсекуреклоккреспонсе

Метод **сетсекуреклоккреспонсе** задает ответ на безопасных синхронизирующих импульсов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбреспонсе* \[ окне\]
</dt> <dd>

Установленный отклик на безопасное время.

</dd> <dt>

*кбреспонсе* \[ окне\]
</dt> <dd>

Заданный размер ответа на безопасное время в байтах.

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

[**жетсекуреклокк**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**Интерфейс Ивмдрмдевице**](iwmdrmdevice.md)
</dt> </dl>

 

 





