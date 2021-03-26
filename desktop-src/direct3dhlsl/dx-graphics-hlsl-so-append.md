---
title: Append (объект DirectX HLSL Stream-Output)
description: Добавление в существующий поток выходных данных с помощью шейдера Geometry-Shader.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97ab88961b22529accb4402fc2bd095ede5275c1
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2019
ms.locfileid: "104335811"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="2a2b7-103">Append (объект DirectX HLSL Stream-Output)</span><span class="sxs-lookup"><span data-stu-id="2a2b7-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="2a2b7-104">Добавление в существующий поток выходных данных с помощью шейдера Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="2a2b7-104">Append geometry-shader-output data to an existing stream.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="2a2b7-105">Append ( *стреамдататипе*);</span><span class="sxs-lookup"><span data-stu-id="2a2b7-105">Append( *StreamDataType*);</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="2a2b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a2b7-106">Parameters</span></span>



| <span data-ttu-id="2a2b7-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="2a2b7-107">Item</span></span>                                                                                                                             | <span data-ttu-id="2a2b7-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2a2b7-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a2b7-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**стреамдататипе**</span><span class="sxs-lookup"><span data-stu-id="2a2b7-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="2a2b7-110">Описание входных данных.</span><span class="sxs-lookup"><span data-stu-id="2a2b7-110">A data input description.</span></span> <span data-ttu-id="2a2b7-111">Это описание должно соответствовать параметру шаблона потока объекта, который называется [DataType](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="2a2b7-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2a2b7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a2b7-112">Return Value</span></span>

<span data-ttu-id="2a2b7-113">None</span><span class="sxs-lookup"><span data-stu-id="2a2b7-113">None</span></span>

## <a name="example"></a><span data-ttu-id="2a2b7-114">Пример</span><span class="sxs-lookup"><span data-stu-id="2a2b7-114">Example</span></span>

<span data-ttu-id="2a2b7-115">В этом фрагменте кода (из [примера CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) показан частичный пример добавления примитивов-треугольников к объекту потокового вывода.</span><span class="sxs-lookup"><span data-stu-id="2a2b7-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="2a2b7-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2a2b7-116">Minimum Shader Model</span></span>

<span data-ttu-id="2a2b7-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="2a2b7-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2a2b7-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2a2b7-118">Shader Model</span></span>                                              | <span data-ttu-id="2a2b7-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2a2b7-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2a2b7-120">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="2a2b7-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2a2b7-121">да</span><span class="sxs-lookup"><span data-stu-id="2a2b7-121">yes</span></span>       |
| [<span data-ttu-id="2a2b7-122">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a2b7-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2a2b7-123">Нет</span><span class="sxs-lookup"><span data-stu-id="2a2b7-123">no</span></span>        |
| [<span data-ttu-id="2a2b7-124">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a2b7-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2a2b7-125">Нет</span><span class="sxs-lookup"><span data-stu-id="2a2b7-125">no</span></span>        |
| [<span data-ttu-id="2a2b7-126">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a2b7-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2a2b7-127">Нет</span><span class="sxs-lookup"><span data-stu-id="2a2b7-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2a2b7-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2a2b7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a2b7-129">Потоковый выходной объект</span><span class="sxs-lookup"><span data-stu-id="2a2b7-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





