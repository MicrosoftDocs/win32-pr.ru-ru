---
title: int, атрибут
description: Ключевое слово int задает 32-разрядное целое число со знаком на 32-разрядных платформах. На 16-разрядных платформах ключевое слово int — это необязательное ключевое слово, которое может сопровождать ключевые слова небольшие, короткие и длинные.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- целочисленный атрибут MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783600"
---
# <a name="int-attribute"></a><span data-ttu-id="e18d4-105">int, атрибут</span><span class="sxs-lookup"><span data-stu-id="e18d4-105">int attribute</span></span>

<span data-ttu-id="e18d4-106">Ключевое слово **int** задает 32-разрядное целое число со знаком на 32-разрядных платформах.</span><span class="sxs-lookup"><span data-stu-id="e18d4-106">The keyword **int** specifies a 32-bit signed integer on 32-bit platforms.</span></span> <span data-ttu-id="e18d4-107">На 16-разрядных платформах ключевое слово **int** — это необязательное ключевое слово, которое может сопровождать ключевые слова [**небольшие**](small.md), [**короткие**](short.md)и [**длинные**](long.md).</span><span class="sxs-lookup"><span data-stu-id="e18d4-107">On 16-bit platforms, the keyword **int** is an optional keyword that can accompany the keywords [**small**](small.md), [**short**](short.md), and [**long**](long.md).</span></span>

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="e18d4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e18d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e18d4-109">*Модификатор Integer-*</span><span class="sxs-lookup"><span data-stu-id="e18d4-109">*integer-modifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e18d4-110">Указывает ключевое слово [**малый**](small.md), [**короткий**](short.md), [**длинный**](long.md), [**Hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)или [**\_ \_ Int64**](--int64.md), которое выбирает размер целочисленных данных.</span><span class="sxs-lookup"><span data-stu-id="e18d4-110">Specifies the keyword [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_\_int3264**](--int3264.md), or [**\_\_int64**](--int64.md),which selects the size of the integer data.</span></span> <span data-ttu-id="e18d4-111">На 16-разрядных платформах должен присутствовать квалификатор size.</span><span class="sxs-lookup"><span data-stu-id="e18d4-111">On 16-bit platforms, the size qualifier must be present.</span></span>

</dd> <dt>

<span data-ttu-id="e18d4-112">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="e18d4-112">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e18d4-113">Указывает один или несколько стандартных деклараторов C, таких как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="e18d4-113">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e18d4-114">(Деклараторы функций и объявления битовых полей не допускаются в структурах, передаваемых в удаленных вызовах процедур.</span><span class="sxs-lookup"><span data-stu-id="e18d4-114">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="e18d4-115">Эти деклараторы разрешены в структурах, которые не передаются.) Несколько деклараторов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="e18d4-115">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e18d4-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e18d4-116">Remarks</span></span>

<span data-ttu-id="e18d4-117">Целочисленные типы являются базовыми типами языка определения интерфейса (IDL).</span><span class="sxs-lookup"><span data-stu-id="e18d4-117">Integer types are among the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="e18d4-118">Они могут отображаться в виде описателей типа в объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора типа "функция-возврат" и спецификатора типа параметра).</span><span class="sxs-lookup"><span data-stu-id="e18d4-118">They can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="e18d4-119">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="e18d4-119">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="e18d4-120">Если нет ни одной спецификации целочисленных знаков, целочисленный тип по умолчанию [**имеет значение signed.**](signed.md)</span><span class="sxs-lookup"><span data-stu-id="e18d4-120">If no integer sign specification is provided, the integer type defaults to [**signed**](signed.md).</span></span>

<span data-ttu-id="e18d4-121">Компиляторы DCE IDL не разрешают ключевому слову [**Sign, чтобы**](signed.md) указать знак целочисленных типов.</span><span class="sxs-lookup"><span data-stu-id="e18d4-121">DCE IDL compilers do not allow the keyword [**signed**](signed.md) to specify the sign of integer types.</span></span> <span data-ttu-id="e18d4-122">Поэтому эта функция недоступна при использовании параметра компилятора MIDL [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="e18d4-122">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="e18d4-123">Корпорация Майкрософт не рекомендует использовать \_ \_ int3264 для удаленного взаимодействия, если это можно избежать.</span><span class="sxs-lookup"><span data-stu-id="e18d4-123">Microsoft does not recommend the use of \_\_int3264 for remoting if it can be avoided.</span></span> <span data-ttu-id="e18d4-124">Дополнительные сведения об использовании и ограничениях см. в разделе [**\_ \_ int3264**](--int3264.md) .</span><span class="sxs-lookup"><span data-stu-id="e18d4-124">Please see the topic on [**\_\_int3264**](--int3264.md) for more information regarding it's use and limitations.</span></span>

## <a name="examples"></a><span data-ttu-id="e18d4-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="e18d4-125">Examples</span></span>

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a><span data-ttu-id="e18d4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e18d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18d4-127">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="e18d4-127">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e18d4-128">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="e18d4-128">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e18d4-129">**Hyper**</span><span class="sxs-lookup"><span data-stu-id="e18d4-129">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="e18d4-130">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="e18d4-130">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e18d4-131">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="e18d4-131">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="e18d4-132">**/осф**</span><span class="sxs-lookup"><span data-stu-id="e18d4-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="e18d4-133">**short**</span><span class="sxs-lookup"><span data-stu-id="e18d4-133">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="e18d4-134">**входил**</span><span class="sxs-lookup"><span data-stu-id="e18d4-134">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="e18d4-135">**значительные**</span><span class="sxs-lookup"><span data-stu-id="e18d4-135">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="e18d4-136">**struct**</span><span class="sxs-lookup"><span data-stu-id="e18d4-136">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e18d4-137">**определение**</span><span class="sxs-lookup"><span data-stu-id="e18d4-137">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="e18d4-138">**наборов**</span><span class="sxs-lookup"><span data-stu-id="e18d4-138">**union**</span></span>](union.md)
</dt> </dl>

 

 




