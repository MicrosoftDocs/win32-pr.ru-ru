---
title: Функция D3DX_SaturateSigned_FLOAT
description: Извлекает значение со знаком, насыщенное заданным значением, из заданного числа с плавающей запятой.
ms.assetid: 2737ea61-5dbf-4451-bb4f-436e6ea95db6
keywords:
- Функция D3DX_SaturateSigned_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_SaturateSigned_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e6ccf5cf941b1abd3577efa5899b8d827e24e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273848"
---
# <a name="d3dx_saturatesigned_float-function"></a><span data-ttu-id="5072b-104">\_Функция D3DX сатуратесигнед \_ float</span><span class="sxs-lookup"><span data-stu-id="5072b-104">D3DX\_SaturateSigned\_FLOAT function</span></span>

<span data-ttu-id="5072b-105">Извлекает значение со знаком, насыщенное заданным значением, из заданного числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="5072b-105">Retrieves a signed saturated value from the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="5072b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5072b-106">Syntax</span></span>

``` syntax
 D3DX_SaturateSigned_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="5072b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5072b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5072b-108">*\_3,3*</span><span class="sxs-lookup"><span data-stu-id="5072b-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="5072b-109">Значение для насыщенности.</span><span class="sxs-lookup"><span data-stu-id="5072b-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5072b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5072b-110">Return value</span></span>

<span data-ttu-id="5072b-111">Насыщенное значение со знаком.</span><span class="sxs-lookup"><span data-stu-id="5072b-111">The signed saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5072b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="5072b-112">Requirements</span></span>



| <span data-ttu-id="5072b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="5072b-113">Requirement</span></span> | <span data-ttu-id="5072b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5072b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5072b-115">Header</span><span class="sxs-lookup"><span data-stu-id="5072b-115">Header</span></span><br/> | <dl> <span data-ttu-id="5072b-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="5072b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5072b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="5072b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5072b-118">Функции</span><span class="sxs-lookup"><span data-stu-id="5072b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5072b-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="5072b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





