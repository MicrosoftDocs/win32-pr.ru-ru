---
title: vararg - атрибут
description: Атрибут \ vararg \ указывает, что функция принимает переменное число параметров. Для этого последний параметр должен быть надежным массивом типа VARIANT, который содержит все остальные параметры.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- атрибут vararg MIDL
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650342"
---
# <a name="vararg-attribute"></a><span data-ttu-id="4a87a-105">vararg - атрибут</span><span class="sxs-lookup"><span data-stu-id="4a87a-105">vararg attribute</span></span>

<span data-ttu-id="4a87a-106">Атрибут **\[ vararg \]** указывает, что функция принимает переменное число параметров.</span><span class="sxs-lookup"><span data-stu-id="4a87a-106">The **\[vararg\]** attribute specifies that the function takes a variable number of parameters.</span></span> <span data-ttu-id="4a87a-107">Для этого последний параметр должен быть надежным массивом типа **Variant** , который содержит все остальные параметры.</span><span class="sxs-lookup"><span data-stu-id="4a87a-107">To accomplish this, the last parameter must be a safe array of **VARIANT** type that contains all the remaining parameters.</span></span>

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a><span data-ttu-id="4a87a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a87a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a87a-109">*необязательные атрибуты*</span><span class="sxs-lookup"><span data-stu-id="4a87a-109">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="4a87a-110">Указывает ноль или более атрибутов, которые должны быть применены к функции.</span><span class="sxs-lookup"><span data-stu-id="4a87a-110">Specifies zero or more attributes to be applied to the function.</span></span> <span data-ttu-id="4a87a-111">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="4a87a-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4a87a-112">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="4a87a-112">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4a87a-113">Тип данных, возвращаемых удаленной процедурой после завершения.</span><span class="sxs-lookup"><span data-stu-id="4a87a-113">The type of the data returned by the remote procedure upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="4a87a-114">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="4a87a-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4a87a-115">Имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="4a87a-115">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="4a87a-116">*Optional-param-Attributes*</span><span class="sxs-lookup"><span data-stu-id="4a87a-116">*optional-param-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="4a87a-117">Указывает ноль или более атрибутов, которые должны быть применены к параметру функции сразу после перечисления атрибутов.</span><span class="sxs-lookup"><span data-stu-id="4a87a-117">Specifies zero or more attributes to be applied to the function parameter immediately following the attribute listing.</span></span>

</dd> <dt>

<span data-ttu-id="4a87a-118">*Param-List*</span><span class="sxs-lookup"><span data-stu-id="4a87a-118">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4a87a-119">Задает все параметры, сохраняет окончательный, отличающийся параметр.</span><span class="sxs-lookup"><span data-stu-id="4a87a-119">Specifies all the parameters, save the final, varying, parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4a87a-120">*Last-param-Name*</span><span class="sxs-lookup"><span data-stu-id="4a87a-120">*last-param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4a87a-121">Имя изменяющегося параметра.</span><span class="sxs-lookup"><span data-stu-id="4a87a-121">The name of the varying parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a87a-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a87a-122">Remarks</span></span>

<span data-ttu-id="4a87a-123">**\[** Атрибуты [**Optional**](optional.md) **\]** и DefaultValue нельзя применять **\[** [](defaultvalue.md) **\]** к параметрам в функции, имеющей атрибут **\[ vararg \]** .</span><span class="sxs-lookup"><span data-stu-id="4a87a-123">You cannot apply the **\[**[**optional**](optional.md)**\]** or **\[**[**defaultvalue**](defaultvalue.md)**\]** attributes to any parameters in a function that has the **\[vararg\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="4a87a-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="4a87a-124">Examples</span></span>

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a><span data-ttu-id="4a87a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a87a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a87a-126">**максимально**</span><span class="sxs-lookup"><span data-stu-id="4a87a-126">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="4a87a-127">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="4a87a-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="4a87a-128">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="4a87a-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4a87a-129">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="4a87a-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4a87a-130">**используемых**</span><span class="sxs-lookup"><span data-stu-id="4a87a-130">**optional**</span></span>](optional.md)
</dt> </dl>

 

 