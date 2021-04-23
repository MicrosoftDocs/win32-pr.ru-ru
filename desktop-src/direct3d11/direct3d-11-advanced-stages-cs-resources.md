---
title: Новые типы ресурсов
description: В Direct3D 11 были добавлены несколько новых типов ресурсов.
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- Буфер байтового адреса (обзор)
- Буфер чтения и записи (обзор)
- Структурированный буфер (обзор)
- Неупорядоченный буфер доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413297"
---
# <a name="new-resource-types"></a><span data-ttu-id="048c0-107">Новые типы ресурсов</span><span class="sxs-lookup"><span data-stu-id="048c0-107">New Resource Types</span></span>

<span data-ttu-id="048c0-108">В Direct3D 11 были добавлены несколько новых типов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="048c0-108">Several new resource types have been added in Direct3D 11.</span></span>

-   [<span data-ttu-id="048c0-109">Буферы чтения и записи и текстуры</span><span class="sxs-lookup"><span data-stu-id="048c0-109">Read/Write Buffers and Textures</span></span>](#readwrite-buffers-and-textures)
-   [<span data-ttu-id="048c0-110">Структурированный буфер</span><span class="sxs-lookup"><span data-stu-id="048c0-110">Structured Buffer</span></span>](#structured-buffer)
-   [<span data-ttu-id="048c0-111">Буфер байтового адреса</span><span class="sxs-lookup"><span data-stu-id="048c0-111">Byte Address Buffer</span></span>](#byte-address-buffer)
-   [<span data-ttu-id="048c0-112">Неупорядоченный буфер или текстура доступа</span><span class="sxs-lookup"><span data-stu-id="048c0-112">Unordered Access Buffer or Texture</span></span>](#unordered-access-buffer-or-texture)
    -   [<span data-ttu-id="048c0-113">Добавление и использование буфера</span><span class="sxs-lookup"><span data-stu-id="048c0-113">Append and Consume Buffer</span></span>](#append-and-consume-buffer)
-   [<span data-ttu-id="048c0-114">См. также</span><span class="sxs-lookup"><span data-stu-id="048c0-114">Related topics</span></span>](#related-topics)

## <a name="readwrite-buffers-and-textures"></a><span data-ttu-id="048c0-115">Буферы чтения и записи и текстуры</span><span class="sxs-lookup"><span data-stu-id="048c0-115">Read/Write Buffers and Textures</span></span>

<span data-ttu-id="048c0-116">Ресурсы Shader Model 4 доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="048c0-116">Shader model 4 resources are read only.</span></span> <span data-ttu-id="048c0-117">В модели шейдеров 5 реализован новый соответствующий набор ресурсов для чтения и записи:</span><span class="sxs-lookup"><span data-stu-id="048c0-117">Shader model 5 implements a new corresponding set of read/write resources:</span></span>

-   [<span data-ttu-id="048c0-118">рвбуффер</span><span class="sxs-lookup"><span data-stu-id="048c0-118">RWBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   <span data-ttu-id="048c0-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span><span class="sxs-lookup"><span data-stu-id="048c0-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span></span>
-   <span data-ttu-id="048c0-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span><span class="sxs-lookup"><span data-stu-id="048c0-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span></span>
-   [<span data-ttu-id="048c0-121">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="048c0-121">RWTexture3D</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

<span data-ttu-id="048c0-122">Для этих ресурсов требуется переменная ресурса для доступа к памяти (посредством индексирования), так как нет методов для прямого доступа к памяти.</span><span class="sxs-lookup"><span data-stu-id="048c0-122">These resources require a resource variable to access memory (through indexing) as there are no methods for accessing memory directly.</span></span> <span data-ttu-id="048c0-123">Переменную ресурса можно использовать в левой и правой частях уравнения. При использовании с правой стороны тип шаблона должен быть единственным компонентом (float, int или uint).</span><span class="sxs-lookup"><span data-stu-id="048c0-123">A resource variable can be used on the left and right sides of an equation; if used on the right side, the template type must be single component (float, int, or uint).</span></span>

## <a name="structured-buffer"></a><span data-ttu-id="048c0-124">Структурированный буфер</span><span class="sxs-lookup"><span data-stu-id="048c0-124">Structured Buffer</span></span>

<span data-ttu-id="048c0-125">Структурированный буфер — это буфер, содержащий элементы одинаковых размеров.</span><span class="sxs-lookup"><span data-stu-id="048c0-125">A structured buffer is a buffer that contains elements of equal sizes.</span></span> <span data-ttu-id="048c0-126">Для определения элемента используйте структуру с одним или несколькими типами элементов.</span><span class="sxs-lookup"><span data-stu-id="048c0-126">Use a structure with one or more member types to define an element.</span></span> <span data-ttu-id="048c0-127">Ниже приведена структура с тремя элементами.</span><span class="sxs-lookup"><span data-stu-id="048c0-127">Here is a structure with three members.</span></span>


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



<span data-ttu-id="048c0-128">Используйте эту структуру для объявления структурированного буфера следующим образом:</span><span class="sxs-lookup"><span data-stu-id="048c0-128">Use this structure to declare a structured buffer like this:</span></span>


```
StructuredBuffer<MyStruct> mySB;
```



<span data-ttu-id="048c0-129">Помимо индексирования, структурированный буфер поддерживает доступ к одному элементу следующим образом:</span><span class="sxs-lookup"><span data-stu-id="048c0-129">In addition to indexing, a structured buffer supports accessing a single member like this:</span></span>


```
float4 myColor = mySb[27].Color;
```



<span data-ttu-id="048c0-130">Для доступа к структурированному буферу используйте следующие типы объектов:</span><span class="sxs-lookup"><span data-stu-id="048c0-130">Use the following object types to access a structured buffer:</span></span>

-   <span data-ttu-id="048c0-131">[Структуредбуффер](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) является структурированным буфером только для чтения.</span><span class="sxs-lookup"><span data-stu-id="048c0-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) is a read only structured buffer.</span></span>
-   <span data-ttu-id="048c0-132">[Рвструктуредбуффер](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) — это структурированный буфер для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="048c0-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) is a read/write structured buffer.</span></span>

<span data-ttu-id="048c0-133">[Атомарные функции](direct3d-11-advanced-stages-cs-atomic-functions.md) , которые реализуют блокируемые операции, допускаются для элементов int и uint в **рвструктуредбуффер**.</span><span class="sxs-lookup"><span data-stu-id="048c0-133">[Atomic functions](direct3d-11-advanced-stages-cs-atomic-functions.md) which implement interlocked operations are allowed on int and uint elements in an **RWStructuredBuffer**.</span></span>

## <a name="byte-address-buffer"></a><span data-ttu-id="048c0-134">Буфер байтового адреса</span><span class="sxs-lookup"><span data-stu-id="048c0-134">Byte Address Buffer</span></span>

<span data-ttu-id="048c0-135">Буфер байтового адреса — это буфер, содержимое которого можно устранить с помощью смещения в байтах.</span><span class="sxs-lookup"><span data-stu-id="048c0-135">A byte address buffer is a buffer whose contents are addressable by a byte offset.</span></span> <span data-ttu-id="048c0-136">Как правило, содержимое [буфера](overviews-direct3d-11-resources-buffers-intro.md) индексируется по каждому элементу с помощью шага для каждого элемента и номера элемента (N), заданного параметром S \* N.</span><span class="sxs-lookup"><span data-stu-id="048c0-136">Normally, the contents of a [buffer](overviews-direct3d-11-resources-buffers-intro.md) are indexed per element using a stride for each element (S) and the element number (N) as given by S\*N.</span></span> <span data-ttu-id="048c0-137">Буфер байтового адреса, который также может называться необработанным буфером, использует смещение байтового значения от начала буфера для доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="048c0-137">A byte address buffer, which can also be called a raw buffer, uses a byte value offset from the beginning of the buffer to access data.</span></span> <span data-ttu-id="048c0-138">Значение байта должно быть кратно четырем, чтобы оно было высвоено по DWORD.</span><span class="sxs-lookup"><span data-stu-id="048c0-138">The byte value must be a multiple of four so that it is DWORD aligned.</span></span> <span data-ttu-id="048c0-139">Если указано любое другое значение, поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="048c0-139">If any other value is provided, behavior is undefined.</span></span>

<span data-ttu-id="048c0-140">В модели шейдеров 5 представлены объекты для доступа к [буферу байтового адреса только для чтения](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) , а также [буферу байтов для чтения и записи](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span><span class="sxs-lookup"><span data-stu-id="048c0-140">Shader model 5 introduces objects for accessing a [read-only byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) as well as a [read-write byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span></span> <span data-ttu-id="048c0-141">Содержимое буфера байтового адреса разработано как 32-разрядное целое число без знака; Если значение в буфере действительно не является целым числом без знака, используйте функцию, например [**асфлоат**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) , чтобы прочитать ее.</span><span class="sxs-lookup"><span data-stu-id="048c0-141">The contents of a byte address buffer is designed to be a 32-bit unsigned integer; if the value in the buffer is not really an unsigned integer, use a function such as [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) to read it.</span></span>

## <a name="unordered-access-buffer-or-texture"></a><span data-ttu-id="048c0-142">Неупорядоченный буфер или текстура доступа</span><span class="sxs-lookup"><span data-stu-id="048c0-142">Unordered Access Buffer or Texture</span></span>

<span data-ttu-id="048c0-143">Неупорядоченный ресурс доступа (который включает буферы, текстуры и массивы текстур без множественной выборки) позволяет временно неупорядоченный доступ на чтение и запись из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="048c0-143">An unordered access resource (which includes buffers, textures, and texture arrays - without multisampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="048c0-144">Это означает, что этот тип ресурса можно считывать и записывать одновременно несколькими потоками, не создавая конфликты памяти за счет использования [атомарных функций](direct3d-11-advanced-stages-cs-atomic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="048c0-144">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts through the use of [Atomic Functions](direct3d-11-advanced-stages-cs-atomic-functions.md).</span></span>

<span data-ttu-id="048c0-145">Создайте неупорядоченный буфер или текстуру доступа, вызвав функцию, такую как [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) или [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) и передав флаг **\_ \_ неупорядоченного \_ доступа D3D11 BIND** в перечислении [**\_ \_ флага привязки D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="048c0-145">Create an unordered access buffer or texture by calling a function such as [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) or [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and passing in the **D3D11\_BIND\_UNORDERED\_ACCESS** flag from the [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) enumeration.</span></span>

<span data-ttu-id="048c0-146">Неупорядоченные ресурсы доступа можно привязывать только к шейдерам пикселей и шейдерам вычислений.</span><span class="sxs-lookup"><span data-stu-id="048c0-146">Unordered access resources can only be bound to pixel shaders and compute shaders.</span></span> <span data-ttu-id="048c0-147">Во время выполнения шейдеры пикселей или шейдеры вычислений, выполняющиеся параллельно, имеют одинаковые привязанные неупорядоченные ресурсы доступа.</span><span class="sxs-lookup"><span data-stu-id="048c0-147">During execution, pixel shaders or compute shaders running in parallel have the same unordered access resources bound.</span></span>

### <a name="append-and-consume-buffer"></a><span data-ttu-id="048c0-148">Добавление и использование буфера</span><span class="sxs-lookup"><span data-stu-id="048c0-148">Append and Consume Buffer</span></span>

<span data-ttu-id="048c0-149">Буфер добавления и использования — это особый тип неупорядоченного ресурса, который поддерживает добавление и удаление значений из конца буфера аналогично тому, как работает стек.</span><span class="sxs-lookup"><span data-stu-id="048c0-149">An append and consume buffer is a special type of an unordered resource that supports adding and removing values from the end of a buffer similar to the way a stack works.</span></span>

<span data-ttu-id="048c0-150">Буфер добавления и использования должен быть структурированным буфером:</span><span class="sxs-lookup"><span data-stu-id="048c0-150">An append and consume buffer must be a structured buffer:</span></span>

-   [<span data-ttu-id="048c0-151">аппендструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="048c0-151">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="048c0-152">консуместруктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="048c0-152">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

<span data-ttu-id="048c0-153">Используйте эти ресурсы в своих методах. Эти ресурсы не используют переменные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="048c0-153">Use these resources through their methods, these resources do not use resource variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="048c0-154">См. также</span><span class="sxs-lookup"><span data-stu-id="048c0-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="048c0-155">Общие сведения о вычислении шейдера</span><span class="sxs-lookup"><span data-stu-id="048c0-155">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 