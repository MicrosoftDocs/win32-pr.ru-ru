---
title: IWMDRMDevice2 Жетлиценсестате, метод
description: Метод Жетлиценсестате получает состояние лицензии.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Метод Жетлиценсестате Windows Media диспетчер устройств
- Метод Жетлиценсестате Windows Media диспетчер устройств, интерфейс IWMDRMDevice2
- Интерфейс IWMDRMDevice2 Windows Media диспетчер устройств, метод Жетлиценсестате
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e068d537f460053800b0d52d667ba39b0577d717b08f83794a73b2bf8c854aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055702"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>Метод IWMDRMDevice2:: Жетлиценсестате

Метод **жетлиценсестате** получает состояние лицензии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбстатекуеридата* \[ окне\]
</dt> <dd>

Указатель на запрашиваемые данные состояния лицензии.

</dd> <dt>

*кбстатекуеридата* \[ окне\]
</dt> <dd>

Количество запрошенных данных.

</dd> <dt>

*пдвкатегори* \[ заполняет\]
</dt> <dd>

Указатель на категорию.

</dd> <dt>

*пкремаинингкаунтс* \[ заполняет\]
</dt> <dd>

Указатель на оставшиеся счетчики.

</dd> <dt>

*пкремаинингхаурс* \[ заполняет\]
</dt> <dd>

Указатель на оставшиеся часы.

</dd> <dt>

*пдвресервед* \[ заполняет\]
</dt> <dd>

Зарезервировано для последующего использования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ВМДДРМСП. idl</dt> </dl> |
| Библиотека<br/> | <dl> <dt>Мссачлп. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





