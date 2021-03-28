---
title: Функция D3DX_FLOAT_to_INT
description: Преобразует значение FLOAT в тип INT.
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- Функция D3DX_FLOAT_to_INT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c127ef20cdd21cbc83e466f75844b4f80f47f948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548111"
---
# <a name="d3dx_float_to_int-function"></a><span data-ttu-id="e09f5-104">\_Функция D3DX float \_ to \_ int</span><span class="sxs-lookup"><span data-stu-id="e09f5-104">D3DX\_FLOAT\_to\_INT function</span></span>

<span data-ttu-id="e09f5-105">Преобразует значение FLOAT в тип INT.</span><span class="sxs-lookup"><span data-stu-id="e09f5-105">Converts a FLOAT value to INT.</span></span>

## <a name="syntax"></a><span data-ttu-id="e09f5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e09f5-106">Syntax</span></span>

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="e09f5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e09f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e09f5-108">*\_3,3*</span><span class="sxs-lookup"><span data-stu-id="e09f5-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="e09f5-109">Значение v.</span><span class="sxs-lookup"><span data-stu-id="e09f5-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="e09f5-110">*\_Измените*</span><span class="sxs-lookup"><span data-stu-id="e09f5-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="e09f5-111">Значение масштаба.</span><span class="sxs-lookup"><span data-stu-id="e09f5-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e09f5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e09f5-112">Return value</span></span>

<span data-ttu-id="e09f5-113">Преобразованное значение FLOAT</span><span class="sxs-lookup"><span data-stu-id="e09f5-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="e09f5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e09f5-114">Requirements</span></span>



| <span data-ttu-id="e09f5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e09f5-115">Requirement</span></span> | <span data-ttu-id="e09f5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e09f5-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e09f5-117">Header</span><span class="sxs-lookup"><span data-stu-id="e09f5-117">Header</span></span><br/> | <dl> <span data-ttu-id="e09f5-118"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="e09f5-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e09f5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e09f5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e09f5-120">Функции</span><span class="sxs-lookup"><span data-stu-id="e09f5-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e09f5-121">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="e09f5-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





