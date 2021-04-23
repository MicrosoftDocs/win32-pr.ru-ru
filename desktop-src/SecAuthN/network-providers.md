---
description: Поставщик сети — это библиотека DLL, которая поддерживает конкретный сетевой протокол.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Поставщики сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265797"
---
# <a name="network-providers"></a><span data-ttu-id="14a8a-103">Поставщики сети</span><span class="sxs-lookup"><span data-stu-id="14a8a-103">Network Providers</span></span>

<span data-ttu-id="14a8a-104">Поставщик сети — это библиотека DLL, которая поддерживает конкретный сетевой протокол.</span><span class="sxs-lookup"><span data-stu-id="14a8a-104">A network provider is a DLL that supports a specific network protocol.</span></span> <span data-ttu-id="14a8a-105">Он также реализует [API поставщика сети](network-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="14a8a-105">It also implements the [Network Provider API](network-provider-api.md).</span></span> <span data-ttu-id="14a8a-106">Это позволяет ему взаимодействовать с операционной системой Windows для получения стандартных сетевых запросов, таких как запросы подключения или отключения.</span><span class="sxs-lookup"><span data-stu-id="14a8a-106">This enables it to interact with the Windows operating system to receive standard network requests, such as connection or disconnection requests.</span></span> <span data-ttu-id="14a8a-107">Для обработки этих запросов поставщик сети вызывает сетевой интерфейс API, соответствующий сетевому протоколу, поддерживаемому поставщиком сети.</span><span class="sxs-lookup"><span data-stu-id="14a8a-107">To handle these requests, the network provider then calls the network-specific API that is appropriate to the network protocol the network provider supports.</span></span> <span data-ttu-id="14a8a-108">Иными словами, поставщик сети создает оболочку для сетевых функций в библиотеке DLL, которая предоставляет стандартный интерфейс для Windows.</span><span class="sxs-lookup"><span data-stu-id="14a8a-108">In other words, the network provider wraps the network-specific functionality in a DLL, which exposes a standard interface to Windows.</span></span>

<span data-ttu-id="14a8a-109">Используя поставщики сетевых услуг, Windows может поддерживать множество различных типов сетевых протоколов, не зная специфических для сети сведений о каждой сети.</span><span class="sxs-lookup"><span data-stu-id="14a8a-109">Using network providers, Windows can support many different types of network protocols without having to know the network-specific details of each network.</span></span> <span data-ttu-id="14a8a-110">Это важно, так как новые сетевые протоколы разрабатываются все время.</span><span class="sxs-lookup"><span data-stu-id="14a8a-110">This is essential because new network protocols are being developed all the time.</span></span> <span data-ttu-id="14a8a-111">При использовании поставщиков сетевых услуг для поддержки нового протокола просто требуется создать и установить новый поставщик сети.</span><span class="sxs-lookup"><span data-stu-id="14a8a-111">With network providers, supporting a new protocol simply requires creating and installing a new network provider.</span></span>

<span data-ttu-id="14a8a-112">Сведения о функциях и структурах поставщика сети см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="14a8a-112">For information about network provider functions and structures, see the following topics:</span></span>

-   [<span data-ttu-id="14a8a-113">Функции поставщика сети</span><span class="sxs-lookup"><span data-stu-id="14a8a-113">Network Provider Functions</span></span>](authentication-functions.md)
-   [<span data-ttu-id="14a8a-114">Структуры поставщиков сети</span><span class="sxs-lookup"><span data-stu-id="14a8a-114">Network Provider Structures</span></span>](authentication-structures.md)

 

 



