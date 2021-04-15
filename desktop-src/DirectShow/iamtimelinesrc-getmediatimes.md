---
description: Метод Жетмедиатимес получает время начала и окончания воспроизведения носителя.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: 'Метод Иамтимелинесрк:: Жетмедиатимес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa6e9cbb69da504a929e23722068583489063b9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689369"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a>Метод Иамтимелинесрк:: Жетмедиатимес

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetMediaTimes`Метод получает время начала и окончания воспроизведения носителя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстарт* 
</dt> <dd>

Получает время начала носителя в 100-наносекундных единицах.

</dd> <dt>

*пстоп* 
</dt> <dd>

Получает время окончания передачи мультимедиа в единицах с 100 нс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Время носителя задается относительно исходного файла мультимедиа. Дополнительные сведения см. [в разделе время в службах редактирования DirectShow](time-in-directshow-editing-services.md).

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

 

 




