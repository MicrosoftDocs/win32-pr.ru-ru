---
description: Включает или отключает оптимизацию ЦП.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: Функция D3DXCpuOptimizations (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821292"
---
# <a name="d3dxcpuoptimizations-function"></a><span data-ttu-id="d2f21-103">Функция D3DXCpuOptimizations</span><span class="sxs-lookup"><span data-stu-id="d2f21-103">D3DXCpuOptimizations function</span></span>

<span data-ttu-id="d2f21-104">Включает или отключает оптимизацию ЦП.</span><span class="sxs-lookup"><span data-stu-id="d2f21-104">Enables or disables CPU optimizations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f21-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2f21-105">Syntax</span></span>


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="d2f21-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2f21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f21-107">*Включить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2f21-107">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f21-108">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f21-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2f21-109">**Значение true** , чтобы включить оптимизацию ЦП; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="d2f21-109">**TRUE** to enable CPU optimizations; otherwise **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f21-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2f21-110">Return value</span></span>

<span data-ttu-id="d2f21-111">Тип: **[ **\_ \_ Оптимизация ЦП D3DX**](d3dx-cpu-optimization.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f21-111">Type: **[**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)**</span></span>

<span data-ttu-id="d2f21-112">Возвращает тип обнаруженного ЦП, для которого существуют оптимизации (см. раздел [**\_ \_ Оптимизация ЦП D3DX**](d3dx-cpu-optimization.md)).</span><span class="sxs-lookup"><span data-stu-id="d2f21-112">Returns the type of CPU detected, and for which optimizations exist (see [**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f21-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d2f21-113">Requirements</span></span>



| <span data-ttu-id="d2f21-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d2f21-114">Requirement</span></span> | <span data-ttu-id="d2f21-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d2f21-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f21-116">Header</span><span class="sxs-lookup"><span data-stu-id="d2f21-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d2f21-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f21-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d2f21-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2f21-118">Library</span></span><br/> | <dl> <span data-ttu-id="d2f21-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2f21-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2f21-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2f21-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f21-121">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d2f21-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
