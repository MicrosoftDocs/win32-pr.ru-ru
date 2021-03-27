---
title: Создание объектов с использованием многопоточности
description: Используйте интерфейс ID3D11Device для создания ресурсов и объектов, используйте ссылку ID3D11DeviceContext для отрисовки.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986499"
---
# <a name="object-creation-with-multithreading"></a><span data-ttu-id="6d854-103">Создание объектов с использованием многопоточности</span><span class="sxs-lookup"><span data-stu-id="6d854-103">Object Creation with Multithreading</span></span>

<span data-ttu-id="6d854-104">Используйте интерфейс [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) для создания ресурсов и объектов, используйте [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) для [отрисовки](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="6d854-104">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

<span data-ttu-id="6d854-105">Ниже приведены некоторые примеры создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d854-105">Here are some examples of how to create resources:</span></span>

-   [<span data-ttu-id="6d854-106">Как создать буфер вершин</span><span class="sxs-lookup"><span data-stu-id="6d854-106">How to: Create a Vertex Buffer</span></span>](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [<span data-ttu-id="6d854-107">Как создать буфер индексов</span><span class="sxs-lookup"><span data-stu-id="6d854-107">How to: Create an Index Buffer</span></span>](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [<span data-ttu-id="6d854-108">Как создать буфер константы</span><span class="sxs-lookup"><span data-stu-id="6d854-108">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [<span data-ttu-id="6d854-109">Как инициализировать текстуру из файла</span><span class="sxs-lookup"><span data-stu-id="6d854-109">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a><span data-ttu-id="6d854-110">Вопросы многопоточности</span><span class="sxs-lookup"><span data-stu-id="6d854-110">Multithreading Considerations</span></span>

<span data-ttu-id="6d854-111">Объем параллелизма создания и подготовки ресурсов, который может достичь приложение, зависит от уровня поддержки многопоточности, реализуемой драйвером.</span><span class="sxs-lookup"><span data-stu-id="6d854-111">The amount of concurrency of resource creation and rendering that your application can achieve depends on the level of multithreading support that the driver implements.</span></span> <span data-ttu-id="6d854-112">Если драйвер поддерживает параллельное создание, приложение должно иметь гораздо меньше проблем параллелизма.</span><span class="sxs-lookup"><span data-stu-id="6d854-112">If the driver supports concurrent creates, then the application should have much less concurrency concerns.</span></span> <span data-ttu-id="6d854-113">Однако если драйвер не поддерживает параллельное создание объектов, то объем параллелизма чрезвычайно ограничен.</span><span class="sxs-lookup"><span data-stu-id="6d854-113">However, if the driver does not support concurrent object creation, the amount of concurrency is extremely limited.</span></span> <span data-ttu-id="6d854-114">Чтобы понять объем доступной в драйвере поддержки, запросите драйвер для значения элемента **дриверконкурренткреатес** в структуре [**\_ \_ \_ потоков данных компонента D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) .</span><span class="sxs-lookup"><span data-stu-id="6d854-114">To understand the amount of support available in a driver, query the driver for the value of the **DriverConcurrentCreates** member of the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure.</span></span> <span data-ttu-id="6d854-115">Дополнительные сведения о проверке поддержки многопоточности драйверами см. [в разделе как проверить наличие поддержки драйверов](overviews-direct3d-11-render-multi-thread-support.md).</span><span class="sxs-lookup"><span data-stu-id="6d854-115">For more information about checking for driver support of multithreading, see [How To: Check for Driver Support](overviews-direct3d-11-render-multi-thread-support.md).</span></span>

<span data-ttu-id="6d854-116">Параллельные операции не обязательно могут привести к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="6d854-116">Concurrent operations do not necessarily lead to better performance.</span></span> <span data-ttu-id="6d854-117">Например, создание и загрузка текстуры обычно ограничены пропускной способностью памяти.</span><span class="sxs-lookup"><span data-stu-id="6d854-117">For example, creating and loading a texture is typically limited by memory bandwidth.</span></span> <span data-ttu-id="6d854-118">Попытка создать и загрузить несколько текстур может выполняться не быстрее, чем за одну текстуру за раз, даже если это оставляет несколько ядер ЦП в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="6d854-118">Attempting to create and load multiple textures might be no faster than doing one texture at a time, even if this leaves multiple CPU cores idle.</span></span> <span data-ttu-id="6d854-119">Однако создание нескольких шейдеров, использующих несколько потоков, может повысить производительность, так как эта операция менее зависит от системных ресурсов, таких как пропускная способность памяти.</span><span class="sxs-lookup"><span data-stu-id="6d854-119">However, creating multiple shaders using multiple threads can increase performance as this operation is less dependent on system resources such as memory bandwidth.</span></span>

<span data-ttu-id="6d854-120">Когда драйвер и графическое оборудование поддерживают многопоточность, вы обычно можете более эффективно инициализировать вновь созданные ресурсы, передав указатель на исходные данные в параметре *пинитиалдата* (например, в вызове метода [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) ).</span><span class="sxs-lookup"><span data-stu-id="6d854-120">When the driver and graphics hardware support multithreading, you can typically initialize newly created resources more efficiently by passing a pointer to initial data in the *pInitialData* parameter (for example, in a call to the [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) method).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d854-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6d854-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d854-122">Многопоточности</span><span class="sxs-lookup"><span data-stu-id="6d854-122">MultiThreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




