---
description: Определяет скалярное произведение двух векторов 4D.
ms.assetid: 565dede8-6cc8-4313-9480-2f252cac94f2
title: Функция D3DXVec4Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0ef075a768fe9b70a38a4bc3d88b094359bd546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424417"
---
# <a name="d3dxvec4dot-function"></a><span data-ttu-id="78141-103">Функция D3DXVec4Dot</span><span class="sxs-lookup"><span data-stu-id="78141-103">D3DXVec4Dot function</span></span>

<span data-ttu-id="78141-104">Определяет скалярное произведение двух векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="78141-104">Determines the dot product of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="78141-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78141-105">Syntax</span></span>


```C++
FLOAT D3DXVec4Dot(
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="78141-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78141-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78141-107">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78141-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78141-108">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="78141-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="78141-109">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="78141-109">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="78141-110">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78141-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78141-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="78141-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="78141-112">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="78141-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78141-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78141-113">Return value</span></span>

<span data-ttu-id="78141-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78141-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78141-115">Скалярное произведение.</span><span class="sxs-lookup"><span data-stu-id="78141-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="78141-116">Требования</span><span class="sxs-lookup"><span data-stu-id="78141-116">Requirements</span></span>



| <span data-ttu-id="78141-117">Требование</span><span class="sxs-lookup"><span data-stu-id="78141-117">Requirement</span></span> | <span data-ttu-id="78141-118">Значение</span><span class="sxs-lookup"><span data-stu-id="78141-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78141-119">Header</span><span class="sxs-lookup"><span data-stu-id="78141-119">Header</span></span><br/>  | <dl> <span data-ttu-id="78141-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="78141-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="78141-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78141-121">Library</span></span><br/> | <dl> <span data-ttu-id="78141-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78141-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78141-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78141-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78141-124">Математические функции</span><span class="sxs-lookup"><span data-stu-id="78141-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="78141-125">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="78141-125">**D3DXVec4Cross**</span></span>](d3dxvec4cross.md)
</dt> </dl>

 

 
