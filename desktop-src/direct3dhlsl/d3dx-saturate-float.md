---
title: Функция D3DX_Saturate_FLOAT
description: Извлекает насыщенное значение заданного числа с плавающей запятой.
ms.assetid: 659df450-3535-44eb-b867-89529369f903
keywords:
- Функция D3DX_Saturate_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_Saturate_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3deabf5140d4f3f3bdfc2d6cce52f32385987ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914760"
---
# <a name="d3dx_saturate_float-function"></a><span data-ttu-id="0a633-104">D3DXая \_ насыщенность с \_ плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="0a633-104">D3DX\_Saturate\_FLOAT function</span></span>

<span data-ttu-id="0a633-105">Извлекает насыщенное значение заданного числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0a633-105">Retrieves the saturated value of the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a633-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a633-106">Syntax</span></span>

``` syntax
FLOAT D3DX_Saturate_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="0a633-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a633-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a633-108">*\_3,3*</span><span class="sxs-lookup"><span data-stu-id="0a633-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="0a633-109">Значение для насыщенности.</span><span class="sxs-lookup"><span data-stu-id="0a633-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a633-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a633-110">Return value</span></span>

<span data-ttu-id="0a633-111">Насыщенное значение.</span><span class="sxs-lookup"><span data-stu-id="0a633-111">The saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a633-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0a633-112">Requirements</span></span>



| <span data-ttu-id="0a633-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0a633-113">Requirement</span></span> | <span data-ttu-id="0a633-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0a633-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a633-115">Header</span><span class="sxs-lookup"><span data-stu-id="0a633-115">Header</span></span><br/> | <dl> <span data-ttu-id="0a633-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="0a633-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a633-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0a633-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a633-118">Функции</span><span class="sxs-lookup"><span data-stu-id="0a633-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="0a633-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="0a633-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





