---
title: retval - атрибут
description: Атрибут \ retval \ обозначает параметр, который получает возвращаемое значение элемента.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- атрибут retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890481"
---
# <a name="retval-attribute"></a><span data-ttu-id="a6886-104">retval - атрибут</span><span class="sxs-lookup"><span data-stu-id="a6886-104">retval attribute</span></span>

<span data-ttu-id="a6886-105">Атрибут **\[ retval \]** задает параметр, который получает возвращаемое значение элемента.</span><span class="sxs-lookup"><span data-stu-id="a6886-105">The **\[retval\]** attribute designates the parameter that receives the return value of the member.</span></span>

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a><span data-ttu-id="a6886-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6886-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6886-107">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="a6886-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a6886-108">Тип данных возвращаемого значения удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="a6886-108">The data type of the return value of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a6886-109">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="a6886-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a6886-110">Имя, используемое для вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="a6886-110">The name used to invoke the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a6886-111">*необязательные атрибуты*</span><span class="sxs-lookup"><span data-stu-id="a6886-111">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="a6886-112">Ноль или несколько атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="a6886-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a6886-113">*тип данных*</span><span class="sxs-lookup"><span data-stu-id="a6886-113">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a6886-114">Тип данных, передаваемых через параметр.</span><span class="sxs-lookup"><span data-stu-id="a6886-114">The type of the data passed through the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a6886-115">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="a6886-115">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a6886-116">Имя идентификатора параметра.</span><span class="sxs-lookup"><span data-stu-id="a6886-116">The identifier name of the parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6886-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6886-117">Remarks</span></span>

<span data-ttu-id="a6886-118">Атрибут **\[ retval \]** можно использовать для параметров членов интерфейса, описывающих методы или получения свойств.</span><span class="sxs-lookup"><span data-stu-id="a6886-118">You can use the **\[retval\]** attribute on parameters of interface members that describe methods or get properties.</span></span> <span data-ttu-id="a6886-119">(Атрибут является обязательным для последнего параметра метода, имеющего **\[** [**propget**](propget.md) **\]** атрибут.) Параметр должен иметь **\[** атрибут [**out**](out-idl.md) **\]** и должен быть типом указателя.</span><span class="sxs-lookup"><span data-stu-id="a6886-119">(The attribute is required on the last parameter of a method that has the **\[**[**propget**](propget.md)**\]** attribute.) The parameter must have the **\[**[**out**](out-idl.md)**\]** attribute and must be a pointer type.</span></span>

<span data-ttu-id="a6886-120">**\[** [**Необязательный**](optional.md) **\]** атрибут нельзя применить к параметру **\[ retval \]** .</span><span class="sxs-lookup"><span data-stu-id="a6886-120">You cannot apply the **\[**[**optional**](optional.md)**\]** attribute to a **\[retval\]** parameter.</span></span>

<span data-ttu-id="a6886-121">Компилятор MIDL принимает следующий порядок параметров (слева направо):</span><span class="sxs-lookup"><span data-stu-id="a6886-121">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="a6886-122">Обязательные параметры (параметры, у которых нет **\[** [**DefaultValue**](defaultvalue.md) **\]** или **\[** [**необязательных**](optional.md) **\]** атрибутов).</span><span class="sxs-lookup"><span data-stu-id="a6886-122">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[**[**optional**](optional.md)**\]** attributes).</span></span>
2.  <span data-ttu-id="a6886-123">Необязательные параметры с **\[** атрибутом [**DefaultValue**](defaultvalue.md) или без него **\]** .</span><span class="sxs-lookup"><span data-stu-id="a6886-123">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
3.  <span data-ttu-id="a6886-124">Параметры с **\[** [**необязательным**](optional.md) **\]** атрибутом и без **\[** [](defaultvalue.md) **\]** атрибута DefaultValue.</span><span class="sxs-lookup"><span data-stu-id="a6886-124">Parameters with the **\[**[**optional**](optional.md)**\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
4.  <span data-ttu-id="a6886-125">**\[** параметр [**LCID**](lcid.md) **\]** , если он есть.</span><span class="sxs-lookup"><span data-stu-id="a6886-125">**\[**[**lcid**](lcid.md)**\]** parameter, if any.</span></span>
5.  <span data-ttu-id="a6886-126">параметр **\[ retval \]** .</span><span class="sxs-lookup"><span data-stu-id="a6886-126">**\[retval\]** parameter.</span></span>

<span data-ttu-id="a6886-127">Параметры с атрибутом **\[ retval \]** не отображаются в ориентированных на пользователей браузерах.</span><span class="sxs-lookup"><span data-stu-id="a6886-127">Parameters with the **\[retval\]** attribute are not displayed in user-oriented browsers.</span></span>

### <a name="flags"></a><span data-ttu-id="a6886-128">Флаги</span><span class="sxs-lookup"><span data-stu-id="a6886-128">Flags</span></span>

<span data-ttu-id="a6886-129">ИДЛФЛАГ \_ фретвал</span><span class="sxs-lookup"><span data-stu-id="a6886-129">IDLFLAG\_FRETVAL</span></span>

## <a name="examples"></a><span data-ttu-id="a6886-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="a6886-130">Examples</span></span>

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a><span data-ttu-id="a6886-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6886-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6886-132">**максимально**</span><span class="sxs-lookup"><span data-stu-id="a6886-132">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="a6886-133">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="a6886-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a6886-134">**намного**</span><span class="sxs-lookup"><span data-stu-id="a6886-134">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="a6886-135">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="a6886-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a6886-136">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="a6886-136">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a6886-137">**используемых**</span><span class="sxs-lookup"><span data-stu-id="a6886-137">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="a6886-138">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="a6886-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="a6886-139">**propget**</span><span class="sxs-lookup"><span data-stu-id="a6886-139">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="a6886-140">**типефлагс**</span><span class="sxs-lookup"><span data-stu-id="a6886-140">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 