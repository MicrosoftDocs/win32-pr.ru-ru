---
description: 'Метод Жетпреролл извлекает объем данных, которые будут помещены в очередь перед начальной позицией. Этот метод реализует метод Имедиасикинг:: Жетпреролл.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Кпоспасссру. Жетпреролл, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675822"
---
# <a name="cpospassthrugetpreroll-method"></a>Кпоспасссру. Жетпреролл, метод

`GetPreroll`Метод получает объем данных, которые будут помещены в очередь перед начальной позицией. Этот метод реализует метод [**имедиасикинг:: жетпреролл**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пллпреролл* 
</dt> <dd>

Указатель на переменную, которая получает время предвыполнения, в единицах текущего формата времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




