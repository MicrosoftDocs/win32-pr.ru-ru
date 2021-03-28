---
title: рвструктуредбуффер
description: Буфер чтения/записи, который может принимать тип T, являющийся структурой.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- Рвструктуредбуффер HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413142"
---
# <a name="rwstructuredbuffer"></a><span data-ttu-id="f8d07-104">рвструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="f8d07-104">RWStructuredBuffer</span></span>

<span data-ttu-id="f8d07-105">Буфер чтения/записи, который может принимать тип T, являющийся структурой.</span><span class="sxs-lookup"><span data-stu-id="f8d07-105">A read/write buffer that can take a T type that is a structure.</span></span>



| <span data-ttu-id="f8d07-106">Метод</span><span class="sxs-lookup"><span data-stu-id="f8d07-106">Method</span></span>                                                                     | <span data-ttu-id="f8d07-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f8d07-107">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="f8d07-108">**декременткаунтер**</span><span class="sxs-lookup"><span data-stu-id="f8d07-108">**DecrementCounter**</span></span>](sm5-object-rwstructuredbuffer-decrementcounter.md) | <span data-ttu-id="f8d07-109">Уменьшает значение скрытого счетчика объекта.</span><span class="sxs-lookup"><span data-stu-id="f8d07-109">Decrements the object's hidden counter.</span></span> |
| [<span data-ttu-id="f8d07-110">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="f8d07-110">**GetDimensions**</span></span>](sm5-object-rwstructuredbuffer-getdimensions.md)       | <span data-ttu-id="f8d07-111">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8d07-111">Gets the resource dimensions.</span></span>           |
| [<span data-ttu-id="f8d07-112">**инкременткаунтер**</span><span class="sxs-lookup"><span data-stu-id="f8d07-112">**IncrementCounter**</span></span>](sm5-object-rwstructuredbuffer-incrementcounter.md) | <span data-ttu-id="f8d07-113">Увеличивает значение скрытого счетчика объекта.</span><span class="sxs-lookup"><span data-stu-id="f8d07-113">Increments the object's hidden counter.</span></span> |
| [<span data-ttu-id="f8d07-114">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="f8d07-114">**Load**</span></span>](rwstructuredbuffer-load.md)                                    | <span data-ttu-id="f8d07-115">Считывает данные буфера.</span><span class="sxs-lookup"><span data-stu-id="f8d07-115">Reads buffer data.</span></span>                      |
| <span data-ttu-id="f8d07-116">[**Оператор\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="f8d07-116">[**Operator\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span></span>        | <span data-ttu-id="f8d07-117">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="f8d07-117">Returns a resource variable.</span></span>            |



 

<span data-ttu-id="f8d07-118">Переменная ресурса также может быть передана в любую неупорядоченную или блокируемую операцию.</span><span class="sxs-lookup"><span data-stu-id="f8d07-118">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="f8d07-119">Для объектов Рвструктуредбуффер можно использовать префикс класса хранения **глобалликохерент**.</span><span class="sxs-lookup"><span data-stu-id="f8d07-119">RWStructuredBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="f8d07-120">Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи.</span><span class="sxs-lookup"><span data-stu-id="f8d07-120">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="f8d07-121">Без этого описателя барьер памяти или синхронизация будут сбрасывать только UAV в пределах текущей группы.</span><span class="sxs-lookup"><span data-stu-id="f8d07-121">Without this specifier, a memory barrier or sync will only flush a UAV within the current group.</span></span>

<span data-ttu-id="f8d07-122">Формат UAV, привязанный к этому ресурсу, должен быть создан с \_ \_ неизвестным форматом DXGI.</span><span class="sxs-lookup"><span data-stu-id="f8d07-122">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="f8d07-123">Дополнительные сведения о [структурированных буферах](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)см. в обзорном материале.</span><span class="sxs-lookup"><span data-stu-id="f8d07-123">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="f8d07-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f8d07-124">Minimum Shader Model</span></span>

<span data-ttu-id="f8d07-125">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f8d07-125">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="f8d07-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f8d07-126">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="f8d07-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f8d07-127">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f8d07-128">[Модель](d3d11-graphics-reference-sm5.md) шейдера модели построителя текстуры 5 и более поздних моделей [построителя текстуры 4](dx-graphics-hlsl-sm4.md) (доступна через API Direct3D 11 с использованием уровня компонентов 10,0 или 10,1 ([**\_ \_ уровень компонента D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) на устройствах, поддерживающих шейдеры вычислений.</span><span class="sxs-lookup"><span data-stu-id="f8d07-128">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="f8d07-129">Дополнительные сведения о поддержке COMPUTE Shader на оборудовании нижнего уровня см. в разделе Вычисление шейдеров на несущем [оборудовании](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).</span><span class="sxs-lookup"><span data-stu-id="f8d07-129">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="f8d07-130">да</span><span class="sxs-lookup"><span data-stu-id="f8d07-130">yes</span></span>       |



 

<span data-ttu-id="f8d07-131">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="f8d07-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f8d07-132">Вершина</span><span class="sxs-lookup"><span data-stu-id="f8d07-132">Vertex</span></span> | <span data-ttu-id="f8d07-133">Поверхности</span><span class="sxs-lookup"><span data-stu-id="f8d07-133">Hull</span></span> | <span data-ttu-id="f8d07-134">Домен</span><span class="sxs-lookup"><span data-stu-id="f8d07-134">Domain</span></span> | <span data-ttu-id="f8d07-135">Геометрия</span><span class="sxs-lookup"><span data-stu-id="f8d07-135">Geometry</span></span> | <span data-ttu-id="f8d07-136">Пиксель</span><span class="sxs-lookup"><span data-stu-id="f8d07-136">Pixel</span></span> | <span data-ttu-id="f8d07-137">Вычисления</span><span class="sxs-lookup"><span data-stu-id="f8d07-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f8d07-138">x</span><span class="sxs-lookup"><span data-stu-id="f8d07-138">x</span></span>     | <span data-ttu-id="f8d07-139">x</span><span class="sxs-lookup"><span data-stu-id="f8d07-139">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f8d07-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8d07-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8d07-141">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="f8d07-141">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

