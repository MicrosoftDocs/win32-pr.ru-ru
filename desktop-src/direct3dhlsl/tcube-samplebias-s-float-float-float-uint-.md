---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, float, uint) для Текстурекубе'
description: 'Функция Самплебиас:: Самплебиас (S, float, float, float, uint) для Текстурекубе выбирает текстуру после применения значения смещения к уровню mipmap.'
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
keywords:
- Функция Самплебиас HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 116749acdc23bb8ac2fd057139bf8ef7c8f5ddcc
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187685"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecube"></a>Функция Самплебиас:: Самплебиас (S, float, float, float, uint) для Текстурекубе

Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод). Возвращает состояние операции.

## <a name="syntax"></a>Синтаксис


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
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

*Уровень защиты* \[ окне\]
</dt> <dd>

Тип: **float**

Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.

</dd> <dt>

*Срез* \[ окне\]
</dt> <dd>

Тип: **float**

Необязательное значение для примера среза Лод значений. Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.

</dd> <dt>

*Состояние* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Состояние операции. Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) . **Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features). Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Самплебиас](texturecube-samplebias.md)
</dt> <dt>

[**текстурекубе**](texturecube.md)
</dt> </dl>

 

 
