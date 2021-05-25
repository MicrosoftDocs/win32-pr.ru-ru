---
description: LPD3DXFILL3D — тип функции, используемый функциями заливки текстур.
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed5845f04486a6ac9cf1c984178fb0ed98447a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342769"
---
# <a name="lpd3dxfill3d"></a><span data-ttu-id="1775c-103">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="1775c-103">LPD3DXFILL3D</span></span>

<span data-ttu-id="1775c-104">Тип функции, используемый функциями заливки текстур.</span><span class="sxs-lookup"><span data-stu-id="1775c-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="1775c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1775c-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="1775c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1775c-106">Parameters</span></span>

<span data-ttu-id="1775c-107">Тоска — указатель на вектор, который функция использует для возврата результата.</span><span class="sxs-lookup"><span data-stu-id="1775c-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="1775c-108">X, Y, Z и W будут сопоставлены с R, G, B и A соответственно.</span><span class="sxs-lookup"><span data-stu-id="1775c-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="1775c-109">Птекскурд — указатель на вектор, содержащий координаты шаг текселя, который в настоящее время вычисляется.</span><span class="sxs-lookup"><span data-stu-id="1775c-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="1775c-110">Компоненты координат текстуры для текстуры и текстуры тома находятся в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="1775c-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="1775c-111">Компоненты координат текстуры для текстур Куба находятся в диапазоне от-1 до 1.</span><span class="sxs-lookup"><span data-stu-id="1775c-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="1775c-112">Птекселсизе — указатель на вектор, содержащий измерения текущего шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="1775c-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="1775c-113">pData — указатель на данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="1775c-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="1775c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1775c-114">Return Value</span></span>

<span data-ttu-id="1775c-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="1775c-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1775c-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="1775c-116">Remarks</span></span>

<span data-ttu-id="1775c-117">Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="1775c-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="1775c-118">В противном случае могут возникать переполняется стек.</span><span class="sxs-lookup"><span data-stu-id="1775c-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="1775c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1775c-119">Requirement</span></span>                         | <span data-ttu-id="1775c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1775c-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="1775c-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1775c-121">Header</span></span>                   | <span data-ttu-id="1775c-122">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="1775c-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="1775c-123">Библиотека импорта</span><span class="sxs-lookup"><span data-stu-id="1775c-123">Import Library</span></span>           | <span data-ttu-id="1775c-124">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="1775c-124">d3dx9.lib</span></span>  |
| <span data-ttu-id="1775c-125">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="1775c-125">Minimum Operating System</span></span> | <span data-ttu-id="1775c-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1775c-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1775c-127">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1775c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1775c-128">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="1775c-128">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="1775c-129">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="1775c-129">LPD3DXFILL2D</span></span>](lpd3dxfill2d.md)
</dt> </dl>

 

 
