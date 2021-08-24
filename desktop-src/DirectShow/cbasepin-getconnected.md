---
description: Метод методом Соединенного соединения извлекает ПИН-код, подключенный к этому ПИН-коду.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Метод Кбасепин. соединен (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8bac5bc971f67c7678d2160cadb452995165638db4bb44d2ed1c89b3ab08f882
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526844"
---
# <a name="cbasepingetconnected-method"></a>Кбасепин. соединенный метод

`GetConnected`Метод извлекает ПИН-код, подключенный к этому ПИН-коду.

## <a name="syntax"></a>Синтаксис


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода.

## <a name="remarks"></a>Remarks

Если ПИН-код не подключен, этот метод возвращает **значение NULL**. Вызовите метод [**кбасепин::**](cbasepin-isconnected.md) , чтобы определить, подключен ли ПИН-код.

Метод не вызывает **AddRef** для интерфейса **Ипин** , поэтому вызывающий объект не должен освобождать интерфейс.

## <a name="examples"></a>Примеры

Так как счетчик ссылок не увеличивается на возвращенном указателе, вызовы метода можно объединить в цепочку.


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Этот шаблон программирования очень удобен; но, как показано в примере, необходимо избегать разыменования **пустого** указателя, если ПИН-код не подключен.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




