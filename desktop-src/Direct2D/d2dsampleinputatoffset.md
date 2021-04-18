---
title: Функция D2DSampleInputAtOffset (D2d1effecthelpers. h)
description: Примеры входных данных N со смещением смещения от входной координаты. Доступно только для сложных входных данных.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- Функция D2DSampleInputAtOffset Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657973"
---
# <a name="d2dsampleinputatoffset-function"></a>Функция D2DSampleInputAtOffset

Примеры входных данных N со смещением смещения от входной координаты. Доступно только для сложных входных данных.

## <a name="syntax"></a>Синтаксис

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*N* \[ в\]
</dt> <dd>

Входной номер.

</dd> <dt>

*смещение* \[ окне\]
</dt> <dd>

Смещение UV.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **float4** в формате текскурдн.

## <a name="remarks"></a>Комментарии

В следующем примере показана функция, используемая как часть маски градиента выделения и тени.

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
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

 

 





