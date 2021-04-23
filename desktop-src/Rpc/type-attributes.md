---
title: Атрибуты типа
description: Удаленный вызов процедур (RPC) и атрибуты типа MIDL, которые могут применяться к объявлениям типов.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890672"
---
# <a name="type-attributes"></a><span data-ttu-id="18bdb-103">Атрибуты типа</span><span class="sxs-lookup"><span data-stu-id="18bdb-103">Type Attributes</span></span>

<span data-ttu-id="18bdb-104">Атрибуты типа — это атрибуты MIDL, которые можно применять к объявлениям типов:</span><span class="sxs-lookup"><span data-stu-id="18bdb-104">Type attributes are the MIDL attributes that can be applied to type declarations:</span></span>

-   <span data-ttu-id="18bdb-105">**\[**[**справиться**](/windows/desktop/Midl/handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="18bdb-105">**\[**[**handle**](/windows/desktop/Midl/handle)**\]**</span></span>
-   <span data-ttu-id="18bdb-106">**\[**[**Контекстный \_ маркер**](/windows/desktop/Midl/context-handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="18bdb-106">**\[**[**context\_handle**](/windows/desktop/Midl/context-handle)**\]**</span></span>
-   <span data-ttu-id="18bdb-107">**\[**[**Тип коммутатора \_**](/windows/desktop/Midl/switch-type)**\]**</span><span class="sxs-lookup"><span data-stu-id="18bdb-107">**\[**[**switch\_type**](/windows/desktop/Midl/switch-type)**\]**</span></span>
-   [<span data-ttu-id="18bdb-108">атрибуты типа указателя</span><span class="sxs-lookup"><span data-stu-id="18bdb-108">pointer type attributes</span></span>](three-pointer-types.md)

<span data-ttu-id="18bdb-109">Атрибут **\[ \_ типа \] переключателя** обозначает тип дискриминатора объединения.</span><span class="sxs-lookup"><span data-stu-id="18bdb-109">The **\[switch\_type\]** attribute designates the type of a union discriminator.</span></span> <span data-ttu-id="18bdb-110">Этот атрибут применяется только к неинкапсулированному объединению.</span><span class="sxs-lookup"><span data-stu-id="18bdb-110">This attribute applies only to a nonencapsulated union.</span></span>

<span data-ttu-id="18bdb-111">Маркер контекста — это указатель с атрибутом **\[ \_ Handle \]** .</span><span class="sxs-lookup"><span data-stu-id="18bdb-111">A context handle is a pointer with a **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="18bdb-112">Атрибут **\[ \_ Handle \] контекста** позволяет создавать процедуры, которые сохраняют сведения о состоянии между вызовами удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="18bdb-112">The **\[context\_handle\]** attribute allows you to write procedures that maintain state information between remote procedure calls.</span></span> <span data-ttu-id="18bdb-113">Обработчик контекста со значением, отличным от NULL, представляет сохраненный контекст и выполняет две задачи:</span><span class="sxs-lookup"><span data-stu-id="18bdb-113">A context handle with a non-null value represents saved context and serves two purposes:</span></span>

-   <span data-ttu-id="18bdb-114">На стороне клиента он содержит сведения, необходимые библиотеке времени выполнения RPC для направления вызова на сервер.</span><span class="sxs-lookup"><span data-stu-id="18bdb-114">On the client side, it contains the information needed by the RPC run-time library to direct the call to the server.</span></span>
-   <span data-ttu-id="18bdb-115">На стороне сервера он выступает в качестве маркера в активном контексте.</span><span class="sxs-lookup"><span data-stu-id="18bdb-115">On the server side, it serves as a handle on active context.</span></span>

<span data-ttu-id="18bdb-116">Атрибут **\[** [**Handle**](/windows/desktop/Midl/handle) **\]** указывает, что тип может использоваться в качестве определяемого пользователем (универсального) маркера.</span><span class="sxs-lookup"><span data-stu-id="18bdb-116">The **\[**[**handle**](/windows/desktop/Midl/handle)**\]** attribute specifies that a type can occur as a user-defined (generic) handle.</span></span> <span data-ttu-id="18bdb-117">Эта функция позволяет разработать дескрипторы, имеющие смысл для приложения.</span><span class="sxs-lookup"><span data-stu-id="18bdb-117">This feature permits the design of handles that are meaningful to the application.</span></span> <span data-ttu-id="18bdb-118">Пользователь должен предоставить подпрограммы привязки и отмены привязки для преобразования между типом определяемого пользователем типа и типом обработчика RPC-примитива, **Handle \_ t**.</span><span class="sxs-lookup"><span data-stu-id="18bdb-118">The user must provide binding and unbinding routines to convert between the user-defined handle type and the RPC primitive handle type, **handle\_t**.</span></span> <span data-ttu-id="18bdb-119">Примитивный маркер содержит целевые сведения, осмысленные для библиотек времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="18bdb-119">A primitive handle contains destination information meaningful to the RPC run-time libraries.</span></span> <span data-ttu-id="18bdb-120">Определяемый пользователем обработчик может быть определен только в объявлении типа, а не в объявлении функции.</span><span class="sxs-lookup"><span data-stu-id="18bdb-120">A user-defined handle can only be defined in a type declaration, not in a function declaration.</span></span> <span data-ttu-id="18bdb-121">Параметр с атрибутом **\[ Handle \]** имеет двойное назначение.</span><span class="sxs-lookup"><span data-stu-id="18bdb-121">A parameter with the **\[handle\]** attribute has a double purpose.</span></span> <span data-ttu-id="18bdb-122">Он используется для определения привязки для вызова и передается в вызываемую процедуру в виде обычного параметра данных.</span><span class="sxs-lookup"><span data-stu-id="18bdb-122">It is used to determine the binding for the call, and it is transmitted to the called procedure as a normal data parameter.</span></span>

 

 