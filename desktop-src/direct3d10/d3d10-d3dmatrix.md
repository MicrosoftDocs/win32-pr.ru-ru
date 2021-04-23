---
description: Крупная матрица 4x4 Row.
ms.assetid: 2253f486-7bb6-4966-b3ec-dba47e53e372
title: Структура D3DMATRIX (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1df0d2171e828b14fba87f6587c604146360d0e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355490"
---
# <a name="d3dmatrix-structure"></a><span data-ttu-id="88aba-103">Структура D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="88aba-103">D3DMATRIX structure</span></span>

<span data-ttu-id="88aba-104">Крупная матрица 4x4 Row.</span><span class="sxs-lookup"><span data-stu-id="88aba-104">A 4x4 row-major matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="88aba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88aba-105">Syntax</span></span>


```C++
typedef struct D3DMATRIX {
  float m[4][4];
} D3DMATRIX, *LPD3DMATRIX;
```



## <a name="members"></a><span data-ttu-id="88aba-106">Члены</span><span class="sxs-lookup"><span data-stu-id="88aba-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="88aba-107">**m \[ 4 \] \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="88aba-107">**m\[4\]\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="88aba-108">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="88aba-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="88aba-109">Основная матрица 4x4 Row.</span><span class="sxs-lookup"><span data-stu-id="88aba-109">The 4x4 row-major matrix.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88aba-110">Требования</span><span class="sxs-lookup"><span data-stu-id="88aba-110">Requirements</span></span>



| <span data-ttu-id="88aba-111">Требование</span><span class="sxs-lookup"><span data-stu-id="88aba-111">Requirement</span></span> | <span data-ttu-id="88aba-112">Значение</span><span class="sxs-lookup"><span data-stu-id="88aba-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88aba-113">Header</span><span class="sxs-lookup"><span data-stu-id="88aba-113">Header</span></span><br/> | <dl> <span data-ttu-id="88aba-114"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="88aba-114"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88aba-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88aba-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88aba-116">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="88aba-116">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 




