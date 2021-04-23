---
title: Жетсамплепоситион (объект текстуры DirectX HLSL)
description: Возвращает расположение указанного образца.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412137"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="84872-103">Жетсамплепоситион (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84872-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="84872-104">Возвращает расположение указанного образца.</span><span class="sxs-lookup"><span data-stu-id="84872-104">Gets the position of the specified sample.</span></span>



|                                        |
|----------------------------------------|
| <span data-ttu-id="84872-105">RET Object. Жетсамплепоситион (int s);</span><span class="sxs-lookup"><span data-stu-id="84872-105">ret Object.GetSamplePosition( int s );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="84872-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84872-106">Parameters</span></span>



| <span data-ttu-id="84872-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="84872-107">Item</span></span>                                                                                           | <span data-ttu-id="84872-108">Описание</span><span class="sxs-lookup"><span data-stu-id="84872-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84872-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Объектами*</span><span class="sxs-lookup"><span data-stu-id="84872-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="84872-110">Тип [объекта текстуры](dx-graphics-hlsl-to-type.md) Texture2DMS или Texture2DMSArray.</span><span class="sxs-lookup"><span data-stu-id="84872-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="84872-111"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="84872-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="84872-112">\[в \] индексе выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="84872-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="84872-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84872-113">Return Value</span></span>

<span data-ttu-id="84872-114">Возвращает позицию образца (x, y) с двумя компонентами в виде вектора с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="84872-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="84872-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="84872-115">Minimum Shader Model</span></span>

<span data-ttu-id="84872-116">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="84872-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="84872-117">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="84872-117">vs\_4\_0</span></span> | <span data-ttu-id="84872-118">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84872-118">vs\_4\_1</span></span>  | <span data-ttu-id="84872-119">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="84872-119">ps\_4\_0</span></span> | <span data-ttu-id="84872-120">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84872-120">ps\_4\_1</span></span>  | <span data-ttu-id="84872-121">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="84872-121">gs\_4\_0</span></span> | <span data-ttu-id="84872-122">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="84872-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="84872-123">x</span><span class="sxs-lookup"><span data-stu-id="84872-123">x</span></span>         |          | <span data-ttu-id="84872-124">x</span><span class="sxs-lookup"><span data-stu-id="84872-124">x</span></span>         |          | <span data-ttu-id="84872-125">x</span><span class="sxs-lookup"><span data-stu-id="84872-125">x</span></span>         |



 

-   <span data-ttu-id="84872-126">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="84872-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="84872-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="84872-127">Remarks</span></span>

<span data-ttu-id="84872-128">Построитель текстуры можно оценить по частоте выборки (запустите построитель текстуры один раз для каждого образца) или с частотой в пикселях (запустите построитель текстуры один раз в пиксель).</span><span class="sxs-lookup"><span data-stu-id="84872-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="84872-129">Присоединение \_ семантики SV SampleIndex к входным шейдером пикселей для вызова построителя текстуры с частотой выборки. Входное значение затем используется в качестве образца индекса при выборке целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="84872-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="84872-130">Вы можете выполнить интерполяцию входных шейдеров пикселей несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="84872-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="84872-131">Для интерполяции в:</span><span class="sxs-lookup"><span data-stu-id="84872-131">To interpolate at:</span></span>

-   <span data-ttu-id="84872-132">В пиксельном центре не следует использовать ни одну семантическую семантику.</span><span class="sxs-lookup"><span data-stu-id="84872-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="84872-133">В качестве примера используйте \_ семантику SV SampleIndex.</span><span class="sxs-lookup"><span data-stu-id="84872-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="84872-134">Центроид расположение, используйте модификатор [ \_ центроид](dx-graphics-hlsl-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="84872-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84872-135">См. также</span><span class="sxs-lookup"><span data-stu-id="84872-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84872-136">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="84872-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





