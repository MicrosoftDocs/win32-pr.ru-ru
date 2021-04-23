---
description: Инкапсулирует кадр преобразования в иерархии фрейма преобразования.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: Структура D3DXFRAME (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273778"
---
# <a name="d3dxframe-structure"></a><span data-ttu-id="38d32-103">Структура D3DXFRAME</span><span class="sxs-lookup"><span data-stu-id="38d32-103">D3DXFRAME structure</span></span>

<span data-ttu-id="38d32-104">Инкапсулирует кадр преобразования в иерархии фрейма преобразования.</span><span class="sxs-lookup"><span data-stu-id="38d32-104">Encapsulates a transform frame in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d32-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38d32-105">Syntax</span></span>


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a><span data-ttu-id="38d32-106">Члены</span><span class="sxs-lookup"><span data-stu-id="38d32-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="38d32-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="38d32-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="38d32-108">Тип: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="38d32-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="38d32-109">Имя кадра.</span><span class="sxs-lookup"><span data-stu-id="38d32-109">Name of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="38d32-110">**трансформатионматрикс**</span><span class="sxs-lookup"><span data-stu-id="38d32-110">**TransformationMatrix**</span></span>
</dt> <dd>

<span data-ttu-id="38d32-111">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="38d32-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38d32-112">Матрица преобразования.</span><span class="sxs-lookup"><span data-stu-id="38d32-112">Transformation matrix.</span></span>

</dd> <dt>

<span data-ttu-id="38d32-113">**пмешконтаинер**</span><span class="sxs-lookup"><span data-stu-id="38d32-113">**pMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="38d32-114">Тип: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="38d32-114">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

</dd> <dd>

<span data-ttu-id="38d32-115">Указатель на контейнер сетки.</span><span class="sxs-lookup"><span data-stu-id="38d32-115">Pointer to the mesh container.</span></span>

</dd> <dt>

<span data-ttu-id="38d32-116">**пфрамесиблинг**</span><span class="sxs-lookup"><span data-stu-id="38d32-116">**pFrameSibling**</span></span>
</dt> <dd>

<span data-ttu-id="38d32-117">Тип: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="38d32-117">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="38d32-118">Указатель на одноуровневый фрейм.</span><span class="sxs-lookup"><span data-stu-id="38d32-118">Pointer to a sibling frame.</span></span>

</dd> <dt>

<span data-ttu-id="38d32-119">**пфрамефирстчилд**</span><span class="sxs-lookup"><span data-stu-id="38d32-119">**pFrameFirstChild**</span></span>
</dt> <dd>

<span data-ttu-id="38d32-120">Тип: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="38d32-120">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="38d32-121">Указатель на дочерний фрейм.</span><span class="sxs-lookup"><span data-stu-id="38d32-121">Pointer to a child frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38d32-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38d32-122">Remarks</span></span>

<span data-ttu-id="38d32-123">Приложение может быть производным от этой структуры для добавления других данных.</span><span class="sxs-lookup"><span data-stu-id="38d32-123">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="38d32-124">Требования</span><span class="sxs-lookup"><span data-stu-id="38d32-124">Requirements</span></span>



| <span data-ttu-id="38d32-125">Требование</span><span class="sxs-lookup"><span data-stu-id="38d32-125">Requirement</span></span> | <span data-ttu-id="38d32-126">Значение</span><span class="sxs-lookup"><span data-stu-id="38d32-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38d32-127">Header</span><span class="sxs-lookup"><span data-stu-id="38d32-127">Header</span></span><br/> | <dl> <span data-ttu-id="38d32-128"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="38d32-128"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d32-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38d32-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d32-130">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="38d32-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




