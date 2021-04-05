---
title: Подпрограммы запуска контекста сервера
description: Если связь нарушается, пока сервер обслуживает контекст от имени клиента, для очистки состояния, поддерживаемого сервером от имени данного клиента, может потребоваться подпрограмма очистки.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ad8afb7f698a258d7c4403143e74d566f813a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068419"
---
# <a name="server-context-run-down-routine"></a><span data-ttu-id="935ee-103">Подпрограммы запуска контекста сервера</span><span class="sxs-lookup"><span data-stu-id="935ee-103">Server Context Run-down Routine</span></span>

<span data-ttu-id="935ee-104">Если связь нарушается, пока сервер обслуживает контекст от имени клиента, для очистки состояния, поддерживаемого сервером от имени данного клиента, может потребоваться подпрограмма очистки.</span><span class="sxs-lookup"><span data-stu-id="935ee-104">If communication breaks down while the server is maintaining context on behalf of the client, a cleanup routine may be needed to clean up the state maintained by the server on behalf of a given client.</span></span> <span data-ttu-id="935ee-105">Эта подпрограмма очистки называется *контекстной подпрограммы запуска*.</span><span class="sxs-lookup"><span data-stu-id="935ee-105">This cleanup routine is called a *context run-down routine*.</span></span> <span data-ttu-id="935ee-106">При разрыве соединения Серверная заглушка и библиотека времени выполнения будут вызывать эту подпрограмму для каждого открытого в клиенте обработчика контекста.</span><span class="sxs-lookup"><span data-stu-id="935ee-106">When a connection breaks, the server stub and the run-time library will call this routine on every context handle opened by the client.</span></span>

<span data-ttu-id="935ee-107">Подпрограммы запуска контекста являются обязательными и неявно объявлены и именованы при применении \[ атрибута **\_ Handle** в \] определении типа.</span><span class="sxs-lookup"><span data-stu-id="935ee-107">The context run-down routine is required, and is implicitly declared and named, when you apply the \[**context\_handle**\] attribute to a type definition.</span></span> <span data-ttu-id="935ee-108">Сервер не будет вызывать подпрограммы контекстной выгрузки, если \[ **атрибут \_ Handle контекста** \] был применен непосредственно к параметру.</span><span class="sxs-lookup"><span data-stu-id="935ee-108">The server will not call the context run-down routine if the \[**context\_handle**\] attribute was applied directly to a parameter.</span></span>

<span data-ttu-id="935ee-109">Синтаксис выполнения контекстного действия:</span><span class="sxs-lookup"><span data-stu-id="935ee-109">The context run-down routine syntax is:</span></span>

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

<span data-ttu-id="935ee-110">Обратите внимание, что имя типа определяет имя подпрограммы запуска контекста.</span><span class="sxs-lookup"><span data-stu-id="935ee-110">Note that the type name determines the name of the context run-down routine.</span></span>

<span data-ttu-id="935ee-111">Фрагмент кода, приведенный ниже, представляет собой подпрограмму выполнения примера контекста.</span><span class="sxs-lookup"><span data-stu-id="935ee-111">The code fragment that follows presents a sample context run-down routine.</span></span> <span data-ttu-id="935ee-112">Это вызывает процедуру Ремотеклосе, используемую в примере в [разработке интерфейса с помощью дескрипторов контекста](interface-development-using-context-handles.md), [разработки сервера с помощью дескрипторов контекста](server-development-using-context-handles.md)и [разработки клиентов с помощью дескрипторов контекста](client-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="935ee-112">that calls the RemoteClose procedure used in the example in [Interface Development Using Context Handles](interface-development-using-context-handles.md), [Server Development Using Context Handles](server-development-using-context-handles.md), and [Client Development Using Context Handles](client-development-using-context-handles.md).</span></span> <span data-ttu-id="935ee-113">Эта процедура закрывает файловый обработчик, освобождает память, связанную с файлом, и присваивает **значение NULL** контексту.</span><span class="sxs-lookup"><span data-stu-id="935ee-113">This procedure closes the file handle, frees the memory associated with the file, and assigns **NULL** to the context handle.</span></span> <span data-ttu-id="935ee-114">Присвоение **значения NULL** является результатом вызова функции ремотеклосе и не является обязательным в сценарии запуска.</span><span class="sxs-lookup"><span data-stu-id="935ee-114">Assigning **NULL** is a result of calling the RemoteClose function, and is not necessary in a run-down scenario.</span></span> <span data-ttu-id="935ee-115">Время выполнения RPC очищает свое состояние независимо от того, задано ли для маркера контекста **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="935ee-115">The RPC run time cleans up its state regardless of whether the context handle is set to **NULL**.</span></span>

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




