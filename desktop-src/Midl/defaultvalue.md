---
title: defaultvalue - атрибут
description: Атрибут \ DefaultValue \ позволяет указать значение по умолчанию для типизированного необязательного параметра.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- атрибут DefaultValue MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337268"
---
# <a name="defaultvalue-attribute"></a><span data-ttu-id="7a734-104">defaultvalue - атрибут</span><span class="sxs-lookup"><span data-stu-id="7a734-104">defaultvalue attribute</span></span>

<span data-ttu-id="7a734-105">Атрибут **\[ DefaultValue \]** позволяет указать значение по умолчанию для типизированного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="7a734-105">The **\[defaultvalue\]** attribute allows you to specify a default value for a typed optional parameter.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a><span data-ttu-id="7a734-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a734-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a734-107">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="7a734-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7a734-108">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7a734-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7a734-109">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="7a734-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7a734-110">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="7a734-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7a734-111">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="7a734-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7a734-112">Указывает имя функции, к которой будет применен атрибут **\[ DefaultValue \]** .</span><span class="sxs-lookup"><span data-stu-id="7a734-112">Specifies the name of the function to which the **\[defaultvalue\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="7a734-113">*обязательный параметр-param-List*</span><span class="sxs-lookup"><span data-stu-id="7a734-113">*mandatory-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7a734-114">Указывает обязательные параметры.</span><span class="sxs-lookup"><span data-stu-id="7a734-114">Specifies on or more required parameters.</span></span>

</dd> <dt>

<span data-ttu-id="7a734-115">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="7a734-115">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7a734-116">Задает список из одного или нескольких атрибутов, разделенных запятыми, которые применяются к параметру.</span><span class="sxs-lookup"><span data-stu-id="7a734-116">Specifies a list of one or more attributes, separated by commas, that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7a734-117">*Param-Type*</span><span class="sxs-lookup"><span data-stu-id="7a734-117">*param-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7a734-118">Указывает тип необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="7a734-118">Indicates the type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7a734-119">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="7a734-119">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7a734-120">Указывает имя необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="7a734-120">Specifies the name of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7a734-121">*Необязательный параметр-param-List*</span><span class="sxs-lookup"><span data-stu-id="7a734-121">*optional-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7a734-122">Указывает ноль или более дополнительных параметров, каждое из которых должно иметь значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a734-122">Specifies zero or more additional parameters, each of which must have a default value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a734-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a734-123">Remarks</span></span>

<span data-ttu-id="7a734-124">Значение по умолчанию, заданное для параметра, может быть любой константой или выражением, которое разрешается в константу, которое может быть представлено **вариантом**.</span><span class="sxs-lookup"><span data-stu-id="7a734-124">The default value you specify for the parameter can be any constant, or an expression that resolves to a constant, that can be represented by a **VARIANT**.</span></span> <span data-ttu-id="7a734-125">В частности, атрибут **\[ \] DefaultValue** нельзя применять к параметру, который является структурой, массивом или типом **SAFEARRAY** .</span><span class="sxs-lookup"><span data-stu-id="7a734-125">Specifically, you cannot apply the **\[defaultvalue\]** attribute to a parameter that is a structure, an array, or a **SAFEARRAY** type.</span></span>

<span data-ttu-id="7a734-126">Компилятор MIDL принимает следующий порядок параметров (слева направо):</span><span class="sxs-lookup"><span data-stu-id="7a734-126">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="7a734-127">Обязательные параметры (параметры, у которых нет **\[ DefaultValue \]** или **\[** [**необязательных**](optional.md) **\]** атрибутов);</span><span class="sxs-lookup"><span data-stu-id="7a734-127">Required parameters (parameters that do not have the **\[defaultvalue\]** or **\[**[**optional**](optional.md)**\]** attributes),</span></span>
2.  <span data-ttu-id="7a734-128">необязательные параметры с атрибутом **\[ DefaultValue \]** или без него</span><span class="sxs-lookup"><span data-stu-id="7a734-128">optional parameters with or without the **\[defaultvalue\]** attribute,</span></span>
3.  <span data-ttu-id="7a734-129">параметры с **\[ необязательным \]** атрибутом и без атрибута **\[ DefaultValue \]** ,</span><span class="sxs-lookup"><span data-stu-id="7a734-129">parameters with the **\[optional\]** attribute and without the **\[defaultvalue\]** attribute,</span></span>
4.  <span data-ttu-id="7a734-130">**\[** параметр [**LCID**](lcid.md) **\]** , если он есть,</span><span class="sxs-lookup"><span data-stu-id="7a734-130">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="7a734-131">**\[**[**retval**](retval.md) **\]** параметр</span><span class="sxs-lookup"><span data-stu-id="7a734-131">**\[**[**retval**](retval.md)**\]** parameter</span></span>

## <a name="examples"></a><span data-ttu-id="7a734-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="7a734-132">Examples</span></span>

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a><span data-ttu-id="7a734-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a734-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a734-134">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="7a734-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="7a734-135">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="7a734-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7a734-136">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="7a734-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="7a734-137">**намного**</span><span class="sxs-lookup"><span data-stu-id="7a734-137">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="7a734-138">**используемых**</span><span class="sxs-lookup"><span data-stu-id="7a734-138">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="7a734-139">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="7a734-139">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7a734-140">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="7a734-140">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7a734-141">**retval**</span><span class="sxs-lookup"><span data-stu-id="7a734-141">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="7a734-142">типефлагс</span><span class="sxs-lookup"><span data-stu-id="7a734-142">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 