---
description: 'Метод Clone создает копию перечислителя с тем же состоянием перечисления. Этот метод реализует метод Иенуммедиатипес:: Clone.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Метод Ценуммедиатипес. Clone (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c624ac933228c769248c2980a250a9f89e9ebdaf386aeff951e70ba966311586
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537312"
---
# <a name="cenummediatypesclone-method"></a>Ценуммедиатипес. Clone, метод

`Clone`Метод создает копию перечислителя с тем же состоянием перечисления. Этот метод реализует метод [**иенуммедиатипес:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппенум* 
</dt> <dd>

Адрес переменной, которая получает указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) нового перечислителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                                | Описание                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                       | Успешно.<br/>                                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | Недостаточно памяти.<br/>                                                     |
| <dl> <dt>**\_указатель E**</dt> </dl>                  | **Пустой** аргумент указателя.<br/>                                               |
| <dl> <dt>**VFW \_ E \_ перечисление не \_ \_ \_ синхронизировано**</dt> </dl> | Состояние ПИН-кода изменилось и теперь не согласуется с перечислителем.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ценуммедиатипес**](cenummediatypes.md)
</dt> </dl>

 

 




