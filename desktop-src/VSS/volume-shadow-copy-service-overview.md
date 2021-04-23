---
description: Служба теневого копирования томов (VSS) — это набор API-интерфейсов COM, который реализует платформу, позволяющую выполнять резервное копирование томов, пока приложения в системе продолжают записывать данные на тома.
ms.assetid: 263b0200-4869-4fb0-ad50-240166d2d32f
title: Обзор служба теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2710ee47e20953b7a7ea86d5b0cb3318fc49bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692383"
---
# <a name="volume-shadow-copy-service-overview"></a><span data-ttu-id="ddd41-103">Обзор служба теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="ddd41-103">Volume Shadow Copy Service Overview</span></span>

<span data-ttu-id="ddd41-104">Служба теневого копирования томов (VSS) — это набор API-интерфейсов COM, который реализует платформу, позволяющую выполнять резервное копирование томов, пока приложения в системе продолжают записывать данные на тома.</span><span class="sxs-lookup"><span data-stu-id="ddd41-104">The Volume Shadow Copy Service (VSS) is a set of COM APIs that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="ddd41-105">Служба VSS обеспечивает согласованный интерфейс, который обеспечивает координацию между пользовательскими приложениями, которые обновляют данные на дисках ([*модулях записи*](vssgloss-w.md)) и резервными копиями приложений ([*запрашивающими*](vssgloss-r.md)стороны).</span><span class="sxs-lookup"><span data-stu-id="ddd41-105">VSS provides a consistent interface that allows coordination between user applications that update data on disk ([*writers*](vssgloss-w.md)) and those that back up applications ([*requesters*](vssgloss-r.md)).</span></span>

-   [<span data-ttu-id="ddd41-106">Новые возможности VSS</span><span class="sxs-lookup"><span data-stu-id="ddd41-106">What's New in VSS</span></span>](what-s-new-in-vss.md)
-   [<span data-ttu-id="ddd41-107">Сведения о служба теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="ddd41-107">About the Volume Shadow Copy Service</span></span>](about-the-volume-shadow-copy-service.md)
-   [<span data-ttu-id="ddd41-108">Использование служба теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="ddd41-108">Using the Volume Shadow Copy Service</span></span>](using-the-volume-shadow-copy-service.md)
-   [<span data-ttu-id="ddd41-109">Сведения о реализации VSS</span><span class="sxs-lookup"><span data-stu-id="ddd41-109">VSS Implementation Details</span></span>](vss-implementation-details.md)
-   [<span data-ttu-id="ddd41-110">Устранение неполадок приложений VSS</span><span class="sxs-lookup"><span data-stu-id="ddd41-110">Troubleshooting VSS Applications</span></span>](troubleshooting-vss-applications.md)

 

 



