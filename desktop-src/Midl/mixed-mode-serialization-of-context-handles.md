---
title: Сериализация дескрипторов контекста в смешанном режиме
description: В Microsoft Windows XP один интерфейс может содержать как сериализованные, так и несериализованные дескрипторы контекста, которые называются сериализацией в смешанном режиме.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- Справочник по языку MIDL MIDL, сериализация дескрипторов контекста в смешанном режиме
- контекстно обрабатывает MIDL
- MIDL сериализации в смешанном режиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0922b53bfc7ba2e30ad8df0764e3cf9a36f0f723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888312"
---
# <a name="mixed-mode-serialization-of-context-handles"></a><span data-ttu-id="136ea-106">Сериализация дескрипторов контекста в смешанном режиме</span><span class="sxs-lookup"><span data-stu-id="136ea-106">Mixed Mode Serialization of Context Handles</span></span>

<span data-ttu-id="136ea-107">Начиная с Windows XP, один интерфейс может размещать как сериализованные, так и несериализованные дескрипторы контекста, позволяя одному методу интерфейса обращаться к дескриптору контекста исключительно (сериализовано), а другие методы — к этому дескриптору контекста в общем режиме (не сериализованном).</span><span class="sxs-lookup"><span data-stu-id="136ea-107">Starting with Windows XP, a single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="136ea-108">Дополнительные сведения об дескрипторах контекста см. в следующих атрибутах:</span><span class="sxs-lookup"><span data-stu-id="136ea-108">For more information about context handles, see the following attributes:</span></span>

-   [<span data-ttu-id="136ea-109">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="136ea-109">**context\_handle**</span></span>](context-handle.md)
-   [<span data-ttu-id="136ea-110">**\_сериализация обработчика контекста \_**</span><span class="sxs-lookup"><span data-stu-id="136ea-110">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
-   [<span data-ttu-id="136ea-111">**несериализуемый контекстный \_ обработчик \_**</span><span class="sxs-lookup"><span data-stu-id="136ea-111">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)

<span data-ttu-id="136ea-112">Функции доступа к сериализованным и общим режимам сравнимы с механизмами блокировки чтения и записи; методы, использующие сериализованный контекстный маркер, являются эксклюзивными пользователями (модулями записи), тогда как методы, использующие несериализованный контекст контекста, являются общими пользователями (читателями).</span><span class="sxs-lookup"><span data-stu-id="136ea-112">Serialized and shared mode access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="136ea-113">Методы, которые удаляют или изменяют состояние обработчика контекста, должны быть сериализованы.</span><span class="sxs-lookup"><span data-stu-id="136ea-113">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="136ea-114">Методы, которые не изменяют состояние маркера контекста, например методы, которые просто считывают из обработчика контекста, могут быть несериализуемыми.</span><span class="sxs-lookup"><span data-stu-id="136ea-114">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="136ea-115">Использование обработчика контекста в смешанном режиме может значительно повысить масштабируемость сервера, особенно если несколько потоков выполняют одновременные вызовы к одному и тому же контекстному обработчику.</span><span class="sxs-lookup"><span data-stu-id="136ea-115">Using a context handle in mixed mode can substantially improve the scalability of a server, especially when multiple threads make simultaneous calls to the same context handle.</span></span>

<span data-ttu-id="136ea-116">RPC не применяет "блокировку записи" для методов, использующих дескриптор контекста в общем режиме. Это означает, что приложения должны гарантировать, что дескрипторы контекста общего режима не изменяются.</span><span class="sxs-lookup"><span data-stu-id="136ea-116">RPC does not enforce "write lock" on methods using a context handle in shared mode, which means applications must ensure that shared mode context handles are not modified.</span></span> <span data-ttu-id="136ea-117">Изменение обработчика контекста, используемого в общем режиме, может привести к незаметному повреждению содержимого контекстного контекста, что не позволяет выполнять отладку.</span><span class="sxs-lookup"><span data-stu-id="136ea-117">Modification of a context handle used in shared mode can result in subtle corruptions of context handle contents, which are impossible to debug.</span></span>

<span data-ttu-id="136ea-118">Изменение логики сериализации контекстного маркера влияет только на сервер.</span><span class="sxs-lookup"><span data-stu-id="136ea-118">Changing the serialization logic of a context handle affects only the server.</span></span> <span data-ttu-id="136ea-119">Кроме того, изменение логики сериализации контекстного маркера не влияет на формат сети, поэтому изменения в логике сериализации на сервере не влияют на возможность взаимодействия существующих клиентов с сервером.</span><span class="sxs-lookup"><span data-stu-id="136ea-119">Also, changing the serialization logic of a context handle does not affect the wire format, and therefore, changes to serialization logic on a server do not affect existing clients' capability to interact with the server.</span></span>

<span data-ttu-id="136ea-120">Использовать только несериализованные дескрипторы контекста не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="136ea-120">Using only nonserialized context handles is not recommended.</span></span> <span data-ttu-id="136ea-121">Серверы, использующие несериализованные дескрипторы, должны переключиться на сериализованный доступ для метода, который закрывает дескриптор контекста.</span><span class="sxs-lookup"><span data-stu-id="136ea-121">Servers that use nonserialized handles are should switch to serialized access for the method that closes the context handle.</span></span>

<span data-ttu-id="136ea-122">Дескрипторы контекста, которые являются \[ выходными, \] обычно используются методами создания и не нуждаются в сериализации.</span><span class="sxs-lookup"><span data-stu-id="136ea-122">Context handles that are \[out\]-only are typically used by creation methods, and do not require any serialization.</span></span> <span data-ttu-id="136ea-123">Таким образом, любой атрибут сериализации, применяемый к \[ \] дескрипторам контекста, таким [**как \_ дескриптор \_ сериализации**](context-handle-serialize.md) или [**\_ \_ дескриптор контекста**](context-handle-noserialize.md), не обрабатывается RPC.</span><span class="sxs-lookup"><span data-stu-id="136ea-123">Therefore, any serialization attribute applied to \[out\]-only context handles, such as [**context\_handle\_serialize**](context-handle-serialize.md) or [**context\_handle\_noserialize**](context-handle-noserialize.md), is ignored by RPC.</span></span>

> [!Note]  
> <span data-ttu-id="136ea-124">Методы создания неявно сериализованы.</span><span class="sxs-lookup"><span data-stu-id="136ea-124">Creation methods are implicitly serialized.</span></span>

 

## <a name="examples"></a><span data-ttu-id="136ea-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="136ea-125">Examples</span></span>

<span data-ttu-id="136ea-126">В следующих двух примерах показано, как включить сериализацию дескрипторов в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="136ea-126">The following two examples show how to enable mixed mode serialization of context handles.</span></span>

<span data-ttu-id="136ea-127">В первом примере показано, как это сделать в IDL-файле:</span><span class="sxs-lookup"><span data-stu-id="136ea-127">The first example shows how to do so in the IDL file:</span></span>

``` syntax
typedef [context_handle] void *TestContextHandleExclusive;
typedef [context_handle] TestContextHandleExclusive TestContextHandleShared;

void
UseShared(...
          [in] TestContextHandleShared *Ctx,
          ...);

void
UseExclusive(...
             [in, out] TestContextHandleExclusive *Ctx,
             ...);
```

<span data-ttu-id="136ea-128">Во втором примере показано, как включить сериализацию дескрипторов контекста в смешанном режиме в файле ACF:</span><span class="sxs-lookup"><span data-stu-id="136ea-128">The second example shows how to enable mixed mode serialization of context handles in the ACF file:</span></span>

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a><span data-ttu-id="136ea-129">См. также</span><span class="sxs-lookup"><span data-stu-id="136ea-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="136ea-130">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="136ea-130">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="136ea-131">**\_сериализация обработчика контекста \_**</span><span class="sxs-lookup"><span data-stu-id="136ea-131">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="136ea-132">**несериализуемый контекстный \_ обработчик \_**</span><span class="sxs-lookup"><span data-stu-id="136ea-132">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> </dl>

 

 




