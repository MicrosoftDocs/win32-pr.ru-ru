---
title: атрибут context_handle
description: Атрибут \ context \_ Handle \ определяет маркер привязки, который сохраняет контекст или сведения о состоянии на сервере между вызовами удаленных процедур.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle атрибута MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789870"
---
# <a name="context_handle-attribute"></a><span data-ttu-id="8a270-104">\_атрибут Handle контекста</span><span class="sxs-lookup"><span data-stu-id="8a270-104">context\_handle attribute</span></span>

<span data-ttu-id="8a270-105">Атрибут **\[ \_ Handle \] контекста** определяет маркер привязки, который сохраняет контекст или сведения о состоянии на сервере между вызовами удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="8a270-105">The **\[context\_handle\]** attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span>

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a><span data-ttu-id="8a270-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a270-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a270-107">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="8a270-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8a270-108">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="8a270-108">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-109">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="8a270-109">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="8a270-110">Указывает тип указателя или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="8a270-110">Specifies a pointer type or a type identifier.</span></span> <span data-ttu-id="8a270-111">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="8a270-111">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-112">*декларатор и декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="8a270-112">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8a270-113">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="8a270-113">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="8a270-114">Декларатор для обработчика контекста должен включать хотя бы один декларатор указателя.</span><span class="sxs-lookup"><span data-stu-id="8a270-114">The declarator for a context handle must include at least one pointer declarator.</span></span> <span data-ttu-id="8a270-115">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="8a270-115">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="8a270-116">*Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="8a270-116">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="8a270-117">Идентификатор параметра-Name в деклараторе функции является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8a270-117">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-118">*Function-attr-список*</span><span class="sxs-lookup"><span data-stu-id="8a270-118">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8a270-119">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="8a270-119">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="8a270-120">Допустимые атрибуты функции — **\[** [**обратный вызов**](callback.md) **\]** , **\[** [**локальный**](local.md) **\]** объект, атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** ; и атрибуты использования **\[** [**строка**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** и **\[ Контекстный \_ маркер \]**.</span><span class="sxs-lookup"><span data-stu-id="8a270-120">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-121">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="8a270-121">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="8a270-122">Указывает ноль или несколько деклараторов указателей.</span><span class="sxs-lookup"><span data-stu-id="8a270-122">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="8a270-123">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из **\*** указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="8a270-123">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a270-124">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="8a270-124">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8a270-125">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="8a270-125">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-126">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="8a270-126">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8a270-127">Указывает ноль или более атрибутов направления, атрибутов полей, атрибутов использования и атрибутов указателя, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="8a270-127">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="8a270-128">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="8a270-128">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="8a270-129">*Контекстный-Handle-тип*</span><span class="sxs-lookup"><span data-stu-id="8a270-129">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8a270-130">Задает идентификатор, указывающий тип обработчика контекста, определенный в объявлении [**typedef**](typedef.md) , который принимает атрибут **\[ \_ Handle \]** .</span><span class="sxs-lookup"><span data-stu-id="8a270-130">Specifies the identifier that specifies the context handle type as defined in a [**typedef**](typedef.md) declaration that takes the **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="8a270-131">Подпрограммы очистки являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="8a270-131">The rundown routine is optional.</span></span>

<span data-ttu-id="8a270-132">**Windows server 2003 и Windows XP:** Один интерфейс может разрешать как сериализованные, так и несериализованные дескрипторы контекста, что позволяет одному методу интерфейса получить доступ к дескриптору контекста исключительно (сериализованный), а другие методы — к этому дескриптору контекста в общем режиме (не сериализованном).</span><span class="sxs-lookup"><span data-stu-id="8a270-132">**Windows ServerÂ 2003 and WindowsÂ XP:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="8a270-133">Эти возможности доступа сравнимы с механизмами блокировки чтения и записи. методы, использующие сериализованный контекстный маркер, являются эксклюзивными пользователями (модулями записи), тогда как методы, использующие несериализованный контекст контекста, являются общими пользователями (читателями).</span><span class="sxs-lookup"><span data-stu-id="8a270-133">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="8a270-134">Методы, которые удаляют или изменяют состояние обработчика контекста, должны быть сериализованы.</span><span class="sxs-lookup"><span data-stu-id="8a270-134">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="8a270-135">Методы, которые не изменяют состояние маркера контекста, например методы, которые просто считывают из обработчика контекста, могут быть несериализуемыми.</span><span class="sxs-lookup"><span data-stu-id="8a270-135">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="8a270-136">Обратите внимание, что методы создания неявно сериализуются.</span><span class="sxs-lookup"><span data-stu-id="8a270-136">Note that creation methods are implicitly serialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a270-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a270-137">Remarks</span></span>

<span data-ttu-id="8a270-138">Атрибут **\[ \_ Handle \] контекста** может отображаться как атрибут типа IDL [**typedef**](typedef.md) , как атрибут типа возвращаемого значения функции, или как атрибут параметра.</span><span class="sxs-lookup"><span data-stu-id="8a270-138">The **\[context\_handle\]** attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span> <span data-ttu-id="8a270-139">При применении атрибута **\[ \_ Handle \] контекста** к определению типа необходимо также предоставить подпрограммы очистки контекста.</span><span class="sxs-lookup"><span data-stu-id="8a270-139">When you apply the **\[context\_handle\]** attribute to a type definition, you must also provide a context rundown routine.</span></span> <span data-ttu-id="8a270-140">Дополнительные сведения см. в разделе [контекст запуска для сервера](/windows/desktop/Rpc/server-context-run-down-routine) .</span><span class="sxs-lookup"><span data-stu-id="8a270-140">See [Server Context Run-down Routine](/windows/desktop/Rpc/server-context-run-down-routine) for details.</span></span>

<span data-ttu-id="8a270-141">При использовании компилятора MIDL в режиме по умолчанию ([**/МС \_ ext**](-ms-ext.md)) дескриптор контекста может быть любым типом указателя, выбранным пользователем, при условии, что он соответствует требованиям для дескрипторов контекста, описанных здесь.</span><span class="sxs-lookup"><span data-stu-id="8a270-141">When you use the MIDL compiler in default ([**/ms\_ext**](-ms-ext.md)) mode, a context handle can be any pointer type selected by the user, as long as it complies with the requirements for context handles described here.</span></span> <span data-ttu-id="8a270-142">Данные, связанные с таким типом обработчика контекста, не передаются в сети и должны управляться только серверным приложением.</span><span class="sxs-lookup"><span data-stu-id="8a270-142">The data associated with such a context handle type is not transmitted on the network and should only be manipulated by the server application.</span></span> <span data-ttu-id="8a270-143">Компиляторы DCE IDL ограничивают дескрипторы контекста указателями типа [**void**](void.md) **\*** .</span><span class="sxs-lookup"><span data-stu-id="8a270-143">DCE IDL compilers restrict context handles to pointers of type [**void**](void.md) **\***.</span></span> <span data-ttu-id="8a270-144">Поэтому эта функция недоступна при использовании параметра компилятора MIDL [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="8a270-144">Therefore this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="8a270-145">Как и в случае с другими типами обработчиков, маркер контекста непрозрачен для клиентского приложения, и все связанные с ним данные не передаются.</span><span class="sxs-lookup"><span data-stu-id="8a270-145">As with other handle types, the context handle is opaque to the client application, and any data associated with it is not transmitted.</span></span> <span data-ttu-id="8a270-146">На сервере обработчик контекста служит в качестве маркера для активного контекста, и все данные, связанные с типом обработчика контекста, доступны.</span><span class="sxs-lookup"><span data-stu-id="8a270-146">On the server, the context handle serves as a handle on active context, and all data associated with the context handle type is accessible.</span></span>

<span data-ttu-id="8a270-147">Чтобы создать маркер контекста, клиент передает на сервер **\[** [](out-idl.md) **\]** указатель out, **\[** [**ref**](ref.md) , **\]** на маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="8a270-147">To create a context handle, the client passes to the server an **\[**[**out**](out-idl.md)**\]**, **\[**[**ref**](ref.md)**\]** pointer to a context handle.</span></span> <span data-ttu-id="8a270-148">(Сам обработчик контекста может иметь значение **null** или не **null** , если его значение согласуется с атрибутами указателя.</span><span class="sxs-lookup"><span data-stu-id="8a270-148">(The context handle itself can have a **NULL** or non-**NULL** value—as long as its value is consistent with its pointer attributes.</span></span> <span data-ttu-id="8a270-149">Например, если к типу обработчика контекста **\[** [](ref.md) **\]** применен атрибут ref, он не может иметь значение **null** .) Для выполнения привязки необходимо указать другой маркер привязки, пока не будет создан маркер контекста.</span><span class="sxs-lookup"><span data-stu-id="8a270-149">For example, when the context handle type has the **\[**[**ref**](ref.md)**\]** attribute applied to it, it cannot have a **NULL** value.) Another binding handle must be supplied to accomplish the binding until the context handle is created.</span></span> <span data-ttu-id="8a270-150">Если явный маркер не указан, используется неявная привязка.</span><span class="sxs-lookup"><span data-stu-id="8a270-150">When no explicit handle is specified, implicit binding is used.</span></span> <span data-ttu-id="8a270-151">Если **\[** [**неявный атрибут \_ Handle**](implicit-handle.md) отсутствует **\]** , используется автоматический обработчик.</span><span class="sxs-lookup"><span data-stu-id="8a270-151">When no **\[**[**implicit\_handle**](implicit-handle.md)**\]** attribute is present, an auto handle is used.</span></span>

<span data-ttu-id="8a270-152">Удаленная процедура на сервере создает Активный обработчик контекста.</span><span class="sxs-lookup"><span data-stu-id="8a270-152">The remote procedure on the server creates an active context handle.</span></span> <span data-ttu-id="8a270-153">Клиент должен использовать этот обработчик контекста в качестве параметра **\[** [**in**](in.md) **\]** или **\[ in**, **out \]** в последующих вызовах.</span><span class="sxs-lookup"><span data-stu-id="8a270-153">The client must use that context handle as an **\[**[**in**](in.md)**\]** or **\[in**, **out\]** parameter in subsequent calls.</span></span> <span data-ttu-id="8a270-154">**\[ В \]** качестве маркера привязки можно использовать только описатель контекста, который должен иметь значение, отличное от **null** .</span><span class="sxs-lookup"><span data-stu-id="8a270-154">An **\[in\]**-only context handle can be used as a binding handle, so it must have a non-**NULL** value.</span></span> <span data-ttu-id="8a270-155">Обработчик контекста только **\[ в \]** режиме не отражает изменения состояния на сервере.</span><span class="sxs-lookup"><span data-stu-id="8a270-155">An **\[in\]**-only context handle does not reflect state changes on the server.</span></span>

<span data-ttu-id="8a270-156">На сервере вызываемая процедура может интерпретировать обработчик контекста по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="8a270-156">On the server, the called procedure can interpret the context handle as needed.</span></span> <span data-ttu-id="8a270-157">Например, вызываемая процедура может выделить хранилище кучи и использовать контекстный маркер в качестве указателя на это хранилище.</span><span class="sxs-lookup"><span data-stu-id="8a270-157">For example, the called procedure can allocate heap storage and use the context handle as a pointer to this storage.</span></span>

<span data-ttu-id="8a270-158">Чтобы закрыть контекстный маркер, клиент передает контекст контекста как **\[** [](in.md) **\]** **\[** аргумент [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="8a270-158">To close a context handle, the client passes the context handle as an **\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]** argument.</span></span> <span data-ttu-id="8a270-159">Сервер должен вернуть **нулевой** обработчик контекста, когда он больше не обслуживает контекст от имени вызывающего.</span><span class="sxs-lookup"><span data-stu-id="8a270-159">The server must return a **NULL** context handle when it is no longer maintaining context on behalf of the caller.</span></span> <span data-ttu-id="8a270-160">Например, если контекстный обработчик представляет открытый файл, а вызов закрывает файл, сервер должен установить для контекста **значение NULL** и вернуть его клиенту.</span><span class="sxs-lookup"><span data-stu-id="8a270-160">For example, if the context handle represents an open file and the call closes the file, the server must set the context handle to **NULL** and return it to the client.</span></span> <span data-ttu-id="8a270-161">Значение **null** в качестве маркера привязки для последующих вызовов является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="8a270-161">A **NULL** value is invalid as a binding handle on subsequent calls.</span></span>

<span data-ttu-id="8a270-162">Маркер контекста допустим только для одного сервера.</span><span class="sxs-lookup"><span data-stu-id="8a270-162">A context handle is only valid for one server.</span></span> <span data-ttu-id="8a270-163">Если функция имеет два параметра дескриптора и дескриптор контекста не равен **null**, дескрипторы привязки должны ссылаться на одно и то же адресное пространство.</span><span class="sxs-lookup"><span data-stu-id="8a270-163">When a function has two handle parameters and the context handle is not **NULL**, the binding handles must refer to the same address space.</span></span>

<span data-ttu-id="8a270-164">Если у функции есть **\[** [](in.md) **\]** обработчик контекста in или **\[ in**, **\]** его контекстный обработчик может использоваться в качестве маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="8a270-164">When a function has an **\[**[**in**](in.md)**\]** or an **\[in**, **out\]** context handle, its context handle can be used as the binding handle.</span></span> <span data-ttu-id="8a270-165">В этом случае неявная привязка не используется, и атрибут **\[** [**неявного \_**](implicit-handle.md) **\]** или **\[** [**автоматического \_ обработчика**](auto-handle.md) **\]** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8a270-165">In this case, implicit binding is not used and the **\[**[**implicit\_handle**](implicit-handle.md)**\]** or **\[**[**auto\_handle**](auto-handle.md)**\]** attribute is ignored.</span></span>

<span data-ttu-id="8a270-166">К дескрипторам контекста применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="8a270-166">The following restrictions apply to context handles:</span></span>

-   <span data-ttu-id="8a270-167">Дескрипторы контекста не могут быть элементами массива, членами структуры или членами объединения.</span><span class="sxs-lookup"><span data-stu-id="8a270-167">Context handles cannot be array elements, structure members, or union members.</span></span> <span data-ttu-id="8a270-168">Они могут быть только параметрами.</span><span class="sxs-lookup"><span data-stu-id="8a270-168">They can only be parameters.</span></span>
-   <span data-ttu-id="8a270-169">Дескрипторы контекста не могут иметь атрибут " **\[** [**передать \_ как**](transmit-as.md) " **\]** или " **\[** [**представить \_ как**](represent-as.md) " **\]** .</span><span class="sxs-lookup"><span data-stu-id="8a270-169">Context handles cannot have the **\[**[**transmit\_as**](transmit-as.md)**\]** or **\[**[**represent\_as**](represent-as.md)**\]** attribute.</span></span>
-   <span data-ttu-id="8a270-170">Параметры, являющиеся указателями **\[** [**на**](out-idl.md) **\]** дескрипторы контекста, должны быть **\[** [**ссылками на REF**](ref.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="8a270-170">Parameters that are pointers to **\[**[**out**](out-idl.md)**\]** context handles must be **\[**[**ref**](ref.md)**\]** pointers.</span></span>
-   <span data-ttu-id="8a270-171">**\[** [**В**](in.md) **\]** качестве маркера привязки можно использовать маркер контекста, который не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8a270-171">An **\[**[**in**](in.md)**\]** context handle can be used as the binding handle and cannot be **NULL**.</span></span>
-   <span data-ttu-id="8a270-172">**\[ В** входном обработчике контекста может быть **значение NULL** , но только в том [**случае, если**](out-idl.md) процедура имеет другой явный параметр Handle.</span><span class="sxs-lookup"><span data-stu-id="8a270-172">An **\[in**, [**out**](out-idl.md) context handle can be **NULL** on input, but only if the procedure has another explicit handle parameter.</span></span> <span data-ttu-id="8a270-173">Если нет других явных параметров обработчика контекста, отличных от **null** , **\[ то обработчик** контекста **\] out** не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8a270-173">If there are no other explicit non-**NULL** context handle parameters, the **\[in**, **out\]** context handle cannot be **NULL**.</span></span>
-   <span data-ttu-id="8a270-174">Описатель контекста не может использоваться с обратными вызовами.</span><span class="sxs-lookup"><span data-stu-id="8a270-174">A context handle cannot be used with callbacks.</span></span>

## <a name="examples"></a><span data-ttu-id="8a270-175">Примеры</span><span class="sxs-lookup"><span data-stu-id="8a270-175">Examples</span></span>

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a><span data-ttu-id="8a270-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a270-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a270-177">**массивы**</span><span class="sxs-lookup"><span data-stu-id="8a270-177">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="8a270-178">**Автоматическая \_ работа**</span><span class="sxs-lookup"><span data-stu-id="8a270-178">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="8a270-179">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="8a270-179">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="8a270-180">Сброс контекста клиента</span><span class="sxs-lookup"><span data-stu-id="8a270-180">Client Context Reset</span></span>](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[<span data-ttu-id="8a270-181">**const**</span><span class="sxs-lookup"><span data-stu-id="8a270-181">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="8a270-182">Дескрипторы контекста</span><span class="sxs-lookup"><span data-stu-id="8a270-182">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="8a270-183">**справиться**</span><span class="sxs-lookup"><span data-stu-id="8a270-183">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="8a270-184">Привязка и дескрипторы</span><span class="sxs-lookup"><span data-stu-id="8a270-184">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="8a270-185">**обращать**</span><span class="sxs-lookup"><span data-stu-id="8a270-185">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="8a270-186">**неявный \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="8a270-186">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="8a270-187">**окне**</span><span class="sxs-lookup"><span data-stu-id="8a270-187">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="8a270-188">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="8a270-188">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="8a270-189">Многопоточные клиенты и дескрипторы контекста</span><span class="sxs-lookup"><span data-stu-id="8a270-189">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="8a270-190">**/МС \_ ext**</span><span class="sxs-lookup"><span data-stu-id="8a270-190">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="8a270-191">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="8a270-191">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="8a270-192">**ptr**</span><span class="sxs-lookup"><span data-stu-id="8a270-192">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="8a270-193">**ref**</span><span class="sxs-lookup"><span data-stu-id="8a270-193">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="8a270-194">**представлять \_ как**</span><span class="sxs-lookup"><span data-stu-id="8a270-194">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="8a270-195">**рпкссдестройклиентконтекст**</span><span class="sxs-lookup"><span data-stu-id="8a270-195">**RpcSsDestroyClientContext**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[<span data-ttu-id="8a270-196">Подпрограммы запуска контекста сервера</span><span class="sxs-lookup"><span data-stu-id="8a270-196">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="8a270-197">**Строка**</span><span class="sxs-lookup"><span data-stu-id="8a270-197">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="8a270-198">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="8a270-198">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="8a270-199">**определение**</span><span class="sxs-lookup"><span data-stu-id="8a270-199">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="8a270-200">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="8a270-200">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="8a270-201">**void**</span><span class="sxs-lookup"><span data-stu-id="8a270-201">**void**</span></span>](void.md)
</dt> </dl>

 

 