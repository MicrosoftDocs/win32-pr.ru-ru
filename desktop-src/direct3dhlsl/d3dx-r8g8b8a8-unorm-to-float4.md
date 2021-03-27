---
title: Функция D3DX_R8G8B8A8_UNORM_to_FLOAT4
description: Распаковать \_ \_ \_ данные шейдера в формате DXGI R8G8B8A8 UNORM в XMFLOAT4. | Функция D3DX_R8G8B8A8_UNORM_to_FLOAT4
ms.assetid: 94430f29-4872-4ecd-99b9-72f3b77c47f2
keywords:
- Функция D3DX_R8G8B8A8_UNORM_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e24b9f29d2e54f62582407e8ad40488032f8a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354550"
---
# <a name="d3dx_r8g8b8a8_unorm_to_float4-function"></a><span data-ttu-id="d09f8-105">D3DX \_ R8G8B8A8 \_ UNORM \_ to \_ FLOAT4 Function</span><span class="sxs-lookup"><span data-stu-id="d09f8-105">D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="d09f8-106">Распаковать \_ \_ \_ данные шейдера в формате DXGI R8G8B8A8 UNORM в XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="d09f8-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09f8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d09f8-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="d09f8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d09f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d09f8-109">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="d09f8-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="d09f8-110">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="d09f8-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d09f8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d09f8-111">Return value</span></span>

<span data-ttu-id="d09f8-112">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="d09f8-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d09f8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d09f8-113">Requirements</span></span>



| <span data-ttu-id="d09f8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d09f8-114">Requirement</span></span> | <span data-ttu-id="d09f8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d09f8-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d09f8-116">Header</span><span class="sxs-lookup"><span data-stu-id="d09f8-116">Header</span></span><br/> | <dl> <span data-ttu-id="d09f8-117"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="d09f8-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09f8-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d09f8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09f8-119">Функции</span><span class="sxs-lookup"><span data-stu-id="d09f8-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="d09f8-120">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="d09f8-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





