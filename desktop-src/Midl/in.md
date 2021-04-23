---
title: in - атрибут
description: Атрибут \ in \ указывает, что параметр передается из вызывающей процедуры в вызываемую процедуру.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- в атрибуте MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791376"
---
# <a name="in-attribute"></a><span data-ttu-id="ca06a-104">in - атрибут</span><span class="sxs-lookup"><span data-stu-id="ca06a-104">in attribute</span></span>

<span data-ttu-id="ca06a-105">Атрибут **\[ in \]** указывает, что параметр передается из вызывающей процедуры в вызываемую процедуру.</span><span class="sxs-lookup"><span data-stu-id="ca06a-105">The **\[in\]** attribute indicates that a parameter is to be passed from the calling procedure to the called procedure.</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="ca06a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca06a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca06a-107">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ca06a-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ca06a-108">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="ca06a-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="ca06a-109">Допустимыми атрибутами функций являются **\[ обратные вызовы \]**, **\[ локальные \]**, атрибуты указателя **\[ ref \]**, **\[ Unique \]** или **\[ ptr \]**, а также строка атрибутов использования, **\[ строковый \]** маркер **\[ \]** **\[ \_ \]**, атрибут Ignore и контекстный.</span><span class="sxs-lookup"><span data-stu-id="ca06a-109">Valid function attributes are **\[callback\]**, **\[local\]**, the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**, and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="ca06a-110">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="ca06a-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="ca06a-111">Задает **Базовый \_ тип**, [**структуру**](struct.md), [**объединение**](union.md)или тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="ca06a-111">Specifies a **base\_type**, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="ca06a-112">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="ca06a-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="ca06a-113">*декларатор указателя*</span><span class="sxs-lookup"><span data-stu-id="ca06a-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="ca06a-114">Указывает ноль или несколько деклараторов указателей.</span><span class="sxs-lookup"><span data-stu-id="ca06a-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="ca06a-115">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="ca06a-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca06a-116">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="ca06a-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ca06a-117">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="ca06a-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="ca06a-118">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="ca06a-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ca06a-119">Указывает ноль или более атрибутов, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="ca06a-119">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="ca06a-120">Атрибуты параметров с атрибутом **\[ in \]** также могут **\[ \] принимать атрибут направления, а атрибуты** Field **\[ \_ \] —**, **\[ Last \_ - \]**, **\[ length \_ — \]**, **\[ Max \_ — \]**, **\[ size \_ — \]** и **\[ \_ тип \] переключателя**; атрибут указателя **\[ ref \]**, **\[ Unique \]** или **\[ ptr \]**, а также **\[ \_ маркер \] контекста** атрибутов использования и **\[ строка \]**.</span><span class="sxs-lookup"><span data-stu-id="ca06a-120">Parameter attributes with the **\[in\]** attribute can also take the directional attribute **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]** and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="ca06a-121">Атрибут использования **\[ Ignore \]** не может использоваться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="ca06a-121">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="ca06a-122">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="ca06a-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ca06a-123">*declarator*</span><span class="sxs-lookup"><span data-stu-id="ca06a-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="ca06a-124">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="ca06a-124">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="ca06a-125">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="ca06a-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="ca06a-126">Декларатор параметра в деклараторе функции, например имя параметра, является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ca06a-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca06a-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca06a-127">Remarks</span></span>

<span data-ttu-id="ca06a-128">Атрибут **\[ in \]** имеет инверсный атрибут, **\[** [](out-idl.md) **\]** который указывает, что параметр должен возвращаться из вызванной процедуры в вызывающую процедуру.</span><span class="sxs-lookup"><span data-stu-id="ca06a-128">The **\[in\]** attribute has a converse attribute, **\[**[**out**](out-idl.md)**\]**, which indicates that a parameter is to be returned from the called procedure to the calling procedure.</span></span> <span data-ttu-id="ca06a-129">Атрибуты **\[ in \]** и **\[ out \]** называются атрибутами двунаправленного параметра, так как они указывают направление, в котором передаются параметры.</span><span class="sxs-lookup"><span data-stu-id="ca06a-129">The **\[in\]** and **\[out\]** attributes are known as directional parameter attributes because they specify the direction in which parameters are passed.</span></span> <span data-ttu-id="ca06a-130">Параметр может быть определен как **\[ in \]**, **\[ \] out** или **\[ in**. **\]**</span><span class="sxs-lookup"><span data-stu-id="ca06a-130">A parameter can be defined as **\[in\]**, **\[out\]**, or **\[in**, **out\]**.</span></span>

<span data-ttu-id="ca06a-131">Атрибут **\[ in \]** определяет параметры, которые маршалируются клиентской заглушкой для передачи на сервер.</span><span class="sxs-lookup"><span data-stu-id="ca06a-131">The **\[in\]** attribute identifies parameters that are marshaled by the client stub for transmission to the server.</span></span>

<span data-ttu-id="ca06a-132">Атрибут **\[ in \]** применяется к параметру по умолчанию, если не указан атрибут параметра Direction.</span><span class="sxs-lookup"><span data-stu-id="ca06a-132">The **\[in\]** attribute is applied to a parameter by default when no directional parameter attribute is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="ca06a-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="ca06a-133">Examples</span></span>

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a><span data-ttu-id="ca06a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca06a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca06a-135">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="ca06a-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ca06a-136">**\_пользовательское \_ выделение MIDL**</span><span class="sxs-lookup"><span data-stu-id="ca06a-136">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="ca06a-137">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="ca06a-137">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 