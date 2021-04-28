---
description: 'Ксаурцесикинг. Сетпоситионс, метод Сетпоситионс задает текущее расположение и точку окончания. Этот метод реализует метод Имедиасикинг:: Сетпоситионс.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Ксаурцесикинг. Сетпоситионс, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085172"
---
# <a name="csourceseekingsetpositions-method"></a>Ксаурцесикинг. Сетпоситионс, метод

`SetPositions`Метод задает текущее расположение и точку окончания. Этот метод реализует метод [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкуррент* 
</dt> <dd>

Указатель на переменную, которая указывает текущую позиции.

</dd> <dt>

*куррентфлагс* 
</dt> <dd>

Побитовое сочетание флагов. См. заметки.

</dd> <dt>

*пстоп* 
</dt> <dd>

Указатель на переменную, задающую время окончания в единицах текущего формата времени.

</dd> <dt>

*стопфлагс* 
</dt> <dd>

Побитовое сочетание флагов. См. заметки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают перечисленные в следующей таблице.



| Код возврата                                                                                  | Описание                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Успешное завершение<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимые флаги<br/>             |
| <dl> <dt>**\_указатель E**</dt> </dl>    | **Пустой** аргумент указателя<br/> |



 

## <a name="remarks"></a>Remarks

Поддерживаются следующие флаги:

-   \_Поиск в \_ позиционировании
-   \_Поиск \_ абсолутепоситионинг
-   \_Поиск \_ релативепоситионинг
-   \_Поиск \_ инкременталпоситионинг (только *пстоп* )

Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

Этот метод обновляет значения переменных членов [**ксаурцесикинг:: m \_ Ртстарт**](csourceseeking-m-rtstart.md) и [**ксаурцесикинг:: m \_ ртстоп**](csourceseeking-m-rtstop.md) , а затем вызывает чистые виртуальные методы [**ксаурцесикинг:: чанжестарт**](csourceseeking-changestart.md) и [**ксаурцесикинг:: ChangeStop**](csourceseeking-changestop.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




