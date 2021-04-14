---
title: Функция D3DX_R16G16_SNORM_to_FLOAT2
description: Распаковать \_ \_ \_ данные шейдера в формате DXGI R16G16 снорм в XMFLOAT2.
ms.assetid: b54df555-b71f-46cd-8be7-34de785d15e2
keywords:
- Функция D3DX_R16G16_SNORM_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3d45f486d2c44e2cbe319e920ab4bdec764fd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998414"
---
# <a name="d3dx_r16g16_snorm_to_float2-function"></a><span data-ttu-id="42fe4-104">D3DX \_ R16G16 \_ снорм \_ to \_ FLOAT2 Function</span><span class="sxs-lookup"><span data-stu-id="42fe4-104">D3DX\_R16G16\_SNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="42fe4-105">Распаковать \_ \_ \_ данные шейдера в формате DXGI R16G16 снорм в XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="42fe4-105">Unpacks DXGI\_FORMAT\_R16G16\_SNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="42fe4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42fe4-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="42fe4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="42fe4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42fe4-108">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="42fe4-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="42fe4-109">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="42fe4-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42fe4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42fe4-110">Return value</span></span>

<span data-ttu-id="42fe4-111">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="42fe4-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="42fe4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="42fe4-112">Requirements</span></span>



| <span data-ttu-id="42fe4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="42fe4-113">Requirement</span></span> | <span data-ttu-id="42fe4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="42fe4-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42fe4-115">Header</span><span class="sxs-lookup"><span data-stu-id="42fe4-115">Header</span></span><br/> | <dl> <span data-ttu-id="42fe4-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="42fe4-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42fe4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="42fe4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42fe4-118">Функции</span><span class="sxs-lookup"><span data-stu-id="42fe4-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="42fe4-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="42fe4-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





