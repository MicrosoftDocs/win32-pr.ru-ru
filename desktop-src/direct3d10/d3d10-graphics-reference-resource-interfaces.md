---
description: 'Direct3D 10 определяет ряд интерфейсов для двух основных типов ресурсов: буферов и текстур.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Интерфейсы ресурсов (графика Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141355"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a><span data-ttu-id="5fb25-103">Интерфейсы ресурсов (графика Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5fb25-103">Resource Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="5fb25-104">Direct3D 10 определяет ряд интерфейсов для двух основных типов ресурсов: [буферов](d3d10-graphics-programming-guide-resources-types.md) и текстур.</span><span class="sxs-lookup"><span data-stu-id="5fb25-104">Direct3D 10 defines a number of interfaces for the two basic types of resources: [buffers](d3d10-graphics-programming-guide-resources-types.md) and textures.</span></span>



| <span data-ttu-id="5fb25-105">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="5fb25-105">Interfaces</span></span>                                           | <span data-ttu-id="5fb25-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5fb25-106">Description</span></span>                                          |
|------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="5fb25-107">**Интерфейс ID3D10Buffer**</span><span class="sxs-lookup"><span data-stu-id="5fb25-107">**ID3D10Buffer Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | <span data-ttu-id="5fb25-108">Обращается к данным буфера.</span><span class="sxs-lookup"><span data-stu-id="5fb25-108">Accesses buffer data.</span></span>                                |
| [<span data-ttu-id="5fb25-109">**Интерфейс ID3D10Resource**</span><span class="sxs-lookup"><span data-stu-id="5fb25-109">**ID3D10Resource Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | <span data-ttu-id="5fb25-110">Базовый класс для ресурса.</span><span class="sxs-lookup"><span data-stu-id="5fb25-110">Base class for a resource.</span></span>                           |
| [<span data-ttu-id="5fb25-111">**Интерфейс ID3D10Texture1D**</span><span class="sxs-lookup"><span data-stu-id="5fb25-111">**ID3D10Texture1D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | <span data-ttu-id="5fb25-112">Обращается к данным в виде одномерной текстуры или массива одномерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="5fb25-112">Accesses data in a 1D texture or a 1D texture array.</span></span> |
| [<span data-ttu-id="5fb25-113">**Интерфейс ID3D10Texture2D**</span><span class="sxs-lookup"><span data-stu-id="5fb25-113">**ID3D10Texture2D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | <span data-ttu-id="5fb25-114">Обращается к данным в двухмерной текстуре или массиве 2D-текстур</span><span class="sxs-lookup"><span data-stu-id="5fb25-114">Accesses data in a 2D texture or a 2D texture array</span></span>  |
| [<span data-ttu-id="5fb25-115">**Интерфейс ID3D10Texture3D**</span><span class="sxs-lookup"><span data-stu-id="5fb25-115">**ID3D10Texture3D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | <span data-ttu-id="5fb25-116">Обращается к данным в трехмерной текстуре или массиве трехмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="5fb25-116">Accesses data in a 3D texture or a 3D texture array.</span></span> |



 

<span data-ttu-id="5fb25-117">Приложение использует представление для привязки ресурса к [этапу конвейера](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="5fb25-117">An application uses a view to bind a resource to a [pipeline stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> <span data-ttu-id="5fb25-118">[Представление](d3d10-graphics-programming-guide-resources-access-views.md) определяет, как к ресурсу можно получить доступ во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="5fb25-118">The [view](d3d10-graphics-programming-guide-resources-access-views.md) defines how the resource can be accessed during rendering.</span></span> <span data-ttu-id="5fb25-119">API содержит эти интерфейсы представления.</span><span class="sxs-lookup"><span data-stu-id="5fb25-119">The API contains these view interfaces.</span></span>



| <span data-ttu-id="5fb25-120">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="5fb25-120">Interfaces</span></span>                                                               | <span data-ttu-id="5fb25-121">Описание</span><span class="sxs-lookup"><span data-stu-id="5fb25-121">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fb25-122">**Интерфейс ID3D10DepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="5fb25-122">**ID3D10DepthStencilView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | <span data-ttu-id="5fb25-123">Обращается к данным в текстуре [набора элементов глубины](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) .</span><span class="sxs-lookup"><span data-stu-id="5fb25-123">Accesses data in a [depth-stencil](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) texture.</span></span> |
| [<span data-ttu-id="5fb25-124">**Интерфейс ID3D10RenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="5fb25-124">**ID3D10RenderTargetView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | <span data-ttu-id="5fb25-125">Обращается к данным в [целевом объекте прорисовки](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="5fb25-125">Accesses data in a [render target](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>        |
| [<span data-ttu-id="5fb25-126">**Интерфейс ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="5fb25-126">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | <span data-ttu-id="5fb25-127">Обращается к данным в шейдере — ресурсе в Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="5fb25-127">Accesses data in a shader-resource in Direct3D 10.0.</span></span>                                                         |
| [<span data-ttu-id="5fb25-128">**Интерфейс ID3D10ShaderResourceView1**</span><span class="sxs-lookup"><span data-stu-id="5fb25-128">**ID3D10ShaderResourceView1 Interface**</span></span>](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | <span data-ttu-id="5fb25-129">Обращается к данным в шейдере — ресурсе в Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="5fb25-129">Accesses data in a shader-resource in Direct3D 10.1.</span></span>                                                         |
| [<span data-ttu-id="5fb25-130">**Интерфейс ID3D10View**</span><span class="sxs-lookup"><span data-stu-id="5fb25-130">**ID3D10View Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | <span data-ttu-id="5fb25-131">Базовый класс для представления.</span><span class="sxs-lookup"><span data-stu-id="5fb25-131">Base class for a view.</span></span>                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="5fb25-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5fb25-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fb25-133">Ссылка на ресурс</span><span class="sxs-lookup"><span data-stu-id="5fb25-133">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
