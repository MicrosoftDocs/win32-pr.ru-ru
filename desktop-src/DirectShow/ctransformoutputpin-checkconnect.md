---
description: Метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Ктрансформаутпутпин. Чеккконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9a20eb8d3e20679cb8805d3a1cd8e167ef0bfd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679699"
---
# <a name="ctransformoutputpincheckconnect-method"></a>Ктрансформаутпутпин. Чеккконнект, метод

`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного контакта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                  | Описание                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Успешно.<br/>                                 |
| <dl> <dt>**\_непредвиденная E**</dt> </dl> | Входной ПИН-код фильтра не подключен.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод переопределяет метод [**кбасеаутпутпин:: чеккконнект**](cbaseoutputpin-checkconnect.md) . Он вызывает метод [**ктрансформфилтер:: чеккконнект**](ctransformfilter-checkconnect.md) фильтра, который возвращает \_ значение s ОК в базовом классе. Производный класс может переопределить метод **ктрансформфилтер:: чеккконнект** для выполнения дополнительных проверок.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




