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
# <a name="getting-the-status-of-a-restart-manager-operation"></a><span data-ttu-id="87bb4-104">Получение состояния операции диспетчера перезапуска</span><span class="sxs-lookup"><span data-stu-id="87bb4-104">Getting the Status of a Restart Manager Operation</span></span>

<span data-ttu-id="87bb4-105">Когда необходимо завершить работу или перезапустить несколько приложений и служб, операция диспетчера перезапуска может занять продолжительное время.</span><span class="sxs-lookup"><span data-stu-id="87bb4-105">When many applications and services must be shut down or restarted, the Restart Manager operation can take an extended period of time.</span></span> <span data-ttu-id="87bb4-106">Для получения состояния текущей операции можно использовать следующий метод.</span><span class="sxs-lookup"><span data-stu-id="87bb4-106">The following method can be used to obtain the status of the current operation.</span></span>

<span data-ttu-id="87bb4-107">**Получение состояния текущей операции диспетчера перезапуска**</span><span class="sxs-lookup"><span data-stu-id="87bb4-107">**To get the status of the current Restart Manager operation**</span></span>

1.  <span data-ttu-id="87bb4-108">Установщик должен реализовать функцию [**\_ \_ \_ обратного вызова состояния записи RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) , которая определяет состояние приложений, которые были выключены или перезапущены.</span><span class="sxs-lookup"><span data-stu-id="87bb4-108">The installer should implement a [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function that determines the status of the applications that have been shut down or restarted.</span></span> <span data-ttu-id="87bb4-109">Функция может предоставить сведения для пользовательского интерфейса или журнала.</span><span class="sxs-lookup"><span data-stu-id="87bb4-109">The function can provide the information to the user interface or log.</span></span>
2.  <span data-ttu-id="87bb4-110">Установщик передает указатель на функцию [**\_ \_ \_ обратного вызова состояния записи RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) при вызове функции [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) или [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="87bb4-110">The installer passes the pointer to the [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function when calling the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>

 

 