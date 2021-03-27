---
title: 'Функция Самплекмп:: Самплекмп (S, float, float, float) для Текстурекубеаррай'
description: 'Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в. | Функция Самплекмп:: Самплекмп (S, float, float, float) для Текстурекубеаррай'
ms.assetid: A8824A82-A3FD-4FEE-BC10-56843997BBCE
keywords:
- Функция Самплекмп HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e65b1747d03b3a0555267f7b57e95a4d5aba54da
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987272"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecubearray"></a>Функция Самплекмп:: Самплекмп (S, float, float, float) для Текстурекубеаррай

Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в.

## <a name="syntax"></a>Синтаксис


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
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

*Компаревалуе* \[ окне\]
</dt> <dd>

Тип: **float**

Значение с плавающей запятой, используемое в качестве значения сравнения.

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

[Методы Самплекмп](texturecubearray-samplecmp.md)
</dt> <dt>

[**текстурекубеаррай**](texturecubearray.md)
</dt> </dl>

 

 
