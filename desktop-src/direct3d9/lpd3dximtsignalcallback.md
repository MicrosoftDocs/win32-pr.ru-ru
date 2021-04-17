---
description: Прототип функции, используемый D3DXComputeIMTFromSignal для описания определяемого пользователем сигнала в u, v пространстве входной сетки. Функция вычисляет процедурный сигнал Усигналдименсион измерения в указанной координате u, v.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710561"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="02909-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="02909-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="02909-105">Прототип функции, используемый [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) для описания определяемого пользователем сигнала в u, v пространстве входной сетки.</span><span class="sxs-lookup"><span data-stu-id="02909-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="02909-106">Функция вычисляет процедурный сигнал Усигналдименсион измерения в указанной координате u, v.</span><span class="sxs-lookup"><span data-stu-id="02909-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="02909-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02909-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="02909-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="02909-108">Parameters</span></span>

<span data-ttu-id="02909-109">\[в \] UV — указатель на вектор, содержащий координату текстуры вершины.</span><span class="sxs-lookup"><span data-stu-id="02909-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="02909-110">\[в \] упримитивеид — индекс входного треугольника в сетке, для которого должен быть вычислен сигнал.</span><span class="sxs-lookup"><span data-stu-id="02909-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="02909-111">\[в \] усигналдименсион — количество элементов типа float для хранения в массиве данных сигнала (пфсигналаут).</span><span class="sxs-lookup"><span data-stu-id="02909-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="02909-112">\[в \] пусердата — указатель Пусердата, переданный в [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span><span class="sxs-lookup"><span data-stu-id="02909-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="02909-113">\[out \] пфсигналаут — массив float, который содержит данные сигнала.</span><span class="sxs-lookup"><span data-stu-id="02909-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="02909-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02909-114">Return Value</span></span>

<span data-ttu-id="02909-115">Эта функция должна быть реализована для возврата значения S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="02909-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="02909-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02909-116">Remarks</span></span>

<span data-ttu-id="02909-117">Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="02909-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="02909-118">В противном случае могут возникать переполняется стек.</span><span class="sxs-lookup"><span data-stu-id="02909-118">Otherwise, stack overflows can occur.</span></span>



|                |             |
|----------------|-------------|
| <span data-ttu-id="02909-119">Header</span><span class="sxs-lookup"><span data-stu-id="02909-119">Header</span></span>         | <span data-ttu-id="02909-120">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="02909-120">d3dx9mesh.h</span></span> |
| <span data-ttu-id="02909-121">Библиотека импорта</span><span class="sxs-lookup"><span data-stu-id="02909-121">Import Library</span></span> | <span data-ttu-id="02909-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="02909-122">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="02909-123">См. также</span><span class="sxs-lookup"><span data-stu-id="02909-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02909-124">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="02909-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
