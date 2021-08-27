---
title: Функция D2D_PS_ENTRY (D2d1effecthelpers. h)
description: Макрос, определяющий точку входа шейдера пикселей с заданным именем функции.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- Функция D2D_PS_ENTRY Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26369ef5be8c9dea81bf95e60c09ca0041d4275114c8892b85b6b5525f45504b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087792"
---
# <a name="d2d_ps_entry-function"></a>\_ \_ Входная функция D2D PS

Макрос, определяющий точку входа шейдера пикселей с заданным именем функции.

## <a name="syntax"></a>Синтаксис

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Имязаписи* \[ окне\]
</dt> <dd>

Имя точки входа шейдера пикселей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Используйте этот макрос вместо указания подписи входных данных точки входа обычным образом: все параметры являются неявными и добавляются с помощью Direct2D во время компиляции в зависимости от типа целевого объекта компиляции (полный шейдер или функция экспорта).

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

В этом коротком примере обратите внимание, что не объявлены параметры функции, что число входов и типов каждого входного параметра объявляется перед функцией ввода, входные данные извлекаются путем вызова [D2DGetInput](d2dgetinput.md), а эти директивы препроцессора должны быть определены до включения вспомогательного файла.

Совместимый с связыванием шейдер должен предоставлять как обычный шейдер пикселей с одним проходом, так и функцию шейдера экспорта. \_ \_ Макрос записи D2D PS позволяет создавать их из одного и того же кода при использовании в сочетании с скриптом компиляции шейдера.

При компиляции полного шейдера макросы разворачиваются в следующий код, имеющий входную подпись, совместимую с эффектами D2D.

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

При компиляции версии функции экспорта одного и того же кода создается следующий код:

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

Обратите внимание, что входные данные текстуры, обычно извлекаемые методом выборки Texture2D, были заменены на входные данные функции input0.

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

 

 





