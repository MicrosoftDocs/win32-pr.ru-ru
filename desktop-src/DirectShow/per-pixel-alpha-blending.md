---
description: Per-Pixel альфа-смешение
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel альфа-смешение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682245"
---
# <a name="per-pixel-alpha-blending"></a><span data-ttu-id="3ed6c-103">Per-Pixel альфа-смешение</span><span class="sxs-lookup"><span data-stu-id="3ed6c-103">Per-Pixel Alpha Blending</span></span>

<span data-ttu-id="3ed6c-104">Для многопиксельного альфа-смешения определены четыре подтипа носителей.</span><span class="sxs-lookup"><span data-stu-id="3ed6c-104">Four media subtypes have been defined for per-pixel alpha blending.</span></span> <span data-ttu-id="3ed6c-105">Эти подтипы поддерживаются, только если VMR находится в режиме смешения.</span><span class="sxs-lookup"><span data-stu-id="3ed6c-105">These subtypes are only supported when the VMR is in mixing mode.</span></span> <span data-ttu-id="3ed6c-106">VMR отклоняет соединение, если он не находится в режиме смешения, когда вышестоящий фильтр пытается подключиться с помощью одного из этих подтипов.</span><span class="sxs-lookup"><span data-stu-id="3ed6c-106">The VMR will reject the connection if it is not in mixing mode when an upstream filter attempts to connect using one of these subtypes.</span></span> <span data-ttu-id="3ed6c-107">Эти подтипы определены в UUID. h:</span><span class="sxs-lookup"><span data-stu-id="3ed6c-107">These subtypes are defined in uuids.h:</span></span>

-   <span data-ttu-id="3ed6c-108">МЕДИАСУБТИПЕ \_ ARGB1555</span><span class="sxs-lookup"><span data-stu-id="3ed6c-108">MEDIASUBTYPE\_ARGB1555</span></span>
-   <span data-ttu-id="3ed6c-109">МЕДИАСУБТИПЕ \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="3ed6c-109">MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="3ed6c-110">МЕДИАСУБТИПЕ \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="3ed6c-110">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="3ed6c-111">МЕДИАСУБТИПЕ \_ айув</span><span class="sxs-lookup"><span data-stu-id="3ed6c-111">MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="3ed6c-112">Дополнительные сведения см. в разделе [несжатые видео подтипы RGB](uncompressed-rgb-video-subtypes.md) и [**подтипы видеороликов YUV**](yuv-video-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="3ed6c-112">For more information, see [Uncompressed RGB Video Subtypes](uncompressed-rgb-video-subtypes.md) and [**YUV Video Subtypes**](yuv-video-subtypes.md).</span></span>

 

 



