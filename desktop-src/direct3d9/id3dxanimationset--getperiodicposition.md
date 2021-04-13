---
description: Возвращает значение времени в локальном интервале в наборе анимации.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'Метод ID3DXAnimationSet:: Жетпериодикпоситион (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355933"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a><span data-ttu-id="6a43e-103">Метод ID3DXAnimationSet:: Жетпериодикпоситион</span><span class="sxs-lookup"><span data-stu-id="6a43e-103">ID3DXAnimationSet::GetPeriodicPosition method</span></span>

<span data-ttu-id="6a43e-104">Возвращает значение времени в локальном интервале в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="6a43e-104">Returns time position in the local timeframe of an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a43e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a43e-105">Syntax</span></span>


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="6a43e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a43e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a43e-107">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6a43e-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a43e-108">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a43e-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a43e-109">Местное время набора анимации.</span><span class="sxs-lookup"><span data-stu-id="6a43e-109">Local time of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a43e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a43e-110">Return value</span></span>

<span data-ttu-id="6a43e-111">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a43e-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a43e-112">Временной интервал, измеряемый в промежутке времени набора анимации.</span><span class="sxs-lookup"><span data-stu-id="6a43e-112">Time position as measured in the timeframe of the animation set.</span></span> <span data-ttu-id="6a43e-113">Это значение будет ограничено периодом набора анимации.</span><span class="sxs-lookup"><span data-stu-id="6a43e-113">This value will be bounded by the period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a43e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a43e-114">Remarks</span></span>

<span data-ttu-id="6a43e-115">Значение времени, возвращаемое этим методом, можно использовать в качестве параметра Периодикпоситион [**ID3DXAnimationSet:: жетсрт**](id3dxanimationset--getsrt.md).</span><span class="sxs-lookup"><span data-stu-id="6a43e-115">The time position returned by this method can be used as the PeriodicPosition parameter of [**ID3DXAnimationSet::GetSRT**](id3dxanimationset--getsrt.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a43e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6a43e-116">Requirements</span></span>



| <span data-ttu-id="6a43e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6a43e-117">Requirement</span></span> | <span data-ttu-id="6a43e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6a43e-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a43e-119">Header</span><span class="sxs-lookup"><span data-stu-id="6a43e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6a43e-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a43e-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6a43e-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6a43e-121">Library</span></span><br/> | <dl> <span data-ttu-id="6a43e-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a43e-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a43e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a43e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a43e-124">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="6a43e-124">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
