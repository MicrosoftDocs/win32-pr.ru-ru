---
title: Ивмдрмдевице Жетсекуреклоккчалленже, метод
description: Метод Жетсекуреклоккчалленже извлекает результат запроса на безопасное время.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Метод Жетсекуреклоккчалленже Windows Media диспетчер устройств
- Метод Жетсекуреклоккчалленже Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Жетсекуреклоккчалленже
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaed21ddffb9c2001c3b57d32d34ac9106ede7cecaff723cb95d8cee1c428fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957254"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a>Метод Ивмдрмдевице:: Жетсекуреклоккчалленже

Метод **жетсекуреклоккчалленже** извлекает результат запроса на безопасное время.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппбчалленже* \[ заполняет\]
</dt> <dd>

Получен результат запроса.

</dd> <dt>

*пкбчалленже* \[ заполняет\]
</dt> <dd>

Размер результата запроса в байтах.

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

[**жетсекуреклокк**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**Интерфейс Ивмдрмдевице**](iwmdrmdevice.md)
</dt> </dl>

 

 





