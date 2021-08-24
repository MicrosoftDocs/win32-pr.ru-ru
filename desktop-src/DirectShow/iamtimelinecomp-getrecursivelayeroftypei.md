---
description: 'Не поддерживается. Вместо этого вызовите метод Иамтимелинекомп:: Жетрекурсивелайерофтипе.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'Метод Иамтимелинекомп:: Жетрекурсивелайерофтипеи (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc62c0813aa38af450e2f5351390ec958dddd533cc203f52b3bfb70ff45344b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756424"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a>Метод Иамтимелинекомп:: Жетрекурсивелайерофтипеи

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Не поддерживается. Вместо этого вызовите метод [**иамтимелинекомп:: жетрекурсивелайерофтипе**](iamtimelinecomp-getrecursivelayeroftype.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппвиртуалтракк* 
</dt> <dd>

Зарезервировано.

</dd> <dt>

*пвхичлайер* 
</dt> <dd>

Зарезервировано.

</dd> <dt>

*Тип* 
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелинекомп**](iamtimelinecomp.md)
</dt> </dl>

 

 




