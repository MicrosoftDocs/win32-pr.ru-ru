---
description: При использовании запрограммированного шейдера вершин элементы, обновленные в целевом буфере вершин, контролируются программой-функцией шейдера.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Программируемая обработка вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691990"
---
# <a name="programmable-vertex-processing-direct3d-9"></a><span data-ttu-id="bce4a-103">Программируемая обработка вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bce4a-103">Programmable Vertex Processing (Direct3D 9)</span></span>

<span data-ttu-id="bce4a-104">При использовании запрограммированного шейдера вершин элементы, обновленные в целевом буфере вершин, контролируются программой-функцией шейдера.</span><span class="sxs-lookup"><span data-stu-id="bce4a-104">When using a programmed vertex shader, the elements updated in the destination vertex buffer are controlled by the shader function program.</span></span> <span data-ttu-id="bce4a-105">Когда приложение записывает данные в один из конечных реестров вершин, обновляется соответствующий элемент в каждой вершине целевого буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="bce4a-105">When the application writes to one of the destination vertex registers, the corresponding element within each vertex of the destination vertex buffer is updated.</span></span> <span data-ttu-id="bce4a-106">Элементы в целевом буфере вершин, которые не записываются приложением, не изменяются.</span><span class="sxs-lookup"><span data-stu-id="bce4a-106">Elements in the destination vertex buffer that are not written to by the application are not modified.</span></span> <span data-ttu-id="bce4a-107">[**IDirect3DDevice9::P роцессвертицес**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) завершится ошибкой, если приложение записывает данные в элементы, отсутствующие в целевом буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="bce4a-107">[**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) will fail if the application writes to elements that are not present in the destination vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bce4a-108">См. также</span><span class="sxs-lookup"><span data-stu-id="bce4a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce4a-109">Буферы вершин</span><span class="sxs-lookup"><span data-stu-id="bce4a-109">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
