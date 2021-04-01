---
description: Дополнительный набор интерфейсов отрисовки поддерживает передачу данных вершин и индексов непосредственно из указателей памяти пользователя. Эти интерфейсы поддерживают только один поток данных вершин. Дополнительные сведения см. в следующих справочных разделах.
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: Отрисовка из указателей памяти пользователя (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b5499032e6fb92ea0f363bba2bd5fd961e53c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262418"
---
# <a name="rendering-from-user-memory-pointers-direct3d-9"></a><span data-ttu-id="85dae-105">Отрисовка из указателей памяти пользователя (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85dae-105">Rendering from User Memory Pointers (Direct3D 9)</span></span>

<span data-ttu-id="85dae-106">Дополнительный набор интерфейсов отрисовки поддерживает передачу данных вершин и индексов непосредственно из указателей памяти пользователя.</span><span class="sxs-lookup"><span data-stu-id="85dae-106">A secondary set of rendering interfaces supports passing vertex and index data directly from user memory pointers.</span></span> <span data-ttu-id="85dae-107">Эти интерфейсы поддерживают только один поток данных вершин.</span><span class="sxs-lookup"><span data-stu-id="85dae-107">These interfaces support a single stream of vertex data only.</span></span> <span data-ttu-id="85dae-108">Дополнительные сведения см. в следующих справочных разделах.</span><span class="sxs-lookup"><span data-stu-id="85dae-108">For more information, see the following reference topics.</span></span>

-   [<span data-ttu-id="85dae-109">**IDirect3DDevice9::DrawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="85dae-109">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
-   [<span data-ttu-id="85dae-110">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="85dae-110">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)

<span data-ttu-id="85dae-111">Эти методы отображаются с данными, заданными указателями памяти пользователя, а не буферами вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="85dae-111">These methods render with data specified by user memory pointers, instead of vertex and index buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85dae-112">См. также</span><span class="sxs-lookup"><span data-stu-id="85dae-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85dae-113">Отрисовка примитивов</span><span class="sxs-lookup"><span data-stu-id="85dae-113">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
