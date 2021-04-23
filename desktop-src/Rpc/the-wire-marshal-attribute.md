---
title: Атрибут wire_marshal
description: Атрибут \ проводное \_ маршалирование \ является атрибутом IDL-типа, аналогичным синтаксису \ "передать \_ как \", но предоставляя более эффективный способ маршалирования данных по сети.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- Удаленный вызов процедур RPC, атрибуты, wire_marshal
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413357"
---
# <a name="the-wire_marshal-attribute"></a><span data-ttu-id="69477-105">Атрибут Wired \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="69477-105">The wire\_marshal Attribute</span></span>

<span data-ttu-id="69477-106">Атрибут \[ [Wired \_ Marshal](/windows/desktop/Midl/wire-marshal) \] — это атрибут IDL-типа, аналогичный синтаксису для \[ [передачи в \_ виде](/windows/desktop/Midl/transmit-as) \] , но предоставляющий более эффективный способ маршалирования данных по сети.</span><span class="sxs-lookup"><span data-stu-id="69477-106">The \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] attribute is an IDL-type attribute similar in syntax to \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\], but providing a more efficient way to marshal data across a network.</span></span>

<span data-ttu-id="69477-107">Используйте \[ атрибут **Wired \_ Marshal** \] , чтобы указать тип данных, который будет передаваться вместо типа данных конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="69477-107">You use the \[**wire\_marshal**\] attribute to specify a data type that will be transmitted in place of the application-specific data type.</span></span> <span data-ttu-id="69477-108">Каждый тип конкретного приложения имеет соответствующий переданный тип, который определяет представление подключения (представление, используемое в сети). Тип, зависящий от приложения, не должен быть передающимся, но должен быть типом, распознаваемым MIDL.</span><span class="sxs-lookup"><span data-stu-id="69477-108">Each application-specific type has a corresponding transmittable type that defines the wire representation (the representation used on the network).The application-specific type need not be transmittable, but it must be a type that MIDL recognizes.</span></span> <span data-ttu-id="69477-109">Чтобы маршалировать тип, неизвестный для MIDL, используйте \[ [пользовательское \_ маршалирование](/windows/desktop/Midl/user-marshal)атрибута ACF \] .</span><span class="sxs-lookup"><span data-stu-id="69477-109">To marshal a type unknown to MIDL, use the ACF attribute \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\].</span></span>

<span data-ttu-id="69477-110">Тип конкретного приложения может быть простым, составным или иметь тип указателя.</span><span class="sxs-lookup"><span data-stu-id="69477-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="69477-111">Основное ограничение заключается в том, что экземпляр типа должен иметь фиксированный, четко определенный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="69477-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="69477-112">Если размер экземпляра типа необходимо изменить, используйте поле указателя вместо согласованного массива.</span><span class="sxs-lookup"><span data-stu-id="69477-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="69477-113">Кроме того, можно определить указатель на изменяемый тип.</span><span class="sxs-lookup"><span data-stu-id="69477-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="69477-114">Необходимо предоставить подпрограммы для изменения размера, маршалирования и распаковки данных, а также для освобождения связанной памяти.</span><span class="sxs-lookup"><span data-stu-id="69477-114">You must supply the routines for sizing, marshaling, and unmarshaling the data as well as freeing the associated memory.</span></span> <span data-ttu-id="69477-115">В следующей таблице описаны четыре имени подпрограммы, предоставляемые пользователем.</span><span class="sxs-lookup"><span data-stu-id="69477-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="69477-116"><type>— Это тип усерм, заданный в \[ определении типа **проводного \_ маршалирования** \] .</span><span class="sxs-lookup"><span data-stu-id="69477-116">The <type> is the userm-type specified in the \[**wire\_marshal**\] type definition.</span></span>



| <span data-ttu-id="69477-117">Подпрограмма</span><span class="sxs-lookup"><span data-stu-id="69477-117">Routine</span></span>                                                            | <span data-ttu-id="69477-118">Описание</span><span class="sxs-lookup"><span data-stu-id="69477-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="69477-119"><type>\_усерсизе</span><span class="sxs-lookup"><span data-stu-id="69477-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="69477-120">Изменяет размер буфера данных RPC перед упаковкой на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="69477-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="69477-121"><type>\_усермаршал</span><span class="sxs-lookup"><span data-stu-id="69477-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="69477-122">Маршалирует данные на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="69477-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="69477-123"><type>\_усерунмаршал</span><span class="sxs-lookup"><span data-stu-id="69477-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="69477-124">Распаковать данные на стороне клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="69477-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="69477-125"><type>\_усерфри</span><span class="sxs-lookup"><span data-stu-id="69477-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="69477-126">Освобождает данные на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="69477-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="69477-127">Эти подпрограммы, предоставляемые программистом, предоставляются как клиентом, так и серверным приложением на основе атрибутов направления.</span><span class="sxs-lookup"><span data-stu-id="69477-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span>

<span data-ttu-id="69477-128">Если параметр доступен только \[ [в](/windows/desktop/Midl/in) \] , клиент передает на сервер.</span><span class="sxs-lookup"><span data-stu-id="69477-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="69477-129">Клиенту требуются функции **<type> \_ усерсизе** и **<type> \_ усермаршал** .</span><span class="sxs-lookup"><span data-stu-id="69477-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="69477-130">Серверу требуются функции **<type> \_ усерунмаршал** и **<type> \_ усерфри** .</span><span class="sxs-lookup"><span data-stu-id="69477-130">The server needs the **<type>\_UserUnmarshal**, and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="69477-131">Для \[ [](/windows/desktop/Midl/out-idl) \] параметра только для выхода сервер передает клиенту.</span><span class="sxs-lookup"><span data-stu-id="69477-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="69477-132">Серверу требуются функции **<type> \_ усерсизе** и **<type> \_ усермаршал** , тогда как клиенту требуется функция **<type> \_ усермаршал** .</span><span class="sxs-lookup"><span data-stu-id="69477-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69477-133">См. также</span><span class="sxs-lookup"><span data-stu-id="69477-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69477-134">Атрибут пользовательской \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="69477-134">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="69477-135">Правила маршалирования для пользовательского \_ маршалирования и передачи проводного \_ маршалирования</span><span class="sxs-lookup"><span data-stu-id="69477-135">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="69477-136">проводное \_ маршалирование</span><span class="sxs-lookup"><span data-stu-id="69477-136">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="69477-137">Пользовательская \_ Упаковка</span><span class="sxs-lookup"><span data-stu-id="69477-137">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="69477-138">**ндржетусермаршалинфо**</span><span class="sxs-lookup"><span data-stu-id="69477-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 