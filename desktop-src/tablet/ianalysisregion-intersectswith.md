---
description: Определяет, пересекаются ли области Ианалисисрегион с указанным прямоугольником.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'Метод Ианалисисрегион:: Интерсектсвис (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 04613e061929bba04c14be37914b22a51de0377f125b21fa29db9c56fc8dfeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720021"
---
# <a name="ianalysisregionintersectswith-method"></a>Метод Ианалисисрегион:: Интерсектсвис

Определяет, пересекаются ли области [**ианалисисрегион**](ianalysisregion.md) с указанным прямоугольником.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пректангле* \[ окне\]
</dt> <dd>

Указатель на прямоугольник, с которым выполняется сравнение, в координатах рукописного ввода.

</dd> <dt>

*пфисинтерсектинг* \[ заполняет\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если область [**ианалисисрегион**](ianalysisregion.md) пересекается с указанным прямоугольником; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Сравнение осуществляется по координатам рукописного ввода.

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

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




