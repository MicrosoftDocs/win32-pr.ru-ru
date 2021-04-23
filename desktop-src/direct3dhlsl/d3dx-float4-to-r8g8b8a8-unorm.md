---
title: Функция D3DX_FLOAT4_to_R8G8B8A8_UNORM
description: Распаковать \_ \_ \_ данные шейдера в формате DXGI R8G8B8A8 UNORM в XMFLOAT4. | Функция D3DX_FLOAT4_to_R8G8B8A8_UNORM
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- Функция D3DX_FLOAT4_to_R8G8B8A8_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821453"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a><span data-ttu-id="3844a-105">D3DX \_ FLOAT4 \_ to \_ R8G8B8A8 \_ UNORM Function</span><span class="sxs-lookup"><span data-stu-id="3844a-105">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM function</span></span>

<span data-ttu-id="3844a-106">Распаковать \_ \_ \_ данные шейдера в формате DXGI R8G8B8A8 UNORM в XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="3844a-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="3844a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3844a-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="3844a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3844a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3844a-109">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="3844a-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="3844a-110">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="3844a-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3844a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3844a-111">Return value</span></span>

<span data-ttu-id="3844a-112">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="3844a-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3844a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3844a-113">Requirements</span></span>



| <span data-ttu-id="3844a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3844a-114">Requirement</span></span> | <span data-ttu-id="3844a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3844a-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3844a-116">Header</span><span class="sxs-lookup"><span data-stu-id="3844a-116">Header</span></span><br/> | <dl> <span data-ttu-id="3844a-117"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="3844a-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3844a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="3844a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3844a-119">Функции</span><span class="sxs-lookup"><span data-stu-id="3844a-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="3844a-120">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="3844a-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





