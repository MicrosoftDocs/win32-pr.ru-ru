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
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675081"
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

*Time* 
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



 

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелинесплиттабле**](iamtimelinesplittable.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




