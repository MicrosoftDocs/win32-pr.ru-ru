---
description: Получение ответа
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Получение ответа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539287"
---
# <a name="receiving-a-response"></a><span data-ttu-id="8ab6e-103">Получение ответа</span><span class="sxs-lookup"><span data-stu-id="8ab6e-103">Receiving a Response</span></span>

<span data-ttu-id="8ab6e-104">Поскольку поставленные в очередь компоненты предназначены для работы в асинхронном режиме, клиентские приложения не должны блокироваться при ожидании ответа от запроса, поставленного в очередь.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-104">Because queued components are designed to work asynchronously, client applications should not block while waiting for a response from a queued request.</span></span> <span data-ttu-id="8ab6e-105">Тем не менее часто бывает полезно, чтобы клиентское приложение или связанное приложение на клиентском компьютере получало ответ в конечном итоге.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-105">Nevertheless, it is often useful for the client application or a related application on the client machine to receive a response eventually.</span></span> <span data-ttu-id="8ab6e-106">Например, клиент может получать уведомления о том, что запрошенная транзакция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-106">For example, a client may want to be notified when a requested transaction has been completed successfully.</span></span>

<span data-ttu-id="8ab6e-107">Существует множество способов, с помощью которых компонент в очереди отправляет ответ обратно вызывающему объекту в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-107">There are a variety of ways for a queued component to send a response back to its caller asynchronously.</span></span> <span data-ttu-id="8ab6e-108">Например, он может отправить сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-108">For example, it could send an email.</span></span> <span data-ttu-id="8ab6e-109">Кроме того, сервер может публиковать слабо связанные события, на которые клиент может подписываться.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-109">Alternatively, the server could publish loosely coupled events to which the client could subscribe.</span></span>

<span data-ttu-id="8ab6e-110">Другой способ получения ответа от компонента очереди, запущенного на сервере, заключается в том, что клиент передает вызванный метод объекту уведомления.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-110">Another way for a client to obtain a response from a queued component that runs on a server is for the client to pass the called method a notification object.</span></span> <span data-ttu-id="8ab6e-111">Объект уведомления — это экземпляр компонента в очереди, который выполняется на клиенте.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-111">A notification object is an instance of a queued component that runs on the client.</span></span> <span data-ttu-id="8ab6e-112">Такой объект уведомления может быть довольно простым, содержащий только целое число, используемое для представления значения ошибки, или может быть довольно сложным, содержащим всю информацию, необходимую для отката транзакции на клиенте.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-112">Such a notification object might be quite simple, containing only an integer that is used to represent an error value, or it might be quite complex, containing all the information necessary to roll back a transaction on the client.</span></span> <span data-ttu-id="8ab6e-113">В любом случае вызывающий клиент передает объект уведомления в качестве входного параметра каждый раз, когда он помещает ответ от компонента очереди, который выполняется на сервере.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-113">In either case, the calling client passes a notification object as an input parameter whenever it desires a response from a queued component that runs on a server.</span></span> <span data-ttu-id="8ab6e-114">Так как объект уведомления помещается в очередь, сервер может вызвать метод для изменения его состояния, которое впоследствии может быть считано клиентом.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-114">Because the notification object is queued, the server can call on its methods to alter its state, which can subsequently be read out by the client.</span></span> <span data-ttu-id="8ab6e-115">В этом сценарии служба очередей компонентов COM+ используется как на клиенте, так и на сервере для обеспечения асинхронного взаимодействия в обоих направлениях.</span><span class="sxs-lookup"><span data-stu-id="8ab6e-115">In this scenario, the COM+ queued components service is used on both the client and the server to allow asynchronous communication in both directions.</span></span>

 

 



