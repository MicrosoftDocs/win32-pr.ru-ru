---
description: 'Метод SetCutPoint2 задает время, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание. Этот метод эквивалентен Иамтимелинетранс:: Сеткутпоинт, но принимает значение РЕФТИМЕ.'
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'Метод Иамтимелинетранс:: SetCutPoint2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9d4dedfb31efab45f56229e2dd4db10fc9e43defe822662bc2d7be06f0c1a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502344"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a>Метод Иамтимелинетранс:: SetCutPoint2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetCutPoint2`Метод задает время, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание. Этот метод эквивалентен [**иамтимелинетранс:: сеткутпоинт**](iamtimelinetrans-setcutpoint.md), но принимает значение [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тлтиме* 
</dt> <dd>

Вырезать точку относительно начала перехода (в секундах).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

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

[**Интерфейс Иамтимелинетранс**](iamtimelinetrans.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




