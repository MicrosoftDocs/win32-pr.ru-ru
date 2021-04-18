---
title: Начало работы с этапом Input-Assembler
description: Для инициализации этапа ввода-ассемблера необходимо выполнить несколько действий.
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413204"
---
# <a name="getting-started-with-the-input-assembler-stage"></a><span data-ttu-id="9dae1-103">Начало работы с этапом Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="9dae1-103">Getting Started with the Input-Assembler Stage</span></span>

<span data-ttu-id="9dae1-104">Для инициализации этапа ввода-ассемблера необходимо выполнить несколько действий.</span><span class="sxs-lookup"><span data-stu-id="9dae1-104">There are a few steps necessary to initialize the input-assembler (IA) stage.</span></span> <span data-ttu-id="9dae1-105">Например, необходимо создать ресурсы буфера с данными вершин, необходимыми для конвейера, сообщить этапу IA, где находятся буферы и какие типы данных они содержат, и указать тип примитивов для сборки из данных.</span><span class="sxs-lookup"><span data-stu-id="9dae1-105">For example, you need to create buffer resources with the vertex data that the pipeline needs, tell the IA stage where the buffers are and what type of data they contain, and specify the type of primitives to assemble from the data.</span></span>

<span data-ttu-id="9dae1-106">Основные шаги, связанные с настройкой этапа IA, как показано в следующей таблице, описаны в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="9dae1-106">The basic steps involved in setting up the IA stage, shown in the following table, are covered in this topic.</span></span>



| <span data-ttu-id="9dae1-107">Шаг</span><span class="sxs-lookup"><span data-stu-id="9dae1-107">Step</span></span>                                                                                    | <span data-ttu-id="9dae1-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9dae1-108">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dae1-109">Создание входных буферов</span><span class="sxs-lookup"><span data-stu-id="9dae1-109">Create Input Buffers</span></span>](#create-input-buffers)                                           | <span data-ttu-id="9dae1-110">Создание и инициализация входных буферов с входными данными вершин.</span><span class="sxs-lookup"><span data-stu-id="9dae1-110">Create and initialize input buffers with input vertex data.</span></span>                                           |
| [<span data-ttu-id="9dae1-111">Создание объекта Input-Layout</span><span class="sxs-lookup"><span data-stu-id="9dae1-111">Create the Input-Layout Object</span></span>](#create-the-input-layout-object)                       | <span data-ttu-id="9dae1-112">Определите, каким способом потоковая передача данных из буфера вершин будет выполняться на этапе IA с помощью объекта input-Layout.</span><span class="sxs-lookup"><span data-stu-id="9dae1-112">Define how the vertex buffer data will be streamed into the IA stage by using an input-layout object.</span></span> |
| [<span data-ttu-id="9dae1-113">Привязка объектов к Input-Assembler этапу</span><span class="sxs-lookup"><span data-stu-id="9dae1-113">Bind Objects to the Input-Assembler Stage</span></span>](#bind-objects-to-the-input-assembler-stage) | <span data-ttu-id="9dae1-114">Привяжите созданные объекты (Входные буферы и объект макета ввода) к этапу IA.</span><span class="sxs-lookup"><span data-stu-id="9dae1-114">Bind the created objects (input buffers and the input-layout object) to the IA stage.</span></span>                 |
| [<span data-ttu-id="9dae1-115">Укажите тип-примитив</span><span class="sxs-lookup"><span data-stu-id="9dae1-115">Specify the Primitive Type</span></span>](#specify-the-primitive-type)                               | <span data-ttu-id="9dae1-116">Определение того, как вершины будут собираться в примитивы.</span><span class="sxs-lookup"><span data-stu-id="9dae1-116">Identify how the vertices will be assembled into primitives.</span></span>                                          |
| [<span data-ttu-id="9dae1-117">Методы рисования вызова</span><span class="sxs-lookup"><span data-stu-id="9dae1-117">Call Draw Methods</span></span>](#call-draw-methods)                                                 | <span data-ttu-id="9dae1-118">Отправьте данные, привязанные к этапу IA через конвейер.</span><span class="sxs-lookup"><span data-stu-id="9dae1-118">Send the data bound to the IA stage through the pipeline.</span></span>                                             |



 

<span data-ttu-id="9dae1-119">Когда вы понимаете эти шаги, переходите к [использованию значений System-Generated](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span><span class="sxs-lookup"><span data-stu-id="9dae1-119">After you understand these steps, move on to [Using System-Generated Values](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span></span>

## <a name="create-input-buffers"></a><span data-ttu-id="9dae1-120">Создание входных буферов</span><span class="sxs-lookup"><span data-stu-id="9dae1-120">Create Input Buffers</span></span>

<span data-ttu-id="9dae1-121">Существует два типа входных буферов: [буферы вершин](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) и буферы индексов.</span><span class="sxs-lookup"><span data-stu-id="9dae1-121">There are two types of input buffers: [vertex buffers](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and index buffers.</span></span> <span data-ttu-id="9dae1-122">Буферы вершин предоставляют данные вершин на этап IA.</span><span class="sxs-lookup"><span data-stu-id="9dae1-122">Vertex buffers supply vertex data to the IA stage.</span></span> <span data-ttu-id="9dae1-123">Буферы индексов необязательны; они предоставляют индексы вершинам из буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="9dae1-123">Index buffers are optional; they provide indices to vertices from the vertex buffer.</span></span> <span data-ttu-id="9dae1-124">Вы можете создать один или несколько буферов вершин и, при необходимости, буфер индексов.</span><span class="sxs-lookup"><span data-stu-id="9dae1-124">You may create one or more vertex buffers and, optionally, an index buffer.</span></span>

<span data-ttu-id="9dae1-125">После создания ресурсов буфера необходимо создать объект макета ввода, чтобы описать макет данных на этапе IA, а затем привязать ресурсы буфера к этапу IA.</span><span class="sxs-lookup"><span data-stu-id="9dae1-125">After you create the buffer resources, you need to create an input-layout object to describe the data layout to the IA stage, and then you need to bind the buffer resources to the IA stage.</span></span> <span data-ttu-id="9dae1-126">Создание и привязка буферов не требуется, если шейдеры не используют буферы.</span><span class="sxs-lookup"><span data-stu-id="9dae1-126">Creating and binding buffers is not necessary if your shaders don't use buffers.</span></span> <span data-ttu-id="9dae1-127">Пример простой вершины и шейдера пикселей, который рисует один треугольник, см. [в разделе использование Input-Assembler этапа без буферов](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="9dae1-127">For an example of a simple vertex and pixel shader that draws a single triangle, see [Using the Input-Assembler Stage without Buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span></span>

<span data-ttu-id="9dae1-128">Дополнительные сведения о создании буфера вершин см. в разделе [Создание буфера вершин](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="9dae1-128">For help with creating a vertex buffer, see [Create a Vertex Buffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span> <span data-ttu-id="9dae1-129">Дополнительные сведения о создании буфера индексов см. в разделе Создание буфера индексов.</span><span class="sxs-lookup"><span data-stu-id="9dae1-129">For help with creating an index buffer, see Create an Index Buffer.</span></span>

## <a name="create-the-input-layout-object"></a><span data-ttu-id="9dae1-130">Создание объекта Input-Layout</span><span class="sxs-lookup"><span data-stu-id="9dae1-130">Create the Input-Layout Object</span></span>

<span data-ttu-id="9dae1-131">Объект входной макет инкапсулирует состояние входного этапа IA.</span><span class="sxs-lookup"><span data-stu-id="9dae1-131">The input-layout object encapsulates the input state of the IA stage.</span></span> <span data-ttu-id="9dae1-132">Сюда входит описание входных данных, привязанных к этапу IA.</span><span class="sxs-lookup"><span data-stu-id="9dae1-132">This includes a description of the input data that is bound to the IA stage.</span></span> <span data-ttu-id="9dae1-133">Данные передаются на стадию IA из памяти из одного или нескольких буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="9dae1-133">The data is streamed into the IA stage from memory, from one or more vertex buffers.</span></span> <span data-ttu-id="9dae1-134">Описание определяет входные данные, привязанные из одного или нескольких буферов вершин, и дает среде выполнения возможность проверять типы входных данных на соответствие типам входных параметров шейдера.</span><span class="sxs-lookup"><span data-stu-id="9dae1-134">The description identifies the input data that is bound from one or more vertex buffers and gives the runtime the ability to check the input data types against the shader input parameter types.</span></span> <span data-ttu-id="9dae1-135">Эта проверка типа не только проверяет совместимость типов, но и то, что каждый из элементов, необходимых шейдеру, доступен в буферных ресурсах.</span><span class="sxs-lookup"><span data-stu-id="9dae1-135">This type checking not only verifies that the types are compatible, but also that each of the elements that the shader requires is available in the buffer resources.</span></span>

<span data-ttu-id="9dae1-136">Объект макета ввода создается из массива описаний входных элементов и указателя на скомпилированный шейдер (см. раздел [**ID3D11Device:: креатеинпутлайаут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span><span class="sxs-lookup"><span data-stu-id="9dae1-136">An input-layout object is created from an array of input-element descriptions and a pointer to the compiled shader (see [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span></span> <span data-ttu-id="9dae1-137">Массив содержит один или несколько входных элементов; Каждый элемент ввода описывает один элемент данных вершины из одного буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="9dae1-137">The array contains one or more input elements; each input element describes a single vertex-data element from a single vertex buffer.</span></span> <span data-ttu-id="9dae1-138">Весь набор описаний input-element описывает все элементы vertex-data из всех буферов вершин, которые будут привязаны на этапе IA.</span><span class="sxs-lookup"><span data-stu-id="9dae1-138">The entire set of input-element descriptions describes all of the vertex-data elements from all of the vertex buffers that will be bound to the IA stage.</span></span>

<span data-ttu-id="9dae1-139">Следующее описание макета описывает один буфер вершин, который содержит три элемента данных вершины:</span><span class="sxs-lookup"><span data-stu-id="9dae1-139">The following layout description describes a single vertex buffer that contains three vertex-data elements:</span></span>


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



<span data-ttu-id="9dae1-140">Описание элемента ввода описывает каждый элемент, содержащийся в одной вершине в буфере вершин, включая размер, тип, расположение и назначение.</span><span class="sxs-lookup"><span data-stu-id="9dae1-140">An input-element description describes each element contained by a single vertex in a vertex buffer, including size, type, location, and purpose.</span></span> <span data-ttu-id="9dae1-141">Каждая строка определяет тип данных с помощью семантики, семантического индекса и формата данных.</span><span class="sxs-lookup"><span data-stu-id="9dae1-141">Each row identifies the type of data by using the semantic, the semantic index, and the data format.</span></span> <span data-ttu-id="9dae1-142">[Семантика](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) — это текстовая строка, которая определяет, как будут использоваться данные.</span><span class="sxs-lookup"><span data-stu-id="9dae1-142">A [semantic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) is a text string that identifies how the data will be used.</span></span> <span data-ttu-id="9dae1-143">В этом примере первая строка определяет данные о положении 3 компонента (например,*XYZ*); Вторая строка определяет 2-компонентные данные текстуры (например,*UV*); Третья строка определяет обычные данные.</span><span class="sxs-lookup"><span data-stu-id="9dae1-143">In this example, the first row identifies 3-component position data (*xyz*, for example); the second row identifies 2-component texture data (*UV*, for example); and the third row identifies normal data.</span></span>

<span data-ttu-id="9dae1-144">В этом примере описания входного элемента семантический индекс (второй параметр) устанавливается в ноль для всех трех строк.</span><span class="sxs-lookup"><span data-stu-id="9dae1-144">In this example of an input-element description, the semantic index (which is the second parameter) is set to zero for all three rows.</span></span> <span data-ttu-id="9dae1-145">Семантический индекс помогает отличать две строки, использующие одну и ту же семантику.</span><span class="sxs-lookup"><span data-stu-id="9dae1-145">The semantic index helps distinguish between two rows that use the same semantics.</span></span> <span data-ttu-id="9dae1-146">Так как в этом примере нет подобной семантики, для семантического индекса можно задать значение по умолчанию, равное нулю.</span><span class="sxs-lookup"><span data-stu-id="9dae1-146">Since there are no similar semantics in this example, the semantic index can be set to its default value, zero.</span></span>

<span data-ttu-id="9dae1-147">Третьим параметром является *Формат*.</span><span class="sxs-lookup"><span data-stu-id="9dae1-147">The third parameter is the *format*.</span></span> <span data-ttu-id="9dae1-148">Формат (см. [**раздел \_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) указывает количество компонентов на элемент и тип данных, определяющий размер данных для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="9dae1-148">The format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifies the number of components per element, and the data type, which defines the size of the data for each element.</span></span> <span data-ttu-id="9dae1-149">Формат можно полностью ввести во время создания ресурса или создать ресурс с помощью **\_ формата DXGI**, который определяет количество компонентов в элементе, но оставляет тип данных не определенным.</span><span class="sxs-lookup"><span data-stu-id="9dae1-149">The format can be fully typed at the time of resource creation, or you may create a resource by using a **DXGI\_FORMAT**, which identifies the number of components in an element, but leaves the data type undefined.</span></span>

### <a name="input-slots"></a><span data-ttu-id="9dae1-150">Входные слоты</span><span class="sxs-lookup"><span data-stu-id="9dae1-150">Input Slots</span></span>

<span data-ttu-id="9dae1-151">Данные поступают на этап IA через входные данные, называемые *входными слотами*, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9dae1-151">Data enters the IA stage through inputs called *input slots*, as shown in the following illustration.</span></span> <span data-ttu-id="9dae1-152">На этапе IA есть *n* слотов ввода, которые предназначены для размещения до *n* буферов вершин, предоставляющих входные данные.</span><span class="sxs-lookup"><span data-stu-id="9dae1-152">The IA stage has *n* input slots, which are designed to accommodate up to *n* vertex buffers that provide input data.</span></span> <span data-ttu-id="9dae1-153">Каждый буфер вершин должен быть назначен другому слоту; Эти сведения сохраняются в объявлении input-Layout при создании объекта input-Layout.</span><span class="sxs-lookup"><span data-stu-id="9dae1-153">Each vertex buffer must be assigned to a different slot; this information is stored in the input-layout declaration when the input-layout object is created.</span></span> <span data-ttu-id="9dae1-154">Вы также можете указать смещение от начала каждого буфера до первого элемента в буфере для чтения.</span><span class="sxs-lookup"><span data-stu-id="9dae1-154">You may also specify an offset from the start of each buffer to the first element in the buffer to be read.</span></span>

![Иллюстрация входных слотов для этапа IA](images/d3d10-ia-slots.png)

<span data-ttu-id="9dae1-156">Следующие два параметра — это *входной слот* и *смещение входных данных*.</span><span class="sxs-lookup"><span data-stu-id="9dae1-156">The next two parameters are the *input slot* and the *input offset*.</span></span> <span data-ttu-id="9dae1-157">При использовании нескольких буферов их можно привязать к одному или нескольким входным слотам.</span><span class="sxs-lookup"><span data-stu-id="9dae1-157">When you use multiple buffers, you can bind them to one or more input slots.</span></span> <span data-ttu-id="9dae1-158">Смещение ввода — это число байтов между началом буфера и началом данных.</span><span class="sxs-lookup"><span data-stu-id="9dae1-158">The input offset is the number of bytes between the start of the buffer and the beginning of the data.</span></span>

### <a name="reusing-input-layout-objects"></a><span data-ttu-id="9dae1-159">Повторное использование объектов Input-Layout</span><span class="sxs-lookup"><span data-stu-id="9dae1-159">Reusing Input-Layout Objects</span></span>

<span data-ttu-id="9dae1-160">Каждый объект макета ввода создается на основе сигнатуры шейдера. Это позволяет API проверить элементы входного макета в соответствии с подписью входного шейдера, чтобы убедиться в точности соответствия типов и семантики.</span><span class="sxs-lookup"><span data-stu-id="9dae1-160">Each input-layout object is created based on a shader signature; this allows the API to validate the input-layout-object elements against the shader-input signature to make sure that there is an exact match of types and semantics.</span></span> <span data-ttu-id="9dae1-161">Можно создать один объект макета ввода для многих шейдеров, если все входные сигнатуры шейдера точно совпадают.</span><span class="sxs-lookup"><span data-stu-id="9dae1-161">You can create a single input-layout object for many shaders, as long as all of the shader-input signatures exactly match.</span></span>

## <a name="bind-objects-to-the-input-assembler-stage"></a><span data-ttu-id="9dae1-162">Привязка объектов к Input-Assembler этапу</span><span class="sxs-lookup"><span data-stu-id="9dae1-162">Bind Objects to the Input-Assembler Stage</span></span>

<span data-ttu-id="9dae1-163">После создания ресурсов буфера вершин и объекта макета входных данных их можно привязать к этапу IA, вызвав [**ссылку ID3D11DeviceContext:: иасетвертексбуфферс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) и [**ссылку ID3D11DeviceContext:: иасетинпутлайаут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span><span class="sxs-lookup"><span data-stu-id="9dae1-163">After you create vertex buffer resources and an input layout object, you can bind them to the IA stage by calling [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) and [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span></span> <span data-ttu-id="9dae1-164">В следующем примере показана привязка одного буфера вершин и объекта макета ввода к этапу IA:</span><span class="sxs-lookup"><span data-stu-id="9dae1-164">The following example shows the binding of a single vertex buffer and an input-layout object to the IA stage:</span></span>


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



<span data-ttu-id="9dae1-165">Для привязки к объекту входного макета требуется только указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="9dae1-165">Binding the input-layout object only requires a pointer to the object.</span></span>

<span data-ttu-id="9dae1-166">В предыдущем примере привязывается один буфер вершин. Однако несколько буферов вершин могут быть привязаны одним вызовом к [**ссылку ID3D11DeviceContext:: иасетвертексбуфферс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), а в следующем коде показан такой вызов для привязки трех буферов вершин:</span><span class="sxs-lookup"><span data-stu-id="9dae1-166">In the preceding example, a single vertex buffer is bound; however, multiple vertex buffers can be bound by a single call to [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), and the following code shows such a call to bind three vertex buffers:</span></span>


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



<span data-ttu-id="9dae1-167">Буфер индекса привязан к этапу IA путем вызова [**ссылку ID3D11DeviceContext:: иасетиндексбуффер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span><span class="sxs-lookup"><span data-stu-id="9dae1-167">An index buffer is bound to the IA stage by calling [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span></span>

## <a name="specify-the-primitive-type"></a><span data-ttu-id="9dae1-168">Укажите тип-примитив</span><span class="sxs-lookup"><span data-stu-id="9dae1-168">Specify the Primitive Type</span></span>

<span data-ttu-id="9dae1-169">После привязки входных буферов на этапе IA необходимо сообщить, как объединить вершины в примитивы.</span><span class="sxs-lookup"><span data-stu-id="9dae1-169">After the input buffers have been bound, the IA stage must be told how to assemble the vertices into primitives.</span></span> <span data-ttu-id="9dae1-170">Это делается путем указания типа- [примитива](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) путем вызова [**ссылку ID3D11DeviceContext:: иасетпримитиветопологи**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); Следующий код вызывает эту функцию для определения данных в виде списка треугольников без соседей:</span><span class="sxs-lookup"><span data-stu-id="9dae1-170">This is done by specifying the [primitive type](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) by calling [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); the following code calls this function to define the data as a triangle list without adjacency:</span></span>


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



<span data-ttu-id="9dae1-171">Остальные типы-примитивы перечислены в [**\_ \_ топологии примитивов D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span><span class="sxs-lookup"><span data-stu-id="9dae1-171">The rest of the primitive types are listed in [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span></span>

## <a name="call-draw-methods"></a><span data-ttu-id="9dae1-172">Методы рисования вызова</span><span class="sxs-lookup"><span data-stu-id="9dae1-172">Call Draw Methods</span></span>

<span data-ttu-id="9dae1-173">После привязки входных ресурсов к конвейеру приложение вызывает метод Draw для отрисовки примитивов.</span><span class="sxs-lookup"><span data-stu-id="9dae1-173">After input resources have been bound to the pipeline, an application calls a draw method to render primitives.</span></span> <span data-ttu-id="9dae1-174">Существует несколько методов Draw, которые показаны в следующей таблице. Некоторые буферы индексов, некоторые используют данные экземпляра и некоторые повторно используемые данные из этапа потоковой передачи переводятся в качестве входных данных на этапе входного ассемблера.</span><span class="sxs-lookup"><span data-stu-id="9dae1-174">There are several draw methods, which are shown in the following table; some use index buffers, some use instance data, and some reuse data from the streaming-output stage as input to the input-assembler stage.</span></span>



| <span data-ttu-id="9dae1-175">Методы рисования</span><span class="sxs-lookup"><span data-stu-id="9dae1-175">Draw Methods</span></span>                                                                                  | <span data-ttu-id="9dae1-176">Описание</span><span class="sxs-lookup"><span data-stu-id="9dae1-176">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dae1-177">**ID3D11DeviceContext::Draw**</span><span class="sxs-lookup"><span data-stu-id="9dae1-177">**ID3D11DeviceContext::Draw**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | <span data-ttu-id="9dae1-178">Рисование неиндексированных, не являющихся экземплярами примитивов.</span><span class="sxs-lookup"><span data-stu-id="9dae1-178">Draw non-indexed, non-instanced primitives.</span></span>                                                            |
| [<span data-ttu-id="9dae1-179">**ID3D11DeviceContext::DrawInstanced**</span><span class="sxs-lookup"><span data-stu-id="9dae1-179">**ID3D11DeviceContext::DrawInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | <span data-ttu-id="9dae1-180">Нарисуйте неиндексированные экземпляры-примитивы.</span><span class="sxs-lookup"><span data-stu-id="9dae1-180">Draw non-indexed, instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="9dae1-181">**ID3D11DeviceContext::DrawIndexed**</span><span class="sxs-lookup"><span data-stu-id="9dae1-181">**ID3D11DeviceContext::DrawIndexed**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | <span data-ttu-id="9dae1-182">Рисование индексированных, не являющихся экземплярами примитивов.</span><span class="sxs-lookup"><span data-stu-id="9dae1-182">Draw indexed, non-instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="9dae1-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="9dae1-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | <span data-ttu-id="9dae1-184">Рисование индексированных, экземплярных примитивов.</span><span class="sxs-lookup"><span data-stu-id="9dae1-184">Draw indexed, instanced primitives.</span></span>                                                                    |
| [<span data-ttu-id="9dae1-185">**ID3D11DeviceContext::DrawAuto**</span><span class="sxs-lookup"><span data-stu-id="9dae1-185">**ID3D11DeviceContext::DrawAuto**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | <span data-ttu-id="9dae1-186">Нарисуйте неиндексированные некластеризованные примитивы из входных данных, поступающих из этапа потокового вывода.</span><span class="sxs-lookup"><span data-stu-id="9dae1-186">Draw non-indexed, non-instanced primitives from input data that comes from the streaming-output stage.</span></span> |



 

<span data-ttu-id="9dae1-187">Каждый метод Draw отображает один тип топологии.</span><span class="sxs-lookup"><span data-stu-id="9dae1-187">Each draw method renders a single topology type.</span></span> <span data-ttu-id="9dae1-188">Во время отрисовки неполные примитивы (без достаточных вершин, отсутствующие индексы, частичные примитивы и т. д.) автоматически отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="9dae1-188">During rendering, incomplete primitives (those without enough vertices, lacking indices, partial primitives, and so on) are silently discarded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dae1-189">См. также</span><span class="sxs-lookup"><span data-stu-id="9dae1-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dae1-190">Этап ввода-ассемблера</span><span class="sxs-lookup"><span data-stu-id="9dae1-190">Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 