---
title: Асинхронные операции
description: При вызове команды RasDial в качестве асинхронной операции функция немедленно возвращает значение.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db434b7e6d080933e7e21de056f9af5ea7d57dfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411063"
---
# <a name="asynchronous-operations"></a><span data-ttu-id="b9872-103">Асинхронные операции</span><span class="sxs-lookup"><span data-stu-id="b9872-103">Asynchronous Operations</span></span>

<span data-ttu-id="b9872-104">При вызове команды [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) в качестве асинхронной операции функция немедленно возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b9872-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as an asynchronous operation, the function returns immediately.</span></span> <span data-ttu-id="b9872-105">В асинхронном режиме вызов **rasdial** должен указывать [обработчик уведомлений](notification-handlers.md) , используемый диспетчером подключений удаленного доступа для информирования клиента при изменении состояния операции подключения или при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9872-105">In asynchronous mode, the **RasDial** call must specify a [notification handler](notification-handlers.md) that the Remote Access Connection Manager uses to inform the client whenever the connection operation changes states or an error occurs.</span></span>

<span data-ttu-id="b9872-106">Обработчик уведомлений может быть окном для получения сообщений или функцией обратного вызова [**расдиалфунк**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)или [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) .</span><span class="sxs-lookup"><span data-stu-id="b9872-106">The notification handler can be a window to receive messages, or a [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1), or [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) callback function.</span></span> <span data-ttu-id="b9872-107">Диспетчер подключений удаленного доступа делает свои асинхронные уведомления в контексте потока, который выполнил вызов [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .</span><span class="sxs-lookup"><span data-stu-id="b9872-107">The Remote Access Connection Manager makes its asynchronous notifications in the context of the thread that made the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call.</span></span> <span data-ttu-id="b9872-108">По этой причине вызывающий поток не должен завершаться до тех пор, пока операция подключения не будет успешно установлена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="b9872-108">For this reason, the calling thread must not terminate until the connection operation has been successfully established or an error occurs.</span></span> <span data-ttu-id="b9872-109">Как и в синхронном режиме, клиентское приложение может безопасно завершиться после установления соединения и должно [завершить операцию подключения в](disconnecting.md) случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9872-109">As in synchronous mode, the client application can safely terminate once the connection has been established, and it must [shut down the connection operation](disconnecting.md) if an error occurs.</span></span>

 

 




