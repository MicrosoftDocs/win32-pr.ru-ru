---
title: пропустить атрибут
description: Атрибут \ Ignore \ указывает, что указатель, содержащийся в структуре или объединении, и на объект, указанный указателем, не передается. Атрибут \ Ignore \ ограничен элементами-указателями структур или объединений.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- игнорировать атрибут MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890513"
---
# <a name="ignore-attribute"></a><span data-ttu-id="8b6db-105">пропустить атрибут</span><span class="sxs-lookup"><span data-stu-id="8b6db-105">ignore attribute</span></span>

<span data-ttu-id="8b6db-106">Атрибут **\[ Ignore \]** указывает, что указатель, содержащийся в структуре или объединении, и на объект, указанный указателем, не передается.</span><span class="sxs-lookup"><span data-stu-id="8b6db-106">The **\[ignore\]** attribute designates that a pointer contained in a structure or union and the object indicated by the pointer is not transmitted.</span></span> <span data-ttu-id="8b6db-107">Атрибут **\[ Ignore \]** ограничен элементами-указателями структур или объединений.</span><span class="sxs-lookup"><span data-stu-id="8b6db-107">The **\[ignore\]** attribute is restricted to pointer members of structures or unions.</span></span>

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a><span data-ttu-id="8b6db-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b6db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b6db-109">*pointer-член-тип*</span><span class="sxs-lookup"><span data-stu-id="8b6db-109">*pointer-member-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8b6db-110">Задает тип элемента указателя структуры или объединения.</span><span class="sxs-lookup"><span data-stu-id="8b6db-110">Specifies the type of the pointer member of the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="8b6db-111">*имя указателя*</span><span class="sxs-lookup"><span data-stu-id="8b6db-111">*pointer-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8b6db-112">Задает имя элемента указателя, который должен игнорироваться во время маршалирования.</span><span class="sxs-lookup"><span data-stu-id="8b6db-112">Specifies the name of the pointer member that is to be ignored during marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b6db-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b6db-113">Remarks</span></span>

<span data-ttu-id="8b6db-114">Значение элемента структуры с атрибутом **\[ Ignore \]** не определено в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="8b6db-114">The value of a structure member with the **\[ignore\]** attribute is undefined at the destination.</span></span> <span data-ttu-id="8b6db-115">Параметр **\[** [**in**](in.md) **\]** не определен на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8b6db-115">An **\[**[**in**](in.md)**\]** parameter is not defined at the remote computer.</span></span> <span data-ttu-id="8b6db-116">Параметр **\[** [**out**](out-idl.md) **\]** не определен на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8b6db-116">An **\[**[**out**](out-idl.md)**\]** parameter is not defined at the local computer.</span></span>

<span data-ttu-id="8b6db-117">Атрибут **\[ Ignore \]** позволяет предотвратить передачу данных.</span><span class="sxs-lookup"><span data-stu-id="8b6db-117">The **\[ignore\]** attribute allows you to prevent transmission of data.</span></span> <span data-ttu-id="8b6db-118">Это полезно в таких ситуациях, как список с двойным связыванием.</span><span class="sxs-lookup"><span data-stu-id="8b6db-118">This is useful in situations such as a double-linked list.</span></span> <span data-ttu-id="8b6db-119">В следующем примере представлен список с двойным связыванием, в котором вводятся псевдонимы данных.</span><span class="sxs-lookup"><span data-stu-id="8b6db-119">The following example includes a double-linked list that introduces data aliasing:</span></span>

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

<span data-ttu-id="8b6db-120">Присвоение псевдонимов происходит в предыдущем примере, так как та же область памяти доступна из двух различных указателей в функции **p** и **p->Next->**.</span><span class="sxs-lookup"><span data-stu-id="8b6db-120">Aliasing occurs in the preceding example because the same memory area is available from two different pointers in the function **p** and **p->next->previous**.</span></span>

<span data-ttu-id="8b6db-121">Обратите внимание, что **\[ Ignore \]** не может использоваться в качестве атрибута типа.</span><span class="sxs-lookup"><span data-stu-id="8b6db-121">Note that **\[ignore\]** cannot be used as a type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="8b6db-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="8b6db-122">Examples</span></span>

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="8b6db-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b6db-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b6db-124">Атрибуты массива и Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="8b6db-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b6db-125">**массивы**</span><span class="sxs-lookup"><span data-stu-id="8b6db-125">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="8b6db-126">Массивы и указатели</span><span class="sxs-lookup"><span data-stu-id="8b6db-126">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="8b6db-127">**окне**</span><span class="sxs-lookup"><span data-stu-id="8b6db-127">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="8b6db-128">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="8b6db-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="8b6db-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="8b6db-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="8b6db-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="8b6db-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="8b6db-131">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="8b6db-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 