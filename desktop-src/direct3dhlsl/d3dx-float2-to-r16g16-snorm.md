---
title: Функция D3DX_FLOAT2_to_R16G16_SNORM
description: Упаковывает заданный XMFLOAT2 обратно в формат DXGI \_ \_ R16G16 \_ снорм.
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- Функция D3DX_FLOAT2_to_R16G16_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000396"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a><span data-ttu-id="f95dd-104">D3DX \_ FLOAT2 \_ to \_ R16G16 \_ снорм Function</span><span class="sxs-lookup"><span data-stu-id="f95dd-104">D3DX\_FLOAT2\_to\_R16G16\_SNORM function</span></span>

<span data-ttu-id="f95dd-105">Упаковывает заданный XMFLOAT2 обратно в формат DXGI \_ \_ R16G16 \_ снорм.</span><span class="sxs-lookup"><span data-stu-id="f95dd-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="f95dd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f95dd-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="f95dd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f95dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f95dd-108">*унпаккединпут*</span><span class="sxs-lookup"><span data-stu-id="f95dd-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="f95dd-109">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="f95dd-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f95dd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f95dd-110">Return value</span></span>

<span data-ttu-id="f95dd-111">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="f95dd-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f95dd-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f95dd-112">Requirements</span></span>



| <span data-ttu-id="f95dd-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f95dd-113">Requirement</span></span> | <span data-ttu-id="f95dd-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f95dd-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f95dd-115">Header</span><span class="sxs-lookup"><span data-stu-id="f95dd-115">Header</span></span><br/> | <dl> <span data-ttu-id="f95dd-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="f95dd-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f95dd-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f95dd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f95dd-118">Функции</span><span class="sxs-lookup"><span data-stu-id="f95dd-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="f95dd-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="f95dd-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





