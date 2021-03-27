---
title: 'Функция Текстурекубеаррай:: Sample (S, float, float, uint)'
description: 'Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции. | Функция Текстурекубеаррай:: Sample (S, float, float, uint)'
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
keywords:
- Пример функции HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24e6d77698507f0d1673b66954db8e78466ac728
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820628"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a>Функция Текстурекубеаррай:: Sample (S, float, float, uint)

Выбирает текстуру с необязательным значением для фиксации в качестве примера значений уровня детализации (Лод) и возвращает состояние операции.

## <a name="syntax"></a>Синтаксис


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*S* \[ в\]
</dt> <dd>

[Состояние образца](dx-graphics-hlsl-sampler.md). Это объект, объявленный в файле эффектов, который содержит назначения состояний.

</dd> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Координаты текстуры. Тип аргумента зависит от типа объекта текстуры.



| Тип Texture-Object                    | Тип параметра |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, Текстурекубе | float3         |
| текстурекубеаррай                       | float4         |



 

</dd> <dt>

*Срез* \[ окне\]
</dt> <dd>

Необязательное значение для примера среза Лод значений. Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.

</dd> <dt>

*Состояние* \[ заполняет\]
</dt> <dd>

Состояние операции. Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) . **Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features). Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Примеры методов](texturecubearray-sample.md)
</dt> <dt>

[**текстурекубеаррай**](texturecubearray.md)
</dt> </dl>

 

 
