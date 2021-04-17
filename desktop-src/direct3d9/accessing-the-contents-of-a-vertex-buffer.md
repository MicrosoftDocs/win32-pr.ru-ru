---
description: Объекты буфера вершин позволяют приложениям получать прямой доступ к памяти, выделенной для данных вершин.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Доступ к содержимому буфера вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673131"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="031db-103">Доступ к содержимому буфера вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="031db-103">Accessing the Contents of a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="031db-104">Объекты буфера вершин позволяют приложениям получать прямой доступ к памяти, выделенной для данных вершин.</span><span class="sxs-lookup"><span data-stu-id="031db-104">Vertex buffer objects enable applications to directly access the memory allocated for vertex data.</span></span> <span data-ttu-id="031db-105">Указатель на память буфера вершин можно получить, вызвав метод [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) , а затем получая доступ к памяти по мере необходимости для заполнения буфера новыми данными вершин или для чтения уже содержащихся в нем данных.</span><span class="sxs-lookup"><span data-stu-id="031db-105">You can retrieve a pointer to vertex buffer memory by calling the [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) method, and then accessing the memory as needed to fill the buffer with new vertex data or to read any data it already contains.</span></span> <span data-ttu-id="031db-106">Метод **IDirect3DVertexBuffer9:: Lock** принимает четыре параметра.</span><span class="sxs-lookup"><span data-stu-id="031db-106">The **IDirect3DVertexBuffer9::Lock** method accepts four parameters.</span></span> <span data-ttu-id="031db-107">Первый, *оффсеттолокк*, является смещением данных вершин.</span><span class="sxs-lookup"><span data-stu-id="031db-107">The first, *OffsetToLock*, is the offset into the vertex data.</span></span> <span data-ttu-id="031db-108">Второй параметр — это размер данных вершин, измеряемый в байтах.</span><span class="sxs-lookup"><span data-stu-id="031db-108">The second parameter is the size, measured in bytes, of the vertex data.</span></span> <span data-ttu-id="031db-109">Третий параметр принят — адрес указателя, указывающего на данные вершин, если вызов выполнен.</span><span class="sxs-lookup"><span data-stu-id="031db-109">The third parameter accepted is the address of a pointer that points to the vertex data, if the call succeeds.</span></span>

<span data-ttu-id="031db-110">Последний параметр, *Флаги* сообщает системе о том, как должна быть заблокирована память.</span><span class="sxs-lookup"><span data-stu-id="031db-110">The last parameter, *Flags*, tells the system how the memory should be locked.</span></span> <span data-ttu-id="031db-111">Укажите константы для параметра *flags* в соответствии с тем, как будет осуществляться доступ к данным вершин.</span><span class="sxs-lookup"><span data-stu-id="031db-111">Specify constants for the *Flags* parameter according to the way the vertex data will be accessed.</span></span> <span data-ttu-id="031db-112">Убедитесь, что значение, выбранное для [**D3DUSAGE**](d3dusage.md) , совпадает со значением, выбранным для [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="031db-112">Make sure the value chosen for [**D3DUSAGE**](d3dusage.md) matches the value chosen for [D3DLOCK](d3dlock.md).</span></span> <span data-ttu-id="031db-113">Например, при создании буфера вершин с доступом только для записи не имеет смысла пытаться прочитать данные, указав D3DLOCK \_ ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="031db-113">For example, if you are creating a vertex buffer with write access only, it doesn't make sense to try to read the data by specifying D3DLOCK\_READONLY.</span></span> <span data-ttu-id="031db-114">Использование этих флагов позволяет драйверу заблокировать память и обеспечить наилучшую производительность с учетом требуемого типа доступа.</span><span class="sxs-lookup"><span data-stu-id="031db-114">Wisely using these flags allows the driver to lock the memory and provide the best performance, given the requested access type.</span></span>

<span data-ttu-id="031db-115">Завершив заполнение или чтение данных вершин, вызовите метод [**IDirect3DVertexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="031db-115">After you finish filling or reading the vertex data, call the [**IDirect3DVertexBuffer9::Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) method, as shown in the following code example.</span></span>


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



<span data-ttu-id="031db-116">Если вы создаете буфер вершин с \_ флагом D3DUSAGE WRITEONLY, не используйте \_ флаг блокировки D3DLOCK ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="031db-116">If you create a vertex buffer with the D3DUSAGE\_WRITEONLY flag, do not use the D3DLOCK\_READONLY locking flag.</span></span> <span data-ttu-id="031db-117">Используйте флаг D3DLOCK \_ ReadOnly, если приложение будет считывать только из памяти буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="031db-117">Use the D3DLOCK\_READONLY flag if your application will read only from the vertex buffer memory.</span></span> <span data-ttu-id="031db-118">Включение этого флага позволяет Direct3D оптимизировать свои внутренние процедуры для повышения эффективности, учитывая, что доступ к памяти будет доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="031db-118">Including this flag enables Direct3D to optimize its internal procedures to improve efficiency, given that access to the memory will be read-only.</span></span>

<span data-ttu-id="031db-119">Сведения [](performance-optimizations.md) об использовании D3DLOCK \_ Discard или D3DLOCK \_ нуверврите для параметра flags командлета [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)см. в разделе Использование динамических буферов вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="031db-119">See [Using Dynamic Vertex and Index Buffers](performance-optimizations.md) for information about using D3DLOCK\_DISCARD or D3DLOCK\_NOOVERWRITE for the Flags parameter of [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).</span></span>

<span data-ttu-id="031db-120">В C++, так как вы напрямую обращаетесь к памяти, выделенной для буфера вершин, убедитесь, что приложение правильно обращается к выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="031db-120">In C++, because you directly access the memory allocated for the vertex buffer, make sure your application properly accesses the allocated memory.</span></span> <span data-ttu-id="031db-121">В противном случае вы рискуете выявление недействительной памяти.</span><span class="sxs-lookup"><span data-stu-id="031db-121">Otherwise, you risk rendering that memory invalid.</span></span> <span data-ttu-id="031db-122">Используйте шаг в формате вершин, который приложение использует для перехода с одной вершины в выделенном буфере на другую.</span><span class="sxs-lookup"><span data-stu-id="031db-122">Use the stride of the vertex format that your application uses to move from one vertex in the allocated buffer to another.</span></span> <span data-ttu-id="031db-123">Память буфера вершин — это простой массив вершин, указанный в ФВФ.</span><span class="sxs-lookup"><span data-stu-id="031db-123">The vertex buffer memory is a simple array of vertices specified in FVF.</span></span> <span data-ttu-id="031db-124">Используйте шаг с любыми определенными структурами формата вершин.</span><span class="sxs-lookup"><span data-stu-id="031db-124">Use the stride of whatever vertex format structure you define.</span></span> <span data-ttu-id="031db-125">Можно вычислить шаг каждой вершины во время выполнения, изучив [D3DFVF](d3dfvf.md) , содержащиеся в описании буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="031db-125">You can calculate the stride of each vertex at run time by examining the [D3DFVF](d3dfvf.md) contained in the vertex buffer description.</span></span> <span data-ttu-id="031db-126">В следующей таблице показан размер каждого компонента вершины.</span><span class="sxs-lookup"><span data-stu-id="031db-126">The following table shows the size for each vertex component.</span></span>



| <span data-ttu-id="031db-127">Флаг формата вершины</span><span class="sxs-lookup"><span data-stu-id="031db-127">Vertex Format Flag</span></span> | <span data-ttu-id="031db-128">Размер</span><span class="sxs-lookup"><span data-stu-id="031db-128">Size</span></span>              |
|--------------------|-------------------|
| <span data-ttu-id="031db-129">D3DFVF \_ диффузный</span><span class="sxs-lookup"><span data-stu-id="031db-129">D3DFVF\_DIFFUSE</span></span>    | <span data-ttu-id="031db-130">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="031db-130">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="031db-131">D3DFVF, \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="031db-131">D3DFVF\_NORMAL</span></span>     | <span data-ttu-id="031db-132">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="031db-132">sizeof(float) x 3</span></span> |
| <span data-ttu-id="031db-133">\_Зеркальное отражение D3DFVF</span><span class="sxs-lookup"><span data-stu-id="031db-133">D3DFVF\_SPECULAR</span></span>   | <span data-ttu-id="031db-134">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="031db-134">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="031db-135">D3DFVF \_ тексн</span><span class="sxs-lookup"><span data-stu-id="031db-135">D3DFVF\_TEXn</span></span>       | <span data-ttu-id="031db-136">sizeof (float) x n</span><span class="sxs-lookup"><span data-stu-id="031db-136">sizeof(float) x n</span></span> |
| <span data-ttu-id="031db-137">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="031db-137">D3DFVF\_XYZ</span></span>        | <span data-ttu-id="031db-138">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="031db-138">sizeof(float) x 3</span></span> |
| <span data-ttu-id="031db-139">D3DFVF \_ ксизрхв</span><span class="sxs-lookup"><span data-stu-id="031db-139">D3DFVF\_XYZRHW</span></span>     | <span data-ttu-id="031db-140">sizeof (float) x 4</span><span class="sxs-lookup"><span data-stu-id="031db-140">sizeof(float) x 4</span></span> |



 

<span data-ttu-id="031db-141">Число координат текстуры, представленных в формате вершины, описывается \_ флагами D3DFVF да n (где n — это значение от 0 до 8).</span><span class="sxs-lookup"><span data-stu-id="031db-141">The number of texture coordinates present in the vertex format is described by the D3DFVF\_TEX n flags (where n is a value from 0 to 8).</span></span> <span data-ttu-id="031db-142">Умножьте число наборов координат текстуры на размер одного набора координат текстуры, которые могут находиться в диапазоне от 1 до четырех с плавающей запятой, чтобы вычислить объем памяти, необходимый для этого числа координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="031db-142">Multiply the number of texture coordinate sets by the size of one set of texture coordinates, which can range from one to four floats, to calculate the memory required for that number of texture coordinates.</span></span>

<span data-ttu-id="031db-143">Используйте итоговый шаг вершины, чтобы увеличить и уменьшить указатель памяти по мере необходимости для доступа к определенным вершинам.</span><span class="sxs-lookup"><span data-stu-id="031db-143">Use the total vertex stride to increment and decrement the memory pointer as needed to access particular vertices.</span></span>

## <a name="retrieving-vertex-buffer-descriptions"></a><span data-ttu-id="031db-144">Получение описания буфера вершин</span><span class="sxs-lookup"><span data-stu-id="031db-144">Retrieving Vertex Buffer Descriptions</span></span>

<span data-ttu-id="031db-145">Сведения о буфере вершин можно получить, вызвав метод [**IDirect3DVertexBuffer9::-DESC**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="031db-145">You can retrieve information about a vertex buffer by calling the [**IDirect3DVertexBuffer9::GetDesc**](/windows/desktop/api) method.</span></span> <span data-ttu-id="031db-146">Этот метод заполняет члены структуры [**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md) сведениями о буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="031db-146">This method fills the members of the [**D3DVERTEXBUFFER\_DESC**](d3dvertexbuffer-desc.md) structure with information about the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="031db-147">См. также</span><span class="sxs-lookup"><span data-stu-id="031db-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="031db-148">Буферы вершин</span><span class="sxs-lookup"><span data-stu-id="031db-148">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
