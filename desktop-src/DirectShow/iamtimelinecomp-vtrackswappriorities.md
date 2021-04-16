---
description: Метод Втракксвапприоритиес переключает уровни приоритета двух дорожек.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'Метод Иамтимелинекомп:: Втракксвапприоритиес (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689504"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a>Метод Иамтимелинекомп:: Втракксвапприоритиес

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`VTrackSwapPriorities`Метод переключает уровни приоритета двух дорожек.

При наличии двух уровней приоритета этот метод переключает Виртуальные дорожки с этими приоритетами. Когда метод возвращает значение, запись, которая была на первом уровне приоритета, теперь находится на втором уровне приоритета, и наоборот.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*виртуалтракка* 
</dt> <dd>

Первый уровень приоритета для переключения виртуальных дорожек.

</dd> <dt>

*виртуалтраккб* 
</dt> <dd>

Второй уровень приоритета для переключения виртуальных дорожек.

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

[**Интерфейс Иамтимелинекомп**](iamtimelinecomp.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




