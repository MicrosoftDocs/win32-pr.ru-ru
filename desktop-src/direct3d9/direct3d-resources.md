---
description: Ресурсы — это текстуры и буферы, используемые для отрисовки сцены.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Ресурсы Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139983"
---
# <a name="direct3d-resources-direct3d-9"></a><span data-ttu-id="f4d8b-103">Ресурсы Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4d8b-103">Direct3D Resources (Direct3D 9)</span></span>

<span data-ttu-id="f4d8b-104">Ресурсы — это текстуры и буферы, используемые для отрисовки сцены.</span><span class="sxs-lookup"><span data-stu-id="f4d8b-104">Resources are the textures and buffers that are used to render a scene.</span></span> <span data-ttu-id="f4d8b-105">Приложения должны создавать, загружать, копировать и использовать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f4d8b-105">Applications need to create, load, copy, and use resources.</span></span> <span data-ttu-id="f4d8b-106">В этом разделе приводятся краткие сведения о ресурсах и действиях и методах, используемых приложениями при работе с ресурсами.</span><span class="sxs-lookup"><span data-stu-id="f4d8b-106">This section gives a brief introduction to resources and the steps and methods used by applications when working with resources.</span></span>

<span data-ttu-id="f4d8b-107">Все ресурсы, включая геометрические ресурсы [**IDirect3DIndexBuffer9**](/windows/desktop/api) и [**IDirect3DVertexBuffer9**](/windows/desktop/api), наследуются от интерфейса [**IDirect3DResource9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="f4d8b-107">All resources, including the geometry resources [**IDirect3DIndexBuffer9**](/windows/desktop/api) and [**IDirect3DVertexBuffer9**](/windows/desktop/api), inherit from the [**IDirect3DResource9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="f4d8b-108">Ресурсы текстуры, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)и [**IDirect3DVolumeTexture9**](/windows/desktop/api)также наследуются от интерфейса [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .</span><span class="sxs-lookup"><span data-stu-id="f4d8b-108">The texture resources, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api), and [**IDirect3DVolumeTexture9**](/windows/desktop/api), also inherit from the [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface.</span></span>

-   [<span data-ttu-id="f4d8b-109">Свойства ресурсов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4d8b-109">Resource Properties (Direct3D 9)</span></span>](resource-properties.md)
-   [<span data-ttu-id="f4d8b-110">Управление ресурсами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4d8b-110">Manipulating Resources (Direct3D 9)</span></span>](manipulating-resources.md)
-   [<span data-ttu-id="f4d8b-111">Блокировка ресурсов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4d8b-111">Locking Resources (Direct3D 9)</span></span>](locking-resources.md)
-   [<span data-ttu-id="f4d8b-112">Связи ресурсов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4d8b-112">Resource Relationships (Direct3D 9)</span></span>](resource-relationships.md)
-   [<span data-ttu-id="f4d8b-113">Управление ресурсами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4d8b-113">Managing Resources (Direct3D 9)</span></span>](managing-resources.md)
-   [<span data-ttu-id="f4d8b-114">Ресурсы и стратегии выделения ресурсов, управляемые приложениями (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4d8b-114">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [<span data-ttu-id="f4d8b-115">Буферы индексов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4d8b-115">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
-   [<span data-ttu-id="f4d8b-116">Буферы вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4d8b-116">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)

## <a name="related-topics"></a><span data-ttu-id="f4d8b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f4d8b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4d8b-118">Начало работы</span><span class="sxs-lookup"><span data-stu-id="f4d8b-118">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
