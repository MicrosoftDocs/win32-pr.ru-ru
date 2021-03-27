---
title: Функция D3DX_IsNan
description: Определяет, является ли значение NaN (не числом).
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- Функция D3DX_IsNan HLSL
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aac82ebfb145bc11aac8d4ab509a4260767a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000494"
---
# <a name="d3dx_isnan-function"></a><span data-ttu-id="a8a97-104">D3DX \_ IsNaN, функция</span><span class="sxs-lookup"><span data-stu-id="a8a97-104">D3DX\_IsNan function</span></span>

<span data-ttu-id="a8a97-105">Определяет, является ли значение NaN (не числом).</span><span class="sxs-lookup"><span data-stu-id="a8a97-105">Determines if the value is a NaN (Not a Number).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8a97-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8a97-106">Syntax</span></span>

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="a8a97-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8a97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a97-108">*\_3,3*</span><span class="sxs-lookup"><span data-stu-id="a8a97-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="a8a97-109">Указанное значение.</span><span class="sxs-lookup"><span data-stu-id="a8a97-109">The specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a97-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8a97-110">Return value</span></span>

<span data-ttu-id="a8a97-111">значение true, если значение NaN; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="a8a97-111">true if a NaN; otherwise false.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8a97-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a8a97-112">Requirements</span></span>



| <span data-ttu-id="a8a97-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a8a97-113">Requirement</span></span> | <span data-ttu-id="a8a97-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a8a97-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a97-115">Header</span><span class="sxs-lookup"><span data-stu-id="a8a97-115">Header</span></span><br/> | <dl> <span data-ttu-id="a8a97-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="a8a97-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8a97-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a8a97-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a97-118">Функции</span><span class="sxs-lookup"><span data-stu-id="a8a97-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="a8a97-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="a8a97-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





