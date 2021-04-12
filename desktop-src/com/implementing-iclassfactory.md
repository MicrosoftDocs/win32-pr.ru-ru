---
title: Реализация IClassFactory
description: Реализация IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413789"
---
# <a name="implementing-iclassfactory"></a><span data-ttu-id="e3f6b-103">Реализация IClassFactory</span><span class="sxs-lookup"><span data-stu-id="e3f6b-103">Implementing IClassFactory</span></span>

<span data-ttu-id="e3f6b-104">Когда клиент использует идентификатор CLSID для запроса создания экземпляра объекта, первым шагом является создание объекта класса, промежуточного объекта, который содержит реализацию методов интерфейса [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) .</span><span class="sxs-lookup"><span data-stu-id="e3f6b-104">When a client uses a CLSID to request the creation of an object instance, the first step is creation of a class object, an intermediate object that contains an implementation of the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface.</span></span> <span data-ttu-id="e3f6b-105">Хотя модель COM предоставляет несколько функций создания экземпляров, первый шаг в реализации этих функций — это создание объекта класса.</span><span class="sxs-lookup"><span data-stu-id="e3f6b-105">While COM provides several instance creation functions, the first step in the implementation of these functions is the creation of a class object.</span></span>

<span data-ttu-id="e3f6b-106">В результате все серверы должны реализовывать методы интерфейса [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , который содержит два метода:</span><span class="sxs-lookup"><span data-stu-id="e3f6b-106">As a result, all servers must implement the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface, which contains two methods:</span></span>

-   <span data-ttu-id="e3f6b-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="e3f6b-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span></span> <span data-ttu-id="e3f6b-108">Этот метод должен создать неинициализированный экземпляр объекта и вернуть указатель на запрошенный интерфейс для объекта.</span><span class="sxs-lookup"><span data-stu-id="e3f6b-108">This method must create an uninitialized instance of the object and return a pointer to a requested interface on the object.</span></span>
-   <span data-ttu-id="e3f6b-109">[**Локксервер**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span><span class="sxs-lookup"><span data-stu-id="e3f6b-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span></span> <span data-ttu-id="e3f6b-110">Этот метод просто увеличивает счетчик ссылок на объект класса, чтобы убедиться, что сервер остается в памяти и не завершает работу до того, как клиент будет готов.</span><span class="sxs-lookup"><span data-stu-id="e3f6b-110">This method just increments the reference count on the class object to ensure that the server stays in memory and does not shut down before the client is ready for it to do so.</span></span>

<span data-ttu-id="e3f6b-111">Чтобы сервер был ответственным за собственное лицензирование, COM определяет [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), который наследует определение от [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="e3f6b-111">To enable a server to be responsible for its own licensing, COM defines [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), which inherits its definition from [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="e3f6b-112">Таким же, сервер, реализующий **IClassFactory2** , должен по определению реализовывать методы **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="e3f6b-112">Thus, a server implementing **IClassFactory2** must, by definition, implement the methods of **IClassFactory**.</span></span>

<span data-ttu-id="e3f6b-113">COM также предоставляет вспомогательные функции для реализации серверов вне процесса.</span><span class="sxs-lookup"><span data-stu-id="e3f6b-113">COM also provides helper functions for implementing out-of-process servers.</span></span> <span data-ttu-id="e3f6b-114">Дополнительные сведения см. в разделе [вспомогательные методы реализации сервера](out-of-process-server-implementation-helpers.md).</span><span class="sxs-lookup"><span data-stu-id="e3f6b-114">For more information, see [Out-of-Process Server Implementation Helpers](out-of-process-server-implementation-helpers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3f6b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e3f6b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3f6b-116">Обязанности сервера COM</span><span class="sxs-lookup"><span data-stu-id="e3f6b-116">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> <dt>

[<span data-ttu-id="e3f6b-117">Лицензирование и IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="e3f6b-117">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 