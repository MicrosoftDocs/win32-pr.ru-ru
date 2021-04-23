---
title: Поиск удаленного объекта
description: Поиск удаленного объекта
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891157"
---
# <a name="locating-a-remote-object"></a><span data-ttu-id="f82a7-103">Поиск удаленного объекта</span><span class="sxs-lookup"><span data-stu-id="f82a7-103">Locating a Remote Object</span></span>

<span data-ttu-id="f82a7-104">С появлением COM для распределенных систем COM использует базовую модель для создания объектов, описанную в разделе [объекты классов COM и CLSID](com-class-objects-and-clsids.md) , и добавляет более одного способа для нахождение объекта, который может находиться в другой системе в сети, без перегрузки клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="f82a7-104">With the advent of COM for distributed systems, COM uses the basic model for object creation described in [COM Class Objects and CLSIDs](com-class-objects-and-clsids.md) and adds more than one way to locate an object that might reside on another system in a network, without overburdening the client application.</span></span>

<span data-ttu-id="f82a7-105">В COM добавлены разделы реестра, позволяющие серверу регистрировать имя компьютера, на котором он находится, или компьютер, на котором находится существующее хранилище.</span><span class="sxs-lookup"><span data-stu-id="f82a7-105">COM has added registry keys that permit a server to register the name of the machine on which it resides or the machine where an existing storage is located.</span></span> <span data-ttu-id="f82a7-106">Поэтому клиентским приложениям необходимо знать только идентификатор CLSID сервера.</span><span class="sxs-lookup"><span data-stu-id="f82a7-106">Therefore, client applications need know only the CLSID of the server.</span></span>

<span data-ttu-id="f82a7-107">Однако в тех случаях, когда это необходимо, COM заменяет ранее зарезервированный параметр [**кожетклассобжект**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) на структуру [**косерверинфо**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , которая позволяет клиенту указать расположение сервера.</span><span class="sxs-lookup"><span data-stu-id="f82a7-107">However, for cases where it is desired, COM has replaced a previously reserved parameter of [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, which allows a client to specify the location of a server.</span></span> <span data-ttu-id="f82a7-108">Еще одним важным значением функции **кожетклассобжект** является перечисление [**клскткс**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , которое указывает, должен ли ожидаемый объект выполняться внутри процесса, вне процесса локального или вне процесса удаленного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f82a7-108">Another important value in the **CoGetClassObject** function is the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration, which specifies whether the expected object is to be run in-process, out-of-process local, or out-of-process remote.</span></span> <span data-ttu-id="f82a7-109">Вместе эти два значения и значения в реестре определяют, как и где будет выполняться объект.</span><span class="sxs-lookup"><span data-stu-id="f82a7-109">Taken together, these two values and the values in the registry determine how and where the object is to be run.</span></span>

> [!Note]  
> <span data-ttu-id="f82a7-110">Вызовы при создании экземпляра при указании расположения сервера могут переопределять параметр реестра.</span><span class="sxs-lookup"><span data-stu-id="f82a7-110">Instance creation calls, when they specify a server location, can override a registry setting.</span></span> <span data-ttu-id="f82a7-111">Алгоритм, используемый COM для этого, описан в справочнике по перечислению [**клскткс**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) .</span><span class="sxs-lookup"><span data-stu-id="f82a7-111">The algorithm COM uses for doing this is described in the reference for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration.</span></span>

 

<span data-ttu-id="f82a7-112">Удаленная активация зависит от отношения безопасности между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="f82a7-112">Remote activation depends on the security relationship between client and server.</span></span> <span data-ttu-id="f82a7-113">Дополнительные сведения см. [в разделе Безопасность в com](security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f82a7-113">For more information, see [Security in COM](security-in-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f82a7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f82a7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f82a7-115">Объекты COM-классов и CLSID</span><span class="sxs-lookup"><span data-stu-id="f82a7-115">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
</dt> <dt>

[<span data-ttu-id="f82a7-116">Создание объекта через объект класса</span><span class="sxs-lookup"><span data-stu-id="f82a7-116">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 