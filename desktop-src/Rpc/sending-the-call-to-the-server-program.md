---
title: Отправка вызова в программу сервера
description: После подключения клиентского времени выполнения RPC к конечной точке сервера он выполняет упаковку аргументов и отправляет их на сервер.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Удаленный вызов процедур RPC, задачи, отправка вызова на сервер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331784"
---
# <a name="sending-the-call-to-the-server-program"></a><span data-ttu-id="d9c4a-104">Отправка вызова в программу сервера</span><span class="sxs-lookup"><span data-stu-id="d9c4a-104">Sending the Call to the Server Program</span></span>

<span data-ttu-id="d9c4a-105">После подключения клиентского времени выполнения RPC к конечной точке сервера он выполняет упаковку аргументов и отправляет их на сервер.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-105">Once the client side RPC run time has connected to the server endpoint, it marshalls the arguments and sends them to the server.</span></span> <span data-ttu-id="d9c4a-106">Время выполнения RPC сервера дает Упакованные аргументы заглушке, которые исменяют их, а затем передаются в серверные процедуры.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-106">The server RPC run time gives the marshalled arguments to the stub that unmarshalls them, and then passes them to the server routines.</span></span> <span data-ttu-id="d9c4a-107">Когда серверные процедуры возвращают, заглушка выбирает \[ выходные \] и выходные параметры, \[ \] а также возвращаемое значение, маршалируется и передает их в серверное время выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-107">When the server routines return, the stub picks up the \[out\] and \[in,out\] parameters and the return value, marshalls them, and sends the marshalled data to the server RPC run time.</span></span> <span data-ttu-id="d9c4a-108">Время выполнения RPC отправляет данные обратно клиенту, где время выполнения RPC клиента направляет их на клиентскую заглушку, которая рассылает их и возвращает вызывающей стороне.</span><span class="sxs-lookup"><span data-stu-id="d9c4a-108">The RPC run time sends the data back to the client, where the client RPC run time hands them off to the client side stub that unmarshalls them and returns them to the caller.</span></span>

 

 




