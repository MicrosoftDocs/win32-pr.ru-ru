---
description: Возвращает ограничивающий прямоугольник Ианалисисрегион.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: Метод Ианалисисрегион::-Bounds (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8481ddda9d0d278d2f24873a0c7d8a993c924c816d58153c38de8ef1063e986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092335"
---
# <a name="ianalysisregiongetbounds-method"></a>Метод Ианалисисрегион:: DataBound

Возвращает ограничивающий прямоугольник [**ианалисисрегион**](ianalysisregion.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбаундингректангле* \[ заполняет\]
</dt> <dd>

Ограничивающий прямоугольник [**ианалисисрегион**](ianalysisregion.md) в координатах рукописного пространства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Границы находятся в координатах для рукописного ввода.

Если [**ианалисисрегион**](ianalysisregion.md) представляет бесконечную область, левая и верхняя границы имеют **тип int \_ min**, а правая и нижняя границы — **int \_ Max**.

Если [**ианалисисрегион**](ianalysisregion.md) представляет пустую область, все границы прямоугольника равны 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисрегион**](ianalysisregion.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Жетрегионсканс**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




