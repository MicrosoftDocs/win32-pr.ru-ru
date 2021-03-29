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
# <a name="canceling-the-current-restart-manager-operation"></a>Отмена текущей операции диспетчера перезапуска

Если пользовательское действие направляет установщик для выполнения другого действия, можно использовать следующий метод для отмены текущей операции диспетчера перезапуска.

**Отмена текущей операции диспетчера перезапуска**

-   Установщик может вызвать функцию [**рмканцелкурренттаск**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) из другого потока, чтобы отменить текущую операцию [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) или [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) . Диспетчер перезапуска может отменить операцию в зависимости от того, в какой степени была выполнена операция при вызове функции **рмканцелкурренттаск** .

 

 




