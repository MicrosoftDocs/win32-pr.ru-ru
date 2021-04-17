---
title: атрибут force_allocate
description: Атрибут ACF \ принудительное \_ выделение \ принудительное выделение параметра указателя с помощью \_ пользовательского выделения MIDL \_ вместо оптимизации выделения.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate атрибута MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487584"
---
# <a name="force_allocate-attribute"></a><span data-ttu-id="61220-104">принудительное \_ выделение атрибута</span><span class="sxs-lookup"><span data-stu-id="61220-104">force\_allocate attribute</span></span>

<span data-ttu-id="61220-105">При принудительном выделении атрибут ACF принудительно выделяется \[ **\_** \] параметр указателя с помощью функции [**\_ \_ выделения пользователя MIDL**](midl-user-allocate-1.md) вместо оптимизации выделения.</span><span class="sxs-lookup"><span data-stu-id="61220-105">The ACF attribute \[**force\_allocate**\] forces a pointer parameter to be allocated using [**midl\_user\_allocate**](midl-user-allocate-1.md) instead of optimizing away the allocation.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a><span data-ttu-id="61220-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61220-106">Parameters</span></span>

<span data-ttu-id="61220-107">Этот атрибут не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="61220-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="61220-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61220-108">Remarks</span></span>

<span data-ttu-id="61220-109">RPC пытается сокращать выделение памяти на сервере, указывая указатели на внутренние буферы памяти.</span><span class="sxs-lookup"><span data-stu-id="61220-109">RPC attempts to minimize memory allocations on the server by supplying pointers to internal memory buffers.</span></span> <span data-ttu-id="61220-110">Такой подход может вызвать проблемы в приложениях, которые пытаются напрямую вызвать непосредственный [**\_ пользователь \_ MIDL**](midl-user-free-1.md) для указателей, предоставленных RPC, так как не удается освободить указатель, который был оптимизирован.</span><span class="sxs-lookup"><span data-stu-id="61220-110">This approach can cause problems for applications that attempt to directly call [**midl\_user\_free**](midl-user-free-1.md) on RPC-supplied pointers, because a pointer that has been optimized cannot be freed.</span></span> <span data-ttu-id="61220-111">Пометка параметра **\[ принудительным \_ выделением \]** позволит предотвратить эту оптимизацию для всех указателей, производных от него.</span><span class="sxs-lookup"><span data-stu-id="61220-111">Marking a parameter with **\[force\_allocate\]** will prevent this optimization for all pointers deriving it.</span></span>

<span data-ttu-id="61220-112">Другим распространенным применением **\[ принудительного \_ выделения \]** является обеспечение выравнивания памяти, на которую указывает, если приложению требуется выравнивание, превышающее размер памяти, на которую указывает.</span><span class="sxs-lookup"><span data-stu-id="61220-112">Another common use for **\[force\_allocate\]** is to guarantee the alignment of the memory being pointed to if an application requires an alignment greater than that of the memory pointed to.</span></span> <span data-ttu-id="61220-113">Например, приложения часто передают данные в универсальном массиве байтов вместо фактического типа, но байт гарантированно выравнивается только по 1, что может вызвать проблемы для приложений, которые предполагают более крупное выравнивание.</span><span class="sxs-lookup"><span data-stu-id="61220-113">For example, applications often pass data in a generic array of bytes rather than using the actual type, but a byte is only guaranteed to be aligned at 1, which may cause problems for applications that assume a larger alignment.</span></span> <span data-ttu-id="61220-114">Пометив параметр **\[ принудительным \_ выделением \]**, приложение может гарантировать, что вся память, на которую указывает, будет иметь выравнивание, равное значению, гарантированному [**\_ \_ выделять пользователем MIDL**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="61220-114">By marking the parameter with **\[force\_allocate\]**, the application can guarantee all memory pointed to will have an alignment equal to that guaranteed by [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span>

## <a name="examples"></a><span data-ttu-id="61220-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="61220-115">Examples</span></span>

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a><span data-ttu-id="61220-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61220-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61220-117">Предотвращение скрытия информации</span><span class="sxs-lookup"><span data-stu-id="61220-117">Avoiding Information Hiding</span></span>](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[<span data-ttu-id="61220-118">Проектирование интерфейсов, совместимых с 64-bit</span><span class="sxs-lookup"><span data-stu-id="61220-118">Designing 64-bit-Compatible Interfaces</span></span>](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[<span data-ttu-id="61220-119">**\_пользовательское \_ выделение MIDL**</span><span class="sxs-lookup"><span data-stu-id="61220-119">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="61220-120">**\_бесплатный пользователь \_ MIDL**</span><span class="sxs-lookup"><span data-stu-id="61220-120">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="61220-121">**allocate**</span><span class="sxs-lookup"><span data-stu-id="61220-121">**allocate**</span></span>](allocate.md)
</dt> </dl>

 

 