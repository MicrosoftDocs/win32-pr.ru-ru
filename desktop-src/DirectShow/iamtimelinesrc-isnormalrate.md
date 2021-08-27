---
description: Метод Иснормалрате указывает, будет ли воспроизводиться воспроизведение клипа с нормальным темпом воспроизведения; то есть скорость воспроизведения исходного файла.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'Метод Иамтимелинесрк:: Иснормалрате (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4d1c0b355b0eedee29dafb92debbabac5c7b3e574d2f161827626bc73f72c035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083874"
---
# <a name="iamtimelinesrcisnormalrate-method"></a>Метод Иамтимелинесрк:: Иснормалрате

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IsNormalRate`Метод указывает, будет ли воспроизведение клипа воспроизводиться с нормальным темпом воспроизведения, то есть от скорости воспроизведения исходного файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pVal* 
</dt> <dd>

Получает логическое значение, указывающее, как будет отображаться клип. Если значение равно **true**, клип будет воспроизводиться по нормальной ставке. В противном случае он будет воспроизводиться быстрее или медленнее, чем обычная.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Скорость воспроизведения клипа определяется временем его начала и окончания, относительно времени его выполнения:


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



Если это соотношение равно 1, клип воспроизводится с созданной скоростью. В противном случае он будет воспроизводиться быстрее или медленнее. дополнительные сведения см. [в разделе время в DirectShow редактирования служб](time-in-directshow-editing-services.md).

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелинесрк**](iamtimelinesrc.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




