---
title: аппендструктуредбуффер
description: Выходной буфер, который отображается в виде потока, к которому может добавляться шейдер. Только структурированные буферы могут принимать типы T, являющиеся структурами.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- Аппендструктуредбуффер HLSL
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792289"
---
# <a name="appendstructuredbuffer"></a><span data-ttu-id="fd2c9-105">аппендструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="fd2c9-105">AppendStructuredBuffer</span></span>

<span data-ttu-id="fd2c9-106">Выходной буфер, который отображается в виде потока, к которому может добавляться шейдер.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-106">Output buffer that appears as a stream the shader may append to.</span></span> <span data-ttu-id="fd2c9-107">Только структурированные буферы могут принимать типы T, являющиеся структурами.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="fd2c9-108">Метод</span><span class="sxs-lookup"><span data-stu-id="fd2c9-108">Method</span></span>                                                                   | <span data-ttu-id="fd2c9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fd2c9-109">Description</span></span>                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="fd2c9-110">**Добавление**</span><span class="sxs-lookup"><span data-stu-id="fd2c9-110">**Append**</span></span>](sm5-object-appendstructuredbuffer-append.md)               | <span data-ttu-id="fd2c9-111">Добавляет значение в конец буфера.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-111">Appends a value to the end of the buffer.</span></span> |
| [<span data-ttu-id="fd2c9-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="fd2c9-112">**GetDimensions**</span></span>](sm5-object-appendstructuredbuffer-getdimensions.md) | <span data-ttu-id="fd2c9-113">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-113">Gets the resource dimensions.</span></span>             |



 

<span data-ttu-id="fd2c9-114">Формат UAV, привязанный к этому ресурсу, должен быть создан с \_ \_ неизвестным форматом DXGI.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="fd2c9-115">UAV, привязанный к этому ресурсу, должен быть создан с [**\_ \_ \_ \_ добавлением флага D3D11 buffer UAV**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="fd2c9-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="fd2c9-116">Дополнительные сведения о добавлении структурированного буфера см. в разделах [Добавление и использование буфера](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) и [структурированный буфер](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="fd2c9-116">For more information about an append structured buffer, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="fd2c9-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fd2c9-117">Minimum Shader Model</span></span>

<span data-ttu-id="fd2c9-118">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fd2c9-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="fd2c9-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fd2c9-119">Shader Model</span></span>                                                                | <span data-ttu-id="fd2c9-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd2c9-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="fd2c9-121">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="fd2c9-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="fd2c9-122">да</span><span class="sxs-lookup"><span data-stu-id="fd2c9-122">yes</span></span>       |



 

<span data-ttu-id="fd2c9-123">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="fd2c9-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fd2c9-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="fd2c9-124">Vertex</span></span> | <span data-ttu-id="fd2c9-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="fd2c9-125">Hull</span></span> | <span data-ttu-id="fd2c9-126">Домен</span><span class="sxs-lookup"><span data-stu-id="fd2c9-126">Domain</span></span> | <span data-ttu-id="fd2c9-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="fd2c9-127">Geometry</span></span> | <span data-ttu-id="fd2c9-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="fd2c9-128">Pixel</span></span> | <span data-ttu-id="fd2c9-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="fd2c9-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="fd2c9-130">x</span><span class="sxs-lookup"><span data-stu-id="fd2c9-130">x</span></span>     | <span data-ttu-id="fd2c9-131">x</span><span class="sxs-lookup"><span data-stu-id="fd2c9-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fd2c9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd2c9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2c9-133">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="fd2c9-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 