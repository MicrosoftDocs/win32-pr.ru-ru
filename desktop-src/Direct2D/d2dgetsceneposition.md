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
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657933"
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

## <a name="remarks"></a>Комментарии

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

 

 





