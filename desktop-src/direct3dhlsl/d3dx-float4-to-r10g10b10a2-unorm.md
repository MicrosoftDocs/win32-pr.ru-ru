---
title: Функция D3DX_FLOAT4_to_R10G10B10A2_UNORM
description: Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ R10G10B10A2 \_ UNORM.
ms.assetid: 20471435-bb1a-4151-a03a-c334b2a7d944
keywords:
- Функция D3DX_FLOAT4_to_R10G10B10A2_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c8d80b8822d03a43e813226c28dde8693397a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986762"
---
# <a name="d3dx_float4_to_r10g10b10a2_unorm-function"></a><span data-ttu-id="8a87e-104">D3DX \_ FLOAT4 \_ to \_ R10G10B10A2 \_ UNORM Function</span><span class="sxs-lookup"><span data-stu-id="8a87e-104">D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM function</span></span>

<span data-ttu-id="8a87e-105">Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ R10G10B10A2 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="8a87e-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R10G10B10A2\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a87e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a87e-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="8a87e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a87e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a87e-108">*унпаккединпут*</span><span class="sxs-lookup"><span data-stu-id="8a87e-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8a87e-109">Данные шейдера для упаковки.</span><span class="sxs-lookup"><span data-stu-id="8a87e-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a87e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a87e-110">Return value</span></span>

<span data-ttu-id="8a87e-111">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="8a87e-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a87e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8a87e-112">Requirements</span></span>



| <span data-ttu-id="8a87e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8a87e-113">Requirement</span></span> | <span data-ttu-id="8a87e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8a87e-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a87e-115">Header</span><span class="sxs-lookup"><span data-stu-id="8a87e-115">Header</span></span><br/> | <dl> <span data-ttu-id="8a87e-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="8a87e-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a87e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8a87e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a87e-118">Функции</span><span class="sxs-lookup"><span data-stu-id="8a87e-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="8a87e-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="8a87e-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





