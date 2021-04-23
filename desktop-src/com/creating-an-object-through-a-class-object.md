---
title: Создание объекта через объект класса
description: Создание объекта через объект класса
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986827"
---
# <a name="creating-an-object-through-a-class-object"></a><span data-ttu-id="dbe07-103">Создание объекта через объект класса</span><span class="sxs-lookup"><span data-stu-id="dbe07-103">Creating an Object Through a Class Object</span></span>

<span data-ttu-id="dbe07-104">Благодаря повышению важности компьютерных сетей она стала необходима для взаимодействия клиентов и серверов, независимо от того, находятся ли они на одном и том же компьютере или по сети.</span><span class="sxs-lookup"><span data-stu-id="dbe07-104">With the increasing importance of computer networks, it has become necessary for clients and servers to interact easily and efficiently, whether they reside on the same machine or across a network.</span></span> <span data-ttu-id="dbe07-105">Критически важным для этого является возможность клиента запустить сервер, создать экземпляр объекта сервера и получить доступ к методам интерфейсов в объекте.</span><span class="sxs-lookup"><span data-stu-id="dbe07-105">Crucial to this is a client's ability to launch a server, create an instance of the server's object, and have access to the methods of the interfaces on the object.</span></span>

<span data-ttu-id="dbe07-106">COM предоставляет расширения для этого базового COM-процесса, которые делают его практически беспрепятственно в сети.</span><span class="sxs-lookup"><span data-stu-id="dbe07-106">COM provides extensions to this basic COM process that make it virtually seamless across a network.</span></span> <span data-ttu-id="dbe07-107">Если клиент способен опознать сервер через его CLSID, вызов нескольких простых функций позволяет COM выполнять всю работу по поиску и запуску сервера и активации объекта.</span><span class="sxs-lookup"><span data-stu-id="dbe07-107">If a client is able to identify the server through its CLSID, calling a few simple functions permit COM to do all the work of locating and launching the server and activating the object.</span></span> <span data-ttu-id="dbe07-108">Подразделы в реестре позволяют удаленным серверам регистрировать свое расположение, поэтому клиент не требует этих сведений.</span><span class="sxs-lookup"><span data-stu-id="dbe07-108">Subkeys in the registry allow remote servers to register their location, so the client does not require that information.</span></span> <span data-ttu-id="dbe07-109">Для приложений, которые хотят воспользоваться преимуществами сетевых функций, функции создания объектов COM обеспечивают большую гибкость и эффективность.</span><span class="sxs-lookup"><span data-stu-id="dbe07-109">For applications that want to take advantage of networking features, the COM object creation functions allow more flexibility and efficiency.</span></span>

<span data-ttu-id="dbe07-110">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="dbe07-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="dbe07-111">Объекты COM-классов и CLSID</span><span class="sxs-lookup"><span data-stu-id="dbe07-111">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
-   [<span data-ttu-id="dbe07-112">Поиск удаленного объекта</span><span class="sxs-lookup"><span data-stu-id="dbe07-112">Locating a Remote Object</span></span>](locating-a-remote-object.md)
-   [<span data-ttu-id="dbe07-113">Вспомогательные функции для создания экземпляра</span><span class="sxs-lookup"><span data-stu-id="dbe07-113">Instance Creation Helper Functions</span></span>](instance-creation-helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="dbe07-114">См. также</span><span class="sxs-lookup"><span data-stu-id="dbe07-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbe07-115">COM-клиенты и серверы</span><span class="sxs-lookup"><span data-stu-id="dbe07-115">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




