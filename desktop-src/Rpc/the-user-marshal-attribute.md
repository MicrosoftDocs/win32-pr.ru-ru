---
title: Атрибут user_marshal
description: Атрибут \ user \_ Marshal \ является атрибутом ACF-Type, аналогичным синтаксису \ представить \_ как \.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Удаленный вызов процедур RPC, атрибуты, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488065"
---
# <a name="the-user_marshal-attribute"></a><span data-ttu-id="b1dc6-105">Атрибут пользовательской \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="b1dc6-105">The user\_marshal Attribute</span></span>

<span data-ttu-id="b1dc6-106">Атрибут \[ [пользовательской \_ маршалирования](/windows/desktop/Midl/user-marshal) \] — это атрибут ACF-Type, аналогичный синтаксису для \[ [представления в \_ виде](/windows/desktop/Midl/represent-as) \] .</span><span class="sxs-lookup"><span data-stu-id="b1dc6-106">The \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attribute is an ACF-type attribute similar in syntax to \[ [represent\_as](/windows/desktop/Midl/represent-as)\].</span></span> <span data-ttu-id="b1dc6-107">Как и в случае с атрибутом IDL, \[ [ \_ ](/windows/desktop/Midl/wire-marshal) \] он обеспечивает более эффективный способ маршалирования данных по сети.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-107">As with the IDL attribute, \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\], it offers a more efficient way to marshal data across a network.</span></span> <span data-ttu-id="b1dc6-108">Как атрибут ACF, **\[ пользовательское \_ маршалирование \]** позволяет маршалировать пользовательские типы данных, неизвестные для MIDL.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-108">As an ACF attribute, **\[user\_marshal\]** lets you marshal custom data types that are unknown to MIDL.</span></span> <span data-ttu-id="b1dc6-109">Каждый тип конкретного приложения имеет соответствующий переданный тип, который определяет представление сети.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-109">Each application-specific type has a corresponding transmittable type that defines the wire representation.</span></span>

<span data-ttu-id="b1dc6-110">Тип конкретного приложения может быть простым, составным или иметь тип указателя.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="b1dc6-111">Основное ограничение заключается в том, что экземпляр типа должен иметь фиксированный, четко определенный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="b1dc6-112">Если размер экземпляра типа необходимо изменить, используйте поле указателя вместо согласованного массива.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="b1dc6-113">Кроме того, можно определить указатель на изменяемый тип.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="b1dc6-114">Как и в случае с атрибутом **\[ проводного \_ маршалирования \]** , вы предоставляете подпрограммы для определения размера, маршалирования, распаковки и освобождения проходов.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-114">As with the **\[wire\_marshal\]** attribute, you supply routines for the sizing, marshaling, unmarshaling, and freeing passes.</span></span> <span data-ttu-id="b1dc6-115">В следующей таблице описаны четыре имени подпрограммы, предоставляемые пользователем.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="b1dc6-116"><type>— Это *тип* усерм, указанный в определении типа **\[ пользовательского \_ маршалирования \]** .</span><span class="sxs-lookup"><span data-stu-id="b1dc6-116">The <type> is the userm-*type* specified in the **\[user\_marshal\]** type definition.</span></span>



| <span data-ttu-id="b1dc6-117">Подпрограмма</span><span class="sxs-lookup"><span data-stu-id="b1dc6-117">Routine</span></span>                                                            | <span data-ttu-id="b1dc6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b1dc6-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="b1dc6-119"><type>\_усерсизе</span><span class="sxs-lookup"><span data-stu-id="b1dc6-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="b1dc6-120">Изменяет размер буфера данных RPC перед упаковкой на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="b1dc6-121"><type>\_усермаршал</span><span class="sxs-lookup"><span data-stu-id="b1dc6-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="b1dc6-122">Маршалирует данные на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="b1dc6-123"><type>\_усерунмаршал</span><span class="sxs-lookup"><span data-stu-id="b1dc6-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="b1dc6-124">Распаковать данные на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="b1dc6-125"><type>\_усерфри</span><span class="sxs-lookup"><span data-stu-id="b1dc6-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="b1dc6-126">Освобождает данные на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="b1dc6-127">Эти пользовательские подпрограммы предоставляются как клиентом, так и серверным приложением на основе атрибутов направления.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-127">These user-supplied routines are provided by either the client or the server application, based on the directional attributes.</span></span>

<span data-ttu-id="b1dc6-128">Если параметр доступен только \[ [в](/windows/desktop/Midl/in) \] , клиент передает на сервер.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="b1dc6-129">Клиенту требуются функции **<type> \_ усерсизе** и **<type> \_ усермаршал** .</span><span class="sxs-lookup"><span data-stu-id="b1dc6-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="b1dc6-130">Серверу требуются функции **<type> \_ усерунмаршал** и **<type> \_ усерфри** .</span><span class="sxs-lookup"><span data-stu-id="b1dc6-130">The server needs the **<type>\_UserUnmarshal** and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="b1dc6-131">Для \[ [](/windows/desktop/Midl/out-idl) \] параметра только для выхода сервер передает клиенту.</span><span class="sxs-lookup"><span data-stu-id="b1dc6-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="b1dc6-132">Серверу требуются функции **<type> \_ усерсизе** и **<type> \_ усермаршал** , тогда как клиенту требуется функция **<type> \_ усермаршал** .</span><span class="sxs-lookup"><span data-stu-id="b1dc6-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1dc6-133">См. также</span><span class="sxs-lookup"><span data-stu-id="b1dc6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1dc6-134">Атрибут Wired \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="b1dc6-134">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="b1dc6-135">Правила маршалирования для пользовательского маршалирования и передачи проводного \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="b1dc6-135">Marshaling Rules for user marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="b1dc6-136">Пользовательская \_ Упаковка</span><span class="sxs-lookup"><span data-stu-id="b1dc6-136">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="b1dc6-137">проводное \_ маршалирование</span><span class="sxs-lookup"><span data-stu-id="b1dc6-137">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="b1dc6-138">**ндржетусермаршалинфо**</span><span class="sxs-lookup"><span data-stu-id="b1dc6-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 