---
title: Атрибут transmit_as
description: Атрибут \ "передать \_ как \" предоставляет способ управления упаковкой данных, не беспокоясь о том, что данные маршалируются на низком уровне \ 8212; то есть не беспокойтесь о размерах данных или обмене байтами в разнородной среде.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- Удаленный вызов процедур RPC, атрибуты, transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413358"
---
# <a name="the-transmit_as-attribute"></a><span data-ttu-id="48e8a-105">Атрибут передачи \_ as</span><span class="sxs-lookup"><span data-stu-id="48e8a-105">The transmit\_as Attribute</span></span>

<span data-ttu-id="48e8a-106">Атрибут " **\[** [**передать \_ как**](/windows/desktop/Midl/transmit-as) " **\]** позволяет управлять упаковкой данных, не беспокоясь о необходимости упаковки данных на низком уровне, то есть не беспокоясь о размерах данных или обмене байтами в разнородной среде.</span><span class="sxs-lookup"><span data-stu-id="48e8a-106">The **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute offers a way to control data marshaling without worrying about marshaling data at a low level—that is, without worrying about data sizes or byte swapping in a heterogeneous environment.</span></span> <span data-ttu-id="48e8a-107">Позволяя сократить объем данных, передаваемых по сети, атрибут **\[ передачи \_ As \]** может повысить эффективность работы приложения.</span><span class="sxs-lookup"><span data-stu-id="48e8a-107">By letting you reduce the amount of data transmitted over the network, the **\[transmit\_as\]** attribute can make your application more efficient.</span></span>

<span data-ttu-id="48e8a-108">Используйте атрибут **\[ передать \_ как \]** , чтобы указать тип данных, который заглушки RPC будет передавать по сети вместо использования типа данных, предоставленного приложением.</span><span class="sxs-lookup"><span data-stu-id="48e8a-108">You use the **\[transmit\_as\]** attribute to specify a data type that the RPC stubs will transmit over the network instead of using the data type provided by the application.</span></span> <span data-ttu-id="48e8a-109">Вы предоставляете подпрограммы, которые преобразуют тип данных в тип, используемый для передачи, и из него.</span><span class="sxs-lookup"><span data-stu-id="48e8a-109">You supply routines that convert the data type to and from the type that is used for transmission.</span></span> <span data-ttu-id="48e8a-110">Кроме того, необходимо предоставить подпрограммы для высвобождения памяти, используемой для типа данных, и переданного типа.</span><span class="sxs-lookup"><span data-stu-id="48e8a-110">You must also supply routines to free the memory used for the data type and the transmitted type.</span></span> <span data-ttu-id="48e8a-111">Например, в следующем примере определяется **\_ тип xmit** , как тип данных, передаваемый для всех данных приложения, указанных как **тип \_ Spec**:</span><span class="sxs-lookup"><span data-stu-id="48e8a-111">For example, the following defines **xmit\_type** as the data type transmitted for all application data specified as being of type **type\_spec**:</span></span>

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

<span data-ttu-id="48e8a-112">В следующей таблице описаны четыре названия подпрограмм, предоставляемых программистом.</span><span class="sxs-lookup"><span data-stu-id="48e8a-112">The following table describes the four programmer-supplied routine names.</span></span> <span data-ttu-id="48e8a-113">**Type** — это тип данных, известный приложению, а **\_ тип xmit** — тип данных, используемый для передачи.</span><span class="sxs-lookup"><span data-stu-id="48e8a-113">**Type** is the data type known to the application, and **xmit\_type** is the data type used for transmission.</span></span>



| <span data-ttu-id="48e8a-114">Подпрограмма</span><span class="sxs-lookup"><span data-stu-id="48e8a-114">Routine</span></span>                                                 | <span data-ttu-id="48e8a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="48e8a-115">Description</span></span>                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48e8a-116">**Введите \_ \_ xmit**</span><span class="sxs-lookup"><span data-stu-id="48e8a-116">**type\_to\_xmit**</span></span>](the-type-to-xmit-function.md)     | <span data-ttu-id="48e8a-117">Выделяет объект переданного типа и преобразовывает тип приложения в тип, передаваемый по сети (вызывающий объект и вызываемый).</span><span class="sxs-lookup"><span data-stu-id="48e8a-117">Allocates an object of the transmitted type and converts from application type to type transmitted over the network (caller and object called).</span></span> |
| [<span data-ttu-id="48e8a-118">**Тип \_ из \_ xmit**</span><span class="sxs-lookup"><span data-stu-id="48e8a-118">**Type\_from\_xmit**</span></span>](the-type-from-xmit-function.md) | <span data-ttu-id="48e8a-119">Преобразует тип переданного переданного типа в тип приложения (вызывающий объект и называемый объектом).</span><span class="sxs-lookup"><span data-stu-id="48e8a-119">Converts from transmitted type to application type (caller and object called).</span></span>                                                                  |
| [<span data-ttu-id="48e8a-120">**Введите \_ бесплатный \_ inst**</span><span class="sxs-lookup"><span data-stu-id="48e8a-120">**Type\_free\_inst**</span></span>](the-type-free-inst-function.md) | <span data-ttu-id="48e8a-121">Освобождает ресурсы, используемые типом приложения (только вызываемый объект).</span><span class="sxs-lookup"><span data-stu-id="48e8a-121">Frees resources used by the application type (object called only).</span></span>                                                                              |
| [<span data-ttu-id="48e8a-122">**Введите \_ бесплатный \_ xmit**</span><span class="sxs-lookup"><span data-stu-id="48e8a-122">**Type\_free\_xmit**</span></span>](the-type-free-xmit-function.md) | <span data-ttu-id="48e8a-123">Освобождает хранилище, возвращенное типом в подпрограмму \*\*\*\*\*\_\*\*\* \_ xmit\*\* (вызывающий и вызываемый объект).</span><span class="sxs-lookup"><span data-stu-id="48e8a-123">Frees storage returned by the **type ***\_*** to\_xmit** routine (caller and object called).</span></span>                                                      |



 

<span data-ttu-id="48e8a-124">За исключением этих четырех предоставленных программистом функций, передаваемый тип не обрабатывается приложением.</span><span class="sxs-lookup"><span data-stu-id="48e8a-124">Other than by these four programmer-supplied functions, the transmitted type is not manipulated by the application.</span></span> <span data-ttu-id="48e8a-125">Передаваемый тип определяется только для перемещения данных по сети.</span><span class="sxs-lookup"><span data-stu-id="48e8a-125">The transmitted type is defined only to move data over the network.</span></span> <span data-ttu-id="48e8a-126">После преобразования данных в тип, используемый приложением, память, используемая передаваемым типом, освобождается.</span><span class="sxs-lookup"><span data-stu-id="48e8a-126">After the data is converted to the type used by the application, the memory used by the transmitted type is freed.</span></span>

<span data-ttu-id="48e8a-127">Эти подпрограммы, предоставляемые программистом, предоставляются как клиентом, так и серверным приложением на основе атрибутов направления.</span><span class="sxs-lookup"><span data-stu-id="48e8a-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span> <span data-ttu-id="48e8a-128">Если параметр доступен только **\[** [**в**](/windows/desktop/Midl/in) **\]** , клиент передает на сервер.</span><span class="sxs-lookup"><span data-stu-id="48e8a-128">If the parameter is **\[**[**in**](/windows/desktop/Midl/in)**\]** only, the client transmits to the server.</span></span> <span data-ttu-id="48e8a-129">Клиенту требуется **тип \_ для \_ xmit** и **Type \_ Free \_ xmit** functions.</span><span class="sxs-lookup"><span data-stu-id="48e8a-129">The client needs the **type\_to\_xmit** and **type\_free\_xmit** functions.</span></span> <span data-ttu-id="48e8a-130">Серверу требуется **тип \_ из \_ xmit** и **введите бесплатные функции \_ \_ inst** .</span><span class="sxs-lookup"><span data-stu-id="48e8a-130">The server needs the **type\_from\_xmit** and **type\_free\_inst** functions.</span></span> <span data-ttu-id="48e8a-131">Для **\[** [](/windows/desktop/Midl/out-idl) **\]** параметра только для выхода сервер передает клиенту.</span><span class="sxs-lookup"><span data-stu-id="48e8a-131">For an **\[**[**out**](/windows/desktop/Midl/out-idl)**\]**-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="48e8a-132">Серверное приложение должно реализовать **тип \_ для \_ xmit** и **ввести бесплатные функции \_ \_ xmit** , тогда как клиентская программа должна предоставить **тип из функции \_ \_ xmit** .</span><span class="sxs-lookup"><span data-stu-id="48e8a-132">The server application must implement the **type\_to\_xmit** and **type\_free\_xmit** functions, while the client program must supply the **type\_from\_xmit** function.</span></span> <span data-ttu-id="48e8a-133">Для временных объектов **\_ типа xmit** заглушка вызывает **Type ***\_*** Free \_ xmit** , чтобы освободить память, выделенную вызовом **типа \_ в \_ xmit**.</span><span class="sxs-lookup"><span data-stu-id="48e8a-133">For the temporary **xmit\_type** objects, the stub will call **type ***\_*** free\_xmit** to free any memory allocated by a call to **type\_to\_xmit**.</span></span>

<span data-ttu-id="48e8a-134">Некоторые рекомендации относятся к экземпляру типа приложения.</span><span class="sxs-lookup"><span data-stu-id="48e8a-134">Certain guidelines apply to the application type instance.</span></span> <span data-ttu-id="48e8a-135">Если тип приложения является указателем или содержит указатель, то **тип** \_ **из подпрограммы \_ xmit** должен выделить память для данных, на которые указывает указатель (сам объект типа приложения управляется заглушкой обычным способом).</span><span class="sxs-lookup"><span data-stu-id="48e8a-135">If the application type is a pointer or contains a pointer, then the **type**\_**from\_xmit** routine must allocate memory for the data that the pointers point to (the application type object itself is manipulated by the stub in the usual way).</span></span>

<span data-ttu-id="48e8a-136">Для исходящих **\[ \] и \]** исходящих параметров или одного из компонентов типа, содержащего атрибут « **\[ передать \_ как \]** », автоматически вызывается подпрограммы **Type** Free **inst для объектов данных, имеющих атрибут. \[ \]** \_ **\_**</span><span class="sxs-lookup"><span data-stu-id="48e8a-136">For **\[out\]** and **\[in, out\] out\]** parameters, or one of their components, of a type that contains the **\[transmit\_as\]** attribute, the **type**\_**free\_inst** routine is automatically called for the data objects that have the attribute.</span></span> <span data-ttu-id="48e8a-137">Для **входных** параметров подпрограммы **типа** \_ **Free \_ inst** вызываются только в том случае, если к параметру был применен атрибут **\[ передачи \_ As \]** .</span><span class="sxs-lookup"><span data-stu-id="48e8a-137">For **in** parameters, the **type**\_**free\_inst** routine is called only if the **\[transmit\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="48e8a-138">Если атрибут применен к компонентам параметра, то подпрограммы **Type** \_ **Free \_ inst** не вызываются.</span><span class="sxs-lookup"><span data-stu-id="48e8a-138">If the attribute has been applied to the components of the parameter, the **type**\_**free\_inst** routine is not called.</span></span> <span data-ttu-id="48e8a-139">Отсутствуют свободные вызовы для внедренных данных и один вызов (связанный с атрибутом верхнего уровня) для параметра только **в** .</span><span class="sxs-lookup"><span data-stu-id="48e8a-139">There are no freeing calls for the embedded data and at-most-one call (related to the top-level attribute) for an **in** only parameter.</span></span>

<span data-ttu-id="48e8a-140">Начиная с MIDL 2,0, клиент и сервер должны предоставлять все четыре функции.</span><span class="sxs-lookup"><span data-stu-id="48e8a-140">Effective with MIDL 2.0, both client and server must supply all four functions.</span></span> <span data-ttu-id="48e8a-141">Например, связанный список может передаваться как массив размеров.</span><span class="sxs-lookup"><span data-stu-id="48e8a-141">For example, a linked list can be transmitted as a sized array.</span></span> <span data-ttu-id="48e8a-142">Подпрограммы с **типом \_ to \_ xmit** просматривает связанный список и копирует упорядоченные данные в массив.</span><span class="sxs-lookup"><span data-stu-id="48e8a-142">The **type\_to\_xmit** routine walks the linked list and copies the ordered data into an array.</span></span> <span data-ttu-id="48e8a-143">Элементы массива упорядочены таким образом, что многие указатели, связанные со структурой списка, не должны передаваться.</span><span class="sxs-lookup"><span data-stu-id="48e8a-143">The array elements are ordered so that the many pointers associated with the list structure do not have to be transmitted.</span></span> <span data-ttu-id="48e8a-144">**Тип из подпрограммы \_ \_ xmit** считывает массив и помещает его элементы в структуру связанного списка.</span><span class="sxs-lookup"><span data-stu-id="48e8a-144">The **type\_from\_xmit** routine reads the array and puts its elements into a linked-list structure.</span></span>

<span data-ttu-id="48e8a-145">Список с двойным связыванием ( \_ список прямых ссылок \_ ) включает данные и указатели на элементы списка "Предыдущий" и "следующий":</span><span class="sxs-lookup"><span data-stu-id="48e8a-145">The double-linked list (DOUBLE\_LINK\_LIST) includes data and pointers to the previous and next list elements:</span></span>

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

<span data-ttu-id="48e8a-146">Вместо того чтобы передавать сложную структуру, **\[** атрибут [**передачи \_ as**](/windows/desktop/Midl/transmit-as) **\]** можно использовать для отправки его по сети в качестве массива.</span><span class="sxs-lookup"><span data-stu-id="48e8a-146">Rather than shipping the complex structure, the **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute can be used to send it over the network as an array.</span></span> <span data-ttu-id="48e8a-147">Последовательность элементов в массиве удерживает порядок элементов в списке по меньшей цене:</span><span class="sxs-lookup"><span data-stu-id="48e8a-147">The sequence of items in the array retains the ordering of the elements in the list at a lower cost:</span></span>

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

<span data-ttu-id="48e8a-148">Атрибут **\[ передачи \_ As \]** отображается в IDL-файле:</span><span class="sxs-lookup"><span data-stu-id="48e8a-148">The **\[transmit\_as\]** attribute appears in the IDL file:</span></span>

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

<span data-ttu-id="48e8a-149">В следующем примере **модифилистпрок** определяет параметр типа Double \_ Link \_ типа **\[ в \]** качестве параметра out:</span><span class="sxs-lookup"><span data-stu-id="48e8a-149">In the following example, **ModifyListProc** defines the parameter of type DOUBLE\_LINK\_TYPE as an **\[in, out\]** parameter:</span></span>

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

<span data-ttu-id="48e8a-150">Четыре определяемые программистом функции используют имя типа в именах функций и при необходимости используют представленные и передаваемые типы в качестве типов параметров:</span><span class="sxs-lookup"><span data-stu-id="48e8a-150">The four programmer-defined functions use the name of the type in the function names, and use the presented and transmitted types as parameter types, as required:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 