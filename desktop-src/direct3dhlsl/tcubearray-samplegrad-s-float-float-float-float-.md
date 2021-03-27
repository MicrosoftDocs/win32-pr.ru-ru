---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, float) для Текстурекубеаррай'
description: Узнайте, как эта функция выбирает текстуру с помощью градиента, влияющей на способ вычисления расположения образца. Для Текстурекубеаррай.
ms.assetid: 0C7DC9AA-3F0A-47E4-852F-7AE25CF67EA3
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
ms.openlocfilehash: 5320f47a5ae4db5bd96232dfa0a1d55b54f29c25
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821557"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecubearray"></a>Функция Самплеград:: Самплеград (S, float, float, float, float) для Текстурекубеаррай

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
| Texture2DMS, Texture2DMSArray            | не поддерживается  |



 

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
| Texture2DMS, Texture2DMSArray            | не поддерживается  |



 

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

[Методы Самплеград](texturecubearray-samplegrad.md)
</dt> <dt>

[**текстурекубеаррай**](texturecubearray.md)
</dt> </dl>

 

 
