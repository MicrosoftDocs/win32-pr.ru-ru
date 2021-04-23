---
title: консуместруктуредбуффер
description: Входной буфер, который отображается в виде потока, который шейдер может извлекать из значений. Только структурированные буферы могут принимать типы T, являющиеся структурами.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- Консуместруктуредбуффер HLSL
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997166"
---
# <a name="consumestructuredbuffer"></a><span data-ttu-id="e17c0-105">консуместруктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="e17c0-105">ConsumeStructuredBuffer</span></span>

<span data-ttu-id="e17c0-106">Входной буфер, который отображается в виде потока, который шейдер может извлекать из значений.</span><span class="sxs-lookup"><span data-stu-id="e17c0-106">An input buffer that appears as a stream the shader may pull values from.</span></span> <span data-ttu-id="e17c0-107">Только структурированные буферы могут принимать типы T, являющиеся структурами.</span><span class="sxs-lookup"><span data-stu-id="e17c0-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="e17c0-108">Метод</span><span class="sxs-lookup"><span data-stu-id="e17c0-108">Method</span></span>                                                                    | <span data-ttu-id="e17c0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e17c0-109">Description</span></span>                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="e17c0-110">**Использование**</span><span class="sxs-lookup"><span data-stu-id="e17c0-110">**Consume**</span></span>](sm5-object-consumestructuredbuffer-consume.md)             | <span data-ttu-id="e17c0-111">Удаляет значение из конца буфера.</span><span class="sxs-lookup"><span data-stu-id="e17c0-111">Removes a value from the end of the buffer.</span></span> |
| [<span data-ttu-id="e17c0-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="e17c0-112">**GetDimensions**</span></span>](sm5-object-consumestructuredbuffer-getdimensions.md) | <span data-ttu-id="e17c0-113">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e17c0-113">Gets the resource dimensions.</span></span>               |



 

<span data-ttu-id="e17c0-114">Формат UAV, привязанный к этому ресурсу, должен быть создан с \_ \_ неизвестным форматом DXGI.</span><span class="sxs-lookup"><span data-stu-id="e17c0-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="e17c0-115">UAV, привязанный к этому ресурсу, должен быть создан с [**\_ \_ \_ \_ добавлением флага D3D11 buffer UAV**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="e17c0-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="e17c0-116">Дополнительные сведения об использовании структурированных буферов см. в обоих разделах: [Добавление и использование буфера](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) и [структурированного буфера](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="e17c0-116">For more info about consume structured buffers, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="e17c0-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e17c0-117">Minimum Shader Model</span></span>

<span data-ttu-id="e17c0-118">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e17c0-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="e17c0-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e17c0-119">Shader Model</span></span>                                                                | <span data-ttu-id="e17c0-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e17c0-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e17c0-121">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="e17c0-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e17c0-122">да</span><span class="sxs-lookup"><span data-stu-id="e17c0-122">yes</span></span>       |



 

<span data-ttu-id="e17c0-123">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e17c0-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e17c0-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="e17c0-124">Vertex</span></span> | <span data-ttu-id="e17c0-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e17c0-125">Hull</span></span> | <span data-ttu-id="e17c0-126">Домен</span><span class="sxs-lookup"><span data-stu-id="e17c0-126">Domain</span></span> | <span data-ttu-id="e17c0-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e17c0-127">Geometry</span></span> | <span data-ttu-id="e17c0-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e17c0-128">Pixel</span></span> | <span data-ttu-id="e17c0-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e17c0-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e17c0-130">x</span><span class="sxs-lookup"><span data-stu-id="e17c0-130">x</span></span>     | <span data-ttu-id="e17c0-131">x</span><span class="sxs-lookup"><span data-stu-id="e17c0-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e17c0-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e17c0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e17c0-133">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="e17c0-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 