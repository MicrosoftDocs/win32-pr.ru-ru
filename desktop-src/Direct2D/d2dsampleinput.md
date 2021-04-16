---
title: Функция D2DSampleInput (D2d1effecthelpers. h)
description: Примеры входных данных N в позиции UV. Доступно только для сложных входных данных.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- Функция D2DSampleInput Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679895"
---
# <a name="d2dsampleinput-function"></a><span data-ttu-id="6bd77-105">Функция D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="6bd77-105">D2DSampleInput function</span></span>

<span data-ttu-id="6bd77-106">Примеры входных данных N в позиции UV.</span><span class="sxs-lookup"><span data-stu-id="6bd77-106">Samples input N at position uv.</span></span> <span data-ttu-id="6bd77-107">Доступно только для сложных входных данных.</span><span class="sxs-lookup"><span data-stu-id="6bd77-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd77-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bd77-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="6bd77-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bd77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bd77-110">*N* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6bd77-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bd77-111">Входной номер.</span><span class="sxs-lookup"><span data-stu-id="6bd77-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="6bd77-112">*UV* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6bd77-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bd77-113">Расположение UV.</span><span class="sxs-lookup"><span data-stu-id="6bd77-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bd77-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bd77-114">Return value</span></span>

<span data-ttu-id="6bd77-115">Функция возвращает **float4** в формате текскурдн.</span><span class="sxs-lookup"><span data-stu-id="6bd77-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bd77-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bd77-116">Remarks</span></span>

<span data-ttu-id="6bd77-117">В следующем примере показана функция, используемая для вычисления нормалей поверхности.</span><span class="sxs-lookup"><span data-stu-id="6bd77-117">The following example shows the function being used to calculate surface normals.</span></span>

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
}  
```

## <a name="requirements"></a><span data-ttu-id="6bd77-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6bd77-118">Requirements</span></span>



| <span data-ttu-id="6bd77-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6bd77-119">Requirement</span></span> | <span data-ttu-id="6bd77-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd77-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd77-121">Header</span><span class="sxs-lookup"><span data-stu-id="6bd77-121">Header</span></span><br/> | <dl> <span data-ttu-id="6bd77-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="6bd77-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="6bd77-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6bd77-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="6bd77-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bd77-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="6bd77-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bd77-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bd77-126">Связывание шейдеров эффектов</span><span class="sxs-lookup"><span data-stu-id="6bd77-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="6bd77-127">Вспомогательные методы HLSL</span><span class="sxs-lookup"><span data-stu-id="6bd77-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





