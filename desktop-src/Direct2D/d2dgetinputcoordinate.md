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
# <a name="d2dgetinputcoordinate-function"></a><span data-ttu-id="5eefe-105">Функция D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="5eefe-105">D2DGetInputCoordinate function</span></span>

<span data-ttu-id="5eefe-106">Возвращает значение входного ТЕКСКУРДН.</span><span class="sxs-lookup"><span data-stu-id="5eefe-106">Returns the value of the input TEXCOORDN.</span></span> <span data-ttu-id="5eefe-107">Доступно только для сложных входных данных.</span><span class="sxs-lookup"><span data-stu-id="5eefe-107">Available only for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eefe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5eefe-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="5eefe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5eefe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eefe-110">*N* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5eefe-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eefe-111">Входной номер.</span><span class="sxs-lookup"><span data-stu-id="5eefe-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eefe-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5eefe-112">Return value</span></span>

<span data-ttu-id="5eefe-113">Функция возвращает **float4** в формате текскурдн.</span><span class="sxs-lookup"><span data-stu-id="5eefe-113">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eefe-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5eefe-114">Remarks</span></span>

<span data-ttu-id="5eefe-115">Координата, возвращаемая этой функцией, находится в шаг текселя пространстве.</span><span class="sxs-lookup"><span data-stu-id="5eefe-115">The coordinate returned by this function is in texel space.</span></span> <span data-ttu-id="5eefe-116">Шейдер не должен зависеть от того, как вычисляется это значение.</span><span class="sxs-lookup"><span data-stu-id="5eefe-116">A shader shouldn't take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="5eefe-117">Он должен использовать его только для выборки входных шейдеров пикселей.</span><span class="sxs-lookup"><span data-stu-id="5eefe-117">It should use it only to sample the pixel shader's input.</span></span> <span data-ttu-id="5eefe-118">Дополнительные сведения см. в разделе [Добавление шейдера пикселей к пользовательскому преобразованию](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span><span class="sxs-lookup"><span data-stu-id="5eefe-118">For more info, see [Adding a pixel shader to a custom transform](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span></span>

<span data-ttu-id="5eefe-119">В следующем примере показана функция, используемая для действия с картой смещения.</span><span class="sxs-lookup"><span data-stu-id="5eefe-119">The following example shows the function used for a displacement map effect.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="5eefe-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5eefe-120">Requirements</span></span>



| <span data-ttu-id="5eefe-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5eefe-121">Requirement</span></span> | <span data-ttu-id="5eefe-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5eefe-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eefe-123">Header</span><span class="sxs-lookup"><span data-stu-id="5eefe-123">Header</span></span><br/> | <dl> <span data-ttu-id="5eefe-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="5eefe-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="5eefe-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5eefe-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="5eefe-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5eefe-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="5eefe-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5eefe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eefe-128">Связывание шейдеров эффектов</span><span class="sxs-lookup"><span data-stu-id="5eefe-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="5eefe-129">Вспомогательные методы HLSL</span><span class="sxs-lookup"><span data-stu-id="5eefe-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

