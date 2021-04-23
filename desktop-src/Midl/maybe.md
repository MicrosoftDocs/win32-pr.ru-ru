---
title: возможно, атрибут
description: Ключевое слово \ возможно \ указывает, что вызов удаленной процедуры не требуется выполнять каждый раз, когда он вызывается и клиент не ждет ответа. Обратите внимание, что протокол \ возможно, не обеспечивает ни доставку, ни завершение вызова.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- возможно, атрибут MIDL
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068830"
---
# <a name="maybe-attribute"></a><span data-ttu-id="7efef-105">возможно, атрибут</span><span class="sxs-lookup"><span data-stu-id="7efef-105">maybe attribute</span></span>

<span data-ttu-id="7efef-106">Ключевое слово **\[ может \]** означать, что вызов удаленной процедуры не требуется выполнять каждый раз, когда он вызывается и клиент не ждет ответа.</span><span class="sxs-lookup"><span data-stu-id="7efef-106">The keyword **\[maybe\]** indicates that the remote procedure call does not need to execute every time it is called and the client does not expect a response.</span></span> <span data-ttu-id="7efef-107">Обратите внимание, что протокол, **\[ возможно \]** , не обеспечивает ни доставку, ни завершение вызова.</span><span class="sxs-lookup"><span data-stu-id="7efef-107">Note that the **\[maybe\]** protocol ensures neither delivery nor completion of the call.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="7efef-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7efef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7efef-109">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="7efef-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7efef-110">Задает список из нуля или нескольких атрибутов IDL, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="7efef-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="7efef-111">При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="7efef-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="7efef-112">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="7efef-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7efef-113">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7efef-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7efef-114">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="7efef-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7efef-115">Задает дополнительные атрибуты, которые будут применены к функции.</span><span class="sxs-lookup"><span data-stu-id="7efef-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="7efef-116">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="7efef-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="7efef-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="7efef-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="7efef-118">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="7efef-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7efef-119">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="7efef-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7efef-120">Указывает имя функции, к которой **\[ \] будет применен атрибут.**</span><span class="sxs-lookup"><span data-stu-id="7efef-120">Specifies the name of the function to which the **\[maybe\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="7efef-121">*params*</span><span class="sxs-lookup"><span data-stu-id="7efef-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="7efef-122">Список параметров функции.</span><span class="sxs-lookup"><span data-stu-id="7efef-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7efef-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7efef-123">Remarks</span></span>

<span data-ttu-id="7efef-124">Вызов с атрибутом с **\[ вероятностью \]** не может содержать выходные параметры и неявно является **\[** [](idempotent.md) **\]** вызовом идемпотентными.</span><span class="sxs-lookup"><span data-stu-id="7efef-124">A call with the **\[maybe\]** attribute cannot contain output parameters and is implicitly an **\[**[**idempotent**](idempotent.md)**\]** call.</span></span>

## <a name="see-also"></a><span data-ttu-id="7efef-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7efef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efef-126">**транслировать**</span><span class="sxs-lookup"><span data-stu-id="7efef-126">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="7efef-127">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="7efef-127">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="7efef-128">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="7efef-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




