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
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810055"
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

## <a name="remarks"></a>Комментарии

Границы находятся в координатах для рукописного ввода.

Если [**ианалисисрегион**](ianalysisregion.md) представляет бесконечную область, левая и верхняя границы имеют **тип int \_ min**, а правая и нижняя границы — **int \_ Max**.

Если [**ианалисисрегион**](ianalysisregion.md) представляет пустую область, все границы прямоугольника равны 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
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

 

 




