---
title: Функция D3DX_SRGB_to_FLOAT_inexact
description: Преобразует значение SRGB в FLOAT. | Функция D3DX_SRGB_to_FLOAT_inexact
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- Функция D3DX_SRGB_to_FLOAT_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986882"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a><span data-ttu-id="4bfdb-105">D3DX \_ sRGB \_ для \_ \_ неточной функции</span><span class="sxs-lookup"><span data-stu-id="4bfdb-105">D3DX\_SRGB\_to\_FLOAT\_inexact function</span></span>

<span data-ttu-id="4bfdb-106">Преобразует значение SRGB в FLOAT.</span><span class="sxs-lookup"><span data-stu-id="4bfdb-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bfdb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bfdb-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="4bfdb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bfdb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bfdb-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="4bfdb-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="4bfdb-110">Значение SRGB для преобразования.</span><span class="sxs-lookup"><span data-stu-id="4bfdb-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bfdb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bfdb-111">Return value</span></span>

<span data-ttu-id="4bfdb-112">Преобразованное значение SRGB.</span><span class="sxs-lookup"><span data-stu-id="4bfdb-112">The converted SRGB value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bfdb-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="4bfdb-113">Remarks</span></span>

<span data-ttu-id="4bfdb-114">Эта функция не имеет достаточно большой точности для получения точного ответа.</span><span class="sxs-lookup"><span data-stu-id="4bfdb-114">This function doesn't have a high enough precision to give the exact answer.</span></span> <span data-ttu-id="4bfdb-115">Альтернативная функция [**D3DX \_ sRGB \_ to \_ float**](d3dx-srgb-to-float.md) использует таблицу уточняющих запросов для точного преобразования sRGB в float.</span><span class="sxs-lookup"><span data-stu-id="4bfdb-115">The alternative function [**D3DX\_SRGB\_to\_FLOAT**](d3dx-srgb-to-float.md) uses a lookup table to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bfdb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4bfdb-116">Requirements</span></span>



| <span data-ttu-id="4bfdb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4bfdb-117">Requirement</span></span> | <span data-ttu-id="4bfdb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4bfdb-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfdb-119">Header</span><span class="sxs-lookup"><span data-stu-id="4bfdb-119">Header</span></span><br/> | <dl> <span data-ttu-id="4bfdb-120"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="4bfdb-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bfdb-121">См. также</span><span class="sxs-lookup"><span data-stu-id="4bfdb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfdb-122">Функции</span><span class="sxs-lookup"><span data-stu-id="4bfdb-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4bfdb-123">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="4bfdb-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





