---
title: Функция D3DX_INT_to_FLOAT
description: Преобразует значение типа INT в тип FLOAT.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- Функция D3DX_INT_to_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987164"
---
# <a name="d3dx_int_to_float-function"></a><span data-ttu-id="946aa-104">\_Функция D3DX int \_ to \_ float</span><span class="sxs-lookup"><span data-stu-id="946aa-104">D3DX\_INT\_to\_FLOAT function</span></span>

<span data-ttu-id="946aa-105">Преобразует значение типа INT в тип FLOAT.</span><span class="sxs-lookup"><span data-stu-id="946aa-105">Converts a INT value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="946aa-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="946aa-106">Syntax</span></span>

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="946aa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="946aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="946aa-108">*\_3,3*</span><span class="sxs-lookup"><span data-stu-id="946aa-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="946aa-109">Значение v.</span><span class="sxs-lookup"><span data-stu-id="946aa-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="946aa-110">*\_Измените*</span><span class="sxs-lookup"><span data-stu-id="946aa-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="946aa-111">Значение масштаба.</span><span class="sxs-lookup"><span data-stu-id="946aa-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="946aa-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="946aa-112">Return value</span></span>

<span data-ttu-id="946aa-113">Преобразованное значение int.</span><span class="sxs-lookup"><span data-stu-id="946aa-113">The converted int value.</span></span>

## <a name="requirements"></a><span data-ttu-id="946aa-114">Требования</span><span class="sxs-lookup"><span data-stu-id="946aa-114">Requirements</span></span>



| <span data-ttu-id="946aa-115">Требование</span><span class="sxs-lookup"><span data-stu-id="946aa-115">Requirement</span></span> | <span data-ttu-id="946aa-116">Значение</span><span class="sxs-lookup"><span data-stu-id="946aa-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946aa-117">Header</span><span class="sxs-lookup"><span data-stu-id="946aa-117">Header</span></span><br/> | <dl> <span data-ttu-id="946aa-118"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="946aa-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="946aa-119">См. также</span><span class="sxs-lookup"><span data-stu-id="946aa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946aa-120">Функции</span><span class="sxs-lookup"><span data-stu-id="946aa-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="946aa-121">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="946aa-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





