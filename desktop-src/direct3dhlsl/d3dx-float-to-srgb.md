---
title: Функция D3DX_FLOAT_to_SRGB
description: Преобразует значение FLOAT в SRGB.
ms.assetid: 734a0837-98da-45ba-bb0b-1e930ba78a7d
keywords:
- Функция D3DX_FLOAT_to_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71afb0c4e601be70c1ec04bd7bcd5e76c6cc573
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998672"
---
# <a name="d3dx_float_to_srgb-function"></a><span data-ttu-id="81ba3-104">D3DX \_ с плавающей запятой \_ к \_ функции sRGB</span><span class="sxs-lookup"><span data-stu-id="81ba3-104">D3DX\_FLOAT\_to\_SRGB function</span></span>

<span data-ttu-id="81ba3-105">Преобразует значение FLOAT в SRGB.</span><span class="sxs-lookup"><span data-stu-id="81ba3-105">Converts a FLOAT value to an SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ba3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81ba3-106">Syntax</span></span>

``` syntax
FLOAT D3DX_FLOAT_to_SRGB(
   FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="81ba3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="81ba3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ba3-108">*Val*</span><span class="sxs-lookup"><span data-stu-id="81ba3-108">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="81ba3-109">Преобразуемое значение FLOAT.</span><span class="sxs-lookup"><span data-stu-id="81ba3-109">FLOAT value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ba3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81ba3-110">Return value</span></span>

<span data-ttu-id="81ba3-111">Преобразованное значение SRGB.</span><span class="sxs-lookup"><span data-stu-id="81ba3-111">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ba3-112">Требования</span><span class="sxs-lookup"><span data-stu-id="81ba3-112">Requirements</span></span>



| <span data-ttu-id="81ba3-113">Требование</span><span class="sxs-lookup"><span data-stu-id="81ba3-113">Requirement</span></span> | <span data-ttu-id="81ba3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="81ba3-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ba3-115">Header</span><span class="sxs-lookup"><span data-stu-id="81ba3-115">Header</span></span><br/> | <dl> <span data-ttu-id="81ba3-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="81ba3-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81ba3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="81ba3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ba3-118">Функции</span><span class="sxs-lookup"><span data-stu-id="81ba3-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="81ba3-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="81ba3-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





