---
title: 'Функция функции Самплеград:: Самплеград (S, float, float, float, int, float) для Texture3D'
description: Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод). Для Texture3D.
ms.assetid: F59D54F8-CC9E-47F8-97DD-735C70939C07
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
ms.openlocfilehash: ba85c752223e3bccd9898a48b884a7149c8203ad7b7542ba22e30fadcdc33773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118044"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture3d"></a>Функция Самплеград:: Самплеград (S, float, float, float, int, float) для Texture3D

Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод).

## <a name="syntax"></a>Синтаксис


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
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

*Смещение* \[ окне\]
</dt> <dd>

Тип: **int**

Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой. Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование. Тип аргумента зависит от типа объекта текстуры. Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).



| Тип Texture-Object           | Тип параметра |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| Текстурекубе, Текстурекубеаррай | Не поддерживается  |



 

</dd> <dt>

*Срез* \[ окне\]
</dt> <dd>

Тип: **float**

Необязательное значение для примера среза Лод значений. Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>См. также

<dl> <dt>

[Методы Самплеград](texture3d-samplegrad.md)
</dt> <dt>

[**Texture3D**](sm5-object-texture3d.md)
</dt> </dl>

 

 
