---
description: Измеряет скорость попадания в кэш для текстур и индексированных вершин.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: Структура D3DDEVINFO_D3D9CACHEUTILIZATION (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547847"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a><span data-ttu-id="f9ebc-103">\_Структура D3D9CACHEUTILIZATION D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="f9ebc-103">D3DDEVINFO\_D3D9CACHEUTILIZATION structure</span></span>

<span data-ttu-id="f9ebc-104">Измеряет скорость попадания в кэш для текстур и индексированных вершин.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-104">Measure the cache hit rate performance for textures and indexed vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9ebc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9ebc-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a><span data-ttu-id="f9ebc-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f9ebc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9ebc-107">**текстурекачехитрате**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-107">**TextureCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="f9ebc-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f9ebc-109">Коэффициент попадания для поиска текстуры в кэше текстуры.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-109">The hit rate for finding a texture in the texture cache.</span></span> <span data-ttu-id="f9ebc-110">В этом случае предполагается наличие кэша текстуры.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-110">This assumes there is a texture cache.</span></span> <span data-ttu-id="f9ebc-111">Увеличение уровня детализации для использования наиболее подробной текстуры, использование большого количества крупных текстур или создание практически случайного шаблона доступа к текстуре на больших текстурах с помощью пользовательского кода шейдера может значительно повлиять на скорость попаданий в кэш текстуры.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-111">Increasing the level-of-detail bias to use the most detailed texture, using many large textures, or producing a near random texture access pattern on large textures with custom shader code can dramatically affect the texture cache hit rate.</span></span>

</dd> <dt>

<span data-ttu-id="f9ebc-112">**посттрансформвертекскачехитрате**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-112">**PostTransformVertexCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="f9ebc-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f9ebc-114">Коэффициент попадания для поиска преобразованных вершин в кэше вершин.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-114">The hit rate for finding transformed vertices in the vertex cache.</span></span> <span data-ttu-id="f9ebc-115">GPU предназначен для преобразования индексированных вершин и может хранить их в кэше вершин.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-115">The GPU is designed to transform indexed vertices and may store them in a vertex cache.</span></span> <span data-ttu-id="f9ebc-116">Если используются сети, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) или [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) могут повысить эффективность использования кэша вершин.</span><span class="sxs-lookup"><span data-stu-id="f9ebc-116">If you are using meshes, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) or [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) may result in better vertex cache utilization.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9ebc-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9ebc-117">Remarks</span></span>

<span data-ttu-id="f9ebc-118">Эффективный кэш, как правило, приближается к проценту попадания в 90 процентов, а неэффективный кэш, как правило, приближается к проценту попадания в 10 процентов (хотя низкий процент не обязательно является проблемой).</span><span class="sxs-lookup"><span data-stu-id="f9ebc-118">An efficient cache is typically closer to a 90 percent hit rate, and an inefficient cache is typically closer to a 10 percent hit rate (although a low percentage is not necessarily a problem).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ebc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f9ebc-119">Requirements</span></span>



| <span data-ttu-id="f9ebc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f9ebc-120">Requirement</span></span> | <span data-ttu-id="f9ebc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f9ebc-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ebc-122">Header</span><span class="sxs-lookup"><span data-stu-id="f9ebc-122">Header</span></span><br/> | <dl> <span data-ttu-id="f9ebc-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9ebc-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9ebc-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9ebc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ebc-125">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="f9ebc-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="f9ebc-126">**GetData**</span><span class="sxs-lookup"><span data-stu-id="f9ebc-126">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
