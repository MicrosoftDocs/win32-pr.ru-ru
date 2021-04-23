---
description: API поставщика сети указывает одну функцию возможностей.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Функции возможностей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080542"
---
# <a name="capabilities-functions"></a><span data-ttu-id="f5fb9-103">Функции возможностей</span><span class="sxs-lookup"><span data-stu-id="f5fb9-103">Capabilities Functions</span></span>

<span data-ttu-id="f5fb9-104">API поставщика сети указывает одну функцию возможностей.</span><span class="sxs-lookup"><span data-stu-id="f5fb9-104">The Network Provider API specifies a single capabilities function.</span></span> <span data-ttu-id="f5fb9-105">Когда операционная система запрашивает сведения о возможностях поставщика сети, [*маршрутизатор с несколькими поставщиками*](/windows/desktop/SecGloss/m-gly) (MPR) вызывает функцию [**нпжеткапс**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) каждого поставщика сети, сеть которого активна.</span><span class="sxs-lookup"><span data-stu-id="f5fb9-105">When the operating system requests information about a network provider's capabilities, the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function of each network provider whose network is active.</span></span>

<span data-ttu-id="f5fb9-106">Функция [**нпжеткапс**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) возвращает битовую маску, указывающую, какие функции API поставщика сети поддерживает поставщик сети.</span><span class="sxs-lookup"><span data-stu-id="f5fb9-106">The [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function returns a bitmask indicating which functions of the Network Provider API the network provider supports.</span></span> <span data-ttu-id="f5fb9-107">Функция **нпжеткапс** является единственной функцией, которую должен реализовать поставщик сети.</span><span class="sxs-lookup"><span data-stu-id="f5fb9-107">The **NPGetCaps** function is the only function that a network provider must implement.</span></span> <span data-ttu-id="f5fb9-108">Операционная система вызывает эту функцию, чтобы определить, какие другие функции API поставщика сети поддерживает поставщик.</span><span class="sxs-lookup"><span data-stu-id="f5fb9-108">The operating system calls this function to determine which other functions of the Network Provider API the provider supports.</span></span>

 

 
