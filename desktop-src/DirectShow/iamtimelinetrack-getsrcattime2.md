---
description: 'Метод GetSrcAtTime2 извлекает исходный объект, ближайший к заданному времени, в соответствии с указанными условиями границ. Этот метод эквивалентен Иамтимелинетракк:: Жетсркаттиме, но принимает значение РЕФТИМЕ.'
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'Метод Иамтимелинетракк:: GetSrcAtTime2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7a1cd2e91f5f9372654fa9cfefddc7e99f5f4bc69be8fa010815902c44e76dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998808"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a>Метод Иамтимелинетракк:: GetSrcAtTime2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetSrcAtTime2`Метод получает исходный объект, ближайший к заданному времени, в соответствии с указанными условиями границ. Этот метод эквивалентен [**иамтимелинетракк:: жетсркаттиме**](iamtimelinetrack-getsrcattime.md), но принимает значение [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппсрк* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) исходного объекта.

</dd> <dt>

*Время* 
</dt> <dd>

Время начала поиска в секундах.

</dd> <dt>

*сеарчдиректион* 
</dt> <dd>

Член перечисляемого типа [**декстерф \_ Track \_ Search \_ flags**](dexterf-track-search-flags.md) , указывающий условия границ для поиска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                                  | Описание                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | Не удалось располагать исходный объект.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>         | Расположение исходного объекта.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый аргумент.<br/>               |
| <dl> <dt>**\_указатель E**</dt> </dl>    | **Пустой** аргумент указателя.<br/>      |



 

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелинетракк**](iamtimelinetrack.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




