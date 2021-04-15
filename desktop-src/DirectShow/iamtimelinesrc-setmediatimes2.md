---
description: 'Метод SetMediaTimes2 задает время начала и окончания воспроизведения носителя. Этот метод эквивалентен Иамтимелинесрк:: Сетмедиатимес, но принимает значения РЕФТИМЕ.'
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: 'Метод Иамтимелинесрк:: SetMediaTimes2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4aa4f68a6fb93c329507edceea4e9665bfecd5f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689357"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a>Метод Иамтимелинесрк:: SetMediaTimes2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetMediaTimes2`Метод задает время начала и окончания воспроизведения носителя. Этот метод эквивалентен [**иамтимелинесрк:: сетмедиатимес**](iamtimelinesrc-setmediatimes.md), но принимает значения [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Запуск* 
</dt> <dd>

Время запуска носителя в секундах.

</dd> <dt>

*Остановить* 
</dt> <dd>

Время окончания носителя в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

[**Интерфейс Иамтимелинесрк**](iamtimelinesrc.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




