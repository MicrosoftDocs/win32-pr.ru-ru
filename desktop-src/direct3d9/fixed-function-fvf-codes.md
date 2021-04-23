---
description: Код ФВФ описывает содержимое вершин, хранимых чередованием, в одном потоке данных.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Фиксированные коды ФВФ функций (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701097"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a><span data-ttu-id="0e620-103">Фиксированные коды ФВФ функций (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0e620-103">Fixed Function FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="0e620-104">Код ФВФ описывает содержимое вершин, хранимых чередованием, в одном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="0e620-104">A FVF code describes the contents of vertices stored interleaved in a single data stream.</span></span> <span data-ttu-id="0e620-105">Обычно в нем указываются данные, которые должны обрабатываться конвейером обработки вершин фиксированной функции.</span><span class="sxs-lookup"><span data-stu-id="0e620-105">It generally specifies data to be processed by the fixed function vertex processing pipeline.</span></span> <span data-ttu-id="0e620-106">Это объявление вершины в старом стиле; чтобы просмотреть текущий стиль объявления вершины, см. раздел [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="0e620-106">This is an older-style vertex declaration; to see the current vertex declaration style, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="0e620-107">Приложения Direct3D могут определять вершины модели различными способами.</span><span class="sxs-lookup"><span data-stu-id="0e620-107">Direct3D applications can define model vertices in several different ways.</span></span> <span data-ttu-id="0e620-108">Поддержка гибких определений вершин, также известных как гибкие форматы вершин или гибкие коды форматов вершин, позволяет вашему приложению использовать только необходимые компоненты вершин, устраняя неиспользуемые компоненты.</span><span class="sxs-lookup"><span data-stu-id="0e620-108">Support for flexible vertex definitions, also known as flexible vertex formats or flexible vertex format codes, makes it possible for your application to use only the vertex components it needs, eliminating those components that aren't used.</span></span> <span data-ttu-id="0e620-109">Используя только необходимые компоненты вершины, приложение может сэкономить память и снизить пропускную способность обработки, необходимую для отрисовки моделей.</span><span class="sxs-lookup"><span data-stu-id="0e620-109">By using only the needed vertex components, your application can conserve memory and minimize the processing bandwidth required to render models.</span></span> <span data-ttu-id="0e620-110">Описание форматирования вершин можно описать с помощью сочетания [D3DFVF](d3dfvf.md) кодов.</span><span class="sxs-lookup"><span data-stu-id="0e620-110">You describe how your vertices are formatted by using a combination of [D3DFVF](d3dfvf.md) codes.</span></span>

<span data-ttu-id="0e620-111">Спецификация ФВФ включает в себя форматы размера точки, заданные параметром D3DFVF \_ псизе.</span><span class="sxs-lookup"><span data-stu-id="0e620-111">The FVF specification includes formats for point size, specified by D3DFVF\_PSIZE.</span></span> <span data-ttu-id="0e620-112">Этот размер выражается в единицах области камеры для непреобразованных и освещенных вершин (TL) и в единицах устройства для вершин TL.</span><span class="sxs-lookup"><span data-stu-id="0e620-112">This size is expressed in camera space units for non-transformed and lit (TL) vertices, and in device-space units for TL vertices.</span></span>

<span data-ttu-id="0e620-113">Методы отрисовки интерфейса [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) предоставляют приложения C++ с методами, которые принимают сочетание этих флагов и используют их для определения способа отрисовки примитивов.</span><span class="sxs-lookup"><span data-stu-id="0e620-113">The rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface provide C++ applications with methods that accept a combination of these flags, and use them to determine how to render primitives.</span></span> <span data-ttu-id="0e620-114">По сути, эти флаги указывают системе, какие компоненты вершины — расположение, весовые коэффициенты смешивания вершин, нормальные, цвета и число и формат координат текстуры — приложение использует и, косвенно, какие части конвейера отрисовки, к которому требуется применить Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0e620-114">Basically, these flags tell the system which vertex components - position, vertex blending weights, normal, colors, and the number and format of texture coordinates - your application uses and, indirectly, which parts of the rendering pipeline you want Direct3D to apply to them.</span></span> <span data-ttu-id="0e620-115">Кроме того, присутствие или отсутствие определенного флага формата вершины обменивается данными с системой, в которой находятся поля компонентов вершины в памяти и которые были пропущены.</span><span class="sxs-lookup"><span data-stu-id="0e620-115">In addition, the presence or absence of a particular vertex format flag communicates to the system which vertex component fields are present in memory and which you've omitted.</span></span>

<span data-ttu-id="0e620-116">Чтобы определить ограничения для устройств, можно запросить у устройства значения D3DFVFCAPS \_ донотстрипелементс и D3DFVFCAPS \_ текскурдкаунтмаск в фвфкапс-члене [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="0e620-116">To determine device limitations, you can query a device for the values of D3DFVFCAPS\_DONOTSTRIPELEMENTS and D3DFVFCAPS\_TEXCOORDCOUNTMASK in the FVFCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="0e620-117">Координаты текстуры могут быть объявлены в разных форматах, что позволяет адресовать текстуры с помощью как минимум одной координаты или до четырех координат текстуры (для 2D-прогнозируемых координат текстуры).</span><span class="sxs-lookup"><span data-stu-id="0e620-117">Texture coordinates can be declared in different formats, allowing textures to be addressed using as few as one coordinate or as many as four texture coordinates (for 2D projected texture coordinates).</span></span> <span data-ttu-id="0e620-118">Дополнительные сведения см. в разделе [форматы координат текстуры (Direct3D 9)](texture-coordinate-formats.md).</span><span class="sxs-lookup"><span data-stu-id="0e620-118">For more information, see [Texture Coordinate Formats (Direct3D 9)](texture-coordinate-formats.md).</span></span> <span data-ttu-id="0e620-119">Используйте набор макросов [**D3DFVF \_ текскурдсизен**](d3dfvf-texcoordsizen.md) для создания битовых шаблонов, которые указывают форматы координат текстуры, используемые в вашем формате вершин.</span><span class="sxs-lookup"><span data-stu-id="0e620-119">Use the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros to create bit patterns that identify the texture coordinate formats that your vertex format uses.</span></span>

<span data-ttu-id="0e620-120">Ни один из приложений не будет использовать каждый компонент.</span><span class="sxs-lookup"><span data-stu-id="0e620-120">No application will use every component.</span></span> <span data-ttu-id="0e620-121">Поля взаимного однородного W (РХВ) и нормали вершины являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="0e620-121">The reciprocal homogeneous W (RHW) and vertex normal fields are mutually exclusive.</span></span> <span data-ttu-id="0e620-122">И большинство приложений пытаются использовать все восемь наборов координат текстуры, но это может быть у Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0e620-122">Nor will most applications try to use all eight sets of texture coordinates, but Direct3D has this capacity.</span></span> <span data-ttu-id="0e620-123">Существует несколько ограничений на флаги, которые можно использовать с другими флагами.</span><span class="sxs-lookup"><span data-stu-id="0e620-123">There are several restrictions on which flags you can use with other flags.</span></span> <span data-ttu-id="0e620-124">Например, нельзя \_ одновременно использовать флаги D3DFVF XYZ и D3DFVF \_ ксизрхв, так как это указывает, что приложение описывает расположение вершины как непреобразованные, так и преобразованные вершины.</span><span class="sxs-lookup"><span data-stu-id="0e620-124">For example, you cannot use the D3DFVF\_XYZ and D3DFVF\_XYZRHW flags together, as this would indicate that your application is describing a vertex's position with both untransformed and transformed vertices.</span></span>

<span data-ttu-id="0e620-125">Чтобы использовать индексированное смешение вершин, в \_ \_ конце объявления фвф должен ПОЯВИТЬСЯ флаг D3DFVF ластбета UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="0e620-125">To use indexed vertex blending, the D3DFVF\_LASTBETA\_UBYTE4 flag should appear at the end of the FVF declaration.</span></span> <span data-ttu-id="0e620-126">Наличие этого флага означает, что Пятый вес смешивания будет рассматриваться как DWORD, а не как float.</span><span class="sxs-lookup"><span data-stu-id="0e620-126">The presence of this flag indicates that the fifth blending weight will be treated as a DWORD instead of float.</span></span> <span data-ttu-id="0e620-127">Дополнительные сведения см. в разделе [индексирование вершинного смешения (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="0e620-127">For more information, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span>

<span data-ttu-id="0e620-128">В следующих примерах кода показано различие между кодом ФВФ, в котором используется \_ флаг D3DFVF ластбета \_ UBYTE4, и другой.</span><span class="sxs-lookup"><span data-stu-id="0e620-128">The following code samples shows the difference between an FVF code that uses the D3DFVF\_LASTBETA\_UBYTE4 flag and one that doesn't.</span></span> <span data-ttu-id="0e620-129">Флаг D3DFVF \_ XYZB3 существует, когда используются четыре индекса смешения, так как всегда вычитаются сумма первых трех значений из числа, чтобы получить четвертый (Blend ₄ = 1-(Blend ₁ + Blend ₂ + Blend ₃)).</span><span class="sxs-lookup"><span data-stu-id="0e620-129">The flag D3DFVF\_XYZB3 is present when four blending indices are used because you always subtract the sum of the first three from the number one to obtain the fourth (blend₄ = 1 - (blend₁ + blend₂ + blend₃)).</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



<span data-ttu-id="0e620-130">В ФВФ, определенном ниже, \_ используется \_ флаг D3DFVF Last UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="0e620-130">The FVF defined below uses the D3DFVF\_LAST\_UBYTE4 flag.</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a><span data-ttu-id="0e620-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0e620-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e620-132">Объявление вершины</span><span class="sxs-lookup"><span data-stu-id="0e620-132">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
