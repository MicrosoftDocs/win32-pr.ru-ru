---
description: Находит дочерний фрейм корневого фрейма.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: Функция D3DXFrameFind (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713685"
---
# <a name="d3dxframefind-function"></a><span data-ttu-id="007e2-103">Функция D3DXFrameFind</span><span class="sxs-lookup"><span data-stu-id="007e2-103">D3DXFrameFind function</span></span>

<span data-ttu-id="007e2-104">Находит дочерний фрейм корневого фрейма.</span><span class="sxs-lookup"><span data-stu-id="007e2-104">Finds the child frame of a root frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="007e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="007e2-105">Syntax</span></span>


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a><span data-ttu-id="007e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="007e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="007e2-107">*пфрамерут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="007e2-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="007e2-108">Тип: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="007e2-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="007e2-109">Указатель на корневой фрейм.</span><span class="sxs-lookup"><span data-stu-id="007e2-109">Pointer to the root frame.</span></span> <span data-ttu-id="007e2-110">См. [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="007e2-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="007e2-111">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="007e2-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="007e2-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="007e2-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="007e2-113">Имя дочернего фрейма, который нужно найти.</span><span class="sxs-lookup"><span data-stu-id="007e2-113">Name of the child frame to find.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="007e2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="007e2-114">Return value</span></span>

<span data-ttu-id="007e2-115">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="007e2-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="007e2-116">Возвращает дочерний фрейм, если он найден, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="007e2-116">Returns the child frame if it is found, or **NULL** otherwise.</span></span> <span data-ttu-id="007e2-117">См. [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="007e2-117">See [**D3DXFRAME**](d3dxframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="007e2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="007e2-118">Requirements</span></span>



| <span data-ttu-id="007e2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="007e2-119">Requirement</span></span> | <span data-ttu-id="007e2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="007e2-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="007e2-121">Header</span><span class="sxs-lookup"><span data-stu-id="007e2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="007e2-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="007e2-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="007e2-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="007e2-123">Library</span></span><br/> | <dl> <span data-ttu-id="007e2-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="007e2-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="007e2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="007e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="007e2-126">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="007e2-126">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
