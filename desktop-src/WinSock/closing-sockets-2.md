---
description: Вспклосесоккет освобождает дескриптор сокета таким образом, что все ожидающие операции в любом потоке того же процесса будут прерваны, а дальнейшая ссылка на нее завершится ошибкой.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Закрывающие сокеты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d0c877767925f67e07427a77dc8ec8445f30c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541610"
---
# <a name="closing-sockets"></a><span data-ttu-id="55919-103">Закрывающие сокеты</span><span class="sxs-lookup"><span data-stu-id="55919-103">Closing Sockets</span></span>

<span data-ttu-id="55919-104">[**Вспклосесоккет**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) освобождает дескриптор сокета таким образом, что все ожидающие операции в любом потоке того же процесса будут прерваны, а дальнейшая ссылка на нее завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="55919-104">[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) releases the socket descriptor so that any pending operations in any threads of the same process will be aborted, and any further reference to it will fail.</span></span> <span data-ttu-id="55919-105">Обратите внимание, что для общих сокетов следует применять счетчик ссылок и только в случае, если это последняя ссылка на базовый сокет, должны ли сведения, связанные с этим сокетом, быть отклонены, если не запрашивается корректное закрытие (т \_ . е. донтлинжер не задано).</span><span class="sxs-lookup"><span data-stu-id="55919-105">Note that a reference count should be employed for shared sockets, and only if this is the last reference to an underlying socket, should the information associated with this socket be discarded, provided graceful close is not requested (that is, SO\_DONTLINGER is not set).</span></span> <span data-ttu-id="55919-106">В случае \_ установки донтлинжер все данные, поставленные в очередь на передачу, будут отправляться, если это возможно, прежде чем будет освобождена информация, связанная с сокетом.</span><span class="sxs-lookup"><span data-stu-id="55919-106">In the case of SO\_DONTLINGER being set, any data queued for transmission will be sent, if possible, before information associated with the socket is released.</span></span> <span data-ttu-id="55919-107">Дополнительные сведения см. в разделе **вспклосесоккет** .</span><span class="sxs-lookup"><span data-stu-id="55919-107">See **WSPCloseSocket** for more information.</span></span>

<span data-ttu-id="55919-108">Для поставщиков услуг Нонифс необходимо вызвать [**впуклосесоккесандле**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) , чтобы освободить обработчик сокетов до DLL-библиотеки Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="55919-108">For nonIFS service providers, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) must be invoked to release the socket handle back to the Windows Sockets 2 DLL.</span></span>

 

 
