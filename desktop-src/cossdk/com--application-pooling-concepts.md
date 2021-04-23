---
description: Пул приложений COM+ позволяет масштабировать однопотоковые процессы, аналогично тому, как пул потоков позволяет масштабировать однопотоковые объекты.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Основные понятия пула приложений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895642"
---
# <a name="com-application-pooling-concepts"></a><span data-ttu-id="7c231-103">Основные понятия пула приложений COM+</span><span class="sxs-lookup"><span data-stu-id="7c231-103">COM+ Application Pooling Concepts</span></span>

<span data-ttu-id="7c231-104">Пул приложений COM+ позволяет масштабировать однопотоковые процессы, аналогично тому, как пул потоков позволяет масштабировать однопотоковые объекты.</span><span class="sxs-lookup"><span data-stu-id="7c231-104">COM+ application pooling allows single-threaded processes to scale, similar to the way that thread pooling allows single-threaded objects to scale.</span></span> <span data-ttu-id="7c231-105">Пулы приложений также могут помочь в восстановлении после сбоев в отдельных процессах, предоставляя другим работающим процессам возможность обработки активаций.</span><span class="sxs-lookup"><span data-stu-id="7c231-105">Application pooling can also help recover from failures in single processes by providing other running processes able to handle activations.</span></span>

> [!Note]  
> <span data-ttu-id="7c231-106">Библиотечные приложения имеют свойства перезапуска и группирования для своего хостового процесса.</span><span class="sxs-lookup"><span data-stu-id="7c231-106">Library applications have the recycling and pooling properties of their host process.</span></span>

 

<span data-ttu-id="7c231-107">Все методы интерфейса [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) поддерживают пулы приложений.</span><span class="sxs-lookup"><span data-stu-id="7c231-107">All methods of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface support application pooling.</span></span>

<span data-ttu-id="7c231-108">Пул приложений COM+ можно настроить для каждого приложения с помощью свойства Конкуррентаппс объекта [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции [**приложений**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="7c231-108">COM+ application pooling is configurable per application by using the ConcurrentApps property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="7c231-109">Конкуррентаппс — это целочисленное значение, указывающее максимальное количество одновременных процессов Dllhost, которые должны быть запущены для активации службы для приложения.</span><span class="sxs-lookup"><span data-stu-id="7c231-109">ConcurrentApps is an integer value that specifies the maximum number of simultaneous Dllhost processes that should be started to service activations for an application.</span></span> <span data-ttu-id="7c231-110">Это свойство можно задать с помощью средства администрирования служб компонентов или программно.</span><span class="sxs-lookup"><span data-stu-id="7c231-110">This property can be set by using the Component Services administration tool or programmatically.</span></span>

<span data-ttu-id="7c231-111">Если свойство Конкуррентаппс имеет значение 1, которое является значением по умолчанию, служба пулов приложений COM+ отключена.</span><span class="sxs-lookup"><span data-stu-id="7c231-111">If the ConcurrentApps property is set to 1, which is the default value, the COM+ Application Pooling service is disabled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c231-112">См. также</span><span class="sxs-lookup"><span data-stu-id="7c231-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c231-113">Задачи пула приложений COM+</span><span class="sxs-lookup"><span data-stu-id="7c231-113">COM+ Application Pooling Tasks</span></span>](com--application-pooling-tasks.md)
</dt> <dt>

[<span data-ttu-id="7c231-114">Основные понятия перезапуска приложений COM+</span><span class="sxs-lookup"><span data-stu-id="7c231-114">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



