---
title: атрибут error_status_t
description: '\_ \_ Ключевое слово Error Status t обозначает тип объекта, который содержит сведения о состоянии связи или состоянии сбоя.'
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t атрибута MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333584"
---
# <a name="error_status_t-attribute"></a><span data-ttu-id="e6d1c-104">\_атрибут состояния ошибки \_ t</span><span class="sxs-lookup"><span data-stu-id="e6d1c-104">error\_status\_t attribute</span></span>

<span data-ttu-id="e6d1c-105">Ключевое слово **Error \_ Status \_ t** обозначает тип объекта, который содержит сведения о состоянии связи или состоянии сбоя.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-105">The **error\_status\_t** keyword designates a type for an object that contains communication-status or fault-status information.</span></span>

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="e6d1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6d1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d1c-107">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="e6d1c-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d1c-108">Указывает ноль или более атрибутов функции ACF, таких как **\[** [**\_ состояние**](comm-status.md)связи **\]** , **\[** [**\_ состояние сбоя**](fault-status.md) **\]** или **\[** [**некод**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e6d1c-108">Specifies zero or more ACF function attributes, such as **\[**[**comm\_status**](comm-status.md)**\]**, **\[**[**fault\_status**](fault-status.md)**\]**, or **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="e6d1c-109">Атрибуты функции заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="e6d1c-110">К функции можно применить ноль или более атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="e6d1c-111">Несколько атрибутов функции разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-111">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e6d1c-112">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="e6d1c-112">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d1c-113">Указывает имя функции, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-113">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="e6d1c-114">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="e6d1c-114">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d1c-115">Задает атрибуты, которые применяются к параметру.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-115">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="e6d1c-116">Обратите внимание, что к параметру можно применить ноль, один или несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-116">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="e6d1c-117">Несколько атрибутов параметров разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-117">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="e6d1c-118">Атрибуты параметров заключаются в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="e6d1c-119">Атрибуты параметров IDL, такие как атрибуты направления, не допускаются в ACF.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-119">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span>

</dd> <dt>

<span data-ttu-id="e6d1c-120">*имя параметра*</span><span class="sxs-lookup"><span data-stu-id="e6d1c-120">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d1c-121">Задает параметр для функции, как определено в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-121">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="e6d1c-122">Каждый параметр функции должен быть указан в одной и той же последовательности, используя то же имя, которое определено в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-122">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6d1c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6d1c-123">Remarks</span></span>

<span data-ttu-id="e6d1c-124">Тип **\_ состояния ошибки \_ t** используется как часть архитектуры обработки исключений в IDL.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-124">The **error\_status\_t** type is used as a part of the exception handling architecture in IDL.</span></span> <span data-ttu-id="e6d1c-125">Этот тип сопоставляется с [**длинными**](long.md)целыми [**числами**](unsigned.md) .</span><span class="sxs-lookup"><span data-stu-id="e6d1c-125">This type maps to an [**unsigned**](unsigned.md) [**long**](long.md).</span></span> <span data-ttu-id="e6d1c-126">Приложения, которые перехватывают ситуации ошибок, имеют **\[** параметр [**out**](out-idl.md) **\]** или тип возвращаемого значения для процедуры, указанной как **\_ состояние ошибки \_ t**, и определяют **\_ состояние ошибки \_ t** с помощью **\[** атрибутов [**\_ состояния**](comm-status.md) связи **\]** или **\[** [**\_ состояния сбоя**](fault-status.md) **\]** в ACF.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-126">Applications that catch error situations have an **\[**[**out**](out-idl.md)**\]** parameter or a return type of a procedure specified as **error\_status\_t**, and qualify the **error\_status\_t** with the **\[**[**comm\_status**](comm-status.md)**\]** or **\[**[**fault\_status**](fault-status.md)**\]** attributes in the ACF.</span></span> <span data-ttu-id="e6d1c-127">Если параметр или тип возвращаемого значения не являются полными атрибутами **\[ \_ состояния \]** связи или **\[ \_ состояния \] сбоя** , параметр работает так, как если бы он был беззнаковым.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-127">If the parameter or return type was not qualified with the **\[comm\_status\]** or **\[fault\_status\]** attributes, then the parameter operates as though it were an unsigned long.</span></span>

<span data-ttu-id="e6d1c-128">Начиная с версии 2,0 компилятор MIDL создает заглушки, которые содержат правильную архитектуру обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-128">Beginning with version 2.0, the MIDL compiler generates stubs that contain the proper error handling architecture.</span></span> <span data-ttu-id="e6d1c-129">Однако более ранние версии компилятора MIDL обрабатывали параметр или возвращаемый тип **ошибки \_ \_ t** , как будто **\[** [**\_**](comm-status.md) **\]** **\[** были применены атрибуты состояния связи и [**\_ состояния сбоя**](fault-status.md) **\]** , даже если они не были.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-129">However, earlier versions of the MIDL compiler handled a parameter or return type of **error\_status\_t** as though the **\[**[**comm\_status**](comm-status.md)**\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes were applied, even if they were not.</span></span> <span data-ttu-id="e6d1c-130">В MIDL 2,0 или более поздней версии необходимо явным образом применить атрибуты **\[ \_ состояния \]** связи и **\[ \_ состояния \] сбоя** к параметру или процедуре в ACF.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-130">With MIDL 2.0 or later, you must explicitly apply the **\[comm\_status\]** and **\[fault\_status\]** attributes to the parameter or procedure in the ACF.</span></span>

<span data-ttu-id="e6d1c-131">Тип **ошибки \_ \_ t** является одним из предопределенных типов языка определения интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-131">The **error\_status\_t** type is one of the predefined types of the interface definition language.</span></span> <span data-ttu-id="e6d1c-132">Предопределенные типы могут отображаться в виде описателей типов в объявлениях [**typedef**](typedef.md) , в общих объявлениях и в деклараторах функций (как в функции-возвращаемом типе, так и в качестве описателей типа параметра).</span><span class="sxs-lookup"><span data-stu-id="e6d1c-132">Predefined types can appear as type specifiers in [**typedef**](typedef.md) declarations, in general declarations, and in function declarators (either as the function-return-type or as parameter-type specifiers).</span></span>

## <a name="see-also"></a><span data-ttu-id="e6d1c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6d1c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d1c-134">**\_состояние связи**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-134">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-135">**\_состояние сбоя**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-135">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-136">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="e6d1c-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-137">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-137">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-138">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-139">**определение**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-139">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-140">**без знака**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-140">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




