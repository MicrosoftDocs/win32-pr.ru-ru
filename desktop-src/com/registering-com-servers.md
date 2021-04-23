---
title: Регистрация серверов COM
description: Регистрация серверов COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134611"
---
# <a name="registering-com-servers"></a><span data-ttu-id="76fd4-103">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="76fd4-103">Registering COM Servers</span></span>

<span data-ttu-id="76fd4-104">Определив класс в коде (убедившись, что он реализует [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) или [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) и назначил ему идентификатор CLSID, необходимо разместить в реестре сведения, позволяющие com, по запросу клиента с идентификатором CLSID, создать экземпляры своих объектов.</span><span class="sxs-lookup"><span data-stu-id="76fd4-104">After you have defined a class in code (ensuring that it implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) and assigned it a CLSID, you need to put information in the registry that will allow COM, on request of a client with the CLSID, to create instances of its objects.</span></span> <span data-ttu-id="76fd4-105">Эти сведения сообщают системе, для определенного идентификатора CLSID, где находится код DLL или EXE для этого класса и как он запускается.</span><span class="sxs-lookup"><span data-stu-id="76fd4-105">This information tells the system, for a given CLSID, where the DLL or EXE code for that class is located and how it is to be launched.</span></span>

<span data-ttu-id="76fd4-106">Существует более одного способа регистрации класса в реестре.</span><span class="sxs-lookup"><span data-stu-id="76fd4-106">There is more than one way of registering a class in the registry.</span></span> <span data-ttu-id="76fd4-107">Кроме того, существует и другие способы «регистрации» класса с системой при его выполнении, чтобы система знала, что выполняющийся объект в данный момент находится в системе.</span><span class="sxs-lookup"><span data-stu-id="76fd4-107">In addition, there are other ways of "registering" a class with the system when it is running, so that the system is aware that a running object is currently in the system.</span></span>

<span data-ttu-id="76fd4-108">Дополнительные сведения о регистрации см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="76fd4-108">See the following topics for more information about registering:</span></span>

-   [<span data-ttu-id="76fd4-109">Регистрация класса при установке</span><span class="sxs-lookup"><span data-stu-id="76fd4-109">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
-   [<span data-ttu-id="76fd4-110">Регистрация работающего сервера EXE</span><span class="sxs-lookup"><span data-stu-id="76fd4-110">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
-   [<span data-ttu-id="76fd4-111">Регистрация объектов в таблице ROT</span><span class="sxs-lookup"><span data-stu-id="76fd4-111">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
-   [<span data-ttu-id="76fd4-112">Самостоятельная регистрация</span><span class="sxs-lookup"><span data-stu-id="76fd4-112">Self-Registration</span></span>](self-registration.md)
-   [<span data-ttu-id="76fd4-113">Установка в качестве приложения службы</span><span class="sxs-lookup"><span data-stu-id="76fd4-113">Installing as a Service Application</span></span>](installing-as-a-service-application.md)

## <a name="related-topics"></a><span data-ttu-id="76fd4-114">См. также</span><span class="sxs-lookup"><span data-stu-id="76fd4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76fd4-115">Обязанности сервера COM</span><span class="sxs-lookup"><span data-stu-id="76fd4-115">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 