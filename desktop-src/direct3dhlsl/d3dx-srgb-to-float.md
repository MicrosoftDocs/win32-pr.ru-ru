---
title: Функция D3DX_SRGB_to_FLOAT
description: Преобразует значение SRGB в FLOAT. | Функция D3DX_SRGB_to_FLOAT
ms.assetid: 03e2ea09-3dd7-48cb-81b3-e11f7a9cf0ee
keywords:
- Функция D3DX_SRGB_to_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e1b5dc6224a06881e227b82e74436c4820aaf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000395"
---
# <a name="d3dx_srgb_to_float-function"></a><span data-ttu-id="98704-105">D3DX \_ sRGB \_ to \_ float, функция</span><span class="sxs-lookup"><span data-stu-id="98704-105">D3DX\_SRGB\_to\_FLOAT function</span></span>

<span data-ttu-id="98704-106">Преобразует значение SRGB в FLOAT.</span><span class="sxs-lookup"><span data-stu-id="98704-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="98704-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98704-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT(
   UINT val
);
```

## <a name="parameters"></a><span data-ttu-id="98704-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="98704-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98704-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="98704-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="98704-110">Значение SRGB для преобразования.</span><span class="sxs-lookup"><span data-stu-id="98704-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98704-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98704-111">Return value</span></span>

<span data-ttu-id="98704-112">Преобразованное значение SRGB.</span><span class="sxs-lookup"><span data-stu-id="98704-112">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="98704-113">Требования</span><span class="sxs-lookup"><span data-stu-id="98704-113">Requirements</span></span>



| <span data-ttu-id="98704-114">Требование</span><span class="sxs-lookup"><span data-stu-id="98704-114">Requirement</span></span> | <span data-ttu-id="98704-115">Значение</span><span class="sxs-lookup"><span data-stu-id="98704-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98704-116">Header</span><span class="sxs-lookup"><span data-stu-id="98704-116">Header</span></span><br/> | <dl> <span data-ttu-id="98704-117"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="98704-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98704-118">См. также</span><span class="sxs-lookup"><span data-stu-id="98704-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98704-119">Функции</span><span class="sxs-lookup"><span data-stu-id="98704-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="98704-120">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="98704-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





