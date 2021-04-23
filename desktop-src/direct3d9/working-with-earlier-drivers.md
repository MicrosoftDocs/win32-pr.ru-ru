---
description: В этом разделе перечислены проблемы, которые могут возникнуть при работе с Direct3D 9 на драйверах, написанных для версий Direct3D, предшествующих Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Работа с более ранними версиями драйверов (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416496"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a><span data-ttu-id="8daee-103">Работа с более ранними версиями драйверов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8daee-103">Working with Earlier Drivers (Direct3D 9)</span></span>

<span data-ttu-id="8daee-104">В этом разделе перечислены проблемы, которые могут возникнуть при работе с Direct3D 9 на драйверах, написанных для версий Direct3D, предшествующих Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="8daee-104">This section lists issues that can be encountered when working with Direct3D 9 on drivers written for versions of Direct3D earlier than Direct3D 9.</span></span>

-   <span data-ttu-id="8daee-105">При работе с устройством HAL T&L интенсивность тумана вычислена, но операция абсолютного значения не применяется к этому значению.</span><span class="sxs-lookup"><span data-stu-id="8daee-105">When working with a T&L HAL device, the fog intensity is computed but the absolute value operation is not applied to this value.</span></span> <span data-ttu-id="8daee-106">Вместо этого значение остается отрицательным, если это то, что является вычисленным.</span><span class="sxs-lookup"><span data-stu-id="8daee-106">Rather, the value is left negative if that is what is computed.</span></span> <span data-ttu-id="8daee-107">Лучший способ избежать этой ситуации — настроить преобразования соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="8daee-107">The best way to avoid this situation is to set up transforms appropriately.</span></span> <span data-ttu-id="8daee-108">Менее предпочтительный метод заключается в том, чтобы значения, заданные при запуске тумана и тумана, были отрицательными.</span><span class="sxs-lookup"><span data-stu-id="8daee-108">A less-preferred method is to make the fog-start and fog-end values negative to match.</span></span>

<span data-ttu-id="8daee-109">Чтобы проверить драйвер Direct3D 9, найдите ненулевое значение для D3DDEVCAPS2 \_ стреамоффсет в DevCaps2 члене [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="8daee-109">To check for a Direct3D 9 driver, look for a nonzero value for D3DDEVCAPS2\_STREAMOFFSET in the DevCaps2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8daee-110">См. также</span><span class="sxs-lookup"><span data-stu-id="8daee-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8daee-111">Советы по программированию</span><span class="sxs-lookup"><span data-stu-id="8daee-111">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



