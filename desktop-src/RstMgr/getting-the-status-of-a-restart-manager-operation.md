---
title: Получение состояния операции диспетчера перезапуска
description: Когда необходимо завершить работу или перезапустить несколько приложений и служб, операция диспетчера перезапуска может занять продолжительное время. Для получения состояния текущей операции можно использовать следующий метод.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f96b7e247bdeb661e29d39cbb64bd8b7aaaa5caf9478bd1f1acc483c1dfbd614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010192"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a>Получение состояния операции диспетчера перезапуска

Когда необходимо завершить работу или перезапустить несколько приложений и служб, операция диспетчера перезапуска может занять продолжительное время. Для получения состояния текущей операции можно использовать следующий метод.

**Получение состояния текущей операции диспетчера перезапуска**

1.  Установщик должен реализовать функцию [**\_ \_ \_ обратного вызова состояния записи RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) , которая определяет состояние приложений, которые были выключены или перезапущены. Функция может предоставить сведения для пользовательского интерфейса или журнала.
2.  Установщик передает указатель на функцию [**\_ \_ \_ обратного вызова состояния записи RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) при вызове функции [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) или [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .

 

 