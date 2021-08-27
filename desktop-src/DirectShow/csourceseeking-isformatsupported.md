---
description: 'Ксаурцесикинг. Исформатсуппортед, метод Исформатсуппортед определяет, поддерживается ли указанный формат времени. Этот метод реализует метод Имедиасикинг:: Исформатсуппортед.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Ксаурцесикинг. Исформатсуппортед, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92349ab37fb677b561f342e99882c27208287310b544880e397f4f5df6cb0c38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083924"
---
# <a name="csourceseekingisformatsupported-method"></a>Ксаурцесикинг. Исформатсуппортед, метод

`IsFormatSupported`Метод определяет, поддерживается ли указанный формат времени. Этот метод реализует метод [**имедиасикинг:: исформатсуппортед**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пформат* 
</dt> <dd>

Указатель на GUID формата времени. См. раздел [**идентификаторы GUID формата времени**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.



| Код возврата                                                                               | Описание                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Формат не поддерживается.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>      | Формат поддерживается.<br/>     |
| <dl> <dt>**\_указатель E**</dt> </dl> | **Пустой** аргумент указателя.<br/>   |



 

## <a name="remarks"></a>Remarks

Единственный формат времени, поддерживаемый базовым классом, — это \_ \_ время носителя формата времени \_ (100-наносекундных единиц).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




