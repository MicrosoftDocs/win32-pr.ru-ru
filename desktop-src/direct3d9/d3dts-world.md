---
description: Определяет матрицу преобразования, заданную как матрица мирового преобразования.
ms.assetid: 2bf7ac8a-43d8-460e-a400-3b33e96441db
title: Макрос D3DTS_WORLD (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLD
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3c8f0ac30230a747fba34d9962791b4b331d647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694122"
---
# <a name="d3dts_world-macro"></a><span data-ttu-id="2f018-103">\_Макрос D3DTS World</span><span class="sxs-lookup"><span data-stu-id="2f018-103">D3DTS\_WORLD macro</span></span>

<span data-ttu-id="2f018-104">Определяет матрицу преобразования, заданную как матрица мирового преобразования.</span><span class="sxs-lookup"><span data-stu-id="2f018-104">Identifies the transformation matrix being set as the world transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f018-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f018-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLD(void);
```



## <a name="parameters"></a><span data-ttu-id="2f018-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f018-106">Parameters</span></span>

<span data-ttu-id="2f018-107">Этот макрос не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2f018-107">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f018-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f018-108">Return value</span></span>

<span data-ttu-id="2f018-109">[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) , эквивалентный [**D3DTS \_ ворлдматрикс (0)**](./d3dts-worldmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="2f018-109">A [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) equivalent to [**D3DTS\_WORLDMATRIX(0)**](./d3dts-worldmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2f018-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f018-110">Remarks</span></span>

<span data-ttu-id="2f018-111">Этот макрос предназначен для упрощения переноса существующих приложений на Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="2f018-111">This macro is provided to facilitate porting existing applications to Direct3D 9.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f018-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2f018-112">Requirements</span></span>



| <span data-ttu-id="2f018-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2f018-113">Requirement</span></span> | <span data-ttu-id="2f018-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2f018-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f018-115">Header</span><span class="sxs-lookup"><span data-stu-id="2f018-115">Header</span></span><br/> | <dl> <span data-ttu-id="2f018-116"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f018-116"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f018-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f018-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f018-118">Макросы</span><span class="sxs-lookup"><span data-stu-id="2f018-118">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="2f018-119">**сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="2f018-119">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="2f018-120">**D3DTS \_ ворлдматрикс**</span><span class="sxs-lookup"><span data-stu-id="2f018-120">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
