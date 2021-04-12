---
title: атрибут midl_user_allocate
description: '\_ \_ Функция пользовательского выделения MIDL — это функция, которую клиентские и серверные приложения предоставляют для выделения памяти.'
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate атрибута MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337377"
---
# <a name="midl_user_allocate-attribute"></a><span data-ttu-id="ee57f-104">\_Пользовательский \_ атрибут пользовательского выделения MIDL</span><span class="sxs-lookup"><span data-stu-id="ee57f-104">midl\_user\_allocate attribute</span></span>

<span data-ttu-id="ee57f-105">Функция **\_ пользовательского \_ выделения MIDL** — это функция, которую клиентские и серверные приложения предоставляют для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="ee57f-105">The **midl\_user\_allocate** function is a function that client and server applications provide to allocate memory.</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a><span data-ttu-id="ee57f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee57f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee57f-107">*кбитес*</span><span class="sxs-lookup"><span data-stu-id="ee57f-107">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="ee57f-108">Указывает число байтов для выделения.</span><span class="sxs-lookup"><span data-stu-id="ee57f-108">Specifies the count of bytes to allocate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee57f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee57f-109">Remarks</span></span>

<span data-ttu-id="ee57f-110">Как клиентские приложения, так и серверные приложения должны реализовывать функцию **\_ пользовательского \_ выделения MIDL** , если только компиляция не выполняется в режиме использование-Compatibility ([**/ОСФ**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="ee57f-110">Both client applications and server applications must implement the **midl\_user\_allocate** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="ee57f-111">Приложения и созданные заглушки **вызывают \_ \_ выделять пользователя MIDL** при работе с объектами, на которые ссылаются указатели:</span><span class="sxs-lookup"><span data-stu-id="ee57f-111">Applications and generated stubs call **midl\_user\_allocate** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="ee57f-112">Серверное приложение должно вызывать **метод \_ MIDL \_ ,** чтобы выделить память для приложения € (например, при создании нового узла).</span><span class="sxs-lookup"><span data-stu-id="ee57f-112">The server application should call **midl\_user\_allocate** to allocate memory for the applicationâ€”for example, when creating a new node.</span></span>
-   <span data-ttu-id="ee57f-113">Заглушка сервера вызывает метод **MIDL, \_ \_ выделяющий пользователя** при демаршалировании данных, указывающих на адресное пространство сервера.</span><span class="sxs-lookup"><span data-stu-id="ee57f-113">The server stub calls **midl\_user\_allocate** when unmarshaling pointed-at data into the server address space.</span></span>
-   <span data-ttu-id="ee57f-114">Клиентская заглушка вызывает метод **MIDL, \_ \_ выделяющий пользователя** при демаршалировании данных с сервера, на который ссылается указатель [**out**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="ee57f-114">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an [**out**](out-idl.md) pointer.</span></span> <span data-ttu-id="ee57f-115">Обратите внимание, что для **\[** [**в**](in.md) **\]** , **\[ \]** и **\[** [**уникальных**](unique.md) **\]** указателей клиентская заглушка вызывает метод **MIDL \_ User, \_ выделяющий** , только если значение **\[ уникального \]** указателя было **равно NULL** во входных данных и при вызове изменяется значение, отличное от **null** .</span><span class="sxs-lookup"><span data-stu-id="ee57f-115">Note that for **\[**[**in**](in.md)**\]**, **\[out\]**, and **\[**[**unique**](unique.md)**\]** pointers, the client stub calls **midl\_user\_allocate** only if the **\[unique\]** pointer value was **NULL** on input and changes to a non-**NULL** value during the call.</span></span> <span data-ttu-id="ee57f-116">Если во входных данных для **\[ \] уникального** указателя задано значение, отличное от **null** , клиентская заглушка записывает связанные данные в существующую память.</span><span class="sxs-lookup"><span data-stu-id="ee57f-116">If the **\[unique\]** pointer was non-**NULL** on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="ee57f-117">Если **\_ пользователю MIDL \_** не удается выделить память, он должен вернуть **пустой** указатель.</span><span class="sxs-lookup"><span data-stu-id="ee57f-117">If **midl\_user\_allocate** fails to allocate memory, it must return a **NULL** pointer.</span></span>

<span data-ttu-id="ee57f-118">Рекомендуется, чтобы пользователь MIDL возвращал указатель, **\_ \_ выделяющий** по 8 байт.</span><span class="sxs-lookup"><span data-stu-id="ee57f-118">It is recommended that **midl\_user\_allocate** return a pointer that is 8 bytes aligned.</span></span>

## <a name="examples"></a><span data-ttu-id="ee57f-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="ee57f-119">Examples</span></span>


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a><span data-ttu-id="ee57f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee57f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee57f-121">**allocate**</span><span class="sxs-lookup"><span data-stu-id="ee57f-121">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="ee57f-122">**массивы**</span><span class="sxs-lookup"><span data-stu-id="ee57f-122">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="ee57f-123">Массивы и указатели</span><span class="sxs-lookup"><span data-stu-id="ee57f-123">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="ee57f-124">Атрибуты массива и Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="ee57f-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee57f-125">**окне**</span><span class="sxs-lookup"><span data-stu-id="ee57f-125">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="ee57f-126">**\_бесплатный пользователь \_ MIDL**</span><span class="sxs-lookup"><span data-stu-id="ee57f-126">**midl\_user\_free**</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="ee57f-127">**/осф**</span><span class="sxs-lookup"><span data-stu-id="ee57f-127">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="ee57f-128">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="ee57f-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="ee57f-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="ee57f-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="ee57f-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="ee57f-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="ee57f-131">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="ee57f-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 