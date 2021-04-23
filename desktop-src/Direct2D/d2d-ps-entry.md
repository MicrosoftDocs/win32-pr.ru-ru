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
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665116"
---
# <a name="d2d_ps_entry-function"></a><span data-ttu-id="a3359-104">\_ \_ Входная функция D2D PS</span><span class="sxs-lookup"><span data-stu-id="a3359-104">D2D\_PS\_ENTRY function</span></span>

<span data-ttu-id="a3359-105">Макрос, определяющий точку входа шейдера пикселей с заданным именем функции.</span><span class="sxs-lookup"><span data-stu-id="a3359-105">A macro that defines a pixel shader entry point with the given function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3359-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3359-106">Syntax</span></span>

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a><span data-ttu-id="a3359-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3359-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3359-108">*Имязаписи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3359-108">*Entryname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3359-109">Имя точки входа шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="a3359-109">The pixel shader entry point name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3359-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3359-110">Return value</span></span>

<span data-ttu-id="a3359-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a3359-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3359-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3359-112">Remarks</span></span>

<span data-ttu-id="a3359-113">Используйте этот макрос вместо указания подписи входных данных точки входа обычным образом: все параметры являются неявными и добавляются с помощью Direct2D во время компиляции в зависимости от типа целевого объекта компиляции (полный шейдер или функция экспорта).</span><span class="sxs-lookup"><span data-stu-id="a3359-113">Use this macro instead of specifying the entry point s input signature in the normal manner: all parameters are implicit and added by Direct2D during compilation depending on the compilation target type (full shader or export function).</span></span>

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

<span data-ttu-id="a3359-114">В этом коротком примере обратите внимание, что не объявлены параметры функции, что число входов и типов каждого входного параметра объявляется перед функцией ввода, входные данные извлекаются путем вызова [D2DGetInput](d2dgetinput.md), а эти директивы препроцессора должны быть определены до включения вспомогательного файла.</span><span class="sxs-lookup"><span data-stu-id="a3359-114">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="a3359-115">Совместимый с связыванием шейдер должен предоставлять как обычный шейдер пикселей с одним проходом, так и функцию шейдера экспорта.</span><span class="sxs-lookup"><span data-stu-id="a3359-115">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="a3359-116">\_ \_ Макрос записи D2D PS позволяет создавать их из одного и того же кода при использовании в сочетании с скриптом компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="a3359-116">The D2D\_PS\_ENTRY macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="a3359-117">При компиляции полного шейдера макросы разворачиваются в следующий код, имеющий входную подпись, совместимую с эффектами D2D.</span><span class="sxs-lookup"><span data-stu-id="a3359-117">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

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

<span data-ttu-id="a3359-118">При компиляции версии функции экспорта одного и того же кода создается следующий код:</span><span class="sxs-lookup"><span data-stu-id="a3359-118">When compiling an export function version of the same code, the following code is generated:</span></span>

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

<span data-ttu-id="a3359-119">Обратите внимание, что входные данные текстуры, обычно извлекаемые методом выборки Texture2D, были заменены на входные данные функции input0.</span><span class="sxs-lookup"><span data-stu-id="a3359-119">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input input0.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3359-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a3359-120">Requirements</span></span>



| <span data-ttu-id="a3359-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a3359-121">Requirement</span></span> | <span data-ttu-id="a3359-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a3359-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3359-123">Header</span><span class="sxs-lookup"><span data-stu-id="a3359-123">Header</span></span><br/> | <dl> <span data-ttu-id="a3359-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="a3359-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="a3359-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a3359-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="a3359-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3359-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="a3359-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3359-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3359-128">Связывание шейдеров эффектов</span><span class="sxs-lookup"><span data-stu-id="a3359-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="a3359-129">Вспомогательные методы HLSL</span><span class="sxs-lookup"><span data-stu-id="a3359-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





