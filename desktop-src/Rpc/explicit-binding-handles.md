---
title: Явные дескрипторы привязки
description: Для максимального контроля над процессом привязки клиентские и серверные приложения могут использовать явные дескрипторы привязки.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672087"
---
# <a name="explicit-binding-handles"></a><span data-ttu-id="53017-103">Явные дескрипторы привязки</span><span class="sxs-lookup"><span data-stu-id="53017-103">Explicit Binding Handles</span></span>

<span data-ttu-id="53017-104">Для максимального контроля над процессом привязки клиентские и серверные приложения могут использовать явные дескрипторы привязки.</span><span class="sxs-lookup"><span data-stu-id="53017-104">For maximum control over the binding process, client/server applications may use explicit binding handles.</span></span> <span data-ttu-id="53017-105">Как и неявные дескрипторы, явные дескрипторы привязки позволяют клиентскому приложению выбирать сервер для выполнения вызовов.</span><span class="sxs-lookup"><span data-stu-id="53017-105">Like implicit handles, explicit binding handles enable your client application to select a server to execute its calls.</span></span> <span data-ttu-id="53017-106">Кроме того, явные дескрипторы привязки позволяют клиентскому и серверному приложениям создавать сеанс связи RPC с проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="53017-106">In addition, explicit binding handles enable your client/server application to create an authenticated RPC communication session.</span></span> <span data-ttu-id="53017-107">С помощью явных дескрипторов клиент может подключаться к нескольким серверам и выполнять удаленные процедуры на нескольких серверах.</span><span class="sxs-lookup"><span data-stu-id="53017-107">With explicit handles, your client can connect to more than one server and execute remote procedures on multiple servers.</span></span> <span data-ttu-id="53017-108">Многопоточные и асинхронные клиентские приложения могут даже подключаться к нескольким серверам и одновременно выполнять несколько удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="53017-108">Multithreaded and asynchronous client applications can even connect to multiple servers and execute multiple remote procedures at the same time.</span></span>

<span data-ttu-id="53017-109">Клиентское приложение должно передать явный обработчик в качестве параметра каждому удаленному вызову процедуры.</span><span class="sxs-lookup"><span data-stu-id="53017-109">Your client application must pass the explicit handle as a parameter to each remote procedure call.</span></span> <span data-ttu-id="53017-110">Чтобы соответствовать стандарту использование, этот обработчик должен быть указан в качестве первого параметра в каждой удаленной процедуре.</span><span class="sxs-lookup"><span data-stu-id="53017-110">To conform to the OSF standard, the handle should be specified as the first parameter on each remote procedure.</span></span> <span data-ttu-id="53017-111">Однако расширения Майкрософт для RPC позволяют указать маркер привязки в других позициях.</span><span class="sxs-lookup"><span data-stu-id="53017-111">However, the Microsoft extensions to RPC enable you to specify the binding handle in other positions.</span></span> <span data-ttu-id="53017-112">Дополнительные сведения см. в разделе [расширения Microsoft RPC Binding-Handle](microsoft-rpc-binding-handle-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="53017-112">For more information, see [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).</span></span>

<span data-ttu-id="53017-113">Чтобы создать явный обработчик, объявите этот обработчик в качестве параметра для удаленных операций в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="53017-113">To create an explicit handle, declare the handle as a parameter to the remote operations in the IDL file.</span></span> <span data-ttu-id="53017-114">[Пример Hello, World](tutorial.md) можно переопределить, чтобы использовать явный маркер, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="53017-114">The [Hello, World example](tutorial.md) can be redefined to use an explicit handle as shown:</span></span>

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

<span data-ttu-id="53017-115">В одном интерфейсе можно сочетать явные и неявные дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="53017-115">You can combine explicit and implicit handles in a single interface.</span></span> <span data-ttu-id="53017-116">Если функция имеет явный маркер в списке параметров, будет использоваться этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="53017-116">If a function has an explicit handle in its parameter list, that handle will be used.</span></span> <span data-ttu-id="53017-117">Если функция в интерфейсе, использующая неявные дескрипторы, не указывает явный дескриптор, будет использоваться неявный дескриптор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53017-117">If a function in an interface using implicit handles does not specify an explicit handle, then the default implicit handle will be used.</span></span>

 

 




