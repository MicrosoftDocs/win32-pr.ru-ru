---
title: битеаддрессбуффер
description: битеаддрессбуффер
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- Битеаддрессбуффер HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984073"
---
# <a name="byteaddressbuffer"></a><span data-ttu-id="f3639-104">битеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="f3639-104">ByteAddressBuffer</span></span>

<span data-ttu-id="f3639-105">Буфер только для чтения, индексируемый в байтах.</span><span class="sxs-lookup"><span data-stu-id="f3639-105">A read-only buffer that is indexed in bytes.</span></span>



| <span data-ttu-id="f3639-106">Метод</span><span class="sxs-lookup"><span data-stu-id="f3639-106">Method</span></span>                                                              | <span data-ttu-id="f3639-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f3639-107">Description</span></span>                   |
|---------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="f3639-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="f3639-108">**GetDimensions**</span></span>](sm5-object-byteaddressbuffer-getdimensions.md) | <span data-ttu-id="f3639-109">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3639-109">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="f3639-110">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="f3639-110">**Load**</span></span>](byteaddressbuffer-load.md)                              | <span data-ttu-id="f3639-111">Возвращает одно значение.</span><span class="sxs-lookup"><span data-stu-id="f3639-111">Gets one value.</span></span>               |
| [<span data-ttu-id="f3639-112">**Load2**</span><span class="sxs-lookup"><span data-stu-id="f3639-112">**Load2**</span></span>](byteaddressbuffer-load2.md)                            | <span data-ttu-id="f3639-113">Возвращает два значения.</span><span class="sxs-lookup"><span data-stu-id="f3639-113">Gets two values.</span></span>              |
| [<span data-ttu-id="f3639-114">**Load3**</span><span class="sxs-lookup"><span data-stu-id="f3639-114">**Load3**</span></span>](byteaddressbuffer-load3.md)                            | <span data-ttu-id="f3639-115">Возвращает три значения.</span><span class="sxs-lookup"><span data-stu-id="f3639-115">Gets three values.</span></span>            |
| [<span data-ttu-id="f3639-116">**Load4**</span><span class="sxs-lookup"><span data-stu-id="f3639-116">**Load4**</span></span>](byteaddressbuffer-load4.md)                            | <span data-ttu-id="f3639-117">Возвращает четыре значения.</span><span class="sxs-lookup"><span data-stu-id="f3639-117">Gets four values.</span></span>             |



 

<span data-ttu-id="f3639-118">Тип объекта **битеаддрессбуффер** можно использовать при работе с необработанными буферами.</span><span class="sxs-lookup"><span data-stu-id="f3639-118">You can use the **ByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="f3639-119">Дополнительные сведения об исходном просмотре буферов см. в разделе [необработанные представления буферов](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="f3639-119">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="f3639-120">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f3639-120">Minimum Shader Model</span></span>

<span data-ttu-id="f3639-121">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f3639-121">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="f3639-122">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f3639-122">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="f3639-123">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f3639-123">Supported</span></span> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f3639-124">[Модель](d3d11-graphics-reference-sm5.md) шейдера модели построителя текстуры 5 и более поздних моделей [построителя текстуры 4](dx-graphics-hlsl-sm4.md) (доступна через API Direct3D 11 с использованием уровня компонентов 10,0 или 10,1 ([**\_ \_ уровень компонента D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) на устройствах, поддерживающих шейдеры вычислений.</span><span class="sxs-lookup"><span data-stu-id="f3639-124">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="f3639-125">Дополнительные сведения о поддержке COMPUTE Shader на оборудовании нижнего уровня см. в разделе Вычисление шейдеров на несущем [оборудовании](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).</span><span class="sxs-lookup"><span data-stu-id="f3639-125">For more info about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="f3639-126">да</span><span class="sxs-lookup"><span data-stu-id="f3639-126">yes</span></span>       |



 

<span data-ttu-id="f3639-127">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="f3639-127">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f3639-128">Вершина</span><span class="sxs-lookup"><span data-stu-id="f3639-128">Vertex</span></span> | <span data-ttu-id="f3639-129">Поверхности</span><span class="sxs-lookup"><span data-stu-id="f3639-129">Hull</span></span> | <span data-ttu-id="f3639-130">Домен</span><span class="sxs-lookup"><span data-stu-id="f3639-130">Domain</span></span> | <span data-ttu-id="f3639-131">Геометрия</span><span class="sxs-lookup"><span data-stu-id="f3639-131">Geometry</span></span> | <span data-ttu-id="f3639-132">Пиксель</span><span class="sxs-lookup"><span data-stu-id="f3639-132">Pixel</span></span> | <span data-ttu-id="f3639-133">Вычисления</span><span class="sxs-lookup"><span data-stu-id="f3639-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f3639-134">x</span><span class="sxs-lookup"><span data-stu-id="f3639-134">x</span></span>      | <span data-ttu-id="f3639-135">x</span><span class="sxs-lookup"><span data-stu-id="f3639-135">x</span></span>    | <span data-ttu-id="f3639-136">x</span><span class="sxs-lookup"><span data-stu-id="f3639-136">x</span></span>      | <span data-ttu-id="f3639-137">x</span><span class="sxs-lookup"><span data-stu-id="f3639-137">x</span></span>        | <span data-ttu-id="f3639-138">x</span><span class="sxs-lookup"><span data-stu-id="f3639-138">x</span></span>     | <span data-ttu-id="f3639-139">x</span><span class="sxs-lookup"><span data-stu-id="f3639-139">x</span></span>       |



 

<span data-ttu-id="f3639-140">Дополнительные сведения о буфере адресов в байтах см. в разделе [тип ресурса с адресом в байтах](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="f3639-140">For more info about a byte address buffer, see the [byte addressable resource type](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

<span data-ttu-id="f3639-141">Шейдер Model 5 также реализует [буфер байтового адреса для чтения и записи](sm5-object-rwbyteaddressbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f3639-141">Shader Model 5 also implements a [read-write byte address buffer](sm5-object-rwbyteaddressbuffer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f3639-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3639-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3639-143">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="f3639-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

