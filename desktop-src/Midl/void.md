---
title: атрибут void
description: Базовый тип void указывает на процедуру без аргументов или процедуру, которая не возвращает результирующее значение.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- void Attribute, MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105661667"
---
# <a name="void-attribute"></a><span data-ttu-id="c82d9-104">атрибут void</span><span class="sxs-lookup"><span data-stu-id="c82d9-104">void attribute</span></span>

<span data-ttu-id="c82d9-105">Базовый тип **void** указывает на процедуру без аргументов или процедуру, которая не возвращает результирующее значение.</span><span class="sxs-lookup"><span data-stu-id="c82d9-105">The base type **void** indicates a procedure with no arguments or a procedure that does not return a result value.</span></span>

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="c82d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c82d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c82d9-107">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="c82d9-107">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c82d9-108">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="c82d9-108">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="c82d9-109">*parameter-list*</span><span class="sxs-lookup"><span data-stu-id="c82d9-109">*parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c82d9-110">Указывает список параметров, передаваемых в функцию вместе со связанными типами параметров и атрибутами параметров.</span><span class="sxs-lookup"><span data-stu-id="c82d9-110">Specifies the list of parameters passed to the function along with the associated parameter types and parameter attributes.</span></span>

</dd> <dt>

<span data-ttu-id="c82d9-111">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="c82d9-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c82d9-112">Указывает имя типа, возвращаемого функцией.</span><span class="sxs-lookup"><span data-stu-id="c82d9-112">Specifies the name of the type returned by the function.</span></span>

</dd> <dt>

<span data-ttu-id="c82d9-113">*Контекстный-Handle-тип*</span><span class="sxs-lookup"><span data-stu-id="c82d9-113">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c82d9-114">Указывает имя типа, который принимает **\[** атрибут [**\_ Handle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="c82d9-114">Specifies the name of the type that takes the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c82d9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c82d9-115">Remarks</span></span>

<span data-ttu-id="c82d9-116">Тип указателя **void \***, который в C описывает универсальный указатель, который может быть приведен для представления любого типа указателя, ограничен в MIDL для его использования с ключевым словом **\[ \_ Handle \] context** .</span><span class="sxs-lookup"><span data-stu-id="c82d9-116">The pointer type **void \***, which in C describes a generic pointer that can be cast to represent any pointer type, is limited in MIDL to its use with the **\[context\_handle\]** keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="c82d9-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="c82d9-117">Examples</span></span>

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a><span data-ttu-id="c82d9-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c82d9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c82d9-119">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="c82d9-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="c82d9-120">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="c82d9-120">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="c82d9-121">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="c82d9-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




