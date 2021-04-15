---
title: атрибут partial_ignore
description: Атрибут ACF \ partial \_ Ignore \ определяет специальную версию \ Unique \ указатели, которая предоставляет необязательную семантику.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore атрибута MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411921"
---
# <a name="partial_ignore-attribute"></a><span data-ttu-id="b131d-104">атрибут частичного \_ игнорирования</span><span class="sxs-lookup"><span data-stu-id="b131d-104">partial\_ignore attribute</span></span>

<span data-ttu-id="b131d-105">Атрибут ACF **\[ partial \_ Ignore \]** определяет специальную версию **\[ уникальных \]** указателей, которая предоставляет необязательную семантику.</span><span class="sxs-lookup"><span data-stu-id="b131d-105">The ACF attribute **\[partial\_ignore\]** defines a specialized version of **\[unique\]** pointers that provides optional-out semantics.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a><span data-ttu-id="b131d-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b131d-106">Remarks</span></span>

<span data-ttu-id="b131d-107">При создании функции обычно пользователи могут указывать **непустой** указатель на необязательные возвращаемые данные, часто называемые необязательным указателем.</span><span class="sxs-lookup"><span data-stu-id="b131d-107">When creating a function, it is common to allow users to specify a non-**NULL** pointer to optional return data, often referred to as an optional-out pointer.</span></span> <span data-ttu-id="b131d-108">Память, на которую указывает пользователь, обычно не требуется инициализировать.</span><span class="sxs-lookup"><span data-stu-id="b131d-108">The memory pointed to by the user is not typically required to be initialized.</span></span> <span data-ttu-id="b131d-109">Эта методика представляет проблему, если функция используется через RPC.</span><span class="sxs-lookup"><span data-stu-id="b131d-109">This technique represents a problem when the function is used over RPC.</span></span>

<span data-ttu-id="b131d-110">Если необязательный указатель является допустимым, но указывает на неинициализированные данные, RPC пытается маршалировать эти данные и отправить их на сервер, что может привести к сбою упаковки и прерыванию вызова.</span><span class="sxs-lookup"><span data-stu-id="b131d-110">If the optional-out pointer is valid, but points to uninitialized data, RPC attempts to marshal that data and send it to the server, which can cause the marshaling to fail and abort the call.</span></span> <span data-ttu-id="b131d-111">Даже в случае успешности упаковки на сервер отправляется потенциально большой объем бесполезным данных.</span><span class="sxs-lookup"><span data-stu-id="b131d-111">Even if the marshaling succeeds, a potentially large amount of useless data is sent to the server.</span></span>

<span data-ttu-id="b131d-112">Эти проблемы решаются путем пометки указателя как «как» **\[ , «out», «Unique», «частично \_ игнорировать \] »**.</span><span class="sxs-lookup"><span data-stu-id="b131d-112">These problems are solved by marking the pointer as **\[in, out, unique, partial\_ignore\]**.</span></span> <span data-ttu-id="b131d-113">Должны присутствовать все четыре атрибута.</span><span class="sxs-lookup"><span data-stu-id="b131d-113">All four attributes must be present.</span></span> <span data-ttu-id="b131d-114">Если на стороне клиента выполняется маршалирование **\[ частично \_ игнорируемого \]** указателя, то только данные, передаваемые на сервер, являются индикатором, который показывает, имеет ли указатель **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b131d-114">When a **\[partial\_ignore\]** pointer is marshaled on the client side, the only data sent to the server is an indicator showing whether the pointer is **NULL**.</span></span> <span data-ttu-id="b131d-115">Если указатель не имеет **значение NULL**, подпрограммы на стороне сервера получают допустимый указатель на блок памяти, инициализированный с нулями.</span><span class="sxs-lookup"><span data-stu-id="b131d-115">If the pointer is non-**NULL**, the server-side routine receives a valid pointer to a block of memory that has been initialized with zeros.</span></span> <span data-ttu-id="b131d-116">Если указатель имеет **значение NULL**, подпрограммы на стороне сервера получают **пустой** указатель.</span><span class="sxs-lookup"><span data-stu-id="b131d-116">If the pointer is **NULL**, the server-side routine receives a **NULL** pointer.</span></span>

<span data-ttu-id="b131d-117">В этом случае максимальный размер указателя должен быть хорошо определен во время компиляции или на основе входных параметров, так как сервер должен выделить место для расположения памяти, на которое указывает.</span><span class="sxs-lookup"><span data-stu-id="b131d-117">In this situation, the maximum size of the pointer must be well defined either at compile time or based on input parameters, because the server needs to allocate space for the memory location being pointed to.</span></span> <span data-ttu-id="b131d-118">Например, простой указатель на **\[ строку \]** не имеет хорошо определенного размера, так как строка неявно завершается символом NULL.</span><span class="sxs-lookup"><span data-stu-id="b131d-118">For example, a simple **\[string\]** pointer does not have a well defined size because the string is implicitly terminated by a NULL character.</span></span> <span data-ttu-id="b131d-119">В этом случае указание максимального размера строки путем добавления атрибута **\[ size \_ \]** приведет к правильному определению требований к размеру.</span><span class="sxs-lookup"><span data-stu-id="b131d-119">In this case, specifying the maximum size of the string by adding a **\[size\_is\]** attribute would achieve the well defined size requirement.</span></span>

## <a name="examples"></a><span data-ttu-id="b131d-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="b131d-120">Examples</span></span>

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a><span data-ttu-id="b131d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b131d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b131d-122">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="b131d-122">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




