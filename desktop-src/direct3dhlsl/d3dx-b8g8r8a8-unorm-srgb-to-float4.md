---
title: Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
description: Распаковка формата DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4. | Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
ms.assetid: f6ce6125-c67e-4545-b25e-3400c0fc62b1
keywords:
- Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91311bb83aa034410361bea631aa79f86737ff65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354300"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4-function"></a><span data-ttu-id="20852-105">D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 Function</span><span class="sxs-lookup"><span data-stu-id="20852-105">D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4 function</span></span>

<span data-ttu-id="20852-106">Распаковка формата DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="20852-106">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="20852-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20852-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="20852-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="20852-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20852-109">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="20852-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="20852-110">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="20852-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20852-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20852-111">Return value</span></span>

<span data-ttu-id="20852-112">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="20852-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="20852-113">Требования</span><span class="sxs-lookup"><span data-stu-id="20852-113">Requirements</span></span>



| <span data-ttu-id="20852-114">Требование</span><span class="sxs-lookup"><span data-stu-id="20852-114">Requirement</span></span> | <span data-ttu-id="20852-115">Значение</span><span class="sxs-lookup"><span data-stu-id="20852-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20852-116">Header</span><span class="sxs-lookup"><span data-stu-id="20852-116">Header</span></span><br/> | <dl> <span data-ttu-id="20852-117"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="20852-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20852-118">См. также</span><span class="sxs-lookup"><span data-stu-id="20852-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20852-119">Функции</span><span class="sxs-lookup"><span data-stu-id="20852-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="20852-120">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="20852-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





