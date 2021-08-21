---
title: Функция Процессисолинетессфакторс
description: Создает округленные факторы тесселяции для исолине.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- Функция Процессисолинетессфакторс HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34c6f4d579ee7fbaee9416d7a607e3856a7793021cca7149723d3d6e5a2b4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986294"
---
# <a name="processisolinetessfactors-function"></a>Функция Процессисолинетессфакторс

Создает округленные факторы тесселяции для исолине.

## <a name="syntax"></a>Синтаксис

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Равдетаилфактор* \[ окне\]
</dt> <dd>

Тип: **float**

Требуемый подробный фактор.

</dd> <dt>

*Равденситифактор* \[ окне\]
</dt> <dd>

Тип: **float**

Требуемый коэффициент плотности.

</dd> <dt>

*Раундеддетаилфактор* \[ заполняет\]
</dt> <dd>

Тип: **float**

Скругленный коэффициент детализации для диапазона, который может использоваться в тесселяции.

</dd> <dt>

*Раундедденситифактор* \[ заполняет\]
</dt> <dd>

Тип: **float**

В качестве коэффициента округления к ранжесат может использоваться тесселяция.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | Да       |



 

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




