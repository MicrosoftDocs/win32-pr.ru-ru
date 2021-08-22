---
title: Отмена текущей операции диспетчера перезапуска
description: Если пользовательское действие направляет установщик для выполнения другого действия, можно использовать следующий метод для отмены текущей операции диспетчера перезапуска.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c745a76ab8c72acaff0b9f1ae85ded380e1113c3687822e916b422cad9ef51f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010252"
---
# <a name="canceling-the-current-restart-manager-operation"></a>Отмена текущей операции диспетчера перезапуска

Если пользовательское действие направляет установщик для выполнения другого действия, можно использовать следующий метод для отмены текущей операции диспетчера перезапуска.

**Отмена текущей операции диспетчера перезапуска**

-   Установщик может вызвать функцию [**рмканцелкурренттаск**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) из другого потока, чтобы отменить текущую операцию [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) или [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) . Диспетчер перезапуска может отменить операцию в зависимости от того, в какой степени была выполнена операция при вызове функции **рмканцелкурренттаск** .

 

 




