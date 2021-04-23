---
title: RPC_BINDING_HANDLE (Рпкдце. h)
description: '\_Тип данных Handle привязки RPC объявляет маркер привязки, содержащий сведения, используемые библиотекой времени выполнения RPC для доступа к сведениям о привязке.'
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803994"
---
# <a name="rpc_binding_handle"></a><span data-ttu-id="74211-104">\_маркер привязки \_ RPC</span><span class="sxs-lookup"><span data-stu-id="74211-104">RPC\_BINDING\_HANDLE</span></span>

<span data-ttu-id="74211-105">Тип **данных \_ Handle привязки RPC** объявляет маркер привязки, содержащий сведения, используемые библиотекой времени выполнения RPC для доступа к сведениям о привязке.</span><span class="sxs-lookup"><span data-stu-id="74211-105">The **RPC\_BINDING HANDLE** data type declares a binding handle containing information that the RPC run-time library uses to access binding information.</span></span>


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="74211-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74211-106">Remarks</span></span>

<span data-ttu-id="74211-107">Библиотека времени выполнения использует сведения о привязке для установления связи «клиент-сервер», которая разрешает выполнение удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="74211-107">The run-time library uses binding information to establish a client-server relationship that allows the execution of remote procedure calls.</span></span> <span data-ttu-id="74211-108">В зависимости от контекста, в котором создается маркер привязки, он считается маркером привязки сервера или маркером привязки клиента.</span><span class="sxs-lookup"><span data-stu-id="74211-108">Based on the context in which a binding handle is created, it is considered a server-binding handle or a client-binding handle.</span></span>

<span data-ttu-id="74211-109">Обработчик привязки сервера содержит сведения, необходимые клиенту для установления связи с конкретным сервером.</span><span class="sxs-lookup"><span data-stu-id="74211-109">A server-binding handle contains the information necessary for a client to establish a relationship with a specific server.</span></span> <span data-ttu-id="74211-110">Любое количество подпрограмм времени выполнения RPC API возвращает маркер привязки сервера, который можно использовать для выполнения удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="74211-110">Any number of RPC API run-time routines return a server-binding handle that can be used for making a remote procedure call.</span></span>

<span data-ttu-id="74211-111">Для удаленного вызова процедур нельзя использовать маркер клиентской привязки.</span><span class="sxs-lookup"><span data-stu-id="74211-111">A client-binding handle cannot be used to make a remote procedure call.</span></span> <span data-ttu-id="74211-112">Библиотека времени выполнения RPC создает и предоставляет маркер привязки клиента для процедуры вызываемого сервера (также называемой подпроцедурой диспетчера сервера) в качестве \_ \_ параметра обработчика привязки RPC.</span><span class="sxs-lookup"><span data-stu-id="74211-112">The RPC run-time library creates and provides a client-binding handle to a called-server procedure (also called a server-manager routine) as the RPC\_BINDING\_HANDLE parameter.</span></span> <span data-ttu-id="74211-113">Маркер привязки клиента содержит сведения о вызывающем клиенте.</span><span class="sxs-lookup"><span data-stu-id="74211-113">The client-binding handle contains information about the calling client.</span></span>

<span data-ttu-id="74211-114">Функции **рпкбиндинг \** _ и _*рпкнсбиндинг \*\*_ возвращают код состояния RPC с неверным типом \_ привязки, \_ \_ \_ \_ когда приложение предоставляет неправильный тип обработчика привязки.</span><span class="sxs-lookup"><span data-stu-id="74211-114">The **RpcBinding\** _ and _*RpcNsBinding\*\*_ functions return the status code RPC\_S\_WRONG\_KIND\_OF\_BINDING when an application provides the incorrect binding-handle type.</span></span>

<span data-ttu-id="74211-115">Приложение может совместно использовать один и тот же маркер привязки для нескольких потоков выполнения.</span><span class="sxs-lookup"><span data-stu-id="74211-115">An application can share a single binding handle across multiple threads of execution.</span></span> <span data-ttu-id="74211-116">Библиотека времени выполнения RPC управляет параллельными удаленными вызовами процедур, которые используют один маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="74211-116">The RPC run-time library manages concurrent remote procedure calls that use a single binding handle.</span></span> <span data-ttu-id="74211-117">Однако приложение отвечает за управление параллелизмом для операций, изменяющих маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="74211-117">However, the application is responsible for binding handle concurrency control for operations that modify a binding handle.</span></span> <span data-ttu-id="74211-118">Эти операции включают в себя следующие подпрограммы:</span><span class="sxs-lookup"><span data-stu-id="74211-118">These operations include the following routines:</span></span>

-   [<span data-ttu-id="74211-119">_ *Рпкбиндингфри*\*</span><span class="sxs-lookup"><span data-stu-id="74211-119">_ *RpcBindingFree*\*</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [<span data-ttu-id="74211-120">**рпкбиндингресет**</span><span class="sxs-lookup"><span data-stu-id="74211-120">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [<span data-ttu-id="74211-121">**рпкбиндингсетаусинфо**</span><span class="sxs-lookup"><span data-stu-id="74211-121">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [<span data-ttu-id="74211-122">**рпкбиндингсетобжект**</span><span class="sxs-lookup"><span data-stu-id="74211-122">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

<span data-ttu-id="74211-123">Например, если приложение совместно использует один и тот же обработчик привязки для двух потоков выполнения и сбрасывает конечную точку обработчика привязки в одном из потоков путем вызова [**рпкбиндингресет**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), результаты не будут определены.</span><span class="sxs-lookup"><span data-stu-id="74211-123">For example, if an application shares a binding handle across two threads of execution and resets the binding-handle endpoint in one of the threads by calling [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), the results are undefined.</span></span> <span data-ttu-id="74211-124">Маркер привязки в другом потоке также может быть сброшен, либо может произойти сбой операции, либо процесс может завершиться сбоем.</span><span class="sxs-lookup"><span data-stu-id="74211-124">The binding handle on the other thread may also be reset, or the operation may fail, or the process may crash.</span></span> <span data-ttu-id="74211-125">Распространенная ошибка освобождает обработчик привязки, пока выполняется вызов. Обычно это вызывает сбой вызывающего процесса.</span><span class="sxs-lookup"><span data-stu-id="74211-125">A common error is freeing a binding handle while a call on it is in progress; this usually crashes the calling process.</span></span>

<span data-ttu-id="74211-126">Если вы не хотите использовать параллелизм, можно разработать приложение, чтобы создать копию маркера привязки путем вызова [**рпкбиндингкопи**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span><span class="sxs-lookup"><span data-stu-id="74211-126">If you do not want concurrency, you can design an application to create a copy of a binding handle by calling [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span></span> <span data-ttu-id="74211-127">В этом случае операция с первым маркером привязки не влияет на второй маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="74211-127">In this case, an operation to the first binding handle has no effect on the second binding handle.</span></span>

<span data-ttu-id="74211-128">Процедуры, которым необходим маркер привязки в качестве параметра, показывают тип данных **\_ \_ маркера привязки RPC**.</span><span class="sxs-lookup"><span data-stu-id="74211-128">Routines requiring a binding handle as a parameter show a data type of **RPC\_BINDING\_HANDLE**.</span></span> <span data-ttu-id="74211-129">Параметры обработчика привязки передаются по значению.</span><span class="sxs-lookup"><span data-stu-id="74211-129">Binding-handle parameters are passed by value.</span></span>

## <a name="requirements"></a><span data-ttu-id="74211-130">Требования</span><span class="sxs-lookup"><span data-stu-id="74211-130">Requirements</span></span>



| <span data-ttu-id="74211-131">Требование</span><span class="sxs-lookup"><span data-stu-id="74211-131">Requirement</span></span> | <span data-ttu-id="74211-132">Значение</span><span class="sxs-lookup"><span data-stu-id="74211-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74211-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74211-133">Minimum supported client</span></span><br/> | <span data-ttu-id="74211-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74211-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="74211-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74211-135">Minimum supported server</span></span><br/> | <span data-ttu-id="74211-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74211-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="74211-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="74211-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="74211-138"><dt>Рпкдце. h (включение RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74211-138"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





