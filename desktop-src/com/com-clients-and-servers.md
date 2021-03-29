---
title: COM-клиенты и серверы
description: Важным аспектом модели COM является взаимодействие клиентов и серверов.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776505"
---
# <a name="com-clients-and-servers"></a><span data-ttu-id="ee708-103">COM-клиенты и серверы</span><span class="sxs-lookup"><span data-stu-id="ee708-103">COM Clients and Servers</span></span>

<span data-ttu-id="ee708-104">Важным аспектом модели COM является взаимодействие клиентов и серверов.</span><span class="sxs-lookup"><span data-stu-id="ee708-104">A critical aspect of COM is how clients and servers interact.</span></span> <span data-ttu-id="ee708-105">*Клиент COM* — это любой код или объект, который получает указатель на COM-сервер и использует его службы путем вызова методов своих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="ee708-105">A *COM client* is whatever code or object gets a pointer to a COM server and uses its services by calling the methods of its interfaces.</span></span> <span data-ttu-id="ee708-106">*Сервер COM* — это любой объект, который предоставляет службы клиентам; Эти службы представлены в виде реализаций COM-интерфейса, которые могут вызываться любым клиентом, который может получить указатель на один из интерфейсов объекта Server.</span><span class="sxs-lookup"><span data-stu-id="ee708-106">A *COM server* is any object that provides services to clients; these services are in the form of COM interface implementations that can be called by any client that is able to get a pointer to one of the interfaces on the server object.</span></span>

<span data-ttu-id="ee708-107">Существует два основных типа серверов: *внутрипроцессный* и *внутрипроцессный*.</span><span class="sxs-lookup"><span data-stu-id="ee708-107">There are two main types of servers, *in-process* and *out-of-process*.</span></span> <span data-ttu-id="ee708-108">Внутрипроцессный сервер реализуется в динамической связанной библиотеке (DLL), а серверы вне обработки реализуются в исполняемом файле (EXE).</span><span class="sxs-lookup"><span data-stu-id="ee708-108">In-process servers are implemented in a dynamic linked library (DLL), and out-of-process servers are implemented in an executable file (EXE).</span></span> <span data-ttu-id="ee708-109">Необработанные серверы могут находиться либо на локальном компьютере, либо на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ee708-109">Out-of-process servers can reside either on the local computer or on a remote computer.</span></span> <span data-ttu-id="ee708-110">Кроме того, COM предоставляет механизм, позволяющий выполнить внутрипроцессный сервер (DLL) в процессе суррогатного EXE-файла, чтобы получить преимущество запуска процесса на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ee708-110">In addition, COM provides a mechanism that allows an in-process server (a DLL) to run in a surrogate EXE process to gain the advantage of being able to run the process on a remote computer.</span></span> <span data-ttu-id="ee708-111">Дополнительные сведения см. в разделе [DLL-суррогаты](dll-surrogates.md).</span><span class="sxs-lookup"><span data-stu-id="ee708-111">For more information, see [DLL Surrogates](dll-surrogates.md).</span></span>

<span data-ttu-id="ee708-112">Модель программирования COM и конструкции теперь расширены таким образом, чтобы клиенты и серверы COM могли работать в сети, а не только на данном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ee708-112">The COM programming model and constructs have now been extended so that COM clients and servers can work together across the network, not just within a given computer.</span></span> <span data-ttu-id="ee708-113">Это позволяет существующим приложениям взаимодействовать с новыми приложениями и между сетями с соответствующим администрированием, а новые приложения могут быть написаны для использования преимуществ сетевых возможностей.</span><span class="sxs-lookup"><span data-stu-id="ee708-113">This enables existing applications to interact with new applications and with each other across networks with proper administration, and new applications can be written to take advantage of networking features.</span></span>

<span data-ttu-id="ee708-114">Клиентским приложениям COM не нужно знать, как упаковываются объекты сервера, будь они упакованы как внутрипроцессный объекты (в библиотеках DLL) или как локальные или удаленные объекты (в exe-файлы).</span><span class="sxs-lookup"><span data-stu-id="ee708-114">COM client applications do not need to be aware of how server objects are packaged, whether they are packaged as in-process objects (in DLLs) or as local or remote objects (in EXEs).</span></span> <span data-ttu-id="ee708-115">Кроме того, распределенная модель COM позволяет упаковывать объекты в приложения служб, а также выполнять синхронизацию COM с широкими возможностями администрирования и интеграции системы Windows.</span><span class="sxs-lookup"><span data-stu-id="ee708-115">Distributed COM further allows objects to be packaged as service applications, synchronizing COM with the rich administrative and system-integration capabilities of Windows.</span></span>

> [!Note]  
> <span data-ttu-id="ee708-116">В этой документации аббревиатура COM используется в настройках DCOM.</span><span class="sxs-lookup"><span data-stu-id="ee708-116">Throughout this documentation the acronym COM is used in preference to DCOM.</span></span> <span data-ttu-id="ee708-117">Это связано с тем, что DCOM не разделяется; это просто модель COM с более длинным каналом передачи.</span><span class="sxs-lookup"><span data-stu-id="ee708-117">This is because DCOM is not separate;it is just COM with a longer wire.</span></span> <span data-ttu-id="ee708-118">В случаях, когда описание является удаленной операцией, используется термин *Распределенная модель COM* .</span><span class="sxs-lookup"><span data-stu-id="ee708-118">In cases where what is being described is specifically a remote operation, the term *distributed COM* is used.</span></span>

 

<span data-ttu-id="ee708-119">Модель COM позволяет добавить поддержку прозрачности расположения, которая распространяется по сети.</span><span class="sxs-lookup"><span data-stu-id="ee708-119">COM is designed to make it possible to add the support for location transparency that extends across a network.</span></span> <span data-ttu-id="ee708-120">Он позволяет приложениям, написанным для отдельных компьютеров, работать по сети и предоставляет функции, расширяющие эти возможности и добавляющие в сеть необходимые компоненты безопасности.</span><span class="sxs-lookup"><span data-stu-id="ee708-120">It allows applications written for single computers to run across a network and provides features that extend these capabilities and add to the security necessary in a network.</span></span> <span data-ttu-id="ee708-121">(Дополнительные сведения см. [в разделе Security in com](security-in-com.md).)</span><span class="sxs-lookup"><span data-stu-id="ee708-121">(For more information, see [Security in COM](security-in-com.md).)</span></span>

<span data-ttu-id="ee708-122">COM указывает механизм, с помощью которого код класса может использоваться многими различными приложениями.</span><span class="sxs-lookup"><span data-stu-id="ee708-122">COM specifies a mechanism by which the class code can be used by many different applications.</span></span>

<span data-ttu-id="ee708-123">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ee708-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ee708-124">Получение указателя на объект</span><span class="sxs-lookup"><span data-stu-id="ee708-124">Getting a Pointer to an Object</span></span>](getting-a-pointer-to-an-object.md)
-   [<span data-ttu-id="ee708-125">Создание объекта через объект класса</span><span class="sxs-lookup"><span data-stu-id="ee708-125">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
-   [<span data-ttu-id="ee708-126">Обязанности сервера COM</span><span class="sxs-lookup"><span data-stu-id="ee708-126">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
-   [<span data-ttu-id="ee708-127">Состояние постоянного объекта</span><span class="sxs-lookup"><span data-stu-id="ee708-127">Persistent Object State</span></span>](persistent-object-state.md)
-   [<span data-ttu-id="ee708-128">Предоставление сведений о классе</span><span class="sxs-lookup"><span data-stu-id="ee708-128">Providing Class Information</span></span>](providing-class-information.md)
-   [<span data-ttu-id="ee708-129">Обмен данными между объектами</span><span class="sxs-lookup"><span data-stu-id="ee708-129">Inter-Object Communication</span></span>](inter-object-communication.md)

## <a name="related-topics"></a><span data-ttu-id="ee708-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ee708-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee708-131">Синхронизация вызовов</span><span class="sxs-lookup"><span data-stu-id="ee708-131">Call Synchronization</span></span>](call-synchronization.md)
</dt> <dt>

[<span data-ttu-id="ee708-132">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="ee708-132">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




