---
title: Функция D3DX_R16G16_UNORM_to_FLOAT2
description: Распаковать \_ \_ \_ данные шейдера в формате DXGI R16G16 UNORM в XMFLOAT2.
ms.assetid: e82e2a47-f494-4085-8c02-1bac3088d29f
keywords:
- Функция D3DX_R16G16_UNORM_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba4ca1bb02e66289ec66d0ec4f58978800f6538
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354553"
---
# <a name="d3dx_r16g16_unorm_to_float2-function"></a><span data-ttu-id="c1765-104">D3DX \_ R16G16 \_ UNORM \_ to \_ FLOAT2 Function</span><span class="sxs-lookup"><span data-stu-id="c1765-104">D3DX\_R16G16\_UNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="c1765-105">Распаковать \_ \_ \_ данные шейдера в формате DXGI R16G16 UNORM в XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="c1765-105">Unpacks DXGI\_FORMAT\_R16G16\_UNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1765-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1765-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="c1765-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1765-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1765-108">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="c1765-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c1765-109">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="c1765-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1765-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1765-110">Return value</span></span>

<span data-ttu-id="c1765-111">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="c1765-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1765-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c1765-112">Requirements</span></span>



| <span data-ttu-id="c1765-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c1765-113">Requirement</span></span> | <span data-ttu-id="c1765-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c1765-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1765-115">Header</span><span class="sxs-lookup"><span data-stu-id="c1765-115">Header</span></span><br/> | <dl> <span data-ttu-id="c1765-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="c1765-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1765-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c1765-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1765-118">Функции</span><span class="sxs-lookup"><span data-stu-id="c1765-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c1765-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="c1765-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





