---
description: Описывает отдельный элемент вершины в объявлении вершины.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: вертекселемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 049511c89b335c0da31a9f41344082c3b818fa0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140147"
---
# <a name="vertexelement"></a><span data-ttu-id="0de2e-103">вертекселемент</span><span class="sxs-lookup"><span data-stu-id="0de2e-103">VertexElement</span></span>

<span data-ttu-id="0de2e-104">Описывает отдельный элемент вершины в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="0de2e-104">Describes an individual vertex element in a vertex declaration.</span></span>

``` syntax
template VertexElement 
{ 
    < F752461C-1E23-48f6-B9F8-8350850F336F > 
    DWORD Type; 
    DWORD Method; 
    DWORD Usage; 
    DWORD UsageIndex; 
} 
```

<span data-ttu-id="0de2e-105">Где:</span><span class="sxs-lookup"><span data-stu-id="0de2e-105">Where:</span></span>

-   <span data-ttu-id="0de2e-106">Тип-вершинный тип данных.</span><span class="sxs-lookup"><span data-stu-id="0de2e-106">Type - Vertex data type.</span></span> <span data-ttu-id="0de2e-107">См. [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="0de2e-107">See [**D3DDECLTYPE**](./d3ddecltype.md).</span></span>
-   <span data-ttu-id="0de2e-108">Метод обработки для тесселяции метода.</span><span class="sxs-lookup"><span data-stu-id="0de2e-108">Method - Tessellator processing method.</span></span> <span data-ttu-id="0de2e-109">См. [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="0de2e-109">See [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>
-   <span data-ttu-id="0de2e-110">Использование данных вершин, предназначенное для использования.</span><span class="sxs-lookup"><span data-stu-id="0de2e-110">Usage - Intended use of the vertex data.</span></span> <span data-ttu-id="0de2e-111">См. [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="0de2e-111">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>
-   <span data-ttu-id="0de2e-112">Усажеиндекс — изменяет данные об использовании.</span><span class="sxs-lookup"><span data-stu-id="0de2e-112">UsageIndex - Modifies the usage data.</span></span> <span data-ttu-id="0de2e-113">См. [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="0de2e-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0de2e-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0de2e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de2e-115">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="0de2e-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="0de2e-116">**D3DVERTEXELEMENT9**</span><span class="sxs-lookup"><span data-stu-id="0de2e-116">**D3DVERTEXELEMENT9**</span></span>](d3dvertexelement9.md)
</dt> </dl>

 

 
