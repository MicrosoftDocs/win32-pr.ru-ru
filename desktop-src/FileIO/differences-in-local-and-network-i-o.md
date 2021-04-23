---
description: Различия между локальными операциями ввода-вывода и сетевыми операциями ввода-вывода в Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Различия в локальных и сетевых операциях ввода-вывода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663609"
---
# <a name="differences-in-local-and-network-io"></a><span data-ttu-id="2a2ea-103">Различия в локальных и сетевых операциях ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="2a2ea-103">Differences in Local and Network I/O</span></span>

<span data-ttu-id="2a2ea-104">Между локальными операциями ввода-вывода и сетевыми операциями ввода-вывода в Windows есть некоторые важные различия:</span><span class="sxs-lookup"><span data-stu-id="2a2ea-104">There are some notable differences between local I/O and network I/O on Windows:</span></span>

-   <span data-ttu-id="2a2ea-105">Поддержка сетевых операций ввода-вывода зависит от перенаправления и сетевого протокола.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-105">Network I/O support depends on the redirector and the network protocol.</span></span>
-   <span data-ttu-id="2a2ea-106">Производительность сетевого ввода-вывода зависит от количества выполняемых сетевых операций ввода-вывода и скорости сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-106">Network I/O performance depends on how many network I/O operations are taking place and the speed of the network connection.</span></span> <span data-ttu-id="2a2ea-107">Приложение должно иметь возможность обрабатывать сетевые операции ввода-вывода с серверами, которые могут выполняться намного быстрее или медленнее, чем на локальном компьютере, а также как временные изменения в емкости сети.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-107">Your application must be able to handle network I/O operations with servers that may be much faster or slower than your local machine, as well as transient changes in network capacity.</span></span> <span data-ttu-id="2a2ea-108">В таких случаях приложению может потребоваться больше времени для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-108">In these cases, your application may need to allow more time for the operation to complete.</span></span>
-   <span data-ttu-id="2a2ea-109">Функции, используемые для выполнения локальных файловых операций ввода-вывода, могут работать по сети по-разному.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-109">The functions you use to perform local file I/O may behave differently over the network.</span></span> <span data-ttu-id="2a2ea-110">Например, операция ввода-вывода в сети, выполнение которой занимает много времени, может истекает. В некоторых ситуациях дескрипторы файлов могут оставаться открытыми неограниченно долго по этой причине.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-110">For example, a network I/O operation that takes a long time to complete may time out. In some situations, file handles may be left open indefinitely because of this.</span></span> <span data-ttu-id="2a2ea-111">Другой пример состоит в том, что функции могут возвращать коды ошибок для конкретного приложения, относящиеся к сетевому вводу-выводу.</span><span class="sxs-lookup"><span data-stu-id="2a2ea-111">Another example is that functions may return error codes for your application to process that are specific to network I/O.</span></span>

 

 



