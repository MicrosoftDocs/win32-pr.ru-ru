---
title: Функция D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
description: Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT3. | Функция D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- Функция D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986786"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a><span data-ttu-id="5c4c7-105">D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3 \_ Точная функция</span><span class="sxs-lookup"><span data-stu-id="5c4c7-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact function</span></span>

<span data-ttu-id="5c4c7-106">Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="5c4c7-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c4c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c4c7-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="5c4c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c4c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c4c7-109">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="5c4c7-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="5c4c7-110">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="5c4c7-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c4c7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c4c7-111">Return value</span></span>

<span data-ttu-id="5c4c7-112">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="5c4c7-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c4c7-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c4c7-113">Remarks</span></span>

<span data-ttu-id="5c4c7-114">Эта функция использует инструкции шейдера, которые не имеют достаточно высокой точности для получения точного ответа.</span><span class="sxs-lookup"><span data-stu-id="5c4c7-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="5c4c7-115">Альтернативная функция [**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) использует таблицу подстановки, хранящуюся в шейдере, чтобы дать точное преобразование sRGB для преобразования с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="5c4c7-115">The alternative function [**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c4c7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5c4c7-116">Requirements</span></span>



| <span data-ttu-id="5c4c7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5c4c7-117">Requirement</span></span> | <span data-ttu-id="5c4c7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5c4c7-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4c7-119">Header</span><span class="sxs-lookup"><span data-stu-id="5c4c7-119">Header</span></span><br/> | <dl> <span data-ttu-id="5c4c7-120"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="5c4c7-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c4c7-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5c4c7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c4c7-122">Функции</span><span class="sxs-lookup"><span data-stu-id="5c4c7-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5c4c7-123">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="5c4c7-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





