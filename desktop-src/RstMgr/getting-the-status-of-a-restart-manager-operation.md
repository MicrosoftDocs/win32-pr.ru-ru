---
title: Получение состояния операции диспетчера перезапуска
description: Когда необходимо завершить работу или перезапустить несколько приложений и служб, операция диспетчера перезапуска может занять продолжительное время. Для получения состояния текущей операции можно использовать следующий метод.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134410"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a>Получение состояния операции диспетчера перезапуска

Когда необходимо завершить работу или перезапустить несколько приложений и служб, операция диспетчера перезапуска может занять продолжительное время. Для получения состояния текущей операции можно использовать следующий метод.

**Получение состояния текущей операции диспетчера перезапуска**

1.  Установщик должен реализовать функцию [**\_ \_ \_ обратного вызова состояния записи RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) , которая определяет состояние приложений, которые были выключены или перезапущены. Функция может предоставить сведения для пользовательского интерфейса или журнала.
2.  Установщик передает указатель на функцию [**\_ \_ \_ обратного вызова состояния записи RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) при вызове функции [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) или [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .

 

 