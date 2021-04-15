---
description: 'Метод SetStartStop2 задает время начала и окончания объекта относительно родителя объекта. Этот метод эквивалентен Иамтимелинеобж:: Сетстартстоп, но принимает значения РЕФТИМЕ.'
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'Метод Иамтимелинеобж:: SetStartStop2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689142"
---
# <a name="iamtimelineobjsetstartstop2-method"></a>Метод Иамтимелинеобж:: SetStartStop2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetStartStop2`Метод задает время начала и окончания объекта относительно родителя объекта. Этот метод эквивалентен [**иамтимелинеобж:: сетстартстоп**](iamtimelineobj-setstartstop.md), но принимает значения [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Запуск* 
</dt> <dd>

Новое время запуска в секундах или – 1 для сохранения существующего времени начала.

</dd> <dt>

*Остановить* 
</dt> <dd>

Новое время окончания, в секундах или – 1 для сохранения текущего времени окончания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                                  | Описание                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Успешно.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый аргумент.<br/> |
| <dl> <dt>**E \_ нотимпл**</dt> </dl>    | Не реализован.<br/>  |



 

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

[**Интерфейс Иамтимелинеобж**](iamtimelineobj.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




