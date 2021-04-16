---
title: Функция D2DGetInputCoordinate (D2d1effecthelpers. h)
description: Возвращает значение входного ТЕКСКУРДН. Доступно только для сложных входных данных.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- Функция D2DGetInputCoordinate Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679834"
---
# <a name="d2dgetinputcoordinate-function"></a>Функция D2DGetInputCoordinate

Возвращает значение входного ТЕКСКУРДН. Доступно только для сложных входных данных.

## <a name="syntax"></a>Синтаксис

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*N* \[ в\]
</dt> <dd>

Входной номер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **float4** в формате текскурдн.

## <a name="remarks"></a>Комментарии

Координата, возвращаемая этой функцией, находится в шаг текселя пространстве. Шейдер не должен зависеть от того, как вычисляется это значение. Он должен использовать его только для выборки входных шейдеров пикселей. Дополнительные сведения см. в разделе [Добавление шейдера пикселей к пользовательскому преобразованию](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).

В следующем примере показана функция, используемая для действия с картой смещения.

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Связывание шейдеров эффектов](effect-shader-linking.md)
</dt> <dt>

[Вспомогательные методы HLSL](hlsl-helpers.md)
</dt> </dl>

 

