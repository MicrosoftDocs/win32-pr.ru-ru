---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, float) для Текстурекубе'
description: Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод). Для Текстурекубе
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
keywords:
- Функция Самплеград HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebaa411ccb6075cfe9aab429912c3644c50e2c8bf1db99faec3328f318700268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043302"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a>Функция Самплеград:: Самплеград (S, float, float, float, float) для Текстурекубе

Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод).

## <a name="syntax"></a>Синтаксис


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*S* \[ в\]
</dt> <dd>

Тип: **самплерстате**

[Состояние образца](dx-graphics-hlsl-sampler.md). Это объект, объявленный в файле эффектов, который содержит назначения состояний.

</dd> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **float**

Координаты текстуры. Тип аргумента зависит от типа объекта текстуры.



| Тип Texture-Object                    | Тип параметра |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, Текстурекубе | float3         |
| текстурекубеаррай                       | float4         |



 

</dd> <dt>

*DDX* \[ в\]
</dt> <dd>

Тип: **float**

Интенсивность изменения геометрии поверхности в направлении x. Тип аргумента зависит от типа объекта текстуры.



| Тип Texture-Object                      | Тип параметра |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, Текстурекубе, Текстурекубеаррай | float3         |
| Texture2DMS, Texture2DMSArray            | Не поддерживается  |



 

</dd> <dt>

*ДДИ* \[ окне\]
</dt> <dd>

Тип: **float**

Интенсивность изменения геометрии поверхности в направлении y. Тип аргумента зависит от типа объекта текстуры.



| Тип Texture-Object                      | Тип параметра |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, Текстурекубе, Текстурекубеаррай | float3         |
| Texture2DMS, Texture2DMSArray            | Не поддерживается  |



 

</dd> <dt>

*Срез* \[ окне\]
</dt> <dd>

Тип: **float**

Необязательное значение для примера среза Лод значений. Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Самплеград](texturecube-samplegrad.md)
</dt> <dt>

[**текстурекубе**](texturecube.md)
</dt> </dl>

 

 
