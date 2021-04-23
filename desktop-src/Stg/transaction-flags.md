---
title: Флаги транзакций
description: Объект может быть открыт в прямом или транзакционном режиме.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258584"
---
# <a name="transaction-flags"></a><span data-ttu-id="a3c3a-103">Флаги транзакций</span><span class="sxs-lookup"><span data-stu-id="a3c3a-103">Transaction Flags</span></span>

<span data-ttu-id="a3c3a-104">Объект может быть открыт в прямом или транзакционном режиме.</span><span class="sxs-lookup"><span data-stu-id="a3c3a-104">An object can be opened in either direct or transacted mode.</span></span> <span data-ttu-id="a3c3a-105">При открытии объекта в прямом режиме изменения вносятся немедленно и постоянно.</span><span class="sxs-lookup"><span data-stu-id="a3c3a-105">When an object is opened in direct mode, changes are made immediately and permanently.</span></span> <span data-ttu-id="a3c3a-106">Когда объект открывается в режиме транзакций, изменения помещаются в буфер, чтобы их можно было явным образом зафиксировать или отменить после завершения редактирования.</span><span class="sxs-lookup"><span data-stu-id="a3c3a-106">When an object is opened in transacted mode, changes are buffered so they can be explicitly committed or reverted once editing is complete.</span></span> <span data-ttu-id="a3c3a-107">Зафиксированные изменения сохраняются в объекте, в то время как отмененные изменения отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="a3c3a-107">Committed changes are saved to the object while reverted changes are discarded.</span></span> <span data-ttu-id="a3c3a-108">Режим доступа по умолчанию используется в режиме Direct.</span><span class="sxs-lookup"><span data-stu-id="a3c3a-108">Direct mode is the default access mode.</span></span>

<span data-ttu-id="a3c3a-109">Режим транзакций не требуется для родительского объекта хранилища, чтобы его можно было использовать во вложенном элементе.</span><span class="sxs-lookup"><span data-stu-id="a3c3a-109">Transacted mode is not required on a parent storage object in order to use it on a nested element.</span></span> <span data-ttu-id="a3c3a-110">Однако транзакция для вложенного элемента вложена в транзакцию для родительского объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="a3c3a-110">A transaction for a nested element, however, is nested within the transaction for its parent storage object.</span></span> <span data-ttu-id="a3c3a-111">Таким образом, изменения, внесенные в дочерний объект, не могут быть зафиксированы, пока они не будут зафиксированы, и оба остаются незафиксированными, пока объект корневого хранилища (родитель верхнего уровня) на самом деле не записывается на диск.</span><span class="sxs-lookup"><span data-stu-id="a3c3a-111">Therefore, changes made to a child object cannot be committed until those made to the parent are committed, and both remain uncommitted until the root storage object (the top-level parent) is actually written to disk.</span></span> <span data-ttu-id="a3c3a-112">Иными словами, изменения перемещаются наружу: внутренние объекты публикуют изменения в транзакциях их непосредственных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a3c3a-112">In other words, the changes move outward: inner objects publish changes to the transactions of their immediate containers.</span></span>

 

 




