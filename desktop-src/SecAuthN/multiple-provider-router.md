---
description: Маршрутизатор с несколькими поставщиками (MPR) обрабатывает связь между операционной системой Windows и установленными поставщиками сети. Она позволяет Windows предоставлять пользователю интегрированную сеть.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Маршрутизатор с несколькими поставщиками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911864"
---
# <a name="multiple-provider-router"></a><span data-ttu-id="7ab56-104">Маршрутизатор с несколькими поставщиками</span><span class="sxs-lookup"><span data-stu-id="7ab56-104">Multiple Provider Router</span></span>

<span data-ttu-id="7ab56-105">[*Маршрутизатор с несколькими поставщиками*](../secgloss/m-gly.md) (MPR) обрабатывает связь между операционной системой Windows и установленными поставщиками сети.</span><span class="sxs-lookup"><span data-stu-id="7ab56-105">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication between the Windows operating system and the installed network providers.</span></span> <span data-ttu-id="7ab56-106">Она позволяет Windows предоставлять пользователю интегрированную сеть.</span><span class="sxs-lookup"><span data-stu-id="7ab56-106">It enables Windows to present an integrated network to the user.</span></span>

<span data-ttu-id="7ab56-107">При запуске многопротокольного маршрутизатора проверяет реестр, чтобы определить, какие поставщики сети установлены в системе, и порядок, в котором они должны циклически проходить.</span><span class="sxs-lookup"><span data-stu-id="7ab56-107">When the MPR starts, it checks the registry to determine which network providers are installed on the system and the order they should be cycled through.</span></span> <span data-ttu-id="7ab56-108">Он загружает все зарегистрированные библиотеки DLL поставщика сети и использует их для обработки последующих вызовов Внет, выполненных пользовательским интерфейсом или другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="7ab56-108">It loads all registered network provider DLLs and uses them to process subsequent WNet calls made by the user interface or other applications.</span></span>

<span data-ttu-id="7ab56-109">Дополнительные сведения о функциях Внет см. в разделе [Сетевые подключения Windows](../wnet/windows-networking-wnet-.md).</span><span class="sxs-lookup"><span data-stu-id="7ab56-109">For more information about WNet functions, see [Windows Networking](../wnet/windows-networking-wnet-.md).</span></span>

 

 
