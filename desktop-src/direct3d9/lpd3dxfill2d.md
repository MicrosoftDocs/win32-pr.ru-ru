---
description: LPD3DXFILL2D — тип функции, используемый функциями заливки текстур.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c341ccfcbcc566d65e7139813c676e2286e25cf
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342849"
---
# <a name="lpd3dxfill2d"></a><span data-ttu-id="4d6f3-103">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="4d6f3-103">LPD3DXFILL2D</span></span>

<span data-ttu-id="4d6f3-104">Тип функции, используемый функциями заливки текстур.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d6f3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d6f3-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="4d6f3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d6f3-106">Parameters</span></span>

<span data-ttu-id="4d6f3-107">Тоска — указатель на вектор, который функция использует для возврата результата.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="4d6f3-108">X, Y, Z и W будут сопоставлены с R, G, B и A соответственно.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="4d6f3-109">Птекскурд — указатель на вектор, содержащий координаты шаг текселя, который в настоящее время вычисляется.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="4d6f3-110">Компоненты координат текстуры для текстуры и текстуры тома находятся в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="4d6f3-111">Компоненты координат текстуры для текстур Куба находятся в диапазоне от-1 до 1.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="4d6f3-112">Птекселсизе — указатель на вектор, содержащий измерения текущего шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="4d6f3-113">pData — указатель на данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d6f3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d6f3-114">Return Value</span></span>

<span data-ttu-id="4d6f3-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d6f3-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="4d6f3-116">Remarks</span></span>

<span data-ttu-id="4d6f3-117">Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="4d6f3-118">В противном случае могут возникать переполняется стек.</span><span class="sxs-lookup"><span data-stu-id="4d6f3-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="4d6f3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4d6f3-119">Requirement</span></span>                         | <span data-ttu-id="4d6f3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4d6f3-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="4d6f3-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4d6f3-121">Header</span></span>                   | <span data-ttu-id="4d6f3-122">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="4d6f3-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="4d6f3-123">Библиотека импорта</span><span class="sxs-lookup"><span data-stu-id="4d6f3-123">Import Library</span></span>           | <span data-ttu-id="4d6f3-124">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="4d6f3-124">d3dx9.lib</span></span>  |
| <span data-ttu-id="4d6f3-125">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="4d6f3-125">Minimum Operating System</span></span> | <span data-ttu-id="4d6f3-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="4d6f3-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4d6f3-127">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4d6f3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d6f3-128">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="4d6f3-128">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="4d6f3-129">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="4d6f3-129">LPD3DXFILL3D</span></span>](lpd3dxfill3d.md)
</dt> </dl>

 

 
