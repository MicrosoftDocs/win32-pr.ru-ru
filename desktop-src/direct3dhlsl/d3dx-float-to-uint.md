---
title: Функция D3DX_FLOAT_to_UINT
description: Преобразует значение FLOAT в тип UINT.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- Функция D3DX_FLOAT_to_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e729ba805d63068844192a134236722288fe8a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354293"
---
# <a name="d3dx_float_to_uint-function"></a><span data-ttu-id="fb973-104">D3DX \_ с плавающей запятой \_ в \_ функцию uint</span><span class="sxs-lookup"><span data-stu-id="fb973-104">D3DX\_FLOAT\_to\_UINT function</span></span>

<span data-ttu-id="fb973-105">Преобразует значение FLOAT в тип UINT.</span><span class="sxs-lookup"><span data-stu-id="fb973-105">Converts a FLOAT value to UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb973-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb973-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="fb973-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb973-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb973-108">*\_3,3*</span><span class="sxs-lookup"><span data-stu-id="fb973-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="fb973-109">Вектор v.</span><span class="sxs-lookup"><span data-stu-id="fb973-109">The v vector.</span></span>

</dd> <dt>

<span data-ttu-id="fb973-110">*\_Измените*</span><span class="sxs-lookup"><span data-stu-id="fb973-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="fb973-111">Значение масштаба.</span><span class="sxs-lookup"><span data-stu-id="fb973-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb973-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb973-112">Return value</span></span>

<span data-ttu-id="fb973-113">Преобразованное значение FLOAT</span><span class="sxs-lookup"><span data-stu-id="fb973-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="fb973-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fb973-114">Requirements</span></span>



| <span data-ttu-id="fb973-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fb973-115">Requirement</span></span> | <span data-ttu-id="fb973-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fb973-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb973-117">Header</span><span class="sxs-lookup"><span data-stu-id="fb973-117">Header</span></span><br/> | <dl> <span data-ttu-id="fb973-118"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="fb973-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb973-119">См. также</span><span class="sxs-lookup"><span data-stu-id="fb973-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb973-120">Функции</span><span class="sxs-lookup"><span data-stu-id="fb973-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="fb973-121">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="fb973-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





