---
title: call_as - атрибут
description: Атрибут \ Call \_ as \ позволяет сопоставлять функцию, которая не может быть удаленно вызвана удаленной функцией.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as атрибута MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105650316"
---
# <a name="call_as-attribute"></a><span data-ttu-id="f05eb-104">вызвать \_ как атрибут</span><span class="sxs-lookup"><span data-stu-id="f05eb-104">call\_as attribute</span></span>

<span data-ttu-id="f05eb-105">Атрибут **\[ вызвать \_ как \]** позволяет сопоставлять функцию, которая не может быть удаленно вызвана удаленной функцией.</span><span class="sxs-lookup"><span data-stu-id="f05eb-105">The **\[call\_as\]** attribute enables you to map a function that cannot be called remotely to a remote function.</span></span>

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a><span data-ttu-id="f05eb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f05eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f05eb-107">*Локальная процедура*</span><span class="sxs-lookup"><span data-stu-id="f05eb-107">*local-proc*</span></span> 
</dt> <dd>

<span data-ttu-id="f05eb-108">Задает определяемую операцией подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="f05eb-108">Specifies an operation-defined routine.</span></span>

</dd> <dt>

<span data-ttu-id="f05eb-109">*Operation-Attribute-список*</span><span class="sxs-lookup"><span data-stu-id="f05eb-109">*operation-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f05eb-110">Указывает один или несколько атрибутов, которые применяются к операции.</span><span class="sxs-lookup"><span data-stu-id="f05eb-110">Specifies one or more attributes that apply to the operation.</span></span> <span data-ttu-id="f05eb-111">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="f05eb-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="f05eb-112">*имя операции*</span><span class="sxs-lookup"><span data-stu-id="f05eb-112">*operation-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f05eb-113">Указывает именованную операцию, представленную для приложения.</span><span class="sxs-lookup"><span data-stu-id="f05eb-113">Specifies the named operation presented to the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f05eb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f05eb-114">Remarks</span></span>

<span data-ttu-id="f05eb-115">Возможность сопоставлять функции, которые нельзя вызывать удаленно в удаленную функцию, особенно полезна в интерфейсах с множеством типов параметров, которые не могут передаваться по сети.</span><span class="sxs-lookup"><span data-stu-id="f05eb-115">The ability to map a function that cannot be called remotely to a remote function is particularly helpful in interfaces that have numerous parameter types that cannot be transmitted across the network.</span></span> <span data-ttu-id="f05eb-116">Вместо того чтобы использовать многие **\[** типы [**представления \_**](represent-as.md) **\]** и передачи в **\[** [**\_ качестве**](transmit-as.md) **\]** типов, можно объединить все преобразования с помощью **\[ вызова \_ в качестве \]** подпрограмм.</span><span class="sxs-lookup"><span data-stu-id="f05eb-116">Rather than using many **\[**[**represent\_as**](represent-as.md)**\]** and **\[**[**transmit\_as**](transmit-as.md)**\]** types, you can combine all the conversions using **\[call\_as\]** routines.</span></span> <span data-ttu-id="f05eb-117">Вы предоставляете два **\[ вызова \_ как \]** подпрограммы (на стороне клиента и на стороне сервера) для привязки подпрограммы между вызовами приложения и удаленными вызовами.</span><span class="sxs-lookup"><span data-stu-id="f05eb-117">You supply the two **\[call\_as\]** routines (client side and server side) to bind the routine between the application calls and the remote calls.</span></span>

<span data-ttu-id="f05eb-118">Для интерфейсов объектов можно использовать атрибут **\[ Call \_ как \]** .</span><span class="sxs-lookup"><span data-stu-id="f05eb-118">The **\[call\_as\]** attribute can be used for object interfaces.</span></span> <span data-ttu-id="f05eb-119">В этом случае определение интерфейса можно использовать для локальных вызовов, а также для удаленных вызовов, так как **\[ вызов \_ как \]** позволяет удаленно сопоставлять интерфейс, который недоступен для прозрачного доступа к удаленному интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="f05eb-119">In this case, the interface definition can be used for local calls as well as remote calls because **\[call\_as\]** allows an interface that can't be accessed remotely to be transparently mapped to a remote interface.</span></span> <span data-ttu-id="f05eb-120">Атрибут **\[ вызова \_ As \]** не может использоваться с режимом [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="f05eb-120">The **\[call\_as\]** attribute cannot be used with [**/osf**](-osf.md) mode.</span></span>

<span data-ttu-id="f05eb-121">Например, предположим, что для подпрограммы **F1** в интерфейсе объектов **IFace** требуется много преобразований между вызовами пользователя и фактически передаваемыми.</span><span class="sxs-lookup"><span data-stu-id="f05eb-121">For example, assume that the routine **f1** in object interface **IFace** requires numerous conversions between the user calls and what is actually transmitted.</span></span> <span data-ttu-id="f05eb-122">В следующих примерах описываются файлы IDL и ACF для интерфейса **IFace**.</span><span class="sxs-lookup"><span data-stu-id="f05eb-122">The following examples describe the IDL and ACF files for interface **IFace**:</span></span>

<span data-ttu-id="f05eb-123">В IDL-файле для интерфейса **IFace**:</span><span class="sxs-lookup"><span data-stu-id="f05eb-123">In the IDL file for interface **IFace**:</span></span>

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

<span data-ttu-id="f05eb-124">В ACF для интерфейса **IFace**:</span><span class="sxs-lookup"><span data-stu-id="f05eb-124">In the ACF for interface **IFace**:</span></span>

``` syntax
[call_as( f1 )] Remf1();
```

<span data-ttu-id="f05eb-125">В результате созданный файл заголовка определяет интерфейс с помощью определения **F1**, но также предоставляет заглушки для **Remf1**.</span><span class="sxs-lookup"><span data-stu-id="f05eb-125">This causes the generated header file to define the interface using the definition of **f1**, yet it also provides stubs for **Remf1**.</span></span>

<span data-ttu-id="f05eb-126">Компилятор MIDL создаст следующую таблицу vtable в файле заголовка для интерфейса **IFace**:</span><span class="sxs-lookup"><span data-stu-id="f05eb-126">The MIDL compiler will generate the following Vtable in the header file for interface **IFace**:</span></span>

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

<span data-ttu-id="f05eb-127">Прокси на стороне клиента будет иметь стандартный созданный MIDL прокси для **Remf1**, а заглушка на стороне сервера для **Remf1** будет такой же, как и стандартная заглушка, созданная MIDL:</span><span class="sxs-lookup"><span data-stu-id="f05eb-127">The client-side proxy would then have a typical MIDL-generated proxy for **Remf1**, while the server side stub for **Remf1** would be the same as the typical MIDL-generated stub:</span></span>

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

<span data-ttu-id="f05eb-128">Затем два **\[ вызова \_ как \]** подпрограммы облигаций (на стороне клиента и на стороне сервера) должны быть закодированы вручную:</span><span class="sxs-lookup"><span data-stu-id="f05eb-128">Then, the two **\[call\_as\]** bond routines (client side and server side) must be manually coded:</span></span>

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

<span data-ttu-id="f05eb-129">Для объектных интерфейсов это прототипы подпрограмм облигаций.</span><span class="sxs-lookup"><span data-stu-id="f05eb-129">For object interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="f05eb-130">Для клиентской стороны:</span><span class="sxs-lookup"><span data-stu-id="f05eb-130">For client side:</span></span>

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

<span data-ttu-id="f05eb-131">Для серверной части:</span><span class="sxs-lookup"><span data-stu-id="f05eb-131">For server side:</span></span>

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

<span data-ttu-id="f05eb-132">Для необъектных интерфейсов это прототипы подпрограмм облигаций.</span><span class="sxs-lookup"><span data-stu-id="f05eb-132">For nonobject interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="f05eb-133">Для клиентской стороны:</span><span class="sxs-lookup"><span data-stu-id="f05eb-133">For client side:</span></span>

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

<span data-ttu-id="f05eb-134">Для серверной части:</span><span class="sxs-lookup"><span data-stu-id="f05eb-134">For server side:</span></span>

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a><span data-ttu-id="f05eb-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f05eb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05eb-136">**/осф**</span><span class="sxs-lookup"><span data-stu-id="f05eb-136">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="f05eb-137">**представлять \_ как**</span><span class="sxs-lookup"><span data-stu-id="f05eb-137">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="f05eb-138">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="f05eb-138">**transmit\_as**</span></span>](transmit-as.md)
</dt> </dl>

 

 




