---
description: В этом разделе описываются шейдеры, которые можно использовать для программируемой модели потока.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Программирование одного или нескольких потоков (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710626"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a><span data-ttu-id="601b7-103">Программирование одного или нескольких потоков (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="601b7-103">Programming One or More Streams (Direct3D 9)</span></span>

<span data-ttu-id="601b7-104">В этом разделе описываются шейдеры, которые можно использовать для программируемой модели потока.</span><span class="sxs-lookup"><span data-stu-id="601b7-104">This section describes shaders that can be used for the programmable stream model.</span></span>

## <a name="using-streams"></a><span data-ttu-id="601b7-105">Использование потоков</span><span class="sxs-lookup"><span data-stu-id="601b7-105">Using Streams</span></span>

<span data-ttu-id="601b7-106">В DirectX 8 представлено понятие потока для привязки данных к входным регистрам для использования шейдерами.</span><span class="sxs-lookup"><span data-stu-id="601b7-106">DirectX 8 introduced the notion of a stream to bind data to input registers for use by shaders.</span></span> <span data-ttu-id="601b7-107">Поток — это универсальный массив данных компонента, каждый компонент которого состоит из одного или нескольких элементов, представляющих одну сущность, такую как «расположение», «нормальный», «цвет» и т. д.</span><span class="sxs-lookup"><span data-stu-id="601b7-107">A stream is a uniform array of component data, where each component consists of one or more elements that represent a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="601b7-108">Потоки позволяют графическим микросхемам выполнять прямой доступ к памяти из нескольких буферов вершин, а также обеспечивать более естественное сопоставление данных приложения.</span><span class="sxs-lookup"><span data-stu-id="601b7-108">Streams enable graphic chips to perform a direct memory access from multiple vertex buffers in parallel and also provide a more natural mapping from application data.</span></span> <span data-ttu-id="601b7-109">Они также позволяют использовать тривиальные многотекстурные и многопроходные.</span><span class="sxs-lookup"><span data-stu-id="601b7-109">They also enable trivial multitexture versus multipass.</span></span> <span data-ttu-id="601b7-110">Его следует рассматривать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="601b7-110">Think of it like this:</span></span>

-   <span data-ttu-id="601b7-111">Вершина состоит из n потоков.</span><span class="sxs-lookup"><span data-stu-id="601b7-111">A vertex is composed of n streams.</span></span>
-   <span data-ttu-id="601b7-112">Поток состоит из элементов m.</span><span class="sxs-lookup"><span data-stu-id="601b7-112">A stream is composed of m elements.</span></span>
-   <span data-ttu-id="601b7-113">Элемент — это \[ положение, цвет, нормальная Координата текстуры \] .</span><span class="sxs-lookup"><span data-stu-id="601b7-113">An element is \[position, color, normal, texture coordinate\].</span></span>

<span data-ttu-id="601b7-114">Метод [**IDirect3DDevice9:: сетстреамсаурце**](/windows/desktop/api) привязывает буфер вершин к потоку данных устройства, создавая связь между данными вершин и одним из нескольких портов потока данных, которые передаются примитивным функциям обработки.</span><span class="sxs-lookup"><span data-stu-id="601b7-114">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="601b7-115">Фактические ссылки на потоковые данные не выполняются до тех пор, пока не будет вызван метод рисования, например [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="601b7-115">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="601b7-116">Сопоставление входных элементов вершины с входными регистрами вершин для программируемых шейдеров вершин определяется в объявлении шейдера, но входные элементы вершины не имеют определенной семантики их использования.</span><span class="sxs-lookup"><span data-stu-id="601b7-116">The mapping of the input vertex elements to the vertex input registers for programmable vertex shaders is defined in the shader declaration, but the input vertex elements do not have specific semantics about their use.</span></span> <span data-ttu-id="601b7-117">Интерпретация входных элементов вершин программируется с помощью инструкций шейдера.</span><span class="sxs-lookup"><span data-stu-id="601b7-117">The interpretation of the input vertex elements is programmed using the shader instructions.</span></span> <span data-ttu-id="601b7-118">Функция шейдера вершин определяется массивом инструкций, которые применяются к каждой вершине.</span><span class="sxs-lookup"><span data-stu-id="601b7-118">The vertex shader function is defined by an array of instructions that are applied to each vertex.</span></span> <span data-ttu-id="601b7-119">Выходные регистры вершин явным образом записываются в, используя инструкции в функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="601b7-119">The vertex output registers are explicitly written to, using instructions in the shader function.</span></span>

<span data-ttu-id="601b7-120">Тем не менее, в этом обсуждении стоит меньше внимания на семантической сопоставлении элементов для регистрации и, что более важно для использования потоков и проблемы, решаемой с помощью потоков.</span><span class="sxs-lookup"><span data-stu-id="601b7-120">For this discussion, though, be less concerned with the semantic mapping of elements to registers and more concerned with the reason for using streams and what problem is solved by using streams.</span></span> <span data-ttu-id="601b7-121">Основное преимущество потоков заключается в том, что они удаляют затраты на вершину данных, ранее связанные с многотекстурной обсчетом.</span><span class="sxs-lookup"><span data-stu-id="601b7-121">The main benefit of streams is that they remove the vertex data costs previously associated with multitexturing.</span></span> <span data-ttu-id="601b7-122">Перед потоками пользователь должен был либо дублировать наборы данных вершин, чтобы обрабатывать одиночный и многотекстурный регистр без неиспользуемых элементов данных, либо содержать элементы данных, которые не будут использоваться, за исключением многотекстурного случая.</span><span class="sxs-lookup"><span data-stu-id="601b7-122">Before streams, a user had to either duplicate vertex data sets to handle the single and multitexture case with no unused data elements, or carry data elements that would be unused except in the multitexture case.</span></span>

<span data-ttu-id="601b7-123">Ниже приведен пример использования двух наборов данных вершин: один для одной текстуры и один для многотекстурного.</span><span class="sxs-lookup"><span data-stu-id="601b7-123">Here is an example of using two sets of vertex data, one for single texture and one for multitexturing.</span></span>


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="601b7-124">Альтернативой было наличие одного элемента вершины, содержащего оба набора координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="601b7-124">The alternative was to have a single vertex element that contained both sets of texture coordinates.</span></span>


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="601b7-125">При использовании этих данных вершин только одна копия данных о положении и цвете переносится в память, за счет того, что оба набора координат текстуры обрабатываются для отрисовки даже в одном случае текстуры.</span><span class="sxs-lookup"><span data-stu-id="601b7-125">With this vertex data, only one copy of the position and color data are carried in memory, at the expense of carrying both sets of texture coordinates around for rendering even in the single texture case.</span></span>

<span data-ttu-id="601b7-126">Теперь, когда компромисс понятен, потоки предоставляют элегантное исправление для этого дилеммой.</span><span class="sxs-lookup"><span data-stu-id="601b7-126">Now that the tradeoff is clear, streams provide an elegant fix to this dilemma.</span></span> <span data-ttu-id="601b7-127">Ниже приведен набор определений вершин для поддержки трех потоков: один с положением и цветом, один с первым набором координат текстуры, а второй — со вторым набором координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="601b7-127">Here is a set of vertex definitions to support three streams: one with position and color, one with the first set of texture coordinates, and one with the second set of texture coordinates.</span></span>


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



<span data-ttu-id="601b7-128">Объявление вершины будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="601b7-128">The vertex declaration would be as follows:</span></span>


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



<span data-ttu-id="601b7-129">Теперь создайте объект объявления вершины и задайте его, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="601b7-129">Now create the vertex declaration object and set it as shown:</span></span>


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a><span data-ttu-id="601b7-130">Примеры комбинаций</span><span class="sxs-lookup"><span data-stu-id="601b7-130">Examples of Combinations</span></span>

### <a name="one-stream-diffuse-color"></a><span data-ttu-id="601b7-131">Один поток рассеянный цвет</span><span class="sxs-lookup"><span data-stu-id="601b7-131">One Stream Diffuse Color</span></span>

<span data-ttu-id="601b7-132">Объявления вершин и параметры потока для рендеринга рассеянного цвета будут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="601b7-132">The vertex declaration and stream settings for diffuse color rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a><span data-ttu-id="601b7-133">Два потока с цветом и текстурой</span><span class="sxs-lookup"><span data-stu-id="601b7-133">Two Streams with Color and Texture</span></span>

<span data-ttu-id="601b7-134">Объявления вершин и параметры потока для отрисовки одной текстуры будут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="601b7-134">The vertex declaration and stream settings for single texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a><span data-ttu-id="601b7-135">Два потока с цветом и двумя текстурами</span><span class="sxs-lookup"><span data-stu-id="601b7-135">Two Streams with Color and two Textures</span></span>

<span data-ttu-id="601b7-136">Объявления вершин и параметры потока для отрисовки с несколькими текстурами будут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="601b7-136">The vertex declaration and stream settings for two-texture multi-texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



<span data-ttu-id="601b7-137">В каждом случае достаточно [**:D IDirect3DDevice9ного вызова равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="601b7-137">In every case, the following [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) invocation suffices.</span></span>


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



<span data-ttu-id="601b7-138">Это показывает гибкость потоков в решении проблемы дублирования данных и избыточной передачи данных по шине (то есть расход полосы пропускания).</span><span class="sxs-lookup"><span data-stu-id="601b7-138">This shows the flexibility of streams in solving the problem of data duplication/redundant data transmission across the bus (that is, of wasting bandwidth).</span></span>

## <a name="related-topics"></a><span data-ttu-id="601b7-139">См. также</span><span class="sxs-lookup"><span data-stu-id="601b7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="601b7-140">Объявление вершины</span><span class="sxs-lookup"><span data-stu-id="601b7-140">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
