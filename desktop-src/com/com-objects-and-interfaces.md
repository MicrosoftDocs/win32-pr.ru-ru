---
title: COM-объекты и интерфейсы
description: COM-объекты и интерфейсы
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773322"
---
# <a name="com-objects-and-interfaces"></a><span data-ttu-id="56a0e-103">COM-объекты и интерфейсы</span><span class="sxs-lookup"><span data-stu-id="56a0e-103">COM Objects and Interfaces</span></span>

<span data-ttu-id="56a0e-104">COM — это технология, которая позволяет объектам взаимодействовать между процессами и компьютерами так же, как и в рамках одного процесса.</span><span class="sxs-lookup"><span data-stu-id="56a0e-104">COM is a technology that allows objects to interact across process and computer boundaries as easily as within a single process.</span></span> <span data-ttu-id="56a0e-105">COM делает это, указывая, что единственный способ манипулировать данными, связанными с объектом, — через *интерфейс* объекта.</span><span class="sxs-lookup"><span data-stu-id="56a0e-105">COM enables this by specifying that the only way to manipulate the data associated with an object is through an *interface* on the object.</span></span> <span data-ttu-id="56a0e-106">Когда этот термин используется в этой документации, он ссылается на реализацию в коде COM-совместимого интерфейса, связанного с объектом.</span><span class="sxs-lookup"><span data-stu-id="56a0e-106">When this term is used in this documentation, it refers to an implementation in code of a COM binary-compliant interface that is associated with an object.</span></span>

<span data-ttu-id="56a0e-107">COM использует слово *Interface* в понятном смысле, отличном от того, который обычно используется в Visual C++ программировании.</span><span class="sxs-lookup"><span data-stu-id="56a0e-107">COM uses the word *interface* in a sense different from that typically used in Visual C++ programming.</span></span> <span data-ttu-id="56a0e-108">Интерфейс C++ ссылается на все функции, поддерживаемые классом, и что клиенты объекта могут вызывать для взаимодействия с ним.</span><span class="sxs-lookup"><span data-stu-id="56a0e-108">A C++ interface refers to all of the functions that a class supports and that clients of an object can call to interact with it.</span></span> <span data-ttu-id="56a0e-109">COM-интерфейс относится к предопределенной группе связанных функций, реализуемых классом COM, но конкретный интерфейс не обязательно представляет все функции, поддерживаемые классом.</span><span class="sxs-lookup"><span data-stu-id="56a0e-109">A COM interface refers to a predefined group of related functions that a COM class implements, but a specific interface does not necessarily represent all the functions that the class supports.</span></span>

<span data-ttu-id="56a0e-110">Ссылка на объект, *реализующий* интерфейс, означает, что объект использует код, реализующий каждый метод интерфейса, и предоставляет совместимые с двоичным кодом com указатели на эти функции в библиотеке COM.</span><span class="sxs-lookup"><span data-stu-id="56a0e-110">Referring to an object *implementing* an interface means that the object uses code that implements each method of the interface and provides COM binary-compliant pointers to those functions to the COM library.</span></span> <span data-ttu-id="56a0e-111">Затем COM предоставляет доступ к этим функциям любому клиенту, запрашивающему указатель на интерфейс, независимо от того, находится ли клиент внутри или вне процесса, реализующего эти функции.</span><span class="sxs-lookup"><span data-stu-id="56a0e-111">COM then makes those functions available to any client who asks for a pointer to the interface, whether the client is inside or outside of the process that implements those functions.</span></span>

<span data-ttu-id="56a0e-112">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="56a0e-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="56a0e-113">Реализации интерфейсов и интерфейсов</span><span class="sxs-lookup"><span data-stu-id="56a0e-113">Interfaces and Interface Implementations</span></span>](interfaces-and-interface-implementations.md)
-   [<span data-ttu-id="56a0e-114">Указатели интерфейса и интерфейсы</span><span class="sxs-lookup"><span data-stu-id="56a0e-114">Interface Pointers and Interfaces</span></span>](interface-pointers-and-interfaces.md)
-   [<span data-ttu-id="56a0e-115">IUnknown и наследование интерфейсов</span><span class="sxs-lookup"><span data-stu-id="56a0e-115">IUnknown and Interface Inheritance</span></span>](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a><span data-ttu-id="56a0e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="56a0e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56a0e-117">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="56a0e-117">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 




