---
description: Метод Сетстреамнумбер указывает, какой поток следует считать из исходного файла, связанного с этим исходным объектом.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'Метод Иамтимелинесрк:: Сетстреамнумбер (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689034"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>Метод Иамтимелинесрк:: Сетстреамнумбер

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetStreamNumber`Метод указывает, какой поток следует считать из исходного файла, связанного с этим исходным объектом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Val* 
</dt> <dd>

Номер потока из набора потоков, соответствующих типу носителя родительской группы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Параметр *Val* указывает номер потока из набора потоков, который соответствует типу носителя родительской группы, а не ко всему набору потоков в исходном файле. Например, предположим, что файл содержит два потока видео и два звуковых потока. Если исходный объект находится внутри видеогруппы, для параметра *Val* значение 0 выбирается первый поток видео. Вызывающий объект отвечает за указание допустимого номера потока.

Номер потока по умолчанию равен нулю.

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

 

 




