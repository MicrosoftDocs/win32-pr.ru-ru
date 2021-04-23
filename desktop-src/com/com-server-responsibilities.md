---
title: Обязанности сервера COM
description: Обязанности сервера COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413829"
---
# <a name="com-server-responsibilities"></a><span data-ttu-id="03907-103">Обязанности сервера COM</span><span class="sxs-lookup"><span data-stu-id="03907-103">COM Server Responsibilities</span></span>

<span data-ttu-id="03907-104">Одним из наиболее важных способов получения указателя на объект является получение клиентом запроса о запуске сервера и его создании и активации экземпляра объекта, предоставленного сервером.</span><span class="sxs-lookup"><span data-stu-id="03907-104">One of the most important ways for a client to get a pointer to an object is for the client to ask that a server be launched and that an instance of the object provided by the server be created and activated.</span></span> <span data-ttu-id="03907-105">Чтобы убедиться, что это происходит правильно, отвечает сервер.</span><span class="sxs-lookup"><span data-stu-id="03907-105">It is the responsibility of the server to ensure that this happens properly.</span></span> <span data-ttu-id="03907-106">Существует несколько важных частей.</span><span class="sxs-lookup"><span data-stu-id="03907-106">There are several important parts to this.</span></span>

<span data-ttu-id="03907-107">Сервер должен реализовать код для объекта класса с помощью реализации интерфейса [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) или [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .</span><span class="sxs-lookup"><span data-stu-id="03907-107">The server must implement code for a class object through an implementation of either the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface.</span></span>

<span data-ttu-id="03907-108">Сервер должен зарегистрировать свой идентификатор CLSID в системном реестре на компьютере, на котором он находится, и, в свою сторону, иметь возможность публикации расположения компьютера в других системах в сети, чтобы позволить клиентам вызывать его, не требуя от клиента получения сведений о расположении сервера.</span><span class="sxs-lookup"><span data-stu-id="03907-108">The server must register its CLSID in the system registry on the machine on which it resides and further, has the option of publishing its machine location to other systems on a network to allow clients to call it without requiring the client to know the server's location.</span></span>

<span data-ttu-id="03907-109">Сервер в основном отвечает за безопасность; то есть, в большинстве случаев сервер определяет, будет ли он предоставлять указатель на один из его объектов клиенту.</span><span class="sxs-lookup"><span data-stu-id="03907-109">The server is primarily responsible for security; that is, for the most part, the server determines whether it will provide a pointer to one of its objects to a client.</span></span>

<span data-ttu-id="03907-110">Серверы внутри процесса должны реализовывать и экспортировать определенные функции, позволяющие клиентскому процессу создавать их экземпляры.</span><span class="sxs-lookup"><span data-stu-id="03907-110">In-process servers should implement and export certain functions that allow the client process to instantiate them.</span></span>

<span data-ttu-id="03907-111">В следующих разделах описаны обязанности сервера COM.</span><span class="sxs-lookup"><span data-stu-id="03907-111">The following topics detail the responsibilities of the COM server:</span></span>

-   [<span data-ttu-id="03907-112">Реализация IClassFactory</span><span class="sxs-lookup"><span data-stu-id="03907-112">Implementing IClassFactory</span></span>](implementing-iclassfactory.md)
-   [<span data-ttu-id="03907-113">Лицензирование и IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="03907-113">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
-   [<span data-ttu-id="03907-114">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="03907-114">Registering COM Servers</span></span>](registering-com-servers.md)
-   [<span data-ttu-id="03907-115">Вспомогательные методы реализации сервера</span><span class="sxs-lookup"><span data-stu-id="03907-115">Out-of-Process Server Implementation Helpers</span></span>](out-of-process-server-implementation-helpers.md)
-   [<span data-ttu-id="03907-116">Создание и оптимизация GUID</span><span class="sxs-lookup"><span data-stu-id="03907-116">GUID Creation and Optimizations</span></span>](guid-creation-and-optimizations.md)

## <a name="related-topics"></a><span data-ttu-id="03907-117">См. также</span><span class="sxs-lookup"><span data-stu-id="03907-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03907-118">COM-клиенты и серверы</span><span class="sxs-lookup"><span data-stu-id="03907-118">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 