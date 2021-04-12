---
title: Enum, атрибут
description: Ключевое слово enum определяет перечисляемый тип.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- атрибут перечисления MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333587"
---
# <a name="enum-attribute"></a><span data-ttu-id="2edc3-104">Enum, атрибут</span><span class="sxs-lookup"><span data-stu-id="2edc3-104">enum attribute</span></span>

<span data-ttu-id="2edc3-105">Ключевое слово **enum** определяет перечисляемый тип.</span><span class="sxs-lookup"><span data-stu-id="2edc3-105">The keyword **enum** identifies an enumerated type.</span></span>

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a><span data-ttu-id="2edc3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2edc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2edc3-107">*тегами*</span><span class="sxs-lookup"><span data-stu-id="2edc3-107">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="2edc3-108">Задает необязательный тег для перечисляемого типа.</span><span class="sxs-lookup"><span data-stu-id="2edc3-108">Specifies an optional tag for the enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="2edc3-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="2edc3-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="2edc3-110">Указывает конкретное перечисление.</span><span class="sxs-lookup"><span data-stu-id="2edc3-110">Specifies the particular enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="2edc3-111">*Целочисленное значение*</span><span class="sxs-lookup"><span data-stu-id="2edc3-111">*integer-value*</span></span> 
</dt> <dd>

<span data-ttu-id="2edc3-112">Задает Постоянное целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="2edc3-112">Specifies a constant integer value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2edc3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2edc3-113">Remarks</span></span>

<span data-ttu-id="2edc3-114">типы **перечисления** могут отображаться в виде описателей типов в объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (как функция-Return-Type или как спецификатор типа параметра).</span><span class="sxs-lookup"><span data-stu-id="2edc3-114">**enum** types can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (either as the function-return-type or as a parameter-type specifier).</span></span> <span data-ttu-id="2edc3-115">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="2edc3-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="2edc3-116">В режиме по умолчанию компилятора MIDL можно присвоить целочисленные значения перечислителям.</span><span class="sxs-lookup"><span data-stu-id="2edc3-116">In the MIDL compiler's default mode, you can assign integer values to enumerators.</span></span> <span data-ttu-id="2edc3-117">(Эта функция недоступна при компиляции с параметром [**/ОСФ**](-osf.md) .) Как и в случае с перечислителями языка C, имена перечислителей должны быть уникальными, но значения перечислителей не требуются.</span><span class="sxs-lookup"><span data-stu-id="2edc3-117">(This feature is not available when you compile with the [**/osf**](-osf.md) switch.) As with C-language enumerators, enumerator names must be unique, but the enumerator values need not be.</span></span>

<span data-ttu-id="2edc3-118">Если операторы присваивания не предоставлены, идентификаторы сопоставляются с последовательными целыми числами слева направо, начиная с нуля.</span><span class="sxs-lookup"><span data-stu-id="2edc3-118">When assignment operators are not provided, identifiers are mapped to consecutive integers from left to right, starting with zero.</span></span> <span data-ttu-id="2edc3-119">При указании операторов присваивания присвоенные значения начинаются с самого последнего присвоенного значения.</span><span class="sxs-lookup"><span data-stu-id="2edc3-119">When assignment operators are provided, assigned values start from the most recently assigned value.</span></span>

<span data-ttu-id="2edc3-120">Максимальное число идентификаторов — 65 535.</span><span class="sxs-lookup"><span data-stu-id="2edc3-120">The maximum number of identifiers is 65,535.</span></span>

<span data-ttu-id="2edc3-121">Объекты типа **enum** имеют тип [**int**](int.md) , а их размер зависит от системы.</span><span class="sxs-lookup"><span data-stu-id="2edc3-121">Objects of type **enum** are [**int**](int.md) types, and their size is system-dependent.</span></span> <span data-ttu-id="2edc3-122">По умолчанию объекты типов **enum** обрабатываются как 16-битовые объекты типа [**без знака**](unsigned.md) [**Short**](short.md) при передаче по сети.</span><span class="sxs-lookup"><span data-stu-id="2edc3-122">By default, objects of **enum** types are treated as 16-bit objects of type [**unsigned**](unsigned.md) [**short**](short.md) when transmitted over a network.</span></span> <span data-ttu-id="2edc3-123">Значения за пределами диапазона 0 – 32 767 приводят к тому, что значение перечисления RPC X исключения времени выполнения \_ \_ \_ \_ выходит за пределы \_ \_ диапазона.</span><span class="sxs-lookup"><span data-stu-id="2edc3-123">Values outside the range 0 - 32,767 cause the run-time exception RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="2edc3-124">Чтобы передать объекты как 32-разрядные сущности, примените **\[** атрибут [**\_ enum версии v1**](v1-enum.md) **\]** к typedef типа **enum** .</span><span class="sxs-lookup"><span data-stu-id="2edc3-124">To transmit objects as 32-bit entities, apply the **\[**[**v1\_enum**](v1-enum.md)**\]** attribute to the **enum** typedef.</span></span>

## <a name="examples"></a><span data-ttu-id="2edc3-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="2edc3-125">Examples</span></span>

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a><span data-ttu-id="2edc3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2edc3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2edc3-127">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="2edc3-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2edc3-128">**INT**</span><span class="sxs-lookup"><span data-stu-id="2edc3-128">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="2edc3-129">**short**</span><span class="sxs-lookup"><span data-stu-id="2edc3-129">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="2edc3-130">**определение**</span><span class="sxs-lookup"><span data-stu-id="2edc3-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="2edc3-131">**без знака**</span><span class="sxs-lookup"><span data-stu-id="2edc3-131">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="2edc3-132">**\_перечисление v1**</span><span class="sxs-lookup"><span data-stu-id="2edc3-132">**v1\_enum**</span></span>](v1-enum.md)
</dt> </dl>

 

 




