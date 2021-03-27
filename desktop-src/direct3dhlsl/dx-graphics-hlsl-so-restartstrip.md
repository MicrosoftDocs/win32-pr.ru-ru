---
title: Рестартстрип (объект DirectX HLSL Stream-Output)
description: Завершает текущую ленту-примитив и запускает новую. Если текущая полоса не имеет достаточного количества вершин, выдаваемых для заливки примитивной топологии, неполный примитив в конце будет отклонен.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16b31bbd1e2f72ce6b31a0c079f7ec5739aba87a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997079"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="217b2-104">Рестартстрип (объект DirectX HLSL Stream-Output)</span><span class="sxs-lookup"><span data-stu-id="217b2-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="217b2-105">Завершает текущую ленту-примитив и запускает новую.</span><span class="sxs-lookup"><span data-stu-id="217b2-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="217b2-106">Если текущая полоса не имеет достаточного количества вершин, выдаваемых для заливки примитивной топологии, неполный примитив в конце будет отклонен.</span><span class="sxs-lookup"><span data-stu-id="217b2-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>



|                 |
|-----------------|
| <span data-ttu-id="217b2-107">Рестартстрип ();</span><span class="sxs-lookup"><span data-stu-id="217b2-107">RestartStrip();</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="217b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="217b2-108">Parameters</span></span>



| <span data-ttu-id="217b2-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="217b2-109">Item</span></span>                                                                                     | <span data-ttu-id="217b2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="217b2-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="217b2-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span><span class="sxs-lookup"><span data-stu-id="217b2-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="217b2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="217b2-112">Return Value</span></span>

<span data-ttu-id="217b2-113">None</span><span class="sxs-lookup"><span data-stu-id="217b2-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="217b2-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="217b2-114">Remarks</span></span>

<span data-ttu-id="217b2-115">Полосковая вырезка приводит к концу текущей полосы и запуску новой ленты.</span><span class="sxs-lookup"><span data-stu-id="217b2-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="217b2-116">Вырезать чередование можно выполнить, явно вызвав этот метод или выполнив отрисовку до максимального значения индекса (1, которое равно 0xFFFFFFFF для 32-разрядных индексов или 0xFFFF для 16-разрядных индексов).</span><span class="sxs-lookup"><span data-stu-id="217b2-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="217b2-117">Каждый экземпляр элемента с индексированным экземпляром Draw автоматически создает полосковую вырезание.</span><span class="sxs-lookup"><span data-stu-id="217b2-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="217b2-118">Это справедливо, даже если топология не является лентой треугольника.</span><span class="sxs-lookup"><span data-stu-id="217b2-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="217b2-119">Поддержка перезагрузки и 1 "магическое значение" для вырезания доступна только на устройствах [уровня](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 или выше.</span><span class="sxs-lookup"><span data-stu-id="217b2-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="217b2-120">Выходные данные всегда считаются треугольными полосками.</span><span class="sxs-lookup"><span data-stu-id="217b2-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="217b2-121">Чтобы выводить список треугольников, необходимо вызвать Рестартстрип между каждым треугольником.</span><span class="sxs-lookup"><span data-stu-id="217b2-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="217b2-122">Вентиляторы с треугольниками не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="217b2-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="217b2-123">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="217b2-123">Minimum Shader Model</span></span>

<span data-ttu-id="217b2-124">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="217b2-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="217b2-125">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="217b2-125">Shader Model</span></span>                                              | <span data-ttu-id="217b2-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="217b2-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="217b2-127">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="217b2-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="217b2-128">да</span><span class="sxs-lookup"><span data-stu-id="217b2-128">yes</span></span>       |
| [<span data-ttu-id="217b2-129">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="217b2-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="217b2-130">Нет</span><span class="sxs-lookup"><span data-stu-id="217b2-130">no</span></span>        |
| [<span data-ttu-id="217b2-131">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="217b2-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="217b2-132">Нет</span><span class="sxs-lookup"><span data-stu-id="217b2-132">no</span></span>        |
| [<span data-ttu-id="217b2-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="217b2-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="217b2-134">Нет</span><span class="sxs-lookup"><span data-stu-id="217b2-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="217b2-135">См. также</span><span class="sxs-lookup"><span data-stu-id="217b2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="217b2-136">Потоковый выходной объект</span><span class="sxs-lookup"><span data-stu-id="217b2-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

