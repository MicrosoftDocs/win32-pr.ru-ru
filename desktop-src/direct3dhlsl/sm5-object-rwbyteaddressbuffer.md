---
title: рвбитеаддрессбуффер
description: Буфер чтения/записи, в котором индексы в байтах.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- Рвбитеаддрессбуффер HLSL
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412990"
---
# <a name="rwbyteaddressbuffer"></a><span data-ttu-id="4edf0-104">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="4edf0-104">RWByteAddressBuffer</span></span>

<span data-ttu-id="4edf0-105">Буфер чтения/записи, в котором индексы в байтах.</span><span class="sxs-lookup"><span data-stu-id="4edf0-105">A read/write buffer that indexes in bytes.</span></span>



| <span data-ttu-id="4edf0-106">Метод</span><span class="sxs-lookup"><span data-stu-id="4edf0-106">Method</span></span>                                                                                          | <span data-ttu-id="4edf0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4edf0-107">Description</span></span>                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="4edf0-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="4edf0-108">**GetDimensions**</span></span>](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | <span data-ttu-id="4edf0-109">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4edf0-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="4edf0-110">**интерлоккедадд**</span><span class="sxs-lookup"><span data-stu-id="4edf0-110">**InterlockedAdd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | <span data-ttu-id="4edf0-111">Атомарно добавляет,</span><span class="sxs-lookup"><span data-stu-id="4edf0-111">Adds, atomically.</span></span>                   |
| [<span data-ttu-id="4edf0-112">**интерлоккеданд**</span><span class="sxs-lookup"><span data-stu-id="4edf0-112">**InterlockedAnd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | <span data-ttu-id="4edf0-113">And, атомарно.</span><span class="sxs-lookup"><span data-stu-id="4edf0-113">ANDs, atomically.</span></span>                   |
| [<span data-ttu-id="4edf0-114">**интерлоккедкомпариксчанже**</span><span class="sxs-lookup"><span data-stu-id="4edf0-114">**InterlockedCompareExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | <span data-ttu-id="4edf0-115">Сравнение и обмен атомарно.</span><span class="sxs-lookup"><span data-stu-id="4edf0-115">Compares and exchanges, atomically.</span></span> |
| [<span data-ttu-id="4edf0-116">**интерлоккедкомпаресторе**</span><span class="sxs-lookup"><span data-stu-id="4edf0-116">**InterlockedCompareStore**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | <span data-ttu-id="4edf0-117">Сравнивает и сохраняет атомарно.</span><span class="sxs-lookup"><span data-stu-id="4edf0-117">Compares and stores, atomically.</span></span>    |
| [<span data-ttu-id="4edf0-118">**интерлоккедексчанже**</span><span class="sxs-lookup"><span data-stu-id="4edf0-118">**InterlockedExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | <span data-ttu-id="4edf0-119">Exchange, атомарно.</span><span class="sxs-lookup"><span data-stu-id="4edf0-119">Exchanges, atomically.</span></span>              |
| [<span data-ttu-id="4edf0-120">**интерлоккедмакс**</span><span class="sxs-lookup"><span data-stu-id="4edf0-120">**InterlockedMax**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | <span data-ttu-id="4edf0-121">Выполняет поиск максимального, атомарного.</span><span class="sxs-lookup"><span data-stu-id="4edf0-121">Finds the max, atomically.</span></span>          |
| [<span data-ttu-id="4edf0-122">**интерлоккедмин**</span><span class="sxs-lookup"><span data-stu-id="4edf0-122">**InterlockedMin**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | <span data-ttu-id="4edf0-123">Найти минимальное и атомарное значение.</span><span class="sxs-lookup"><span data-stu-id="4edf0-123">Find the min, atomically.</span></span>           |
| [<span data-ttu-id="4edf0-124">**Взаимоблокировка**</span><span class="sxs-lookup"><span data-stu-id="4edf0-124">**InterlockedOr**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | <span data-ttu-id="4edf0-125">OR, атомарно.</span><span class="sxs-lookup"><span data-stu-id="4edf0-125">ORs, atomically.</span></span>                    |
| [<span data-ttu-id="4edf0-126">**интерлоккедксор**</span><span class="sxs-lookup"><span data-stu-id="4edf0-126">**InterlockedXor**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | <span data-ttu-id="4edf0-127">Ксорс, атомарно.</span><span class="sxs-lookup"><span data-stu-id="4edf0-127">XORs, atomically.</span></span>                   |
| [<span data-ttu-id="4edf0-128">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="4edf0-128">**Load**</span></span>](rwbyteaddressbuffer-load.md)                                                        | <span data-ttu-id="4edf0-129">Возвращает одно значение.</span><span class="sxs-lookup"><span data-stu-id="4edf0-129">Gets one value.</span></span>                     |
| [<span data-ttu-id="4edf0-130">**Load2**</span><span class="sxs-lookup"><span data-stu-id="4edf0-130">**Load2**</span></span>](rwbyteaddressbuffer-load2.md)                                                      | <span data-ttu-id="4edf0-131">Возвращает два значения.</span><span class="sxs-lookup"><span data-stu-id="4edf0-131">Gets two values.</span></span>                    |
| [<span data-ttu-id="4edf0-132">**Load3**</span><span class="sxs-lookup"><span data-stu-id="4edf0-132">**Load3**</span></span>](rwbyteaddressbuffer-load3.md)                                                      | <span data-ttu-id="4edf0-133">Возвращает три значения.</span><span class="sxs-lookup"><span data-stu-id="4edf0-133">Gets three values.</span></span>                  |
| [<span data-ttu-id="4edf0-134">**Load4**</span><span class="sxs-lookup"><span data-stu-id="4edf0-134">**Load4**</span></span>](rwbyteaddressbuffer-load4.md)                                                      | <span data-ttu-id="4edf0-135">Возвращает четыре значения.</span><span class="sxs-lookup"><span data-stu-id="4edf0-135">Gets four values.</span></span>                   |
| [<span data-ttu-id="4edf0-136">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="4edf0-136">**Store**</span></span>](sm5-object-rwbyteaddressbuffer-store.md)                                           | <span data-ttu-id="4edf0-137">Задает одно значение.</span><span class="sxs-lookup"><span data-stu-id="4edf0-137">Sets one value.</span></span>                     |
| [<span data-ttu-id="4edf0-138">**Store2**</span><span class="sxs-lookup"><span data-stu-id="4edf0-138">**Store2**</span></span>](sm5-object-rwbyteaddressbuffer-store2.md)                                         | <span data-ttu-id="4edf0-139">Задает два значения.</span><span class="sxs-lookup"><span data-stu-id="4edf0-139">Sets two values.</span></span>                    |
| [<span data-ttu-id="4edf0-140">**Store3**</span><span class="sxs-lookup"><span data-stu-id="4edf0-140">**Store3**</span></span>](sm5-object-rwbyteaddressbuffer-store3.md)                                         | <span data-ttu-id="4edf0-141">Задает три значения.</span><span class="sxs-lookup"><span data-stu-id="4edf0-141">Sets three values.</span></span>                  |
| [<span data-ttu-id="4edf0-142">**Store4**</span><span class="sxs-lookup"><span data-stu-id="4edf0-142">**Store4**</span></span>](sm5-object-rwbyteaddressbuffer-store4.md)                                         | <span data-ttu-id="4edf0-143">Задает четыре значения.</span><span class="sxs-lookup"><span data-stu-id="4edf0-143">Sets four values.</span></span>                   |



 

<span data-ttu-id="4edf0-144">Для объектов Рвбитеаддрессбуффер можно использовать префикс класса хранения **глобалликохерент**.</span><span class="sxs-lookup"><span data-stu-id="4edf0-144">RWByteAddressBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="4edf0-145">Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи.</span><span class="sxs-lookup"><span data-stu-id="4edf0-145">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="4edf0-146">Без этого описателя барьер памяти или синхронизация будут сбрасывать UAV только в пределах текущей группы.</span><span class="sxs-lookup"><span data-stu-id="4edf0-146">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="4edf0-147">Формат UAV, привязанный к этому ресурсу, должен быть создан в формате DXGI \_ \_ R32 без \_ типа.</span><span class="sxs-lookup"><span data-stu-id="4edf0-147">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_R32\_TYPELESS format.</span></span>

<span data-ttu-id="4edf0-148">UAV, привязанный к этому ресурсу, должен быть создан с помощью [**D3D11 \_ buffer \_ UAV \_ флаг \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="4edf0-148">The UAV bound to this resource must have been created with the [**D3D11\_BUFFER\_UAV\_FLAG\_RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="4edf0-149">Тип объекта **рвбитеаддрессбуффер** можно использовать при работе с необработанными буферами.</span><span class="sxs-lookup"><span data-stu-id="4edf0-149">You can use the **RWByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="4edf0-150">Дополнительные сведения об исходном просмотре буферов см. в разделе [необработанные представления буферов](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="4edf0-150">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="4edf0-151">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4edf0-151">Minimum Shader Model</span></span>

<span data-ttu-id="4edf0-152">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4edf0-152">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="4edf0-153">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4edf0-153">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="4edf0-154">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4edf0-154">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4edf0-155">[Модель](d3d11-graphics-reference-sm5.md) шейдера модели построителя текстуры 5 и более поздних моделей [построителя текстуры 4](dx-graphics-hlsl-sm4.md) (доступна через API Direct3D 11 с использованием уровня компонентов 10,0 или 10,1 ([**\_ \_ уровень компонента D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) на устройствах, поддерживающих шейдеры вычислений.</span><span class="sxs-lookup"><span data-stu-id="4edf0-155">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="4edf0-156">Дополнительные сведения о поддержке COMPUTE Shader на оборудовании нижнего уровня см. в разделе Вычисление шейдеров на несущем [оборудовании](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).</span><span class="sxs-lookup"><span data-stu-id="4edf0-156">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="4edf0-157">да</span><span class="sxs-lookup"><span data-stu-id="4edf0-157">yes</span></span>       |



 

<span data-ttu-id="4edf0-158">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="4edf0-158">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4edf0-159">Вершина</span><span class="sxs-lookup"><span data-stu-id="4edf0-159">Vertex</span></span> | <span data-ttu-id="4edf0-160">Поверхности</span><span class="sxs-lookup"><span data-stu-id="4edf0-160">Hull</span></span> | <span data-ttu-id="4edf0-161">Домен</span><span class="sxs-lookup"><span data-stu-id="4edf0-161">Domain</span></span> | <span data-ttu-id="4edf0-162">Геометрия</span><span class="sxs-lookup"><span data-stu-id="4edf0-162">Geometry</span></span> | <span data-ttu-id="4edf0-163">Пиксель</span><span class="sxs-lookup"><span data-stu-id="4edf0-163">Pixel</span></span> | <span data-ttu-id="4edf0-164">Вычисления</span><span class="sxs-lookup"><span data-stu-id="4edf0-164">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4edf0-165">x</span><span class="sxs-lookup"><span data-stu-id="4edf0-165">x</span></span>     | <span data-ttu-id="4edf0-166">x</span><span class="sxs-lookup"><span data-stu-id="4edf0-166">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4edf0-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4edf0-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4edf0-168">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="4edf0-168">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

