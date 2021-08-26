---
title: 'Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture2D'
description: Эта функция выбирает Texture2D, используя значение сравнения для отклонения выборок, с необязательным значением для фиксации значений уровня детализации (Лод) в.
ms.assetid: 1B5E6559-2524-4557-8F43-7AF258C39FB2
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
ms.openlocfilehash: 0dfd7e15b49eac739c069ea113c8daca996e7eb48e6b769f4b27934f891cbda7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023494"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2d"></a>Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture2D

Примеры [**Texture2D**](sm5-object-texture2d.md)с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в.

## <a name="syntax"></a>Синтаксис


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
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

*Компаревалуе* \[ окне\]
</dt> <dd>

Тип: **float**

Значение с плавающей запятой, используемое в качестве значения сравнения.

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

[Методы Самплекмп](texture2d-samplecmp.md)
</dt> </dl>

 

 
