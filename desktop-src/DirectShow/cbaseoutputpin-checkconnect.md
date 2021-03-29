---
description: Метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Кбасеаутпутпин. Чеккконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3274e47e9a77d86f350c17aaca04ec0cdb95ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657520"
---
# <a name="cbaseoutputpincheckconnect-method"></a>Кбасеаутпутпин. Чеккконнект, метод

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

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного контакта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** .



| Код возврата                                                                                               | Описание                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                      | Успешно.<br/>                                                         |
| <dl> <dt>**\_интерфейс E**</dt> </dl>             | ПИН-код ввода не поддерживает [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).<br/> |
| <dl> <dt>**VFW \_ E \_ недопустимое \_ направление**</dt> </dl> | Направления ПИН-кода несовместимы.<br/>                               |



 

## <a name="remarks"></a>Комментарии

Этот метод вызывает метод [**кбасепин:: чеккконнект**](cbasepin-checkconnect.md) базового класса, а затем запрашивает входной ПИН-код для своего интерфейса [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




