---
description: Тип функции, используемый функциями заливки текстур.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8c9d9ef610ee10faa069841a05f43c17b0885c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262337"
---
# <a name="lpd3dxfill2d"></a><span data-ttu-id="3521a-103">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="3521a-103">LPD3DXFILL2D</span></span>

<span data-ttu-id="3521a-104">Тип функции, используемый функциями заливки текстур.</span><span class="sxs-lookup"><span data-stu-id="3521a-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3521a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3521a-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="3521a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3521a-106">Parameters</span></span>

<span data-ttu-id="3521a-107">Тоска — указатель на вектор, который функция использует для возврата результата.</span><span class="sxs-lookup"><span data-stu-id="3521a-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="3521a-108">X, Y, Z и W будут сопоставлены с R, G, B и A соответственно.</span><span class="sxs-lookup"><span data-stu-id="3521a-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="3521a-109">Птекскурд — указатель на вектор, содержащий координаты шаг текселя, который в настоящее время вычисляется.</span><span class="sxs-lookup"><span data-stu-id="3521a-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="3521a-110">Компоненты координат текстуры для текстуры и текстуры тома находятся в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="3521a-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="3521a-111">Компоненты координат текстуры для текстур Куба находятся в диапазоне от-1 до 1.</span><span class="sxs-lookup"><span data-stu-id="3521a-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="3521a-112">Птекселсизе — указатель на вектор, содержащий измерения текущего шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="3521a-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="3521a-113">pData — указатель на данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="3521a-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="3521a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3521a-114">Return Value</span></span>

<span data-ttu-id="3521a-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="3521a-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3521a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3521a-116">Remarks</span></span>

<span data-ttu-id="3521a-117">Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3521a-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="3521a-118">В противном случае могут возникать переполняется стек.</span><span class="sxs-lookup"><span data-stu-id="3521a-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="3521a-119">Header</span><span class="sxs-lookup"><span data-stu-id="3521a-119">Header</span></span>                   | <span data-ttu-id="3521a-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="3521a-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="3521a-121">Библиотека импорта</span><span class="sxs-lookup"><span data-stu-id="3521a-121">Import Library</span></span>           | <span data-ttu-id="3521a-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="3521a-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="3521a-123">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="3521a-123">Minimum Operating System</span></span> | <span data-ttu-id="3521a-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3521a-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3521a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3521a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3521a-126">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="3521a-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="3521a-127">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="3521a-127">LPD3DXFILL3D</span></span>](lpd3dxfill3d.md)
</dt> </dl>

 

 
