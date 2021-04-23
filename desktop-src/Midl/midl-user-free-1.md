---
title: атрибут midl_user_free
description: '\_ \_ Функция пользовательского освобождения MIDL обеспечивается клиентскими и серверными приложениями для освобождения динамически выделяемой памяти.'
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free атрибута MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337164"
---
# <a name="midl_user_free-attribute"></a><span data-ttu-id="47a4a-104">\_свободный пользовательский \_ атрибут MIDL</span><span class="sxs-lookup"><span data-stu-id="47a4a-104">midl\_user\_free attribute</span></span>

<span data-ttu-id="47a4a-105">Функция **\_ пользовательского \_ освобождения MIDL** обеспечивается клиентскими и серверными приложениями для освобождения динамически выделяемой памяти.</span><span class="sxs-lookup"><span data-stu-id="47a4a-105">The **midl\_user\_free** function is provided by client and server applications to deallocate dynamically allocated memory.</span></span>

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a><span data-ttu-id="47a4a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47a4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47a4a-107">*ш*</span><span class="sxs-lookup"><span data-stu-id="47a4a-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="47a4a-108">Указатель на блок памяти, который должен быть освобожден.</span><span class="sxs-lookup"><span data-stu-id="47a4a-108">A pointer to the memory block to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47a4a-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47a4a-109">Remarks</span></span>

<span data-ttu-id="47a4a-110">Как клиентское приложение, так и серверное приложение должны реализовывать функцию **\_ пользовательского \_ освобождения MIDL** , если только компиляция не выполняется в режиме использование-Compatibility ([**/ОСФ**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="47a4a-110">Both client application and server application must implement the **midl\_user\_free** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="47a4a-111">Функция **\_ \_ бесплатного пользователя MIDL** должна иметь возможность освободить все хранилище, выделенное [**пользователем MIDL \_ \_**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="47a4a-111">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span>

<span data-ttu-id="47a4a-112">Приложения и заглушки **вызывают \_ \_ свободный пользователь MIDL** при работе с объектами, на которые ссылаются указатели:</span><span class="sxs-lookup"><span data-stu-id="47a4a-112">Applications and stubs call **midl\_user\_free** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="47a4a-113">Серверное приложение должно вызывать **MIDL- \_ пользователь \_** , чтобы освободить память, выделенную приложения €, например при удалении указанного узла.</span><span class="sxs-lookup"><span data-stu-id="47a4a-113">The server application should call **midl\_user\_free** to free memory allocated by the applicationâ€”for example, when deleting a specified node.</span></span>
-   <span data-ttu-id="47a4a-114">Заглушка сервера вызывает **функцию \_ MIDL \_ для освобождения** памяти на сервере после маршалирования всех **\[** аргументов [**out**](out-idl.md) **\]** , **\[** [**in**](in.md), **out \]** и возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="47a4a-114">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all **\[**[**out**](out-idl.md)**\]** arguments, **\[**[**in**](in.md), **out\]** arguments, and the return value.</span></span>

## <a name="examples"></a><span data-ttu-id="47a4a-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="47a4a-115">Examples</span></span>


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a><span data-ttu-id="47a4a-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47a4a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a4a-117">**массивы**</span><span class="sxs-lookup"><span data-stu-id="47a4a-117">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="47a4a-118">Массивы и указатели</span><span class="sxs-lookup"><span data-stu-id="47a4a-118">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="47a4a-119">Атрибуты массива и Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="47a4a-119">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="47a4a-120">**окне**</span><span class="sxs-lookup"><span data-stu-id="47a4a-120">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="47a4a-121">**\_пользовательское \_ выделение MIDL**</span><span class="sxs-lookup"><span data-stu-id="47a4a-121">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="47a4a-122">**/осф**</span><span class="sxs-lookup"><span data-stu-id="47a4a-122">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="47a4a-123">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="47a4a-123">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="47a4a-124">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="47a4a-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 