---
title: Программная инициализация текстуры
description: В этом разделе есть несколько примеров, показывающих, как инициализировать текстуры, созданные с использованием различных типов использования.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888660"
---
# <a name="how-to-initialize-a-texture-programmatically"></a><span data-ttu-id="1909b-103">Как программно инициализировать текстуру</span><span class="sxs-lookup"><span data-stu-id="1909b-103">How to: Initialize a Texture Programmatically</span></span>

<span data-ttu-id="1909b-104">Вы можете инициализировать текстуру во время создания объекта или заполнять объект программным способом после его создания.</span><span class="sxs-lookup"><span data-stu-id="1909b-104">You can initialize a texture during object creation, or you can fill the object programmatically after it is created.</span></span> <span data-ttu-id="1909b-105">В этом разделе есть несколько примеров, показывающих, как инициализировать текстуры, созданные с использованием различных типов использования.</span><span class="sxs-lookup"><span data-stu-id="1909b-105">This topic has several examples showing how to initialize textures that are created with different types of usages.</span></span> <span data-ttu-id="1909b-106">В этом примере предполагается, что вы уже знакомы с [созданием текстуры](overviews-direct3d-11-resources-textures-create.md).</span><span class="sxs-lookup"><span data-stu-id="1909b-106">This example assumes you already know how to [Create a Texture](overviews-direct3d-11-resources-textures-create.md).</span></span>

-   [<span data-ttu-id="1909b-107">Использование по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1909b-107">Default Usage</span></span>](#default-usage)
-   [<span data-ttu-id="1909b-108">Динамическое использование</span><span class="sxs-lookup"><span data-stu-id="1909b-108">Dynamic Usage</span></span>](#dynamic-usage)
-   [<span data-ttu-id="1909b-109">Использование промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="1909b-109">Staging Usage</span></span>](#staging-usage)
-   [<span data-ttu-id="1909b-110">См. также</span><span class="sxs-lookup"><span data-stu-id="1909b-110">Related topics</span></span>](#related-topics)

## <a name="default-usage"></a><span data-ttu-id="1909b-111">Использование по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1909b-111">Default Usage</span></span>

<span data-ttu-id="1909b-112">Наиболее распространенным типом использования является использование по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1909b-112">The most common type of usage is default usage.</span></span> <span data-ttu-id="1909b-113">Чтобы заполнить текстуру по умолчанию (созданную с использованием **D3D11 \_ \_ по умолчанию**), можно выполнить одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="1909b-113">To fill a default texture (one created with **D3D11\_USAGE\_DEFAULT**) you can either:</span></span>

-   <span data-ttu-id="1909b-114">Вызовите [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) и инициализируйте *пинитиалдата* , чтобы указать данные, предоставленные приложением.</span><span class="sxs-lookup"><span data-stu-id="1909b-114">Call [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and initialize *pInitialData* to point to data provided from an application.</span></span>

    <span data-ttu-id="1909b-115">или</span><span class="sxs-lookup"><span data-stu-id="1909b-115">or</span></span>

-   <span data-ttu-id="1909b-116">После вызова [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)используйте [**ссылку ID3D11DeviceContext:: упдатесубресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) для заполнения текстуры по умолчанию данными из указателя, предоставленного приложением.</span><span class="sxs-lookup"><span data-stu-id="1909b-116">After calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to fill the default texture with data from a pointer provided by the application.</span></span>

## <a name="dynamic-usage"></a><span data-ttu-id="1909b-117">Динамическое использование</span><span class="sxs-lookup"><span data-stu-id="1909b-117">Dynamic Usage</span></span>

<span data-ttu-id="1909b-118">Для заполнения динамической текстуры (созданной с использованием **D3D11 \_ \_ dynamic**):</span><span class="sxs-lookup"><span data-stu-id="1909b-118">To fill a dynamic texture (one created with **D3D11\_USAGE\_DYNAMIC**):</span></span>

1.  <span data-ttu-id="1909b-119">Получите указатель на память текстуры, передав при вызове [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) **D3D11- \_ \_ запись \_** .</span><span class="sxs-lookup"><span data-stu-id="1909b-119">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE\_DISCARD** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="1909b-120">Запись данных в память.</span><span class="sxs-lookup"><span data-stu-id="1909b-120">Write data to the memory.</span></span>
3.  <span data-ttu-id="1909b-121">По завершении записи данных вызовите метод [**ссылку ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) uncall.</span><span class="sxs-lookup"><span data-stu-id="1909b-121">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

## <a name="staging-usage"></a><span data-ttu-id="1909b-122">Использование промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="1909b-122">Staging Usage</span></span>

<span data-ttu-id="1909b-123">Для заполнения промежуточной текстуры (созданной с использованием **\_ \_ промежуточного хранения D3D11**):</span><span class="sxs-lookup"><span data-stu-id="1909b-123">To fill a staging texture (one created with **D3D11\_USAGE\_STAGING**):</span></span>

1.  <span data-ttu-id="1909b-124">Получите указатель на память текстуры, передав **D3D11 \_ Map \_ Write** при вызове [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="1909b-124">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="1909b-125">Запись данных в память.</span><span class="sxs-lookup"><span data-stu-id="1909b-125">Write data to the memory.</span></span>
3.  <span data-ttu-id="1909b-126">По завершении записи данных вызовите метод [**ссылку ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) uncall.</span><span class="sxs-lookup"><span data-stu-id="1909b-126">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

<span data-ttu-id="1909b-127">После этого промежуточная текстура может использоваться в качестве исходного параметра для [**ссылку ID3D11DeviceContext:: копиресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) или [**ссылку ID3D11DeviceContext:: кописубресаурцерегион**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) для заполнения по умолчанию или динамического ресурса.</span><span class="sxs-lookup"><span data-stu-id="1909b-127">A staging texture can then be used as the source parameter to [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) or [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) to fill a default or dynamic resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1909b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1909b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1909b-129">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1909b-129">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="1909b-130">Текстуры</span><span class="sxs-lookup"><span data-stu-id="1909b-130">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




