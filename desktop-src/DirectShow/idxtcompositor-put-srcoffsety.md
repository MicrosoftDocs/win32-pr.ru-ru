---
description: Метод размещения \_ сркоффсети задает вертикальное смещение исходного прямоугольника.
ms.assetid: abdc520f-8de6-4a4f-aa8f-facedaa8fce1
title: 'Идксткомпоситор: метод ut_SrcOffsetY:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcOffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e12a6b253b1b8704092dcb9c776120917104277b52e1c6fe815bf365ba7dd691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651254"
---
# <a name="idxtcompositorput_srcoffsety-method"></a>Идксткомпоситор::p UT \_ сркоффсети метод

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_SrcOffsetY`Метод задает вертикальное смещение исходного прямоугольника.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_SrcOffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Вертикальное смещение исходного прямоугольника в пикселях.

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

[**Интерфейс Идксткомпоситор**](idxtcompositor.md)
</dt> </dl>

 

 




