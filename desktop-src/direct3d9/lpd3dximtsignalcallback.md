---
description: Прототип функции, используемый D3DXComputeIMTFromSignal для описания определяемого пользователем сигнала в u, v пространстве входной сетки. Функция вычисляет процедурный сигнал Усигналдименсион измерения в указанной координате u, v.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342839"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="fd934-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="fd934-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="fd934-105">Прототип функции, используемый [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) для описания определяемого пользователем сигнала в u, v пространстве входной сетки.</span><span class="sxs-lookup"><span data-stu-id="fd934-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="fd934-106">Функция вычисляет процедурный сигнал Усигналдименсион измерения в указанной координате u, v.</span><span class="sxs-lookup"><span data-stu-id="fd934-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd934-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd934-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="fd934-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd934-108">Parameters</span></span>

<span data-ttu-id="fd934-109">\[в \] UV — указатель на вектор, содержащий координату текстуры вершины.</span><span class="sxs-lookup"><span data-stu-id="fd934-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="fd934-110">\[в \] упримитивеид — индекс входного треугольника в сетке, для которого должен быть вычислен сигнал.</span><span class="sxs-lookup"><span data-stu-id="fd934-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="fd934-111">\[в \] усигналдименсион — количество элементов типа float для хранения в массиве данных сигнала (пфсигналаут).</span><span class="sxs-lookup"><span data-stu-id="fd934-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="fd934-112">\[в \] пусердата — указатель Пусердата, переданный в [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span><span class="sxs-lookup"><span data-stu-id="fd934-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="fd934-113">\[out \] пфсигналаут — массив float, который содержит данные сигнала.</span><span class="sxs-lookup"><span data-stu-id="fd934-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd934-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd934-114">Return Value</span></span>

<span data-ttu-id="fd934-115">Эта функция должна быть реализована для возврата значения S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fd934-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd934-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="fd934-116">Remarks</span></span>

<span data-ttu-id="fd934-117">Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fd934-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="fd934-118">В противном случае могут возникать переполняется стек.</span><span class="sxs-lookup"><span data-stu-id="fd934-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="fd934-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fd934-119">Requirement</span></span>               | <span data-ttu-id="fd934-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fd934-120">Value</span></span>            |
|----------------|-------------|
| <span data-ttu-id="fd934-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fd934-121">Header</span></span>         | <span data-ttu-id="fd934-122">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="fd934-122">d3dx9mesh.h</span></span> |
| <span data-ttu-id="fd934-123">Библиотека импорта</span><span class="sxs-lookup"><span data-stu-id="fd934-123">Import Library</span></span> | <span data-ttu-id="fd934-124">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="fd934-124">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="fd934-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fd934-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd934-126">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="fd934-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
