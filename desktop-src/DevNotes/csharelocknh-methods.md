---
description: Группа методов, используемых для управления блокировками.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Методы Кшарелоккнх
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655767"
---
# <a name="csharelocknh-methods"></a><span data-ttu-id="94e05-103">Методы Кшарелоккнх</span><span class="sxs-lookup"><span data-stu-id="94e05-103">CShareLockNH Methods</span></span>

<span data-ttu-id="94e05-104">Группа методов, используемых для управления блокировками.</span><span class="sxs-lookup"><span data-stu-id="94e05-104">A group of methods that is used to manipulate locks.</span></span>

## <a name="methods"></a><span data-ttu-id="94e05-105">Методы</span><span class="sxs-lookup"><span data-stu-id="94e05-105">Methods</span></span>

<span data-ttu-id="94e05-106">Ниже приведены методы, экспортируемые с помощью Rwnh.dll.</span><span class="sxs-lookup"><span data-stu-id="94e05-106">The following are methods exported by Rwnh.dll.</span></span>



| <span data-ttu-id="94e05-107">Метод</span><span class="sxs-lookup"><span data-stu-id="94e05-107">Method</span></span>                                                                   | <span data-ttu-id="94e05-108">Описание</span><span class="sxs-lookup"><span data-stu-id="94e05-108">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="94e05-109">**ексклусивелокк**</span><span class="sxs-lookup"><span data-stu-id="94e05-109">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)                     | <span data-ttu-id="94e05-110">Получает блокировку потоков чтения/записи.</span><span class="sxs-lookup"><span data-stu-id="94e05-110">Acquires a reader/writer lock.</span></span>                                  |
| [<span data-ttu-id="94e05-111">**ексклусиветопартиал**</span><span class="sxs-lookup"><span data-stu-id="94e05-111">**ExclusiveToPartial**</span></span>](csharelocknh--exclusivetopartial.md)           | <span data-ttu-id="94e05-112">Изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="94e05-112">Changes the state.</span></span>                                              |
| [<span data-ttu-id="94e05-113">**ексклусивеунлокк**</span><span class="sxs-lookup"><span data-stu-id="94e05-113">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)                 | <span data-ttu-id="94e05-114">Снимает блокировку.</span><span class="sxs-lookup"><span data-stu-id="94e05-114">Releases a lock.</span></span>                                                |
| [<span data-ttu-id="94e05-115">**фирстпартиалтоексклусиве**</span><span class="sxs-lookup"><span data-stu-id="94e05-115">**FirstPartialToExclusive**</span></span>](csharelocknh--firstpartialtoexclusive.md) | <span data-ttu-id="94e05-116">Используется при преобразовании частичной блокировки в монопольную блокировку.</span><span class="sxs-lookup"><span data-stu-id="94e05-116">Used in converting a partial lock to an exclusive lock.</span></span>         |
| [<span data-ttu-id="94e05-117">**партиаллокк**</span><span class="sxs-lookup"><span data-stu-id="94e05-117">**PartialLock**</span></span>](csharelocknh--partiallock.md)                         | <span data-ttu-id="94e05-118">Предотвращает получение блокировки более чем одним потоком.</span><span class="sxs-lookup"><span data-stu-id="94e05-118">Prevents more than one thread from completing acquiring a lock.</span></span> |
| [<span data-ttu-id="94e05-119">**партиалунлокк**</span><span class="sxs-lookup"><span data-stu-id="94e05-119">**PartialUnlock**</span></span>](csharelocknh--partialunlock.md)                     | <span data-ttu-id="94e05-120">Освобождает частичную блокировку.</span><span class="sxs-lookup"><span data-stu-id="94e05-120">Releases a partial lock.</span></span>                                        |
| [<span data-ttu-id="94e05-121">**шарелокк**</span><span class="sxs-lookup"><span data-stu-id="94e05-121">**ShareLock**</span></span>](csharelocknh--sharelock.md)                             | <span data-ttu-id="94e05-122">Получает блокировку для общего режима.</span><span class="sxs-lookup"><span data-stu-id="94e05-122">Obtains a lock for shared mode.</span></span>                                 |
| [<span data-ttu-id="94e05-123">**шареунлокк**</span><span class="sxs-lookup"><span data-stu-id="94e05-123">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)                         | <span data-ttu-id="94e05-124">Снимает блокировку с общего режима.</span><span class="sxs-lookup"><span data-stu-id="94e05-124">Releases a lock from shared mode.</span></span>                               |
| [<span data-ttu-id="94e05-125">**шаредтопартиал**</span><span class="sxs-lookup"><span data-stu-id="94e05-125">**SharedToPartial**</span></span>](csharelocknh--sharedtopartial.md)                 | <span data-ttu-id="94e05-126">Получает частичную блокировку.</span><span class="sxs-lookup"><span data-stu-id="94e05-126">Obtains a partial lock.</span></span>                                         |
| [<span data-ttu-id="94e05-127">**трексклусивелокк**</span><span class="sxs-lookup"><span data-stu-id="94e05-127">**TryExclusiveLock**</span></span>](csharelocknh--tryexclusivelock.md)               | <span data-ttu-id="94e05-128">Получает монопольную блокировку.</span><span class="sxs-lookup"><span data-stu-id="94e05-128">Obtains a lock exclusively.</span></span>                                     |



 

 

 



