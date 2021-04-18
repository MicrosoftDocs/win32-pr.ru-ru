---
description: Разворачивает область этого Ианалисисрегиона в область, созданную его объединением с указанным прямоугольником.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'Метод Ианалисисрегион:: Унионректангле (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692452"
---
# <a name="ianalysisregionunionrectangle-method"></a>Метод Ианалисисрегион:: Унионректангле

Разворачивает область этого [**ианалисисрегиона**](ianalysisregion.md) в область, созданную его объединением с указанным прямоугольником.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пректангле* \[ окне\]
</dt> <dd>

Указатель на прямоугольник, с которым выполняется объединение, в координатах рукописного ввода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Координаты прямоугольника находятся в единицах HIMETRIC.

Если любая из этих областей бесконечно, Новая область также будет бесконечна.

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

[**Ианалисисрегион:: Ексклудеректангле**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Ексклудерегион**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Интерсектректангле**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Интерсектрегион**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Метод Ианалисисрегион:: Унионрегион**](ianalysisregion-unionregion.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




