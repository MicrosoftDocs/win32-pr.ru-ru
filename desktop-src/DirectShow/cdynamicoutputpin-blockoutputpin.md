---
description: Метод Блоккаутпутпин блокирует ПИН-код.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Кдинамикаутпутпин. Блоккаутпутпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9dc1f4cdafd732821398ee04e127c0525798dd6cc02f67f8af5d977b195a6a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983364"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>Кдинамикаутпутпин. Блоккаутпутпин, метод

`BlockOutputPin`Метод блокирует ПИН-код. Пока ПИН-код заблокирован, метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) ожидает, пока ПИН-код не будет разблокирован. Состояние блокировки предотвращает появление образцов, изменение выходного формата или повторное подключение к выходным данным.

## <a name="syntax"></a>Синтаксис


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Перед вызовом этого метода удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) . Не вызывайте этот метод, если поток потоковой передачи использует ПИН-код для доставки данных или изменения соединения. Чтобы проверить, использует ли поток потоковой передачи ПИН-код, вызовите метод [**кдинамикаутпутпин:: стреамингсреадусингаутпутпин**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




