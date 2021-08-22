---
title: Функция D2DGetScenePosition (D2d1effecthelpers. h)
description: Возвращает значение расположения входной сцены \_ . Доступно только в том \_ случае \_ \_ , если в исходном файле объявлено, что для D2D требуется указать расположение сцены.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- Функция D2DGetScenePosition Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcd7a1ee987cf64a92aa76b0f8910bee1c9a15465872bbd3ccfe2502629f700
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641644"
---
# <a name="d2dgetsceneposition-function"></a>Функция D2DGetScenePosition

Возвращает значение расположения входной сцены \_ . Доступно только в том \_ случае \_ \_ , если в исходном файле объявлено, что для D2D требуется указать расположение сцены.

## <a name="syntax"></a>Синтаксис

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **float4** в положении сцены формата \_ .

## <a name="remarks"></a>Remarks

В следующем примере показано использование функции при формировании шаблона разрешения конфликтов.

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
}  
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>См. также

<dl> <dt>

[Связывание шейдеров эффектов](effect-shader-linking.md)
</dt> <dt>

[Вспомогательные методы HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





