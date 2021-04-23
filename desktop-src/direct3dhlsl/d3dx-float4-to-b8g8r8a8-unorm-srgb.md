---
title: Функция D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
description: Упаковывает заданный XMFLOAT4 в формат DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB uint.
ms.assetid: 2fc36f19-44ce-43ba-9d9f-e8061f94a207
keywords:
- Функция D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c20292e1038d31c6d853eb8ae62f7e764e722a6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273904"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a><span data-ttu-id="5d515-104">D3DX \_ FLOAT4 \_ в \_ B8G8R8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="5d515-104">D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="5d515-105">Упаковывает заданный XMFLOAT4 в формат DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB uint.</span><span class="sxs-lookup"><span data-stu-id="5d515-105">Packs the given XMFLOAT4 into a DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d515-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d515-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="5d515-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d515-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d515-108">*унпаккединпут*</span><span class="sxs-lookup"><span data-stu-id="5d515-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="5d515-109">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="5d515-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d515-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d515-110">Return value</span></span>

<span data-ttu-id="5d515-111">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="5d515-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d515-112">Требования</span><span class="sxs-lookup"><span data-stu-id="5d515-112">Requirements</span></span>



| <span data-ttu-id="5d515-113">Требование</span><span class="sxs-lookup"><span data-stu-id="5d515-113">Requirement</span></span> | <span data-ttu-id="5d515-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5d515-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d515-115">Header</span><span class="sxs-lookup"><span data-stu-id="5d515-115">Header</span></span><br/> | <dl> <span data-ttu-id="5d515-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="5d515-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d515-117">См. также</span><span class="sxs-lookup"><span data-stu-id="5d515-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d515-118">Функции</span><span class="sxs-lookup"><span data-stu-id="5d515-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5d515-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="5d515-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





