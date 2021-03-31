---
title: Как клиент устанавливает подключение
description: Чтобы установить сеанс связи между клиентом и сервером с серверной программой, клиентские приложения с явными дескрипторами должны создать дескриптор привязки.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068091"
---
# <a name="how-the-client-establishes-a-connection"></a><span data-ttu-id="03826-103">Как клиент устанавливает подключение</span><span class="sxs-lookup"><span data-stu-id="03826-103">How the Client Establishes a Connection</span></span>

<span data-ttu-id="03826-104">Чтобы установить сеанс связи между клиентом и сервером с серверной программой, клиентские приложения с явными дескрипторами должны создать дескриптор привязки.</span><span class="sxs-lookup"><span data-stu-id="03826-104">To establish a client/server communication session with a server program, client applications with explicit handles need to create a binding handle.</span></span> <span data-ttu-id="03826-105">После этого библиотека времени выполнения RPC находит компьютер, на котором размещена серверная программа.</span><span class="sxs-lookup"><span data-stu-id="03826-105">After they do, the RPC run-time library finds the computer that hosts the server program.</span></span> <span data-ttu-id="03826-106">Затем он находит конечную точку, которую серверная программа прослушивает, и направляет ее вызов.</span><span class="sxs-lookup"><span data-stu-id="03826-106">It then finds the endpoint that the server program is listening to and directs the call to it.</span></span> <span data-ttu-id="03826-107">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="03826-107">The following diagram illustrates this process.</span></span>

![Клиент RPC устанавливает подключение к серверу RPC.](images/clntcon.png)

<span data-ttu-id="03826-109">В этом разделе представлены сведения о том, как клиент подключается к серверной программе и выполняет удаленные процедуры, которые она предлагает.</span><span class="sxs-lookup"><span data-stu-id="03826-109">This section presents information about how the client connects to the server program and executes remote procedures that it offers.</span></span> <span data-ttu-id="03826-110">Существует множество подходов к выполнению этих шагов. в зависимости от выбранной структуры приложение может выбрать другой набор действий.</span><span class="sxs-lookup"><span data-stu-id="03826-110">There are many approaches to completing these steps; depending on the design chosen, an application may choose a different set of steps.</span></span> <span data-ttu-id="03826-111">Этот пример является просто одним из способов.</span><span class="sxs-lookup"><span data-stu-id="03826-111">This example is simply one way of doing so.</span></span>

<span data-ttu-id="03826-112">Обсуждение состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="03826-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="03826-113">Создание маркера привязки</span><span class="sxs-lookup"><span data-stu-id="03826-113">Creating a Binding Handle</span></span>](creating-a-binding-handle.md)
-   [<span data-ttu-id="03826-114">Выполнение удаленного вызова процедур</span><span class="sxs-lookup"><span data-stu-id="03826-114">Making a Remote Procedure Call</span></span>](making-a-remote-procedure-call.md)
-   [<span data-ttu-id="03826-115">Поиск программы сервера</span><span class="sxs-lookup"><span data-stu-id="03826-115">Finding the Server Program</span></span>](finding-the-server-program.md)
-   [<span data-ttu-id="03826-116">Отправка вызова в программу сервера</span><span class="sxs-lookup"><span data-stu-id="03826-116">Sending the Call to the Server Program</span></span>](sending-the-call-to-the-server-program.md)

 

 




