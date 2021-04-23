---
title: optional - атрибут
description: Атрибут \ Optional \ указывает необязательный параметр для функции-члена.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- Необязательный атрибут MIDL
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890613"
---
# <a name="optional-attribute"></a><span data-ttu-id="1c632-104">optional - атрибут</span><span class="sxs-lookup"><span data-stu-id="1c632-104">optional attribute</span></span>

<span data-ttu-id="1c632-105">**\[ Необязательный \]** атрибут указывает необязательный параметр для функции-члена.</span><span class="sxs-lookup"><span data-stu-id="1c632-105">The **\[optional\]** attribute specifies an optional parameter for a member function.</span></span>

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a><span data-ttu-id="1c632-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c632-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c632-107">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="1c632-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1c632-108">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="1c632-108">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="1c632-109">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="1c632-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1c632-110">Указывает имя функции, определенное в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="1c632-110">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="1c632-111">*другие атрибуты*</span><span class="sxs-lookup"><span data-stu-id="1c632-111">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="1c632-112">Ноль или несколько необязательных атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="1c632-112">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="1c632-113">*тип параметра*</span><span class="sxs-lookup"><span data-stu-id="1c632-113">*parameter-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1c632-114">Тип данных необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="1c632-114">The data type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1c632-115">*имя параметра*</span><span class="sxs-lookup"><span data-stu-id="1c632-115">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1c632-116">Указывает имя необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="1c632-116">Specifies the name of the optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c632-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c632-117">Remarks</span></span>

<span data-ttu-id="1c632-118">**\[ Необязательный \]** атрибут допустим только в том случае, если параметр относится к типу **Variant** или **Variant** в \* .</span><span class="sxs-lookup"><span data-stu-id="1c632-118">The **\[optional\]** attribute is valid only if the parameter is of type **VARIANT** or **VARIANT** Â \*.</span></span>

<span data-ttu-id="1c632-119">Компилятор MIDL принимает следующий порядок параметров (слева направо):</span><span class="sxs-lookup"><span data-stu-id="1c632-119">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="1c632-120">Обязательные параметры (параметры, у которых нет **\[** [**DefaultValue**](defaultvalue.md) **\]** или **\[ необязательных \]** атрибутов);</span><span class="sxs-lookup"><span data-stu-id="1c632-120">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[optional\]** attributes),</span></span>
2.  <span data-ttu-id="1c632-121">Необязательные параметры с **\[** [](defaultvalue.md) атрибутом DefaultValue или без него **\]**</span><span class="sxs-lookup"><span data-stu-id="1c632-121">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
3.  <span data-ttu-id="1c632-122">Параметры с **\[ необязательным \]** атрибутом и без **\[** [](defaultvalue.md) **\]** атрибута DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="1c632-122">Parameters with the **\[optional\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
4.  <span data-ttu-id="1c632-123">**\[** параметр [**LCID**](lcid.md) **\]** , если он есть,</span><span class="sxs-lookup"><span data-stu-id="1c632-123">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="1c632-124">**\[**[**retval**](retval.md) **\]** параметр</span><span class="sxs-lookup"><span data-stu-id="1c632-124">**\[**[**retval**](retval.md)**\]** parameter</span></span>

<span data-ttu-id="1c632-125">**\[ Необязательный \]** атрибут нельзя применить к параметру, который также имеет **\[** [](lcid.md) **\]** атрибуты LCID или **\[** [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="1c632-125">You cannot apply the **\[optional\]** attribute to a parameter that also has the **\[**[**lcid**](lcid.md)**\]** or **\[**[**retval**](retval.md)**\]** attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="1c632-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="1c632-126">Examples</span></span>

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a><span data-ttu-id="1c632-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c632-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c632-128">**максимально**</span><span class="sxs-lookup"><span data-stu-id="1c632-128">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="1c632-129">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="1c632-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="1c632-130">**намного**</span><span class="sxs-lookup"><span data-stu-id="1c632-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="1c632-131">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="1c632-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="1c632-132">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="1c632-132">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="1c632-133">**retval**</span><span class="sxs-lookup"><span data-stu-id="1c632-133">**retval**</span></span>](retval.md)
</dt> </dl>

 

 