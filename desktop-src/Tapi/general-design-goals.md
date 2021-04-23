---
description: Следующий список содержит цели проектирования для TAPI MSP.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Общие цели проектирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682888"
---
# <a name="general-design-goals"></a><span data-ttu-id="2f192-103">Общие цели проектирования</span><span class="sxs-lookup"><span data-stu-id="2f192-103">General Design Goals</span></span>

<span data-ttu-id="2f192-104">Следующий список содержит цели проектирования для TAPI MSP.</span><span class="sxs-lookup"><span data-stu-id="2f192-104">The following list contains the TAPI MSP design goals.</span></span>

-   <span data-ttu-id="2f192-105">Базовые классы были сохранены простыми, и члены и методы появились только при крайней необходимости.</span><span class="sxs-lookup"><span data-stu-id="2f192-105">Base classes have been kept simple, with members and methods introduced only when absolutely necessary.</span></span>
-   <span data-ttu-id="2f192-106">Простое наследование.</span><span class="sxs-lookup"><span data-stu-id="2f192-106">Simple inheritance.</span></span> <span data-ttu-id="2f192-107">Нет множественного наследования между классами, хотя для интерфейсов используется несколько наследований.</span><span class="sxs-lookup"><span data-stu-id="2f192-107">No multiple inheritance among classes, although multiple inheritance is used for the interfaces.</span></span>
-   <span data-ttu-id="2f192-108">Блокировка происходит только в одном направлении, чтобы предотвратить взаимоблокировку.</span><span class="sxs-lookup"><span data-stu-id="2f192-108">Locking happens only in one direction to prevent deadlock.</span></span> <span data-ttu-id="2f192-109">Методы для объекта вызова, требующего блокировки вызова, могут вызывать методы в потоке, для которого требуется блокировка потока.</span><span class="sxs-lookup"><span data-stu-id="2f192-109">Methods on the call object that require the lock on the call might call methods on the stream that require the lock on the stream.</span></span> <span data-ttu-id="2f192-110">Однако методы в потоке, требующем блокировки потока, никогда не будут вызывать метод для вызова, для которого требуется блокировка вызова.</span><span class="sxs-lookup"><span data-stu-id="2f192-110">However, methods on the stream that require the lock on the stream will never call a method on the call that requires a lock on the call.</span></span>
-   <span data-ttu-id="2f192-111">Рефкаунтс используются для защиты доступа.</span><span class="sxs-lookup"><span data-stu-id="2f192-111">Refcounts are used to protect access.</span></span> <span data-ttu-id="2f192-112">Все обратные вызовы, отправленные в пул потоков, содержат рефкаунтс.</span><span class="sxs-lookup"><span data-stu-id="2f192-112">All callbacks posted to the thread pool hold refcounts.</span></span> <span data-ttu-id="2f192-113">Значение refcount отменяется при отмене ожидания.</span><span class="sxs-lookup"><span data-stu-id="2f192-113">The refcount is canceled when the wait is canceled.</span></span> <span data-ttu-id="2f192-114">Объект Address имеет рефкаунтс на терминалах.</span><span class="sxs-lookup"><span data-stu-id="2f192-114">The Address object has refcounts on Terminals.</span></span> <span data-ttu-id="2f192-115">Объекты Call имеют рефкаунтс в адресе и в потоках.</span><span class="sxs-lookup"><span data-stu-id="2f192-115">Call objects have refcounts on the Address and on Streams.</span></span> <span data-ttu-id="2f192-116">Объекты потока имеют рефкаунтс на вызовы и терминалы.</span><span class="sxs-lookup"><span data-stu-id="2f192-116">Stream objects have refcounts on Calls and Terminals.</span></span> <span data-ttu-id="2f192-117">У терминалов есть рефкаунтс потоков.</span><span class="sxs-lookup"><span data-stu-id="2f192-117">The Terminals have refcounts on Streams.</span></span> <span data-ttu-id="2f192-118">Циклическая рефкаунтс прерывается при вызове метода Shutdown объектов Address и Call.</span><span class="sxs-lookup"><span data-stu-id="2f192-118">The circular refcounts break when the shutdown method on the Address and Call objects is called.</span></span>

 

 



