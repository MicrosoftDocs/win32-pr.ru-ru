---
title: Тестирование и отладка
description: Имеется \ 0034; Echo \ 0034; прослушиватель, реализованный клиентом подключение к удаленному рабочему столу (RDC), который всегда имеется и ожидает входящих подключений.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672024"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="db4d9-103">Тестирование и отладка</span><span class="sxs-lookup"><span data-stu-id="db4d9-103">Testing and Debugging</span></span>

<span data-ttu-id="db4d9-104">Существует прослушиватель "echo", реализованный клиентом подключение к удаленному рабочему столу (RDC), который всегда присутствует и ожидает входящих подключений.</span><span class="sxs-lookup"><span data-stu-id="db4d9-104">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span> <span data-ttu-id="db4d9-105">При записи на стороне сервера модуля динамического виртуального канала (DVC) в качестве быстрой проверки можно открыть конечную точку с именем ECHO.</span><span class="sxs-lookup"><span data-stu-id="db4d9-105">When you are writing the server side of a dynamic virtual channel (DVC) module, as a quick test you can open an endpoint named "ECHO".</span></span> <span data-ttu-id="db4d9-106">Любая запись в канал, созданная из этой конечной точки, приведет к поставке одних и тех же данных.</span><span class="sxs-lookup"><span data-stu-id="db4d9-106">Any write to a channel that is instantiated from this endpoint will result in the receipt of the same data.</span></span>

<span data-ttu-id="db4d9-107">Этот метод можно использовать для тестирования реализации ввода-вывода на стороне сервера для измерения времени отклика для подключаемого модуля клиента подключение к удаленному рабочему столу (RDC) или для измерения задержки сети для клиента подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="db4d9-107">You can use this technique to test an input/output (I/O) implementation of the server-side module, to measure the response time for a Remote Desktop Connection (RDC) client plug-in, or to measure the network delay for the Remote Desktop Connection (RDC) client.</span></span> <span data-ttu-id="db4d9-108">Нет ограничений на объем данных, которые могут быть отправлены по этому каналу.</span><span class="sxs-lookup"><span data-stu-id="db4d9-108">There is no limitation on the amount of data that can be sent over this channel.</span></span>

 

 




