---
description: Подсчитывает количество кадров в поддереве с именами, отличными от NULL.
ms.assetid: bc1cb985-acd1-4ba0-bb3c-3e86fea559da
title: Функция D3DXFrameNumNamedMatrices (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameNumNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c2d535a41d15987df7816cfc23f1bb213b6adc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000362"
---
# <a name="d3dxframenumnamedmatrices-function"></a><span data-ttu-id="ad79f-103">Функция D3DXFrameNumNamedMatrices</span><span class="sxs-lookup"><span data-stu-id="ad79f-103">D3DXFrameNumNamedMatrices function</span></span>

<span data-ttu-id="ad79f-104">Подсчитывает количество кадров в поддереве с именами, отличными от NULL.</span><span class="sxs-lookup"><span data-stu-id="ad79f-104">Counts number of frames in a subtree that have non-null names.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad79f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad79f-105">Syntax</span></span>


```C++
UINT D3DXFrameNumNamedMatrices(
  _In_ const D3DXFRAME *pFrameRoot
);
```



## <a name="parameters"></a><span data-ttu-id="ad79f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad79f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad79f-107">*пфрамерут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad79f-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad79f-108">Тип: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad79f-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="ad79f-109">Указатель на корневой узел поддерева.</span><span class="sxs-lookup"><span data-stu-id="ad79f-109">Pointer to the root node of the subtree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad79f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad79f-110">Return value</span></span>

<span data-ttu-id="ad79f-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad79f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad79f-112">Возвращает число кадров.</span><span class="sxs-lookup"><span data-stu-id="ad79f-112">Returns the frame count.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad79f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ad79f-113">Requirements</span></span>



| <span data-ttu-id="ad79f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ad79f-114">Requirement</span></span> | <span data-ttu-id="ad79f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ad79f-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad79f-116">Header</span><span class="sxs-lookup"><span data-stu-id="ad79f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ad79f-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad79f-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ad79f-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad79f-118">Library</span></span><br/> | <dl> <span data-ttu-id="ad79f-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad79f-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad79f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad79f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad79f-121">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="ad79f-121">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
