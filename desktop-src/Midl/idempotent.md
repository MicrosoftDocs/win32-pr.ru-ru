---
title: атрибут идемпотентными
description: Атрибут \ идемпотентными \ указывает, что операция не изменяет сведения о состоянии и возвращает одинаковые результаты при каждом выполнении. Выполнение подпрограммы более одного раза оказывает тот же результат, что и однократное выполнение.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- атрибут идемпотентными MIDL
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532603"
---
# <a name="idempotent-attribute"></a><span data-ttu-id="025e2-105">атрибут идемпотентными</span><span class="sxs-lookup"><span data-stu-id="025e2-105">idempotent attribute</span></span>

<span data-ttu-id="025e2-106">Атрибут **\[ идемпотентными \]** указывает, что операция не изменяет сведения о состоянии и возвращает одинаковые результаты при каждом выполнении.</span><span class="sxs-lookup"><span data-stu-id="025e2-106">The **\[idempotent\]** attribute specifies that an operation does not modify state information and returns the same results each time it is performed.</span></span> <span data-ttu-id="025e2-107">Выполнение подпрограммы более одного раза оказывает тот же результат, что и однократное выполнение.</span><span class="sxs-lookup"><span data-stu-id="025e2-107">Performing the routine more than once has the same effect as performing it once.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="025e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="025e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="025e2-109">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="025e2-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="025e2-110">Задает список из нуля или нескольких атрибутов IDL, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="025e2-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="025e2-111">При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="025e2-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="025e2-112">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="025e2-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="025e2-113">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="025e2-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="025e2-114">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="025e2-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="025e2-115">Задает дополнительные атрибуты, которые будут применены к функции.</span><span class="sxs-lookup"><span data-stu-id="025e2-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="025e2-116">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="025e2-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="025e2-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="025e2-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="025e2-118">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="025e2-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="025e2-119">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="025e2-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="025e2-120">Указывает имя функции, к которой будет применен атрибут **\[ идемпотентными \]** .</span><span class="sxs-lookup"><span data-stu-id="025e2-120">Specifies the name of the function to which the **\[idempotent\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="025e2-121">*params*</span><span class="sxs-lookup"><span data-stu-id="025e2-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="025e2-122">Список параметров функции.</span><span class="sxs-lookup"><span data-stu-id="025e2-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="025e2-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="025e2-123">Remarks</span></span>

<span data-ttu-id="025e2-124">RPC поддерживает два типа семантики удаленного вызова: вызовы операций с атрибутом **\[ идемпотентными \]** и вызовы операций (*идемпотентными* Operations) без атрибута **\[ идемпотентными \]** (операции,*не связанные с идемпотентными* ).</span><span class="sxs-lookup"><span data-stu-id="025e2-124">RPC supports two types of remote call semantics: calls to operations with the **\[idempotent\]** attribute and calls to operations (*idempotent* operations) without the **\[idempotent\]** attribute (*non-idempotent* operations).</span></span> <span data-ttu-id="025e2-125">Операция идемпотентными может быть выполнена более одного раза без некорректного воздействия.</span><span class="sxs-lookup"><span data-stu-id="025e2-125">An idempotent operation can be carried out more than once with no ill effect.</span></span> <span data-ttu-id="025e2-126">И наоборот, операция, не относящаяся к идемпотентными, не может быть выполнена несколько раз, поскольку она будет возвращать разные результаты каждый раз или из-за того, что она изменяет какое-либо состояние.</span><span class="sxs-lookup"><span data-stu-id="025e2-126">Conversely, a non-idempotent operation cannot be executed more than once because it will either return different results each time or because it modifies some state.</span></span>

<span data-ttu-id="025e2-127">Чтобы обеспечить автоматическое повторное выполнение процедуры, если вызов не завершен, используйте атрибут **\[ идемпотентными \]** .</span><span class="sxs-lookup"><span data-stu-id="025e2-127">To ensure that a procedure is automatically re-executed if the call does not complete, use the **\[idempotent\]** attribute.</span></span> <span data-ttu-id="025e2-128">Если атрибуты **\[ идемпотентными \]**, **\[** [**Broadcast**](broadcast.md) **\]** или может отсутствовать **\[** [](maybe.md) **\]** , процедура по умолчанию будет использовать семантику, отличную от идемпотентными.</span><span class="sxs-lookup"><span data-stu-id="025e2-128">If the **\[idempotent\]**, **\[**[**broadcast**](broadcast.md)**\]**, or **\[**[**maybe**](maybe.md)**\]** attributes are not present, the procedure will use non-idempotent semantics by default.</span></span> <span data-ttu-id="025e2-129">В этом случае операция выполняется только один раз.</span><span class="sxs-lookup"><span data-stu-id="025e2-129">In this case, the operation is executed only once.</span></span>

## <a name="see-also"></a><span data-ttu-id="025e2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="025e2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="025e2-131">**транслировать**</span><span class="sxs-lookup"><span data-stu-id="025e2-131">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="025e2-132">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="025e2-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="025e2-133">**Ну**</span><span class="sxs-lookup"><span data-stu-id="025e2-133">**maybe**</span></span>](maybe.md)
</dt> </dl>

 

 




