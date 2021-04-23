---
description: Многие приложения C++ перед отрисовкой каждого нового кадра очищают буфер глубины.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Очистка буферов глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ad415b5c92e62da4f64eb590a0e202ffa3e0c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710731"
---
# <a name="clearing-depth-buffers-direct3d-9"></a><span data-ttu-id="3813a-103">Очистка буферов глубины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3813a-103">Clearing Depth Buffers (Direct3D 9)</span></span>

<span data-ttu-id="3813a-104">Многие приложения C++ перед отрисовкой каждого нового кадра очищают буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="3813a-104">Many C++ applications clear the depth buffer before rendering each new frame.</span></span> <span data-ttu-id="3813a-105">Можно явным образом очистить буфер глубины с помощью Direct3D, вызвав [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) и указав D3DCLEAR \_ Збуффер для параметра flags.</span><span class="sxs-lookup"><span data-stu-id="3813a-105">You can explicitly clear the depth buffer through Direct3D by calling [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) and specifying D3DCLEAR\_ZBUFFER for the Flags parameter.</span></span> <span data-ttu-id="3813a-106">Метод **IDirect3DDevice9:: Clear** позволяет указать произвольное значение глубины в параметре Z.</span><span class="sxs-lookup"><span data-stu-id="3813a-106">The **IDirect3DDevice9::Clear** method allows you to specify an arbitrary depth value in the Z parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3813a-107">См. также</span><span class="sxs-lookup"><span data-stu-id="3813a-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3813a-108">Буферы глубины</span><span class="sxs-lookup"><span data-stu-id="3813a-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
