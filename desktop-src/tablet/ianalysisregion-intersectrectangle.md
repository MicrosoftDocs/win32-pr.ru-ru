---
description: Область этого Ианалисисрегиона ограничена областью, созданной ее пересечением с указанным прямоугольником.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'Метод Ианалисисрегион:: Интерсектректангле (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 074e3cee4cd20a35c780ce0c644b24c7688956d85a631f3563dd678c70c82822
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935494"
---
# <a name="ianalysisregionintersectrectangle-method"></a>Метод Ианалисисрегион:: Интерсектректангле

Область этого [**ианалисисрегиона**](ianalysisregion.md) ограничена областью, созданной ее пересечением с указанным прямоугольником.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинтерсектингректангле* \[ окне\]
</dt> <dd>

Указатель на прямоугольник, с которым производится пересечение, в координатах рукописного ввода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Координаты прямоугольника находятся в единицах HIMETRIC.

Если две области не пересекаются, Новая область будет пустой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисрегион**](ianalysisregion.md)
</dt> <dt>

[**Ианалисисрегион:: Ексклудеректангле**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Ексклудерегион**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Интерсектрегион**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Унионректангле**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Унионрегион**](ianalysisregion-unionregion.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




