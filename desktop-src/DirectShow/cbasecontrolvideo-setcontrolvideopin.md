---
description: Метод Сетконтролвидеопин задает ПИН-код, используемый фильтром.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Кбасеконтролвидео. Сетконтролвидеопин, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6169b5d2ec71148cd868e340c5a2f4e206355044ce55e0905c20787ddb3a263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660789"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a>Кбасеконтролвидео. Сетконтролвидеопин, метод

`SetControlVideoPin`Метод задает ПИН-код, используемый фильтром.

## <a name="syntax"></a>Синтаксис


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппин* 
</dt> <dd>

Указатель на ПИН-код, с которым синхронизируется интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Интерфейс можно вызывать только после успешного подключения фильтра. Объект передается через этот метод в ПИН-код, с которым он синхронизирован; в большинстве случаев он определяет, подключен ли ПИН-код при вызове метода интерфейса, и при сбое возвращает VFW \_ E \_ Not \_ Connected.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




