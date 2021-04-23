---
title: Разработка интерфейса с использованием дескрипторов контекста
description: Как правило, обработчик контекста создается путем указания атрибута \ context \_ Handle \ в определении типа в IDL-файле.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793134"
---
# <a name="interface-development-using-context-handles"></a><span data-ttu-id="b3b5d-103">Разработка интерфейса с использованием дескрипторов контекста</span><span class="sxs-lookup"><span data-stu-id="b3b5d-103">Interface Development Using Context Handles</span></span>

<span data-ttu-id="b3b5d-104">Как правило, обработчик контекста создается путем указания \[ атрибута [**\_ Handle контекста**](/windows/desktop/Midl/context-handle) \] для определения типа в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-104">Typically, you create a context handle by specifying the \[[**context\_handle**](/windows/desktop/Midl/context-handle)\] attribute on a type definition in the IDL file.</span></span> <span data-ttu-id="b3b5d-105">Определение типа также неявно указывает подпрограммы запуска контекста, которую необходимо предоставить.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-105">The type definition also implicitly specifies a context run-down routine, which you must provide.</span></span> <span data-ttu-id="b3b5d-106">Если связь между клиентом и сервером нарушается, время выполнения сервера вызывает эту подпрограммы для выполнения необходимой очистки.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-106">If communication between the client and server breaks down, the server run time invokes this routine to perform any needed cleanup.</span></span> <span data-ttu-id="b3b5d-107">Дополнительные сведения о подразделах выполнения контекста см. в разделе [подпрограммы запуска контекста сервера](server-context-run-down-routine.md).</span><span class="sxs-lookup"><span data-stu-id="b3b5d-107">For more information on context run-down routines, see [Server Context Run-down Routine](server-context-run-down-routine.md).</span></span>

<span data-ttu-id="b3b5d-108">Интерфейс, использующий обработчик контекста, должен иметь маркер привязки для начальной привязки, который должен быть выполнен до того, как сервер сможет вернуть контекстный маркер.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-108">An interface that uses a context handle must have a binding handle for the initial binding, which has to take place before the server can return a context handle.</span></span> <span data-ttu-id="b3b5d-109">Для создания привязки и установки контекста можно использовать автоматический, неявный или явный маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-109">You can use an automatic, implicit, or explicit binding handle to create the binding and establish the context.</span></span>

<span data-ttu-id="b3b5d-110">Маркер контекста должен иметь тип [**void \***](/windows/desktop/Midl/void) или тип, который разрешается в [**void \***](/windows/desktop/Midl/void).</span><span class="sxs-lookup"><span data-stu-id="b3b5d-110">A context handle must be of the [**void \***](/windows/desktop/Midl/void) type, or a type that resolves to [**void \***](/windows/desktop/Midl/void).</span></span> <span data-ttu-id="b3b5d-111">Серверная программа приводит ее к требуемому типу.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-111">The server program casts it to the required type.</span></span>

> [!Note]  
> <span data-ttu-id="b3b5d-112">Использование \[ [**в**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] для параметров дескриптора контекста не рекомендуется, за исключением подпрограмм, которые закрывают дескрипторы контекста.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-112">The use of \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] for context handle parameters is discouraged except for routines that close context handles.</span></span> <span data-ttu-id="b3b5d-113">Если контекст обрабатывает параметры, помеченные как \[ [](/windows/desktop/Midl/in), используется параметр [**out**](/windows/desktop/Midl/out-idl) \] , не передающий на сервер дескриптор контекста, **равный null** или неинициализированному клиенту.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-113">If context handles parameters marked \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)\] are used, do not pass a **NULL** or uninitialized context handle from the client to the server.</span></span> <span data-ttu-id="b3b5d-114">Вместо этого следует передать указатель на маркер **null** для обработчика контекста.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-114">A **NULL** pointer to a context handle should be passed instead.</span></span> <span data-ttu-id="b3b5d-115">Обратите внимание, что параметры обработчика контекста, помеченные \[ [**в**](/windows/desktop/Midl/in) \] , не принимают **пустые** указатели.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-115">Please note, context handle parameters marked \[[**in**](/windows/desktop/Midl/in)\] do not accept **NULL** pointers.</span></span>

 

<span data-ttu-id="b3b5d-116">В следующем фрагменте определения интерфейса показано, как распределенное приложение может использовать контекстный обработчик для открытия сервером и обновления файла данных для каждого клиента.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-116">The following fragment of a sample interface definition shows how a distributed application can use a context handle to have a server open and update a data file for each client.</span></span>

<span data-ttu-id="b3b5d-117">Интерфейс должен содержать удаленный вызов процедуры для инициализации обработчика и присвоения ему значения, отличного от **null** .</span><span class="sxs-lookup"><span data-stu-id="b3b5d-117">The interface must contain a remote procedure call to initialize the handle and set it to a non-**null** value.</span></span> <span data-ttu-id="b3b5d-118">В этом примере функция Ремотеопен выполняет эту операцию.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-118">In this example, the RemoteOpen function performs this operation.</span></span> <span data-ttu-id="b3b5d-119">Он задает маркер контекста с \[ атрибутом [**Outing**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="b3b5d-119">It specifies the context handle with an \[[**out**](/windows/desktop/Midl/out-idl)\] directional attribute.</span></span> <span data-ttu-id="b3b5d-120">Кроме того, можно вернуть контекстный маркер в качестве возвращаемого значения процедуры.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-120">Alternatively, you could return the context handle as the procedure's return value.</span></span> <span data-ttu-id="b3b5d-121">Однако в этом примере мы передаем контекстный обработчик в список параметров.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-121">However in this example, we'll pass the context handle out through the parameter list.</span></span>

<span data-ttu-id="b3b5d-122">В этом примере сведения о контексте являются маркером файла.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-122">In this example, the context information is a file handle.</span></span> <span data-ttu-id="b3b5d-123">Он отслеживает текущее расположение в файле.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-123">It keeps track of the current location in the file.</span></span> <span data-ttu-id="b3b5d-124">Интерфейс упаковывает файл как обработчик контекста и передает его в качестве параметра в вызовы удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-124">The interface packages the file handle as a context handle and passes it as a parameter to remote procedure calls.</span></span> <span data-ttu-id="b3b5d-125">Структура содержит имя файла и файловый обработчик.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-125">A structure contains the file name and the file handle.</span></span>

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

<span data-ttu-id="b3b5d-126">Функция Ремотеопен создает допустимый **ненулевой** маркер контекста, отличный от NULL.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-126">The RemoteOpen function creates a valid, non-**null** context handle.</span></span> <span data-ttu-id="b3b5d-127">Он передает контекстный указатель клиенту.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-127">It passes the context handle to the client.</span></span> <span data-ttu-id="b3b5d-128">Последующие удаленные вызовы процедур, такие как Ремотереад, используют описатель контекста в качестве указателя в.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-128">Subsequent remote procedure calls, such as RemoteRead, use the context handle as an in pointer.</span></span>

<span data-ttu-id="b3b5d-129">В дополнение к удаленной процедуре, которая инициализирует маркер контекста, интерфейс должен содержать процедуру, которая освобождает контекст сервера и устанавливает для контекстного маркера **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-129">In addition to the remote procedure that initializes the context handle, the interface must contain a procedure that frees the server context and sets context handle to **NULL**.</span></span> <span data-ttu-id="b3b5d-130">В предыдущем примере функция Ремотеклосе выполняет эту операцию.</span><span class="sxs-lookup"><span data-stu-id="b3b5d-130">In the preceding example, the RemoteClose function performs this operation.</span></span>

 

 