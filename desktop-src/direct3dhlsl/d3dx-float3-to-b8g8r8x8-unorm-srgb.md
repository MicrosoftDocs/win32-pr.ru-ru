---
title: Функция D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
description: Упаковывает заданный XMFLOAT3 обратно в формат DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB.
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- Функция D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74dd5fbc1329d884968d76039061fceb22aafbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998369"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a><span data-ttu-id="de4f5-104">D3DX \_ FLOAT3 \_ в \_ B8G8R8X8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="de4f5-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="de4f5-105">Упаковывает заданный XMFLOAT3 обратно в формат DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="de4f5-105">Packs the given XMFLOAT3 back into a DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4f5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de4f5-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="de4f5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="de4f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4f5-108">*унпаккединпут*</span><span class="sxs-lookup"><span data-stu-id="de4f5-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="de4f5-109">Данные шейдера для упаковки.</span><span class="sxs-lookup"><span data-stu-id="de4f5-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de4f5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de4f5-110">Return value</span></span>

<span data-ttu-id="de4f5-111">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="de4f5-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="de4f5-112">Требования</span><span class="sxs-lookup"><span data-stu-id="de4f5-112">Requirements</span></span>



| <span data-ttu-id="de4f5-113">Требование</span><span class="sxs-lookup"><span data-stu-id="de4f5-113">Requirement</span></span> | <span data-ttu-id="de4f5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="de4f5-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de4f5-115">Header</span><span class="sxs-lookup"><span data-stu-id="de4f5-115">Header</span></span><br/> | <dl> <span data-ttu-id="de4f5-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="de4f5-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de4f5-117">См. также</span><span class="sxs-lookup"><span data-stu-id="de4f5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4f5-118">Функции</span><span class="sxs-lookup"><span data-stu-id="de4f5-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="de4f5-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="de4f5-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





