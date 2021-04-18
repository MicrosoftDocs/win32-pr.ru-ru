---
title: Интерфейс IUniversalOrchestrator
description: COM-интерфейс, предоставляющий методы, позволяющие клиенту обмениваться данными с универсальной Orchestrator.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105719755"
---
# <a name="iuniversalorchestrator-interface"></a><span data-ttu-id="940c6-103">Интерфейс IUniversalOrchestrator</span><span class="sxs-lookup"><span data-stu-id="940c6-103">IUniversalOrchestrator interface</span></span>

> [!NOTE] 
> <span data-ttu-id="940c6-104">Этот API принадлежит к универсальному API Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="940c6-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="940c6-105">**Иуниверсалорчестратор** — это COM-интерфейс, предоставляющий следующие методы, позволяющие клиенту обмениваться данными с универсальной Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="940c6-105">**IUniversalOrchestrator** is a COM interface that provides the following methods to allow a client to communicate with the Universal Orchestrator.</span></span>

## <a name="methods"></a><span data-ttu-id="940c6-106">Методы</span><span class="sxs-lookup"><span data-stu-id="940c6-106">Methods</span></span>

|<span data-ttu-id="940c6-107">Метод</span><span class="sxs-lookup"><span data-stu-id="940c6-107">Method</span></span> | <span data-ttu-id="940c6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="940c6-108">Description</span></span> |
|---|---|
|[<span data-ttu-id="940c6-109">:: Счедулеворк</span><span class="sxs-lookup"><span data-stu-id="940c6-109">::ScheduleWork</span></span>](universalorchestrator-schedulework.md) | <span data-ttu-id="940c6-110">Регистрирует ожидающие работы с универсальной Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="940c6-110">Registers pending work with the Universal Orchestrator.</span></span> |
|[<span data-ttu-id="940c6-111">:: Ворккомплетед</span><span class="sxs-lookup"><span data-stu-id="940c6-111">::WorkCompleted</span></span>](universalorchestrator-workcompleted.md) | <span data-ttu-id="940c6-112">Информирует универсальную Orchestrator о том, что вся работа завершена.</span><span class="sxs-lookup"><span data-stu-id="940c6-112">Informs the Universal Orchestrator that all work is complete.</span></span> |
|[<span data-ttu-id="940c6-113">:: Хасмораториумпассед</span><span class="sxs-lookup"><span data-stu-id="940c6-113">::HasMoratoriumPassed</span></span>](universalorchestrator-hasmoratoriumpassed.md) | <span data-ttu-id="940c6-114">Запрашивает универсальную Orchestrator, чтобы определить, работает ли она сразу после завершения работы нового устройства.</span><span class="sxs-lookup"><span data-stu-id="940c6-114">Queries Universal Orchestrator to determine if it is operating immediately after the new device Out of Box Experience.</span></span> |


## <a name="requirements"></a><span data-ttu-id="940c6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="940c6-115">Requirements</span></span>

| <span data-ttu-id="940c6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="940c6-116">Requirement</span></span> | <span data-ttu-id="940c6-117">Версия</span><span class="sxs-lookup"><span data-stu-id="940c6-117">Version</span></span> |
|---|---|
| <span data-ttu-id="940c6-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="940c6-118">Minimum supported client</span></span> | <span data-ttu-id="940c6-119">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="940c6-119">Windows 10 1903</span></span> |
|   |   |