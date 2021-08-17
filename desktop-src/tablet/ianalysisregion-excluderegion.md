---
description: Ограничивающий область Ианалисисрегион до части области, которая не пересекается с заданным Ианалисисрегион.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'Метод Ианалисисрегион:: Ексклудерегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4a26bc234a5a99d2ba692b02097d348b83878c47ea3c9a1cbd21e1558fc41950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092355"
---
# <a name="ianalysisregionexcluderegion-method"></a>Метод Ианалисисрегион:: Ексклудерегион

Ограничивающий область [**ианалисисрегион**](ianalysisregion.md) до части области, которая не пересекается с заданным **ианалисисрегион**.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прегионтоексклуде* \[ окне\]
</dt> <dd>

[**Ианалисисрегион**](ianalysisregion.md) , исключаемый из этого **ианалисисрегион**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Если две области не пересекаются, это [**ианалисисрегион**](ianalysisregion.md) не изменяется.

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

[**Ианалисисрегион:: Ексклудеректангле**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Интерсектректангле**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Интерсектрегион**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Унионректангле**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Унионрегион**](ianalysisregion-unionregion.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




