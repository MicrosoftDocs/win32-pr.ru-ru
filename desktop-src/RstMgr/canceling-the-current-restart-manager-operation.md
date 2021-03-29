---
title: Отмена текущей операции диспетчера перезапуска
description: Если пользовательское действие направляет установщик для выполнения другого действия, можно использовать следующий метод для отмены текущей операции диспетчера перезапуска.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780195"
---
# <a name="canceling-the-current-restart-manager-operation"></a><span data-ttu-id="70f52-103">Отмена текущей операции диспетчера перезапуска</span><span class="sxs-lookup"><span data-stu-id="70f52-103">Canceling the Current Restart Manager Operation</span></span>

<span data-ttu-id="70f52-104">Если пользовательское действие направляет установщик для выполнения другого действия, можно использовать следующий метод для отмены текущей операции диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="70f52-104">When a user action directs the installer to perform a different action, the following method can be used to cancel the current Restart Manager operation.</span></span>

<span data-ttu-id="70f52-105">**Отмена текущей операции диспетчера перезапуска**</span><span class="sxs-lookup"><span data-stu-id="70f52-105">**To cancel the current Restart Manager operation**</span></span>

-   <span data-ttu-id="70f52-106">Установщик может вызвать функцию [**рмканцелкурренттаск**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) из другого потока, чтобы отменить текущую операцию [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) или [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="70f52-106">The installer can call the [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) function from another thread to cancel the current [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) operation.</span></span> <span data-ttu-id="70f52-107">Диспетчер перезапуска может отменить операцию в зависимости от того, в какой степени была выполнена операция при вызове функции **рмканцелкурренттаск** .</span><span class="sxs-lookup"><span data-stu-id="70f52-107">The Restart Manager may cancel the operation depending on the extent to which the operation has completed when the **RMCancelCurrentTask** function is called.</span></span>

 

 




