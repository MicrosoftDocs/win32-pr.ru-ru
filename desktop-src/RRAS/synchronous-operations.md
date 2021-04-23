---
title: Синхронные операции
description: При вызове команды RasDial в качестве синхронной операции функция не возвращает значение, пока не будет установлено соединение или не произойдет ошибка.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068458"
---
# <a name="synchronous-operations"></a><span data-ttu-id="b4a06-103">Синхронные операции</span><span class="sxs-lookup"><span data-stu-id="b4a06-103">Synchronous Operations</span></span>

<span data-ttu-id="b4a06-104">При вызове команды [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) в качестве синхронной операции функция не возвращает значение, пока не будет установлено соединение или не произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="b4a06-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as a synchronous operation, the function does not return until the connection has been established or an error occurs.</span></span> <span data-ttu-id="b4a06-105">Синхронный режим предоставляет клиенту службы удаленного доступа простой способ установить соединение.</span><span class="sxs-lookup"><span data-stu-id="b4a06-105">Synchronous mode provides a simple way for a RAS client to establish a connection.</span></span> <span data-ttu-id="b4a06-106">Клиент может просто вызвать **rasdial**, подождать, пока функция вернет, а затем вызвать функцию [**расжетконнектстатус**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) , чтобы определить, была ли операция подключения успешной.</span><span class="sxs-lookup"><span data-stu-id="b4a06-106">The client can simply call **RasDial**, wait for the function to return, and then call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to determine whether the connection operation was successful.</span></span> <span data-ttu-id="b4a06-107">После установки соединения клиентское приложение может завершиться без разрыва соединения.</span><span class="sxs-lookup"><span data-stu-id="b4a06-107">Once the connection has been established, the client application can terminate without breaking the connection.</span></span> <span data-ttu-id="b4a06-108">При возникновении ошибки клиентское приложение должно [завершить операцию подключения](disconnecting.md) до завершения работы.</span><span class="sxs-lookup"><span data-stu-id="b4a06-108">If an error occurs, the client application must [shut down the connection operation](disconnecting.md) before terminating.</span></span>

<span data-ttu-id="b4a06-109">Недостаток синхронного режима заключается в том, что клиент не получает уведомления о ходе выполнения, так как операция подключения продолжается.</span><span class="sxs-lookup"><span data-stu-id="b4a06-109">The disadvantage of synchronous mode is that the client does not receive progress notifications as the connection operation proceeds.</span></span> <span data-ttu-id="b4a06-110">В качестве обходного решения для такого отсутствия уведомлений о ходе выполнения клиент синхронного режима может использовать отдельный поток, который вызывает [**расжетконнектстатус**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) для опроса и отображения текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="b4a06-110">As a workaround for this lack of progress notifications, a synchronous mode client can use a separate thread that calls [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) to poll for and display the current state.</span></span> <span data-ttu-id="b4a06-111">Однако для клиентов RAS, желающих получить сведения о ходе выполнения, предпочтительным методом является асинхронный вызов команды [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .</span><span class="sxs-lookup"><span data-stu-id="b4a06-111">However, for RAS clients that want to receive progress information, the preferred technique is to invoke [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchronously.</span></span>

 

 




