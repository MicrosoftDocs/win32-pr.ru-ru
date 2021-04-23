---
description: Для повышения производительности доступ к объектам интерфейса графических устройств (GDI) (таким как палитры, контексты устройств, регионы и т. д.) не сериализуется.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Несколько потоков и объектов GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673762"
---
# <a name="multiple-threads-and-gdi-objects"></a><span data-ttu-id="6d4b7-103">Несколько потоков и объектов GDI</span><span class="sxs-lookup"><span data-stu-id="6d4b7-103">Multiple Threads and GDI Objects</span></span>

<span data-ttu-id="6d4b7-104">Для повышения производительности доступ к объектам интерфейса графических устройств (GDI) (таким как палитры, контексты устройств, регионы и т. д.) не сериализуется.</span><span class="sxs-lookup"><span data-stu-id="6d4b7-104">To enhance performance, access to graphics device interface (GDI) objects (such as palettes, device contexts, regions, and the like) is not serialized.</span></span> <span data-ttu-id="6d4b7-105">Это создает потенциальную опасность для процессов, имеющих несколько потоков, совместно использующих эти объекты.</span><span class="sxs-lookup"><span data-stu-id="6d4b7-105">This creates a potential danger for processes that have multiple threads sharing these objects.</span></span> <span data-ttu-id="6d4b7-106">Например, если один поток удаляет объект GDI, а другой поток использует его, результаты становятся непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="6d4b7-106">For example, if one thread deletes a GDI object while another thread is using it, the results are unpredictable.</span></span> <span data-ttu-id="6d4b7-107">Эту опасность можно избежать, просто не отправляя общий доступ к объектам GDI.</span><span class="sxs-lookup"><span data-stu-id="6d4b7-107">This danger can be avoided simply by not sharing GDI objects.</span></span> <span data-ttu-id="6d4b7-108">Если общий доступ невозможен (или желательно), приложение должно предоставить собственные механизмы для синхронизации доступа.</span><span class="sxs-lookup"><span data-stu-id="6d4b7-108">If sharing is unavoidable (or desirable), the application must provide its own mechanisms for synchronizing access.</span></span> <span data-ttu-id="6d4b7-109">Дополнительные сведения о синхронизации доступа см. в разделе [Синхронизация выполнения нескольких потоков](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="6d4b7-109">For more information about synchronizing access, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

 

 



