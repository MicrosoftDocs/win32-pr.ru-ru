---
description: Задает параметры упрощения для сетки.
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: Перечисление D3DXMESHSIMP (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157179"
---
# <a name="d3dxmeshsimp-enumeration"></a><span data-ttu-id="ae30e-103">Перечисление D3DXMESHSIMP</span><span class="sxs-lookup"><span data-stu-id="ae30e-103">D3DXMESHSIMP enumeration</span></span>

<span data-ttu-id="ae30e-104">Задает параметры упрощения для сетки.</span><span class="sxs-lookup"><span data-stu-id="ae30e-104">Specifies simplification options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae30e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae30e-105">Syntax</span></span>


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a><span data-ttu-id="ae30e-106">Константы</span><span class="sxs-lookup"><span data-stu-id="ae30e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ae30e-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**\_Вершина D3DXMESHSIMP**</span><span class="sxs-lookup"><span data-stu-id="ae30e-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP\_VERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="ae30e-108">Сетка будет упрощена числом вершин, указанным в параметре MinValue.</span><span class="sxs-lookup"><span data-stu-id="ae30e-108">The mesh will be simplified by the number of vertices specified in the MinValue parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ae30e-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP \_ лицо**</span><span class="sxs-lookup"><span data-stu-id="ae30e-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP\_FACE**</span></span>
</dt> <dd>

<span data-ttu-id="ae30e-110">Сетка будет упрощена количеством сторон, указанным в параметре MinValue.</span><span class="sxs-lookup"><span data-stu-id="ae30e-110">The mesh will be simplified by the number of faces specified in the MinValue parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae30e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ae30e-111">Requirements</span></span>



| <span data-ttu-id="ae30e-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ae30e-112">Requirement</span></span> | <span data-ttu-id="ae30e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ae30e-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae30e-114">Header</span><span class="sxs-lookup"><span data-stu-id="ae30e-114">Header</span></span><br/> | <dl> <span data-ttu-id="ae30e-115"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae30e-115"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae30e-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae30e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae30e-117">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="ae30e-117">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="ae30e-118">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="ae30e-118">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 




