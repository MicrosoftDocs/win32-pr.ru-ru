---
description: 'Метод Кбасеинпутпин начинает операцию очистки. Этот метод реализует метод Ипин:: Бегинфлуш.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Кбасеинпутпин. Бегинфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b9e5e4e97a3a010523f61cc9efedf224d8dfc7fa373c9514b6d38dc0105d2d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103214"
---
# <a name="cbaseinputpinbeginflush-method"></a>Кбасеинпутпин. Бегинфлуш, метод

`CBaseInputPin`Метод начинает операцию записи на диск. Этот метод реализует метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод задает для флага [**кбасеинпутпин:: m \_ Бфлушинг**](cbaseinputpin-m-bflushing.md) **значение true**, что приводит к тому, что метод [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) отклоняет любые другие выборки.

Производный класс должен переопределить этот метод и выполнить следующие действия:

1.  Вызовите метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) для подчиненных входных контактов. Если ПИН-код еще не доставил никаких образцов мультимедиа, этот шаг можно пропустить. Если выходные контакты являются производными от класса [**кбасеаутпутпин**](cbaseoutputpin.md) , можно вызвать метод [**Кбасеаутпутпин::D еливербегинфлуш**](cbaseoutputpin-deliverbeginflush.md) .
2.  Вызовите метод базового класса.
3.  Начинает отменять данные в очереди.
4.  Возврат из всех заблокированных вызовов метода **Receive** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеинпутпин**](cbaseinputpin.md)
</dt> </dl>

 

 




