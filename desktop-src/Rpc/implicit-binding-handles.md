---
title: Неявные дескрипторы привязки
description: Неявные дескрипторы привязок позволяют приложению выбрать конкретный сервер для выполнения удаленных вызовов процедур.
ms.assetid: cf4e179b-8d97-4597-89e6-c8967b9db6c7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fda8501224d66518ad2e86f13fb769c4b2fa0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070114"
---
# <a name="implicit-binding-handles"></a><span data-ttu-id="44a47-103">Неявные дескрипторы привязки</span><span class="sxs-lookup"><span data-stu-id="44a47-103">Implicit Binding Handles</span></span>

<span data-ttu-id="44a47-104">Неявные дескрипторы привязок позволяют приложению выбрать конкретный сервер для выполнения удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="44a47-104">Implicit binding handles allow your application to select a specific server to execute its remote procedure calls.</span></span> <span data-ttu-id="44a47-105">Дополнительные сведения см. в разделе [Привязка на стороне клиента](client-side-binding.md).</span><span class="sxs-lookup"><span data-stu-id="44a47-105">For details, see [Client-Side Binding](client-side-binding.md).</span></span> <span data-ttu-id="44a47-106">Они также позволяют клиентской и серверной программе использовать привязку с проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="44a47-106">They also enable your client/server program to use authenticated bindings.</span></span> <span data-ttu-id="44a47-107">То есть клиент может указать сведения о проверке подлинности в неявном обработчике привязки.</span><span class="sxs-lookup"><span data-stu-id="44a47-107">That is, the client can specify authentication information in an implicit binding handle.</span></span> <span data-ttu-id="44a47-108">Библиотека времени выполнения RPC использует данные проверки подлинности для установления сеанса RPC с проверкой подлинности между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="44a47-108">The RPC run-time library uses the authentication information to establish an authenticated RPC session between the client and the server.</span></span> <span data-ttu-id="44a47-109">Дополнительные сведения см. в статье [Безопасность](security.md).</span><span class="sxs-lookup"><span data-stu-id="44a47-109">For more information, see [Security](security.md).</span></span>

> [!Note]  
> <span data-ttu-id="44a47-110">Неявные дескрипторы привязки не являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="44a47-110">Implicit binding handles are not thread safe.</span></span> <span data-ttu-id="44a47-111">Поэтому многопоточные приложения не должны использовать неявные дескрипторы привязки.</span><span class="sxs-lookup"><span data-stu-id="44a47-111">Multi-threaded applications therefore should avoid using implicit binding handles.</span></span>

 

<span data-ttu-id="44a47-112">Если приложение использует неявные привязки, клиент должен задать сведения о привязке, чтобы они могли создать привязку.</span><span class="sxs-lookup"><span data-stu-id="44a47-112">When your application uses implicit bindings, the client must set the binding information so that it can create the binding.</span></span> <span data-ttu-id="44a47-113">После того как клиент создаст неявную привязку, ему не нужно передавать никакие дескрипторы привязки удаленным процедурам.</span><span class="sxs-lookup"><span data-stu-id="44a47-113">After the client creates an implicit binding, it does not need to pass any binding handles to remote procedures.</span></span> <span data-ttu-id="44a47-114">Библиотека RPC обрабатывает оставшуюся часть механики сеанса связи.</span><span class="sxs-lookup"><span data-stu-id="44a47-114">The RPC library handles the rest of the mechanics of the communication session.</span></span>

<span data-ttu-id="44a47-115">Клиент сохраняет сведения о привязке для неявного маркера в глобальной переменной.</span><span class="sxs-lookup"><span data-stu-id="44a47-115">The client stores the binding information for an implicit handle in a global variable.</span></span> <span data-ttu-id="44a47-116">Когда компилятор MIDL создает клиентскую заглушку и файл заголовка из спецификации интерфейса в файле MIDL, он также создает код для переменной универсального обработчика привязки.</span><span class="sxs-lookup"><span data-stu-id="44a47-116">When the MIDL compiler generates the client stub and header file from the interface specification in your MIDL file, it also generates code for a global binding handle variable.</span></span> <span data-ttu-id="44a47-117">Клиентская программа инициализирует этот обработчик, а затем не ссылается на него, пока не уничтожит привязку.</span><span class="sxs-lookup"><span data-stu-id="44a47-117">Your client program initializes the handle and then does not refer to it again until it destroys the binding.</span></span>

<span data-ttu-id="44a47-118">Неявный обработчик создается путем указания \[ [**неявного атрибута \_ Handle**](/windows/desktop/Midl/implicit-handle) \] в ACF для интерфейса следующим образом:</span><span class="sxs-lookup"><span data-stu-id="44a47-118">You create an implicit handle by specifying the \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] attribute in the ACF for an interface as follows:</span></span>

``` syntax
/* ACF file (complete) */
 
[
  implicit_handle(handle_t hHello)
]
interface hello
{
}
```

<span data-ttu-id="44a47-119">Тип **дескриптора \_ t** , используемый в предыдущем примере, является типом данных MIDL, используемым для определения дескрипторов привязки.</span><span class="sxs-lookup"><span data-stu-id="44a47-119">The **handle\_t** type, which is used in the preceding example, is a MIDL data type used for defining binding handles.</span></span>

<span data-ttu-id="44a47-120">После создания неявного маркера приложение должно использовать его в качестве параметра для функций библиотеки времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="44a47-120">After creating the implicit handle, the application needs to use it as a parameter to the RPC run-time library functions.</span></span> <span data-ttu-id="44a47-121">Не используйте неявный обработчик в качестве параметра для вызовов удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="44a47-121">Do not use the implicit handle as a parameter to remote procedure calls.</span></span> <span data-ttu-id="44a47-122">В следующем образце кода показано использование неявных дескрипторов привязки.</span><span class="sxs-lookup"><span data-stu-id="44a47-122">The following code sample demonstrates the use of implicit binding handles.</span></span>

``` syntax
RPC_STATUS status;
status = RpcBindingFromStringBinding(
            pszStringBinding,
            &hHello);
 
status = MyRemoteProcedure();
 
status = RpcBindingFree(hHello);
...
```

<span data-ttu-id="44a47-123">В предыдущем примере функции библиотеки времени выполнения RPC [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) и [**рпкбиндингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) требовали передачи неявного маркера привязки в списки параметров.</span><span class="sxs-lookup"><span data-stu-id="44a47-123">In the preceding example, the RPC run-time library functions [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) and [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) both required the implicit binding handle to be passed in their parameter lists.</span></span> <span data-ttu-id="44a47-124">Однако Удаленная процедура Миремотепроцедуре не была, так как она не является функцией библиотеки времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="44a47-124">However, the remote procedure MyRemoteProcedure did not, since it is not an RPC run-time library function.</span></span>

 

 