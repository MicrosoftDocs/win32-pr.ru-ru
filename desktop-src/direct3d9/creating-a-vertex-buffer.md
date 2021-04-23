---
description: 'Объект буфера вершин создается путем вызова метода IDirect3DDevice9:: Креатевертексбуффер, который принимает пять параметров.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Создание буфера вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710783"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="8ecbf-103">Создание буфера вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8ecbf-103">Creating a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="8ecbf-104">Объект буфера вершин создается путем вызова метода [**IDirect3DDevice9:: креатевертексбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , который принимает пять параметров.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-104">You create a vertex buffer object by calling the [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method, which accepts five parameters.</span></span> <span data-ttu-id="8ecbf-105">Первый параметр указывает длину буфера вершин в байтах.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-105">The first parameter specifies the vertex buffer length, in bytes.</span></span> <span data-ttu-id="8ecbf-106">Используйте оператор sizeof для определения размера формата вершины в байтах.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-106">Use the sizeof operator to determine the size of a vertex format, in bytes.</span></span> <span data-ttu-id="8ecbf-107">Рассмотрим следующий пользовательский формат вершин.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-107">Consider the following custom vertex format.</span></span>


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



<span data-ttu-id="8ecbf-108">Чтобы создать буфер вершин для хранения четырех структур КУСТОМВЕРТЕКС, укажите \[ \* \] в параметре *length* 4 sizeof (кустомвертекс).</span><span class="sxs-lookup"><span data-stu-id="8ecbf-108">To create a vertex buffer to hold four CUSTOMVERTEX structures, specify \[4\*sizeof(CUSTOMVERTEX)\] for the *Length* parameter.</span></span>

<span data-ttu-id="8ecbf-109">Второй параметр — это набор элементов управления использованием.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-109">The second parameter is a set of usage controls.</span></span> <span data-ttu-id="8ecbf-110">Помимо прочего, его значение определяет, может ли буфер вершин содержать сведения об обрезке в форме флагов клипов — для вершин, которые существуют за пределами области просмотра.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-110">Among other things, its value determines whether the vertex buffer is capable of containing clipping information - in the form of clip flags - for vertices that exist outside the viewing area.</span></span> <span data-ttu-id="8ecbf-111">Чтобы создать буфер вершин, который не может содержать флаги обрезки, включите \_ флаг D3DUSAGE донотклип для параметра *использования* .</span><span class="sxs-lookup"><span data-stu-id="8ecbf-111">To create a vertex buffer that cannot contain clip flags, include the D3DUSAGE\_DONOTCLIP flag for the *Usage* parameter.</span></span> <span data-ttu-id="8ecbf-112">Флаг D3DUSAGE \_ донотклип применяется только в том случае, если также указано, что буфер вершин будет содержать преобразованные вершины — флаг D3DFVF \_ ксизрхв включен в параметр *фвф* .</span><span class="sxs-lookup"><span data-stu-id="8ecbf-112">The D3DUSAGE\_DONOTCLIP flag is applied only if you also indicate that the vertex buffer will contain transformed vertices - the D3DFVF\_XYZRHW flag is included in the *FVF* parameter.</span></span> <span data-ttu-id="8ecbf-113">Метод [**IDirect3DDevice9:: креатевертексбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) ИГНОРИРУЕТ \_ флаг D3DUSAGE донотклип, если вы указываете, что буфер будет содержать непреобразованные вершины ( \_ флаг D3DFVF XYZ).</span><span class="sxs-lookup"><span data-stu-id="8ecbf-113">The [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method ignores the D3DUSAGE\_DONOTCLIP flag if you indicate that the buffer will contain untransformed vertices (the D3DFVF\_XYZ flag).</span></span> <span data-ttu-id="8ecbf-114">Флаги обрезки занимают дополнительную память, что делает буфер вершин, поддерживающий отрезки, немного больше, чем буфер вершин, в котором не может составляться флаги обрезки.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-114">Clipping flags occupy additional memory, making a clipping-capable vertex buffer slightly larger than a vertex buffer incapable of containing clipping flags.</span></span> <span data-ttu-id="8ecbf-115">Так как эти ресурсы выделяются при создании буфера вершин, необходимо заранее запросить буфер вершин, поддерживающий обрезку.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-115">Because these resources are allocated when the vertex buffer is created, you must request a clipping-capable vertex buffer ahead of time.</span></span>

<span data-ttu-id="8ecbf-116">Третий параметр, *фвф*, представляет собой сочетание [D3DFVF](d3dfvf.md) , описывающее формат вершины буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-116">The third parameter, *FVF*, is a combination of [D3DFVF](d3dfvf.md) that describe the vertex format of the vertex buffer.</span></span> <span data-ttu-id="8ecbf-117">Если для этого параметра задано значение 0, то буфер вершин представляет собой буфер вершин, отличный от ФВФ.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-117">If you specify 0 for this parameter, then the vertex buffer is a non-FVF vertex buffer.</span></span> <span data-ttu-id="8ecbf-118">Дополнительные сведения см. в разделе [Фвф вершинные буферы (Direct3D 9)](fvf-vertex-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="8ecbf-118">For more information, see [FVF Vertex Buffers (Direct3D 9)](fvf-vertex-buffers.md).</span></span> <span data-ttu-id="8ecbf-119">Четвертый параметр описывает класс памяти, в который помещается буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-119">The fourth parameter describes the memory class into which to place the vertex buffer.</span></span>

<span data-ttu-id="8ecbf-120">Последний параметр, [**IDirect3DDevice9:: креатевертексбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , принимает адрес переменной, которая будет заполнена указателем на новый интерфейс [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) объекта буфера вершин, если вызов завершается.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-120">The final parameter that [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accepts is the address of a variable that will be filled with a pointer to the new [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface of the vertex buffer object, if the call succeeds.</span></span>

<span data-ttu-id="8ecbf-121">Нельзя создавать флаги клипов для буфера вершин, созданного без поддержки.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-121">You cannot produce clip flags for a vertex buffer that was created without support for them.</span></span>

<span data-ttu-id="8ecbf-122">В следующем примере кода C++ показано, что создание буфера вершин может выглядеть как в коде.</span><span class="sxs-lookup"><span data-stu-id="8ecbf-122">The following C++ code example shows what creating a vertex buffer might look like in code.</span></span>


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a><span data-ttu-id="8ecbf-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8ecbf-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ecbf-124">Буферы вершин</span><span class="sxs-lookup"><span data-stu-id="8ecbf-124">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
