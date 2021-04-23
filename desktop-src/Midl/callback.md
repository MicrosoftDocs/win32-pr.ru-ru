---
title: атрибут обратного вызова
description: Атрибут \ callback \ объявляет статическую функцию обратного вызова, которая существует на стороне клиента распределенного приложения. Функции обратного вызова предоставляют серверу возможность выполнять код на клиенте.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- атрибут обратного вызова MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412898"
---
# <a name="callback-attribute"></a><span data-ttu-id="461d4-105">атрибут обратного вызова</span><span class="sxs-lookup"><span data-stu-id="461d4-105">callback attribute</span></span>

<span data-ttu-id="461d4-106">Атрибут **\[ обратного вызова \]** объявляет статическую функцию обратного вызова, которая существует на стороне клиента распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="461d4-106">The **\[callback\]** attribute declares a static callback function that exists on the client side of the distributed application.</span></span> <span data-ttu-id="461d4-107">Функции обратного вызова предоставляют серверу возможность выполнять код на клиенте.</span><span class="sxs-lookup"><span data-stu-id="461d4-107">Callback functions provide a way for the server to execute code on the client.</span></span>

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="461d4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="461d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="461d4-109">*Function-attr-список*</span><span class="sxs-lookup"><span data-stu-id="461d4-109">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="461d4-110">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="461d4-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="461d4-111">Допустимые атрибуты функции — **\[** [**Local**](local.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** ; и атрибут использования **\[** [**строка**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** и **\[** [**Контекстный \_ маркер**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="461d4-111">Valid function attributes are **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span> <span data-ttu-id="461d4-112">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="461d4-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="461d4-113">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="461d4-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="461d4-114">Задает [Базовый \_ тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md), тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="461d4-114">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="461d4-115">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="461d4-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="461d4-116">*декларатор указателя*</span><span class="sxs-lookup"><span data-stu-id="461d4-116">*ptr-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="461d4-117">Указывает ноль или несколько деклараторов указателей.</span><span class="sxs-lookup"><span data-stu-id="461d4-117">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="461d4-118">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="461d4-118">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="461d4-119">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="461d4-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="461d4-120">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="461d4-120">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="461d4-121">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="461d4-121">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="461d4-122">Указывает ноль или более атрибутов направления, атрибутов полей, атрибутов использования и атрибутов указателя, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="461d4-122">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="461d4-123">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="461d4-123">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="461d4-124">*declarator*</span><span class="sxs-lookup"><span data-stu-id="461d4-124">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="461d4-125">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="461d4-125">Specifies a standard C declarator such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="461d4-126">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="461d4-126">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="461d4-127">Идентификатор параметра-name является необязательным.</span><span class="sxs-lookup"><span data-stu-id="461d4-127">The parameter-name identifier is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="461d4-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="461d4-128">Remarks</span></span>

<span data-ttu-id="461d4-129">Функция **\[ обратного вызова \]** полезна, когда сервер должен получить сведения от клиента.</span><span class="sxs-lookup"><span data-stu-id="461d4-129">The **\[callback\]** function is useful when the server must obtain information from the client.</span></span> <span data-ttu-id="461d4-130">Если серверные приложения поддерживались в Windows 3. *x*, сервер может выполнить вызов удаленной процедуры в Windows 3. *x* сервер для получения необходимой информации.</span><span class="sxs-lookup"><span data-stu-id="461d4-130">If server applications were supported on Windows 3.*x*, the server could make a call to a remote procedure on the Windows 3.*x* server to obtain the needed information.</span></span> <span data-ttu-id="461d4-131">Функция обратного вызова выполняет ту же цель и позволяет серверу запросить у клиента информацию в контексте исходного вызова.</span><span class="sxs-lookup"><span data-stu-id="461d4-131">The callback function accomplishes the same purpose and lets the server query the client for information in the context of the original call.</span></span>

<span data-ttu-id="461d4-132">Обратные вызовы — это особые случаи удаленных вызовов, которые выполняются как часть одного потока.</span><span class="sxs-lookup"><span data-stu-id="461d4-132">Callbacks are special cases of remote calls that execute as part of a single thread.</span></span> <span data-ttu-id="461d4-133">Обратный вызов выполняется в контексте удаленного вызова.</span><span class="sxs-lookup"><span data-stu-id="461d4-133">A callback is issued in the context of a remote call.</span></span> <span data-ttu-id="461d4-134">Любая Удаленная процедура, определенная как часть того же интерфейса, что и статическая функция обратного вызова, может вызывать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="461d4-134">Any remote procedure defined as part of the same interface as the static callback function can call the callback function.</span></span>

<span data-ttu-id="461d4-135">Важно отметить, что использование \[ обратного вызова \] не рекомендуется в многопоточном программировании.</span><span class="sxs-lookup"><span data-stu-id="461d4-135">It is important to note that the use of \[callback\] is not recommended in multi-thread programming.</span></span> <span data-ttu-id="461d4-136">Как однопотоковое программное обеспечение, оно не поддерживает требования безопасности для многопотоковой среды.</span><span class="sxs-lookup"><span data-stu-id="461d4-136">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

<span data-ttu-id="461d4-137">Функция **рпкканцелсреад** не может использоваться для отмены вызова, который может отправлять статический обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="461d4-137">The **RpcCancelThread** function cannot be used to cancel a call that may dispatch a static callback.</span></span> <span data-ttu-id="461d4-138">Если определенный удаленный вызов процедуры никогда не приведет к обратному вызову, его можно отменить.</span><span class="sxs-lookup"><span data-stu-id="461d4-138">If a particular remote procedure call will never result in a callback, then it can be canceled.</span></span> <span data-ttu-id="461d4-139">В противном случае вызов можно отменить, только если он может гарантировать, что обратный вызов для него не был выдан.</span><span class="sxs-lookup"><span data-stu-id="461d4-139">Otherwise, a call can be canceled only if it can be guaranteed that a callback for it has not been issued.</span></span>

<span data-ttu-id="461d4-140">Атрибут обратного вызова поддерживается только последовательностями, ориентированным на подключение, и локальным протоколом.</span><span class="sxs-lookup"><span data-stu-id="461d4-140">Only the connection-oriented and local-protocol sequences support the callback attribute.</span></span> <span data-ttu-id="461d4-141">Размер \[ \] данных для обратных вызовов в последовательности локальных протоколов ограничен 150 байт.</span><span class="sxs-lookup"><span data-stu-id="461d4-141">The size of the \[out\] data for callbacks over the local-protocol sequence is limited to 150 bytes.</span></span> <span data-ttu-id="461d4-142">Если интерфейс RPC использует последовательность протокола датаграммы, вызовы процедур с атрибутом обратного вызова завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="461d4-142">If an RPC interface uses a connectionless (datagram) protocol sequence, calls to procedures with the callback attribute will fail.</span></span>

<span data-ttu-id="461d4-143">Дескрипторы не могут использоваться в качестве параметров в функциях обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="461d4-143">Handles cannot be used as parameters in callback functions.</span></span> <span data-ttu-id="461d4-144">Поскольку обратные вызовы всегда выполняются в контексте вызова, маркер привязки, используемый клиентом для выполнения вызова сервера, также используется в качестве обработчика привязки от сервера к клиенту.</span><span class="sxs-lookup"><span data-stu-id="461d4-144">Because callbacks always execute in the context of a call, the binding handle used by the client to make the call to the server is also used as the binding handle from the server to the client.</span></span>

<span data-ttu-id="461d4-145">Обратные вызовы могут быть вложены в любую глубину.</span><span class="sxs-lookup"><span data-stu-id="461d4-145">Callbacks can nest to any depth.</span></span>

## <a name="examples"></a><span data-ttu-id="461d4-146">Примеры</span><span class="sxs-lookup"><span data-stu-id="461d4-146">Examples</span></span>

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a><span data-ttu-id="461d4-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="461d4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="461d4-148">**массивы**</span><span class="sxs-lookup"><span data-stu-id="461d4-148">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="461d4-149">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="461d4-149">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="461d4-150">**const**</span><span class="sxs-lookup"><span data-stu-id="461d4-150">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="461d4-151">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="461d4-151">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="461d4-152">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="461d4-152">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="461d4-153">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="461d4-153">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="461d4-154">**обращать**</span><span class="sxs-lookup"><span data-stu-id="461d4-154">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="461d4-155">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="461d4-155">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="461d4-156">**/осф**</span><span class="sxs-lookup"><span data-stu-id="461d4-156">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="461d4-157">**ref**</span><span class="sxs-lookup"><span data-stu-id="461d4-157">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="461d4-158">**ptr**</span><span class="sxs-lookup"><span data-stu-id="461d4-158">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="461d4-159">**Строка**</span><span class="sxs-lookup"><span data-stu-id="461d4-159">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="461d4-160">**struct**</span><span class="sxs-lookup"><span data-stu-id="461d4-160">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="461d4-161">**наборов**</span><span class="sxs-lookup"><span data-stu-id="461d4-161">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="461d4-162">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="461d4-162">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="461d4-163">**рпкканцелсреад**</span><span class="sxs-lookup"><span data-stu-id="461d4-163">**RpcCancelThread**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 