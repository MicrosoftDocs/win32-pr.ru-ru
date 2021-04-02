---
description: Описание функциональных возможностей перенаправителя сети.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Сетевые перенаправителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913532"
---
# <a name="network-redirectors"></a><span data-ttu-id="60805-103">Сетевые перенаправителя</span><span class="sxs-lookup"><span data-stu-id="60805-103">Network Redirectors</span></span>

<span data-ttu-id="60805-104">Сетевой перенаправитель — это драйвер файловой системы (или ФСД), который работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="60805-104">A network redirector is a file system driver (or FSD) that functions in the following manner:</span></span>

-   <span data-ttu-id="60805-105">В качестве клиента в сетевой операции ввода-вывода путем отправки запросов ввода-вывода на серверы и обработки ответов от серверов.</span><span class="sxs-lookup"><span data-stu-id="60805-105">As a client in a network I/O operation by sending I/O requests to servers and processing the responses from the servers.</span></span>
-   <span data-ttu-id="60805-106">Как сервер в сетевой операции ввода-вывода, получая запросы ввода-вывода от серверов и обрабатывая запросы.</span><span class="sxs-lookup"><span data-stu-id="60805-106">As a server in a network I/O operation by receiving I/O requests from servers and processing the requests.</span></span>

<span data-ttu-id="60805-107">Он выполняет все низкоуровневые действия с сервером при разрешении имени файла, предоставленного приложением, с расположением ресурса на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="60805-107">It performs all of the low-level interaction with the server in resolving the file name provided by the application with the location of the resource on the remote server.</span></span> <span data-ttu-id="60805-108">Таким образом перенаправитель позволяет приложению получать доступ к ресурсам на удаленных серверах и управлять ими, как если бы они находились на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="60805-108">In this way, the redirector enables the application to access and manipulate resources on remote servers as if they were located on the local machine.</span></span>

<span data-ttu-id="60805-109">Перенаправления работают полностью в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="60805-109">Redirectors operate entirely within kernel mode.</span></span> <span data-ttu-id="60805-110">Это обеспечивает следующие преимущества производительности по сравнению с альтернативами пользовательского режима:</span><span class="sxs-lookup"><span data-stu-id="60805-110">This provides the following performance advantages over user-mode alternatives:</span></span>

-   <span data-ttu-id="60805-111">Он может взаимодействовать с ФСДС режима ядра, работающим на сервере, например ФСД сервера, без необходимости переключения контекста пользователя на ядро и режима ядра в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="60805-111">It can interact with kernel-mode FSDs running on the server, such as the server FSD, without the need for user-to-kernel mode and kernel-to-user mode context switches.</span></span>
-   <span data-ttu-id="60805-112">Он может взаимодействовать в режиме ядра с диспетчером кэша на сервере для кэширования данных ввода-вывода, которые диспетчер кэша сервера отправляет клиенту.</span><span class="sxs-lookup"><span data-stu-id="60805-112">It can interact in kernel mode with the cache manager on the server to cache I/O data that the server cache manager sends on the client.</span></span>
-   <span data-ttu-id="60805-113">Функции API, настраиваемые для удаленных запросов ввода-вывода, и изменения стандартных функций файлового ввода-вывода для предоставления этой функции не требуются.</span><span class="sxs-lookup"><span data-stu-id="60805-113">API functions custom-made for remote I/O requests, and changes to the standard file I/O functions to provide this functionality, are not necessary.</span></span>

 

 



