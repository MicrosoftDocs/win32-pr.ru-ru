---
description: Граф фильтра и его компоненты
ms.assetid: 3747bfcd-1e4a-404c-a493-26d3c20bab21
title: Граф фильтра и его компоненты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473fb3dfe327eb43bb2065417c7be80f7537d06a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684114"
---
# <a name="the-filter-graph-and-its-components"></a><span data-ttu-id="78e19-103">Граф фильтра и его компоненты</span><span class="sxs-lookup"><span data-stu-id="78e19-103">The Filter Graph and Its Components</span></span>

<span data-ttu-id="78e19-104">В этой статье описываются основные компоненты DirectShow.</span><span class="sxs-lookup"><span data-stu-id="78e19-104">This article describes the major components of DirectShow.</span></span> <span data-ttu-id="78e19-105">Он предназначен для ознакомления с разработчиками приложений, а также для разработчиков, занимающихся написанием пользовательских фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="78e19-105">It is intended as an introduction for application developers and for developers writing custom DirectShow filters.</span></span> <span data-ttu-id="78e19-106">Разработчики приложений обычно игнорируют многие низкоуровневые сведения о DirectShow.</span><span class="sxs-lookup"><span data-stu-id="78e19-106">Application developers can usually ignore many of the low-level details of DirectShow.</span></span> <span data-ttu-id="78e19-107">Однако рекомендуется прочитать этот раздел, чтобы получить общее представление об архитектуре DirectShow.</span><span class="sxs-lookup"><span data-stu-id="78e19-107">However, it is still a good idea to read this section, to have a general understanding of the DirectShow architecture.</span></span>

<span data-ttu-id="78e19-108">В этом разделе содержатся следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="78e19-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="78e19-109">О фильтрах DirectShow</span><span class="sxs-lookup"><span data-stu-id="78e19-109">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="78e19-110">О диспетчере графов фильтров</span><span class="sxs-lookup"><span data-stu-id="78e19-110">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
-   [<span data-ttu-id="78e19-111">О типах носителей</span><span class="sxs-lookup"><span data-stu-id="78e19-111">About Media Types</span></span>](about-media-types.md)
-   [<span data-ttu-id="78e19-112">О примерах носителей и распределителях</span><span class="sxs-lookup"><span data-stu-id="78e19-112">About Media Samples and Allocators</span></span>](about-media-samples-and-allocators.md)
-   [<span data-ttu-id="78e19-113">Как аппаратные устройства участвуют в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="78e19-113">How Hardware Devices Participate in the Filter Graph</span></span>](how-hardware-devices-participate-in-the-filter-graph.md)

 

 



