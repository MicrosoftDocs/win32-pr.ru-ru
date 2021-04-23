---
title: атрибут context_handle_noserialize
description: Атрибут \ context \_ дескриптора \_ NONSERIALIZED \ ACF гарантирует, что дескриптор контекста не будет сериализован, независимо от поведения приложения по умолчанию.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize атрибута MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789871"
---
# <a name="context_handle_noserialize-attribute"></a><span data-ttu-id="180fc-104">\_атрибут несериализации контекстного обработчика \_</span><span class="sxs-lookup"><span data-stu-id="180fc-104">context\_handle\_noserialize attribute</span></span>

<span data-ttu-id="180fc-105">Атрибут ACF **\[ \_ дескриптора \_ \] несериализации** гарантирует, что дескриптор контекста не будет сериализован, независимо от поведения приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="180fc-105">The **\[context\_handle\_noserialize\]** ACF attribute guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="180fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="180fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="180fc-107">*Type-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="180fc-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="180fc-108">Любые другие атрибуты ACF, применяемые к типу.</span><span class="sxs-lookup"><span data-stu-id="180fc-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="180fc-109">*Контекстный-Handle-тип*</span><span class="sxs-lookup"><span data-stu-id="180fc-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="180fc-110">Идентификатор, указывающий тип обработчика контекста, как определено в объявлении [**typedef**](typedef.md) .</span><span class="sxs-lookup"><span data-stu-id="180fc-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="180fc-111">Это тип, который получает атрибут [**\[ \_ Handle \] для контекста**](context-handle.md) в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="180fc-111">This is the type that receives the [**\[context\_handle\]**](context-handle.md) attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="180fc-112">*Функция-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="180fc-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="180fc-113">Любые дополнительные атрибуты ACF, применяемые к функции.</span><span class="sxs-lookup"><span data-stu-id="180fc-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="180fc-114">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="180fc-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="180fc-115">Имя функции, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="180fc-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="180fc-116">*параметр-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="180fc-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="180fc-117">Любые другие атрибуты ACF, применяемые к параметру.</span><span class="sxs-lookup"><span data-stu-id="180fc-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="180fc-118">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="180fc-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="180fc-119">Имя параметра, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="180fc-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="180fc-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="180fc-120">Remarks</span></span>

<span data-ttu-id="180fc-121">Атрибут [**\[ \_ Handle \] контекста**](context-handle.md) определяет маркер привязки, который сохраняет контекст или сведения о состоянии на сервере между вызовами удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="180fc-121">The [**\[context\_handle\]**](context-handle.md) attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span> <span data-ttu-id="180fc-122">Атрибут может отображаться как атрибут типа IDL [**typedef**](typedef.md) , как атрибут типа возвращаемого значения функции, или как атрибут параметра.</span><span class="sxs-lookup"><span data-stu-id="180fc-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="180fc-123">По умолчанию вызовы дескрипторов контекста сериализуются.</span><span class="sxs-lookup"><span data-stu-id="180fc-123">By default, calls on context handles are serialized.</span></span> <span data-ttu-id="180fc-124">Приложение может вызвать [**рпкссдонтсериализеконтекст**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) , чтобы переопределить это поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="180fc-124">An application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="180fc-125">Использование атрибута [**\[ \_ дескриптора \] контекста**](context-handle.md) в файле ACF гарантирует, что вызовы в данном конкретном дескрипторе контекста не будут сериализованы независимо от поведения вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="180fc-125">Using the [**\[context\_handle\]**](context-handle.md) attribute in an ACF file guarantees that calls on this particular context handle will not be serialized, regardless of the calling application's behavior.</span></span> <span data-ttu-id="180fc-126">Предоставление подпрограммы очистки контекста является необязательным.</span><span class="sxs-lookup"><span data-stu-id="180fc-126">Providing a context rundown routine is optional.</span></span>

<span data-ttu-id="180fc-127">Этот атрибут доступен в MIDL версии 5,0.</span><span class="sxs-lookup"><span data-stu-id="180fc-127">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="180fc-128">**Windows server 2003 и Windows XP или более поздней версии:** Один интерфейс может разрешать как сериализованные, так и несериализованные дескрипторы контекста, что позволяет одному методу интерфейса получить доступ к дескриптору контекста исключительно (сериализованный), а другие методы — к этому дескриптору контекста в общем режиме (не сериализованном).</span><span class="sxs-lookup"><span data-stu-id="180fc-128">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="180fc-129">Эти возможности доступа сравнимы с механизмами блокировки чтения и записи. методы, использующие сериализованный контекстный маркер, являются эксклюзивными пользователями (модулями записи), тогда как методы, использующие несериализованный контекст контекста, являются общими пользователями (читателями).</span><span class="sxs-lookup"><span data-stu-id="180fc-129">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="180fc-130">Методы, которые удаляют или изменяют состояние обработчика контекста, должны быть сериализованы.</span><span class="sxs-lookup"><span data-stu-id="180fc-130">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="180fc-131">Методы, которые не изменяют состояние маркера контекста, например методы, которые просто считывают из обработчика контекста, могут быть несериализуемыми.</span><span class="sxs-lookup"><span data-stu-id="180fc-131">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="180fc-132">Обратите внимание, что методы создания неявно сериализуются.</span><span class="sxs-lookup"><span data-stu-id="180fc-132">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="180fc-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="180fc-133">Examples</span></span>

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="180fc-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="180fc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="180fc-135">Атрибуты ACF</span><span class="sxs-lookup"><span data-stu-id="180fc-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="180fc-136">**\_сериализация обработчика контекста \_**</span><span class="sxs-lookup"><span data-stu-id="180fc-136">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="180fc-137">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="180fc-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="180fc-138">Дескрипторы контекста</span><span class="sxs-lookup"><span data-stu-id="180fc-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="180fc-139">**рпкссдонтсериализеконтекст**</span><span class="sxs-lookup"><span data-stu-id="180fc-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="180fc-140">Подпрограммы запуска контекста сервера</span><span class="sxs-lookup"><span data-stu-id="180fc-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="180fc-141">Многопоточные клиенты и дескрипторы контекста</span><span class="sxs-lookup"><span data-stu-id="180fc-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="180fc-142">**определение**</span><span class="sxs-lookup"><span data-stu-id="180fc-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 