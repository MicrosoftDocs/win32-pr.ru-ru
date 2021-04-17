---
description: 'Метод GetTransAtTime2 извлекает переход, ближайший к заданному времени, в соответствии с указанными условиями границ. Этот метод эквивалентен Иамтимелинетрансабле:: Жеттрансаттиме, но принимает параметр РЕФТИМЕ.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'Метод Иамтимелинетрансабле:: GetTransAtTime2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689415"
---
# <a name="iamtimelinetransablegettransattime2-method"></a>Метод Иамтимелинетрансабле:: GetTransAtTime2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetTransAtTime2`Метод извлекает переход, ближайший к заданному времени, в соответствии с указанными условиями границ. Этот метод эквивалентен [**иамтимелинетрансабле:: жеттрансаттиме**](iamtimelinetransable-gettransattime.md), но принимает параметр [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппобж* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) перехода.

</dd> <dt>

*Time* 
</dt> <dd>

Время начала поиска в секундах.

</dd> <dt>

*сеарчдиректион* 
</dt> <dd>

Член перечисляемого типа [**декстерф \_ Track \_ Search \_ flags**](dexterf-track-search-flags.md) , указывающий условия границ для поиска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                                  | Описание                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | Переход не найден.<br/>   |
| <dl> <dt>**\_ОК**</dt> </dl>         | Обнаружен переход.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый аргумент.<br/>          |
| <dl> <dt>**\_указатель E**</dt> </dl>    | **Пустой** аргумент указателя.<br/> |



 

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

[**Интерфейс Иамтимелинетрансабле**](iamtimelinetransable.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




