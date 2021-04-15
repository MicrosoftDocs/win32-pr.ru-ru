---
description: Текстуры тома — это трехмерные коллекции пикселей (пикселей текстуры), которые можно использовать для рисования двумерного примитива, такого как треугольник или линия.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Ресурсы текстуры тома (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c66ff97d04e3c7c6c0a032f9a230dfd511b38c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569849"
---
# <a name="volume-texture-resources-direct3d-9"></a><span data-ttu-id="7d857-103">Ресурсы текстуры тома (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7d857-103">Volume Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="7d857-104">Текстуры тома — это трехмерные коллекции пикселей (пикселей текстуры), которые можно использовать для рисования двумерного примитива, такого как треугольник или линия.</span><span class="sxs-lookup"><span data-stu-id="7d857-104">Volume textures are three-dimensional collections of pixels (texels) that can be used to paint a two-dimensional primitive such as a triangle or a line.</span></span> <span data-ttu-id="7d857-105">Для каждой вершины примитива, который должен быть текстурирован с помощью тома, необходимы координаты текстуры из трех элементов.</span><span class="sxs-lookup"><span data-stu-id="7d857-105">Three-element texture coordinates are required for each vertex of a primitive that is to be textured with a volume.</span></span> <span data-ttu-id="7d857-106">При прорисовке примитива Каждая содержащаяся точка заполняется значением цвета из некоторой точки в томе в соответствии с правилами, аналогичными правилам двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="7d857-106">As the primitive is drawn, each contained pixel is filled with the color value from some pixel within the volume, in accordance with rules analogous to the two-dimensional texture case.</span></span> <span data-ttu-id="7d857-107">Тома не подготавливаются к просмотру напрямую из-за отсутствия трехмерных примитивов, которые могут быть окрашены.</span><span class="sxs-lookup"><span data-stu-id="7d857-107">Volumes are not rendered directly because there are no three-dimensional primitives that can be painted with them.</span></span>

<span data-ttu-id="7d857-108">Текстуры тома можно использовать для специальных эффектов, таких как туманы с исправлениями, взрывные развертывания и т. д.</span><span class="sxs-lookup"><span data-stu-id="7d857-108">You can use volume textures for special effects such as patchy fog, explosions, and so on.</span></span>

<span data-ttu-id="7d857-109">Тома организованы в срезы и могут быть представлены в виде двумерных поверхностей с шириной x высота, которые помещаются в стек, чтобы сделать ширину x высота x глубины.</span><span class="sxs-lookup"><span data-stu-id="7d857-109">Volumes are organized into slices and can be thought of as width x height 2D surfaces stacked to make a width x height x depth volume.</span></span> <span data-ttu-id="7d857-110">Каждый срез является одной строкой.</span><span class="sxs-lookup"><span data-stu-id="7d857-110">Each slice is a single row.</span></span> <span data-ttu-id="7d857-111">Тома могут иметь последующие уровни, в которых размер каждого уровня усекается до половины измерений предыдущего уровня.</span><span class="sxs-lookup"><span data-stu-id="7d857-111">Volumes can have subsequent levels in which the dimensions of each level are truncated to half the dimensions of the previous level.</span></span> <span data-ttu-id="7d857-112">На следующей диаграмме показано, как выглядит текстура тома с несколькими уровнями.</span><span class="sxs-lookup"><span data-stu-id="7d857-112">The following diagram shows what a volume texture with multiple levels looks like.</span></span>

![Схема текстуры тома с представлениями Куба 8x2x4, 4x1x2 и 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a><span data-ttu-id="7d857-114">Создание текстуры тома</span><span class="sxs-lookup"><span data-stu-id="7d857-114">Creating a Volume Texture</span></span>

<span data-ttu-id="7d857-115">В приведенных ниже примерах кода показаны шаги, необходимые для использования текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="7d857-115">The code examples below show the steps required to use a volume texture.</span></span>

<span data-ttu-id="7d857-116">Сначала укажите пользовательский тип вершины с тремя координатами текстуры для каждой вершины, как показано в этом примере кода.</span><span class="sxs-lookup"><span data-stu-id="7d857-116">First, specify a custom vertex type that has three texture coordinates for each vertex, as shown in this code example.</span></span>


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



<span data-ttu-id="7d857-117">Затем заполните вершины данными.</span><span class="sxs-lookup"><span data-stu-id="7d857-117">Next, fill the vertices with data.</span></span>


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



<span data-ttu-id="7d857-118">Теперь создайте буфер вершин и заполните его данными из вершин.</span><span class="sxs-lookup"><span data-stu-id="7d857-118">Now, create a vertex buffer and fill it with data from the vertices.</span></span>

<span data-ttu-id="7d857-119">Следующим шагом является использование метода [**IDirect3DDevice9:: креатеволуметекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) для создания текстуры тома, как показано в этом примере кода.</span><span class="sxs-lookup"><span data-stu-id="7d857-119">The next step is to use the [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) method to create a volume texture, as shown in this code example.</span></span>


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



<span data-ttu-id="7d857-120">Перед отрисовкой примитива установите текущую текстуру в текстуру тома, созданную выше.</span><span class="sxs-lookup"><span data-stu-id="7d857-120">Before rendering the primitive, set the current texture to the volume texture created above.</span></span> <span data-ttu-id="7d857-121">В приведенном ниже примере кода показан весь процесс отрисовки для полос треугольников.</span><span class="sxs-lookup"><span data-stu-id="7d857-121">The code example below shows the entire rendering process for a strip of triangles.</span></span>


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a><span data-ttu-id="7d857-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7d857-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d857-123">Текстуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="7d857-123">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
