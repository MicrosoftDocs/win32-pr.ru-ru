---
description: 'Метод FixMediaTimes2 округляет указанные значения времени до ближайшей границы фрейма, как определено частотой выходного кадра. Этот метод эквивалентен Иамтимелинесрк:: Фиксмедиатимес, но принимает значения РЕФТИМЕ.'
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: 'Метод Иамтимелинесрк:: FixMediaTimes2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e38b6c1ea4c49372a52a805920fa95ccf795f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685082"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a>Метод Иамтимелинесрк:: FixMediaTimes2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`FixMediaTimes2`Метод округляет указанные значения времени до ближайшей границы фрейма, как определено частотой выходного кадра. Этот метод эквивалентен [**иамтимелинесрк:: фиксмедиатимес**](iamtimelinesrc-fixmediatimes.md), но принимает значения [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстарт* 
</dt> <dd>

Указатель на переменную, содержащую время начала в секундах. Если вызов будет выполнен, для этой переменной задается округленное время.

</dd> <dt>

*пстоп* 
</dt> <dd>

Указатель на переменную, содержащую время окончания (в секундах). Если вызов будет выполнен, для этой переменной задается округленное время.

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

 

 




