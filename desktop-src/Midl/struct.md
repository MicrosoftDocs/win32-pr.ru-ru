---
title: атрибут struct
description: Ключевое слово struct используется в спецификаторе типа структуры.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- атрибут структуры MIDL
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661713"
---
# <a name="struct-attribute"></a><span data-ttu-id="721b2-104">атрибут struct</span><span class="sxs-lookup"><span data-stu-id="721b2-104">struct attribute</span></span>

<span data-ttu-id="721b2-105">Ключевое слово **struct** используется в спецификаторе типа структуры.</span><span class="sxs-lookup"><span data-stu-id="721b2-105">The **struct** keyword is used in a structure type specifier.</span></span>

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="721b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="721b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="721b2-107">*Тег struct*</span><span class="sxs-lookup"><span data-stu-id="721b2-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="721b2-108">Указывает необязательный тег для структуры.</span><span class="sxs-lookup"><span data-stu-id="721b2-108">Specifies an optional tag for the structure.</span></span>

</dd> <dt>

<span data-ttu-id="721b2-109">*Список атрибутов Field*</span><span class="sxs-lookup"><span data-stu-id="721b2-109">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="721b2-110">Указывает ноль или более атрибутов полей, применимых к элементу структуры.</span><span class="sxs-lookup"><span data-stu-id="721b2-110">Specifies zero or more field attributes that apply to the structure member.</span></span> <span data-ttu-id="721b2-111">К допустимым атрибутам полей относятся: **\[** [**First \_**](first-is.md)—, **\]** **\[** [**Last \_ —**](last-is.md), **\]** **\[** [**length \_ —**](length-is.md) **\]** , **\[** [**Max \_ —**](max-is.md) **\]** , и **\[** [**size \_ —**](size-is.md) **\]** строка атрибутов использования **\[** [](string.md) **\]** и **\[** [**игнорируется**](ignore.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** , **\[** [**ptr**](ptr.md), **\]** и **\[** [**\_ Тип переключателя**](switch-type.md)атрибута Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="721b2-111">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="721b2-112">Несколько атрибутов полей разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="721b2-112">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="721b2-113">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="721b2-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="721b2-114">Задает [базовый тип](midl-base-types.md), **структуру**, [**объединение**](union.md)или тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="721b2-114">Specifies a [base type](midl-base-types.md), **struct**, [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="721b2-115">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="721b2-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="721b2-116">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="721b2-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="721b2-117">Указывает один или несколько стандартных деклараторов C, таких как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="721b2-117">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="721b2-118">(Деклараторы функций и объявления битовых полей не допускаются в структурах, передаваемых в удаленных вызовах процедур.</span><span class="sxs-lookup"><span data-stu-id="721b2-118">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="721b2-119">Эти деклараторы разрешены в структурах, которые не передаются.) Несколько деклараторов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="721b2-119">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="721b2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="721b2-120">Remarks</span></span>

<span data-ttu-id="721b2-121">Спецификатор типа структуры IDL, **Структура**, отличается от спецификатора стандартного типа C следующим образом:</span><span class="sxs-lookup"><span data-stu-id="721b2-121">The IDL structure type specifier, **struct**, differs from the standard C type specifier in the following ways:</span></span>

-   <span data-ttu-id="721b2-122">Каждый член структуры может быть связан с необязательными атрибутами поля, описывающими характеристики этого члена структуры в целях удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="721b2-122">Each structure member can be associated with optional field attributes that describe characteristics of that structure member for the purposes of a remote procedure call.</span></span>
-   <span data-ttu-id="721b2-123">Битовые поля и деклараторы функций не допускаются в структурах, используемых в удаленных вызовах процедур.</span><span class="sxs-lookup"><span data-stu-id="721b2-123">Bit fields and function declarators are not allowed in structures that are used in remote procedure calls.</span></span> <span data-ttu-id="721b2-124">Эти стандартные конструкции декларатора C могут использоваться только в том случае, если структура не передается в сети.</span><span class="sxs-lookup"><span data-stu-id="721b2-124">These standard C declarator constructs can be used only if the structure is not transmitted on the network.</span></span>

<span data-ttu-id="721b2-125">Чтобы обеспечить взаимодействие, форма структур должна быть одинаковой на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="721b2-125">The shape of structures must be the same across platforms to ensure interconnectivity.</span></span>

## <a name="examples"></a><span data-ttu-id="721b2-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="721b2-126">Examples</span></span>

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="721b2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="721b2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="721b2-128">**массивы**</span><span class="sxs-lookup"><span data-stu-id="721b2-128">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="721b2-129">Массивы и указатели</span><span class="sxs-lookup"><span data-stu-id="721b2-129">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="721b2-130">Атрибуты массива и Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="721b2-130">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="721b2-131">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="721b2-131">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="721b2-132">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="721b2-132">**/c\_ext**</span></span>](-c-ext.md)
</dt> <dt>

[<span data-ttu-id="721b2-133">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="721b2-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="721b2-134">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="721b2-134">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="721b2-135">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="721b2-135">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="721b2-136">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="721b2-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="721b2-137">**обращать**</span><span class="sxs-lookup"><span data-stu-id="721b2-137">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="721b2-138">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="721b2-138">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="721b2-139">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="721b2-139">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="721b2-140">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="721b2-140">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="721b2-141">**/осф**</span><span class="sxs-lookup"><span data-stu-id="721b2-141">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="721b2-142">**ptr**</span><span class="sxs-lookup"><span data-stu-id="721b2-142">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="721b2-143">**ref**</span><span class="sxs-lookup"><span data-stu-id="721b2-143">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="721b2-144">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="721b2-144">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="721b2-145">**Строка**</span><span class="sxs-lookup"><span data-stu-id="721b2-145">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="721b2-146">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="721b2-146">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="721b2-147">**наборов**</span><span class="sxs-lookup"><span data-stu-id="721b2-147">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="721b2-148">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="721b2-148">**unique**</span></span>](unique.md)
</dt> </dl>

 

 