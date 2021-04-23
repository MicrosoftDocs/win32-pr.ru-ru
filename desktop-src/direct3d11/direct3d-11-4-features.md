---
title: Функции Direct3D 11,4
description: В Direct3D 11,4 добавлены следующие функциональные возможности.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987668"
---
# <a name="direct3d-114-features"></a><span data-ttu-id="e38ea-103">Функции Direct3D 11,4</span><span class="sxs-lookup"><span data-stu-id="e38ea-103">Direct3D 11.4 Features</span></span>

<span data-ttu-id="e38ea-104">В Direct3D 11,4 добавлены следующие функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="e38ea-104">The following functionality has been added in Direct3D 11.4.</span></span>

<span data-ttu-id="e38ea-105">Также посмотрите [, где находится пакет SDK DirectX?](../directx-sdk--august-2009-.md)</span><span class="sxs-lookup"><span data-stu-id="e38ea-105">Also see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="direct3d-device-removal"></a><span data-ttu-id="e38ea-106">Удаление устройства Direct3D</span><span class="sxs-lookup"><span data-stu-id="e38ea-106">Direct3D device removal</span></span>

<span data-ttu-id="e38ea-107">Методы [**регистердевицеремоведевент**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)и [**унрегистердевицеремовед**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) поддерживаются новым интерфейсом [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4)для поддержки получения асинхронного уведомления о событии при удалении устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e38ea-107">The [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent), and [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) methods are supported by a new interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), to support receiving an asynchronous event notification when a Direct3D device has been removed.</span></span>

## <a name="multithreaded-protection"></a><span data-ttu-id="e38ea-108">Многопоточная защита</span><span class="sxs-lookup"><span data-stu-id="e38ea-108">Multithreaded protection</span></span>

<span data-ttu-id="e38ea-109">Чтобы гарантировать, что команды графики в частности выполняются в определенном порядке, интерфейс [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) имеет методы для включения и отключения многопотоковой защиты, а также методы для входа и выхода из критического кода, которому требуется эта защита.</span><span class="sxs-lookup"><span data-stu-id="e38ea-109">To ensure that graphics commands in particular are executed in a specific order, the [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) interface has methods to turn multithread protection on and off, and methods to enter and leave critical code requiring this protection.</span></span>

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a><span data-ttu-id="e38ea-110">Ограждения для синхронизации нескольких устройств и взаимодействия с Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e38ea-110">Fences for multi-device synchronization and interop with Direct3D 12</span></span>

<span data-ttu-id="e38ea-111">[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) и [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) предоставляют те же функции ограждения, что и Direct3D 12 для Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="e38ea-111">The [**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) and [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) provide the same fence functionality as Direct3D 12 for Direct3D 11.</span></span> <span data-ttu-id="e38ea-112">Границы используются для синхронизации нескольких устройств Direct3D11 и для взаимодействия между Direct3D 11 и Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e38ea-112">Fences are used to synchronize multiple Direct3D11 devices, and for interop between Direct3D 11 and Direct3D 12.</span></span> <span data-ttu-id="e38ea-113">Границы поддерживаются в обновлении Windows 10 для дизайнеров.</span><span class="sxs-lookup"><span data-stu-id="e38ea-113">Fences are supported in the Windows 10 Creators Update.</span></span>

## <a name="extended-nv12-texture-support"></a><span data-ttu-id="e38ea-114">Расширенная поддержка текстур NV12</span><span class="sxs-lookup"><span data-stu-id="e38ea-114">Extended NV12 texture support</span></span>

<span data-ttu-id="e38ea-115">Текстуры NV12 с возможностями записи и кодирования видео теперь поддерживают совместное использование.</span><span class="sxs-lookup"><span data-stu-id="e38ea-115">NV12 textures with capture and video encode capabilities now support sharing.</span></span> <span data-ttu-id="e38ea-116">Более старые флаги текстуры D3D11 для кодирования и записи видео являются устаревшими для NV12, так как они будут установлены в течение всего времени для новых драйверов.</span><span class="sxs-lookup"><span data-stu-id="e38ea-116">Older D3D11 texture flags for video encode and capture are deprecated for NV12, as it will be set all the time for new drivers.</span></span> <span data-ttu-id="e38ea-117">Такие текстуры могут использоваться не только с D3D11, но и с D3D12.</span><span class="sxs-lookup"><span data-stu-id="e38ea-117">Such textures can be shared not only with D3D11, but also with D3D12.</span></span> <span data-ttu-id="e38ea-118">В D3D12 новые флаги не представляют эти возможности текстуры.</span><span class="sxs-lookup"><span data-stu-id="e38ea-118">In D3D12, no new flags represent these texture capabilities.</span></span>

<span data-ttu-id="e38ea-119">См. логический параметр в [**D3D11 \_ Data Feature \_ \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span><span class="sxs-lookup"><span data-stu-id="e38ea-119">Refer to the boolean setting in [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span></span>

## <a name="shader-caching"></a><span data-ttu-id="e38ea-120">Кэширование шейдера</span><span class="sxs-lookup"><span data-stu-id="e38ea-120">Shader Caching</span></span>

<span data-ttu-id="e38ea-121">Драйверы могут поддерживать кэширование шейдера, управляемого операционной системой, для Direct3D11 приложений в обновлении Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="e38ea-121">Drivers may support OS-managed shader caching of Direct3D11 applications in the Windows 10 Creators update.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e38ea-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e38ea-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e38ea-123">Новые возможности Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e38ea-123">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 