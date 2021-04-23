---
description: По умолчанию системе Direct3D разрешено выполнять запись в буфер глубины. Большинство приложений оставляет запись в буфер глубины включенным, но можно добиться некоторых специальных эффектов, не разрешая системе Direct3D выполнять запись в буфер глубины.
ms.assetid: d426ebff-bfce-4e5b-a97b-7b2539b4a9de
title: Изменение доступа на запись в буфер глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a261c4d30c9d0bd9edfbf07f765b2037e8195
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710732"
---
# <a name="changing-depth-buffer-write-access-direct3d-9"></a><span data-ttu-id="213c4-104">Изменение доступа на запись в буфер глубины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="213c4-104">Changing Depth Buffer Write Access (Direct3D 9)</span></span>

<span data-ttu-id="213c4-105">По умолчанию системе Direct3D разрешено выполнять запись в буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="213c4-105">By default, the Direct3D system is allowed to write to the depth buffer.</span></span> <span data-ttu-id="213c4-106">Большинство приложений оставляет запись в буфер глубины включенным, но можно добиться некоторых специальных эффектов, не разрешая системе Direct3D выполнять запись в буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="213c4-106">Most applications leave writing to the depth buffer enabled, but you can achieve some special effects by not allowing the Direct3D system to write to the depth buffer.</span></span>

<span data-ttu-id="213c4-107">Вы можете отключить операции записи в буфер глубины в C++, вызвав метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) с параметром State, ИМЕЮЩИМ значение D3DRS \_ звритинабле, а параметр value — равным 0.</span><span class="sxs-lookup"><span data-stu-id="213c4-107">You can disable depth buffer writes in C++ by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the State parameter set to D3DRS\_ZWRITEENABLE and the Value parameter set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="213c4-108">См. также</span><span class="sxs-lookup"><span data-stu-id="213c4-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="213c4-109">Буферы глубины</span><span class="sxs-lookup"><span data-stu-id="213c4-109">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
