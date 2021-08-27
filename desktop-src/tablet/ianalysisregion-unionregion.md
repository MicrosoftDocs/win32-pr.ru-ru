---
description: Разворачивает область этого Ианалисисрегиона в область, созданную с помощью объединения, с указанным Ианалисисрегион.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'Метод Ианалисисрегион:: Унионрегион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 760296552dc13ac394d4554903d84f596faba14318db9af3145c79f156c736fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720011"
---
# <a name="ianalysisregionunionregion-method"></a>Метод Ианалисисрегион:: Унионрегион

Разворачивает область этого [**ианалисисрегиона**](ianalysisregion.md) в область, созданную с помощью объединения, с указанным **ианалисисрегион**.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прегионтаунион* \[ окне\]
</dt> <dd>

[**Ианалисисрегион**](ianalysisregion.md) , с которым необходимо выполнить объединение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Если любая из этих областей бесконечно, Новая область также будет бесконечна.

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

[**Метод Ианалисисрегион:: Ексклудерегион**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Интерсектректангле**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Интерсектрегион**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Унионректангле**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




