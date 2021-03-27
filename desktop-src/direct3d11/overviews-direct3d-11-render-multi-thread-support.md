---
title: Проверка поддержки драйверов
description: В этом разделе показано, как определить, поддерживаются ли для аппаратного ускорения возможности многопотоковой обработки (включая создание ресурсов и списки команд).
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae42bbb3eedb76d049479839d497a79db81b5697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996755"
---
# <a name="how-to-check-for-driver-support"></a><span data-ttu-id="81864-103">Как проверить наличие поддержки драйверов</span><span class="sxs-lookup"><span data-stu-id="81864-103">How To: Check for Driver Support</span></span>

<span data-ttu-id="81864-104">В этом разделе показано, как определить, поддерживаются ли для аппаратного ускорения возможности многопотоковой обработки (включая [Создание ресурсов](overviews-direct3d-11-render-multi-thread-intro.md) и [списки команд](overviews-direct3d-11-render-multi-thread-command-list.md)).</span><span class="sxs-lookup"><span data-stu-id="81864-104">This topic shows how to determine whether multithreading features (including [resource creation](overviews-direct3d-11-render-multi-thread-intro.md) and [command lists](overviews-direct3d-11-render-multi-thread-command-list.md)) are supported for hardware acceleration.</span></span>

<span data-ttu-id="81864-105">Для приложений рекомендуется проверять поддержку многопоточности в графическом оборудовании.</span><span class="sxs-lookup"><span data-stu-id="81864-105">We recommend for applications to check for graphics hardware support of multithreading.</span></span> <span data-ttu-id="81864-106">Если драйвер и графическое оборудование не поддерживают создание многопоточного объекта, производительность может быть ограничена следующими способами.</span><span class="sxs-lookup"><span data-stu-id="81864-106">If the driver and graphics hardware do not support multithreaded object creation, performance can be limited in the following ways:</span></span>

-   <span data-ttu-id="81864-107">Одновременное создание нескольких объектов (даже разных типов) может быть ограничено.</span><span class="sxs-lookup"><span data-stu-id="81864-107">Creating multiple objects (even of different types) at the same time might be limited.</span></span>
-   <span data-ttu-id="81864-108">Создание объекта при отрисовке графических команд с помощью [непосредственных контекстов](overviews-direct3d-11-render-multi-thread-render.md) может быть ограничено.</span><span class="sxs-lookup"><span data-stu-id="81864-108">Creating an object while rendering graphics commands by using an [immediate context](overviews-direct3d-11-render-multi-thread-render.md) might be limited.</span></span> <span data-ttu-id="81864-109">Например, если оборудование не поддерживает многопоточность, приложение должно избегать создания в фоновом потоке объекта, для создания которого требуется очень много времени.</span><span class="sxs-lookup"><span data-stu-id="81864-109">For example, if hardware does not support multithreading, an application should avoid creating on a background thread an object that requires a very long time to create.</span></span> <span data-ttu-id="81864-110">Операция создания, которая занимает очень много времени, может блокировать немедленную визуализацию контекста и повысить риск перебоиности визуальных кадров.</span><span class="sxs-lookup"><span data-stu-id="81864-110">A create operation that takes very long can block immediate context rendering and increase the risk of a visual frame rate stutter.</span></span>

<span data-ttu-id="81864-111">Среда выполнения поддерживает многопоточность и списки команд независимо от поддержки драйверов и оборудования. Если драйвер и аппаратная поддержка для многопотоковых или списков команд не поддерживаются, среда выполнения будет эмулировать функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="81864-111">The runtime supports multithreading and command lists regardless of driver and hardware support; if there is no driver and hardware support for either multithreads or command lists, the runtime will emulate the functionality.</span></span> <span data-ttu-id="81864-112">Дополнительные сведения о многопоточности см. в статье [Введение в многопоточность в Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).</span><span class="sxs-lookup"><span data-stu-id="81864-112">For more information about multithreading, see [Introduction to Multithreading in Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).</span></span>

<span data-ttu-id="81864-113">**Для проверки поддержки многопоточности драйверов выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="81864-113">**To check for driver support for multithreading:**</span></span>

1.  <span data-ttu-id="81864-114">Инициализируйте объект интерфейса [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="81864-114">Initialize an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface object.</span></span> <span data-ttu-id="81864-115">По умолчанию многопоточность включена.</span><span class="sxs-lookup"><span data-stu-id="81864-115">By default, multithreading is enabled.</span></span>
2.  <span data-ttu-id="81864-116">Вызовите [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="81864-116">Call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="81864-117">Передайте **значение \_ \_ многопоточности функции D3D11** в параметр *функции* , передайте структуру [**\_ \_ \_ потоковой передачи данных функции D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) в параметр *пфеатуресуппортдата* и передайте размер структуры **\_ \_ \_ потоковой передачи данных функции D3D11** в параметр *феатуресуппортдатасизе* .</span><span class="sxs-lookup"><span data-stu-id="81864-117">Pass the **D3D11\_FEATURE\_THREADING** value to the *Feature* parameter, pass the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_THREADING** structure to the *FeatureSupportDataSize* parameter.</span></span>
3.  <span data-ttu-id="81864-118">Если метод [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) выполняется успешно, то структура [**\_ \_ \_ потоков данных компонента D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) , передаваемая на предыдущем шаге, будет инициализирована сведениями о поддержке многопоточности.</span><span class="sxs-lookup"><span data-stu-id="81864-118">If the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) method succeeds, the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure that you passed in the previous step will be initialized with information about multithreading support.</span></span>
    -   <span data-ttu-id="81864-119">Если **дриверконкурренткреатес** имеет **значение true**, драйвер может одновременно создавать несколько ресурсов (параллельно) в разных потоках.</span><span class="sxs-lookup"><span data-stu-id="81864-119">If **DriverConcurrentCreates** is **TRUE**, a driver can create more than one resource at the same time (concurrently) on different threads.</span></span>

        <span data-ttu-id="81864-120">Если **дриверкоммандлистс** имеет **значение true**, драйвер поддерживает списки команд.</span><span class="sxs-lookup"><span data-stu-id="81864-120">If **DriverCommandLists** is **TRUE**, the driver supports command lists.</span></span> <span data-ttu-id="81864-121">То есть команды отрисовки, выдаваемые непосредственным контекстом, могут одновременно создавать объекты в отдельных потоках с низким риском частоты кадров перебои.</span><span class="sxs-lookup"><span data-stu-id="81864-121">That is, rendering commands issued by an immediate context can be concurrent with object creation on separate threads with low risk of a frame rate stutter.</span></span>

    -   <span data-ttu-id="81864-122">Если **дриверконкурренткреатес** имеет **значение false**, драйвер не поддерживает параллельное создание, а это означает, что объем параллелизма чрезвычайно ограничен.</span><span class="sxs-lookup"><span data-stu-id="81864-122">If **DriverConcurrentCreates** is **FALSE**, a driver does not support concurrent creation, which means the amount of concurrency possible is extremely limited.</span></span> <span data-ttu-id="81864-123">Графическое оборудование не может создавать объекты различных типов в разных потоках симултануеаусли.</span><span class="sxs-lookup"><span data-stu-id="81864-123">The graphics hardware cannot create objects of different types on different threads simultanueously.</span></span> <span data-ttu-id="81864-124">Кроме того, графическое оборудование не может использовать непосредственный контекст для выпуска команд визуализации, пока графическое оборудование пытается создать ресурс в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="81864-124">Additionally, the graphics hardware cannot use an immediate context to issue render commands while the graphics hardware attempts to create a resource on another thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81864-125">См. также</span><span class="sxs-lookup"><span data-stu-id="81864-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81864-126">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="81864-126">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="81864-127">Многопоточность</span><span class="sxs-lookup"><span data-stu-id="81864-127">Multithreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




