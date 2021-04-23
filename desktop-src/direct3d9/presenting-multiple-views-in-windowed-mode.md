---
description: В дополнение к цепочке подкачки, которая владеет и управляется через интерфейс IDirect3DDevice9, приложение может создавать дополнительные цепочки подкачки для представления нескольких представлений с одного устройства.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Представление нескольких представлений в оконном режиме (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538228"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="2a9fb-103">Представление нескольких представлений в оконном режиме (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2a9fb-103">Presenting Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="2a9fb-104">В дополнение к цепочке подкачки, которая владеет и управляется через интерфейс [**IDirect3DDevice9**](/windows/desktop/api) , приложение может создавать дополнительные цепочки подкачки для представления нескольких представлений с одного устройства.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-104">In addition to the swap chain that is owned and manipulated through the [**IDirect3DDevice9**](/windows/desktop/api) interface, an application can create additional swap chains in order to present multiple views from the same device.</span></span> <span data-ttu-id="2a9fb-105">Приложение обычно создает одну цепочку подкачки на представление с помощью метода [**IDirect3DDevice9:: креатеаддитионалсвапчаин**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) и связывает каждую цепочку подкачки с определенным окном.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-105">The application typically creates one swap chain per view by using the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method, and associates each swap chain with a particular window.</span></span> <span data-ttu-id="2a9fb-106">Приложение визуализирует изображения в задние буферы каждой цепочки буферов, а затем представляет их по отдельности.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-106">The application renders images into the back buffers of each swap chain, and then presents them individually.</span></span>

<span data-ttu-id="2a9fb-107">Только одна цепочка подкачки одновременно может быть полноэкранной на каждом адаптере.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-107">Only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a9fb-108">См. также</span><span class="sxs-lookup"><span data-stu-id="2a9fb-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a9fb-109">Советы по программированию</span><span class="sxs-lookup"><span data-stu-id="2a9fb-109">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
