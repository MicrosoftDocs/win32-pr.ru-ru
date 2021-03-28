---
title: структуредбуффер
description: Буфер только для чтения, который может принимать тип T, являющийся структурой.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- Структуредбуффер HLSL
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997071"
---
# <a name="structuredbuffer"></a><span data-ttu-id="6ca56-104">структуредбуффер</span><span class="sxs-lookup"><span data-stu-id="6ca56-104">StructuredBuffer</span></span>

<span data-ttu-id="6ca56-105">Буфер только для чтения, который может принимать тип T, являющийся структурой.</span><span class="sxs-lookup"><span data-stu-id="6ca56-105">A read-only buffer, which can take a T type that is a structure.</span></span>



| <span data-ttu-id="6ca56-106">Метод</span><span class="sxs-lookup"><span data-stu-id="6ca56-106">Method</span></span>                                                             | <span data-ttu-id="6ca56-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6ca56-107">Description</span></span>                            |
|--------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="6ca56-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="6ca56-108">**GetDimensions**</span></span>](sm5-object-structuredbuffer-getdimensions.md) | <span data-ttu-id="6ca56-109">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ca56-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="6ca56-110">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="6ca56-110">**Load**</span></span>](structuredbuffer-load.md)                              | <span data-ttu-id="6ca56-111">Считывает данные буфера.</span><span class="sxs-lookup"><span data-stu-id="6ca56-111">Reads buffer data.</span></span>                     |
| <span data-ttu-id="6ca56-112">[**Оператор\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="6ca56-112">[**Operator\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="6ca56-113">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6ca56-113">Returns a read-only resource variable.</span></span> |



 

<span data-ttu-id="6ca56-114">Формат UAV, привязанный к этому ресурсу, должен быть создан с \_ \_ неизвестным форматом DXGI.</span><span class="sxs-lookup"><span data-stu-id="6ca56-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="6ca56-115">Дополнительные сведения о [структурированных буферах](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)см. в обзорном материале.</span><span class="sxs-lookup"><span data-stu-id="6ca56-115">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="6ca56-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6ca56-116">Minimum Shader Model</span></span>

<span data-ttu-id="6ca56-117">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="6ca56-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="6ca56-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6ca56-118">Shader Model</span></span>                                                                                                                                                                                                            | <span data-ttu-id="6ca56-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6ca56-119">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6ca56-120">[Модель](d3d11-graphics-reference-sm5.md) шейдера модели построителя текстуры 5 и более поздних моделей шейдер [4](dx-graphics-hlsl-sm4.md) (доступна для вычислений и шейдеров пикселей в Direct3D 11 на некоторых устройствах Direct3D 10).</span><span class="sxs-lookup"><span data-stu-id="6ca56-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available for compute and pixel shaders in Direct3D 11 on some Direct3D 10 devices.)</span></span><br/> | <span data-ttu-id="6ca56-121">да</span><span class="sxs-lookup"><span data-stu-id="6ca56-121">yes</span></span>       |



 

<span data-ttu-id="6ca56-122">Этот объект поддерживается для следующих типов шейдеров.</span><span class="sxs-lookup"><span data-stu-id="6ca56-122">This object is supported for the following types of shaders.</span></span>



| <span data-ttu-id="6ca56-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="6ca56-123">Vertex</span></span> | <span data-ttu-id="6ca56-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="6ca56-124">Hull</span></span> | <span data-ttu-id="6ca56-125">Домен</span><span class="sxs-lookup"><span data-stu-id="6ca56-125">Domain</span></span> | <span data-ttu-id="6ca56-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="6ca56-126">Geometry</span></span> | <span data-ttu-id="6ca56-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="6ca56-127">Pixel</span></span> | <span data-ttu-id="6ca56-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="6ca56-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6ca56-129">x</span><span class="sxs-lookup"><span data-stu-id="6ca56-129">x</span></span>      | <span data-ttu-id="6ca56-130">x</span><span class="sxs-lookup"><span data-stu-id="6ca56-130">x</span></span>    | <span data-ttu-id="6ca56-131">x</span><span class="sxs-lookup"><span data-stu-id="6ca56-131">x</span></span>      | <span data-ttu-id="6ca56-132">x</span><span class="sxs-lookup"><span data-stu-id="6ca56-132">x</span></span>        | <span data-ttu-id="6ca56-133">x</span><span class="sxs-lookup"><span data-stu-id="6ca56-133">x</span></span>     | <span data-ttu-id="6ca56-134">x</span><span class="sxs-lookup"><span data-stu-id="6ca56-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6ca56-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ca56-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca56-136">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="6ca56-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

