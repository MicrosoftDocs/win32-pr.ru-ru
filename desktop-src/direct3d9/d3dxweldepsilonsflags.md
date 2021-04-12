---
description: Параметры для Велдинг вершин.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Перечисление D3DXWELDEPSILONSFLAGS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355040"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a><span data-ttu-id="9ed43-103">Перечисление D3DXWELDEPSILONSFLAGS</span><span class="sxs-lookup"><span data-stu-id="9ed43-103">D3DXWELDEPSILONSFLAGS enumeration</span></span>

<span data-ttu-id="9ed43-104">Параметры для Велдинг вершин.</span><span class="sxs-lookup"><span data-stu-id="9ed43-104">Options for welding together vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed43-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ed43-105">Syntax</span></span>


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a><span data-ttu-id="9ed43-106">Константы</span><span class="sxs-lookup"><span data-stu-id="9ed43-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9ed43-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ велдалл**</span><span class="sxs-lookup"><span data-stu-id="9ed43-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS\_WELDALL**</span></span>
</dt> <dd>

<span data-ttu-id="9ed43-108">Расшва все вершины, расположенные в одном месте.</span><span class="sxs-lookup"><span data-stu-id="9ed43-108">Weld together all vertices that are at the same location.</span></span> <span data-ttu-id="9ed43-109">Использование этого флага позволяет избежать сравнения Эпсилон между компонентами вершины.</span><span class="sxs-lookup"><span data-stu-id="9ed43-109">Using this flag avoids an epsilon comparison between vertex components.</span></span>

</dd> <dt>

<span data-ttu-id="9ed43-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ велдпартиалматчес**</span><span class="sxs-lookup"><span data-stu-id="9ed43-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS\_WELDPARTIALMATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="9ed43-111">Если данный компонент вершины находится в пределах Эпсилон, измените частично совпадающие вершины так, чтобы оба компонента совпадали.</span><span class="sxs-lookup"><span data-stu-id="9ed43-111">If a given vertex component is within epsilon, modify partially matched vertices so that both components are identical.</span></span> <span data-ttu-id="9ed43-112">Если все компоненты равны, удалите один из вершин.</span><span class="sxs-lookup"><span data-stu-id="9ed43-112">If all components are equal, remove one of the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="9ed43-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ донотремовевертицес**</span><span class="sxs-lookup"><span data-stu-id="9ed43-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS\_DONOTREMOVEVERTICES**</span></span>
</dt> <dd>

<span data-ttu-id="9ed43-114">Указывает, что монтажный шов должен разрешать только изменения в вершинах и не удалять их.</span><span class="sxs-lookup"><span data-stu-id="9ed43-114">Instructs the weld to allow only modifications to vertices and not removal.</span></span> <span data-ttu-id="9ed43-115">Этот флаг допустим, только если задан параметр D3DXWELDEPSILONS \_ велдпартиалматчес.</span><span class="sxs-lookup"><span data-stu-id="9ed43-115">This flag is valid only if D3DXWELDEPSILONS\_WELDPARTIALMATCHES is set.</span></span> <span data-ttu-id="9ed43-116">Полезно изменить вершины, чтобы они были равны, но не разрешать удаление вершин.</span><span class="sxs-lookup"><span data-stu-id="9ed43-116">It is useful to modify vertices to be equal, but not to allow vertices to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="9ed43-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ донотсплит**</span><span class="sxs-lookup"><span data-stu-id="9ed43-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="9ed43-118">Указывает, что расшов не следует разбивать вершины, наявляющиеся в отдельных группах атрибутов.</span><span class="sxs-lookup"><span data-stu-id="9ed43-118">Instructs the weld not to split vertices that are in separate attribute groups.</span></span> <span data-ttu-id="9ed43-119">Если метод [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) вызывается с \_ флагом D3DXMESHOPT аттрсорт, то \_ также будет установлен флаг D3DXMESHOPT донотсплит.</span><span class="sxs-lookup"><span data-stu-id="9ed43-119">When the [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) method is called with the D3DXMESHOPT\_ATTRSORT flag, then the D3DXMESHOPT\_DONOTSPLIT flag will also be set.</span></span> <span data-ttu-id="9ed43-120">Установка этого флага может замедлить обработку вершин программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="9ed43-120">Setting this flag can slow down software vertex processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ed43-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9ed43-121">Requirements</span></span>



| <span data-ttu-id="9ed43-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9ed43-122">Requirement</span></span> | <span data-ttu-id="9ed43-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9ed43-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed43-124">Header</span><span class="sxs-lookup"><span data-stu-id="9ed43-124">Header</span></span><br/> | <dl> <span data-ttu-id="9ed43-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ed43-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed43-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ed43-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed43-127">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="9ed43-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="9ed43-128">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="9ed43-128">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 




