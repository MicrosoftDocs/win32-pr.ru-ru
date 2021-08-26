---
description: 'Метод SplitAt2 разделяет объект в указанное время. Этот метод эквивалентен Иамтимелинесплиттабле:: Сплитат, но принимает значение РЕФТИМЕ.'
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'Метод Иамтимелинесплиттабле:: SplitAt2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9c3a5720ade42291037611c155c2cb9e834f0734e7af6e2c36277c409592143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904914"
---
# <a name="iamtimelinesplittablesplitat2-method"></a>Метод Иамтимелинесплиттабле:: SplitAt2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SplitAt2`Метод разделяет объект в указанное время. Этот метод эквивалентен [**иамтимелинесплиттабле:: сплитат**](iamtimelinesplittable-splitat.md), но принимает значение [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Время* 
</dt> <dd>

Время разделения объекта относительно начала временной шкалы в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения:



| Код возврата                                                                                   | Описание                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Нет для разбиения.<br/>                       |
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | В данный момент объект не существует.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                    |



 

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелинесплиттабле**](iamtimelinesplittable.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




