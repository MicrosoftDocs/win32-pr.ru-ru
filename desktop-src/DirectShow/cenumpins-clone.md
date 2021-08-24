---
description: 'Метод Clone создает копию перечислителя с тем же состоянием перечисления. Этот метод реализует метод Иенумпинс:: Clone.'
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Метод Ценумпинс. Clone (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a0d14f0caf30f6037d53639ff54d2e21d6d0fb0eee5cfa493aba248e84d48e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688614"
---
# <a name="cenumpinsclone-method"></a>Ценумпинс. Clone, метод

`Clone`Метод создает копию перечислителя с тем же состоянием перечисления. Этот метод реализует метод [**иенумпинс:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппенум* 
</dt> <dd>

Адрес переменной, которая получает указатель на интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) нового перечислителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                                | Описание                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                       | Успешно.<br/>                                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | Недостаточно памяти.<br/>                                                        |
| <dl> <dt>**\_указатель E**</dt> </dl>                  | **Пустой** аргумент указателя.<br/>                                                  |
| <dl> <dt>**VFW \_ E \_ перечисление не \_ \_ \_ синхронизировано**</dt> </dl> | Состояние фильтра изменилось и теперь не согласуется с перечислителем.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ценумпинс**](cenumpins.md)
</dt> </dl>

 

 




