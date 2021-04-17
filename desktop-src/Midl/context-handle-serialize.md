---
title: атрибут context_handle_serialize
description: Атрибут \ " \_ сериализация дескриптора контекста \_ \ ACF \" гарантирует, что дескриптор контекста будет всегда сериализован независимо от поведения приложения по умолчанию.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize атрибута MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681600"
---
# <a name="context_handle_serialize-attribute"></a><span data-ttu-id="3ed99-104">\_атрибут сериализации обработчика контекста \_</span><span class="sxs-lookup"><span data-stu-id="3ed99-104">context\_handle\_serialize attribute</span></span>

<span data-ttu-id="3ed99-105">Атрибут **\[ \_ \_ сериализации \] дескриптора контекста** ACF гарантирует, что дескриптор контекста будет всегда сериализован независимо от поведения приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ed99-105">The **\[context\_handle\_serialize\]** ACF attribute guarantees that a context handle will always be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="3ed99-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ed99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ed99-107">*Type-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="3ed99-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed99-108">Любые другие атрибуты ACF, применяемые к типу.</span><span class="sxs-lookup"><span data-stu-id="3ed99-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="3ed99-109">*Контекстный-Handle-тип*</span><span class="sxs-lookup"><span data-stu-id="3ed99-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed99-110">Идентификатор, указывающий тип обработчика контекста, как определено в объявлении [**typedef**](typedef.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed99-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="3ed99-111">Это тип, который получает атрибут " **\[ \_ \_ \] СЕРИАЛИЗОВАТЬ обработчик контекста** " в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="3ed99-111">This is the type that receives the **\[context\_handle\_serialize\]** attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="3ed99-112">*Функция-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="3ed99-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed99-113">Любые дополнительные атрибуты ACF, применяемые к функции.</span><span class="sxs-lookup"><span data-stu-id="3ed99-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="3ed99-114">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="3ed99-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed99-115">Имя функции, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="3ed99-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="3ed99-116">*параметр-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="3ed99-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed99-117">Любые другие атрибуты ACF, применяемые к параметру.</span><span class="sxs-lookup"><span data-stu-id="3ed99-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3ed99-118">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="3ed99-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed99-119">Имя параметра, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="3ed99-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ed99-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ed99-120">Remarks</span></span>

<span data-ttu-id="3ed99-121">Атрибут **\[ \_ \_ сериализации \] обработчика контекста** определяет маркер привязки, который хранит сведения о контексте или состоянии на сервере между вызовами удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="3ed99-121">The **\[context\_handle\_serialize\]** attribute identifies a binding handle that maintains context or state information on the server between remote procedure calls.</span></span> <span data-ttu-id="3ed99-122">Атрибут может отображаться как атрибут типа IDL [**typedef**](typedef.md) , как атрибут типа возвращаемого значения функции, или как атрибут параметра.</span><span class="sxs-lookup"><span data-stu-id="3ed99-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="3ed99-123">По умолчанию вызовы дескрипторов контекста сериализуются, но приложение может вызвать [**рпкссдонтсериализеконтекст**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) , чтобы переопределить это поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ed99-123">By default, calls on context handles are serialized, but an application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="3ed99-124">Использование атрибута **\[ \_ \_ сериализации \] дескриптора контекста** в файле ACF гарантирует, что вызовы в данном конкретном дескрипторе контекста будут сериализованы, даже если вызывающее приложение переопределило сериализацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ed99-124">Using the **\[context\_handle\_serialize\]** attribute in an ACF file guarantees that calls on this particular context handle will be serialized, even if the calling application has overridden the default serialization.</span></span> <span data-ttu-id="3ed99-125">Подпрограммы очистки контекста необязательны.</span><span class="sxs-lookup"><span data-stu-id="3ed99-125">A context rundown routine is optional.</span></span>

<span data-ttu-id="3ed99-126">Этот атрибут доступен в MIDL версии 5,0.</span><span class="sxs-lookup"><span data-stu-id="3ed99-126">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="3ed99-127">**Windows server 2003 и Windows XP или более поздней версии:** Один интерфейс может разрешать как сериализованные, так и несериализованные дескрипторы контекста, что позволяет одному методу интерфейса получить доступ к дескриптору контекста исключительно (сериализованный), а другие методы — к этому дескриптору контекста в общем режиме (не сериализованном).</span><span class="sxs-lookup"><span data-stu-id="3ed99-127">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="3ed99-128">Эти возможности доступа сравнимы с механизмами блокировки чтения и записи. методы, использующие сериализованный контекстный маркер, являются эксклюзивными пользователями (модулями записи), тогда как методы, использующие несериализованный контекст контекста, являются общими пользователями (читателями).</span><span class="sxs-lookup"><span data-stu-id="3ed99-128">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="3ed99-129">Методы, которые удаляют или изменяют состояние обработчика контекста, должны быть сериализованы.</span><span class="sxs-lookup"><span data-stu-id="3ed99-129">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="3ed99-130">Методы, которые не изменяют состояние маркера контекста, например методы, которые просто считывают из обработчика контекста, могут быть несериализуемыми.</span><span class="sxs-lookup"><span data-stu-id="3ed99-130">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="3ed99-131">Обратите внимание, что методы создания неявно сериализуются.</span><span class="sxs-lookup"><span data-stu-id="3ed99-131">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="3ed99-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="3ed99-132">Examples</span></span>

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="3ed99-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ed99-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed99-134">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="3ed99-134">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="3ed99-135">Атрибуты ACF</span><span class="sxs-lookup"><span data-stu-id="3ed99-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ed99-136">**несериализуемый контекстный \_ обработчик \_**</span><span class="sxs-lookup"><span data-stu-id="3ed99-136">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="3ed99-137">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="3ed99-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="3ed99-138">Дескрипторы контекста</span><span class="sxs-lookup"><span data-stu-id="3ed99-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="3ed99-139">**рпкссдонтсериализеконтекст**</span><span class="sxs-lookup"><span data-stu-id="3ed99-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="3ed99-140">Подпрограммы запуска контекста сервера</span><span class="sxs-lookup"><span data-stu-id="3ed99-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="3ed99-141">Многопоточные клиенты и дескрипторы контекста</span><span class="sxs-lookup"><span data-stu-id="3ed99-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="3ed99-142">**определение**</span><span class="sxs-lookup"><span data-stu-id="3ed99-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 