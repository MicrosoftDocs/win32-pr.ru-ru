---
title: 'Функция Самплелевел:: Самплелевел (S, float, float, uint) для Текстурекубе'
description: 'Производит выборку текстуры на указанном уровне mipmap и возвращает сведения о состоянии операции. | Функция Самплелевел:: Самплелевел (S, float, float, uint)'
ms.assetid: DB27D8B9-11AB-4F0C-947A-9469BA565F41
keywords:
- Функция Самплелевел HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 844ccc5b3f340b2d219865adb34f7717996bfbd2285d3f80337ce2f9ea4d31df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043202"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function-for-texturecube"></a>Функция Самплелевел:: Самплелевел (S, float, float, uint) для Текстурекубе

Производит выборку текстуры на указанном уровне mipmap и возвращает состояние операции.

## <a name="syntax"></a>Синтаксис


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
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

*Лод* \[ окне\]
</dt> <dd>

Тип: **float**

\[\]число, указывающее уровень mipmap. Если значение равно ≤ 0, то используется mipmap уровень 0 (самая большая схема). Дробное значение (если оно указано) используется для интерполяции между двумя уровнями mipmap.

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

[Методы Самплелевел](texturecube-samplelevel.md)
</dt> <dt>

[**текстурекубе**](texturecube.md)
</dt> </dl>

 

 
