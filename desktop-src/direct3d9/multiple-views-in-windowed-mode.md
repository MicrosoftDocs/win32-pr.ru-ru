---
description: 'В дополнение к цепочке подкачки, которая владеет и управляется через объект Direct3DDevice, приложение может использовать метод IDirect3DDevice9:: Креатеаддитионалсвапчаин для создания дополнительных цепочек подкачки для предоставления нескольких представлений из одного устройства.'
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Несколько представлений в оконном режиме (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710605"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="4c898-103">Несколько представлений в оконном режиме (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4c898-103">Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="4c898-104">В дополнение к цепочке подкачки, которая владеет и управляется через объект Direct3DDevice, приложение может использовать метод [**IDirect3DDevice9:: креатеаддитионалсвапчаин**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) для создания дополнительных цепочек подкачки для предоставления нескольких представлений из одного устройства.</span><span class="sxs-lookup"><span data-stu-id="4c898-104">In addition to the swap chain that is owned and manipulated through the Direct3DDevice object, an application can use the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method to create additional swap chains to present multiple views from the same device.</span></span>

<span data-ttu-id="4c898-105">Как правило, приложение создает одну цепочку подкачки для каждого представления и связывает каждую цепочку подкачки с определенным представлением.</span><span class="sxs-lookup"><span data-stu-id="4c898-105">Typically, the application creates one swap chain per view, and it associates each swap chain with a particular view.</span></span> <span data-ttu-id="4c898-106">Приложение визуализирует изображения в задних буферах каждой цепочки буферов, а затем использует метод [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) повторной передачи, чтобы предоставить их по отдельности.</span><span class="sxs-lookup"><span data-stu-id="4c898-106">The application renders images in the back buffers of each swap chain, and then uses the [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method to present them individually.</span></span> <span data-ttu-id="4c898-107">Обратите внимание, что только одна цепочка подкачки одновременно может быть полноэкранной на каждом адаптере.</span><span class="sxs-lookup"><span data-stu-id="4c898-107">Note that only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c898-108">См. также</span><span class="sxs-lookup"><span data-stu-id="4c898-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c898-109">Представление сцены</span><span class="sxs-lookup"><span data-stu-id="4c898-109">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 
