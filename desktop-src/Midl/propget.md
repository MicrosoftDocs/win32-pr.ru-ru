---
title: propget - атрибут
description: Атрибут \ propget \ задает функцию доступа к свойству. Свойство должно иметь то же имя, что и функция.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- атрибут propget MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069848"
---
# <a name="propget-attribute"></a><span data-ttu-id="a153e-105">propget - атрибут</span><span class="sxs-lookup"><span data-stu-id="a153e-105">propget attribute</span></span>

<span data-ttu-id="a153e-106">Атрибут **\[ propget \]** задает функцию доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="a153e-106">The **\[propget\]** attribute specifies a property accessor function.</span></span> <span data-ttu-id="a153e-107">Свойство должно иметь то же имя, что и функция.</span><span class="sxs-lookup"><span data-stu-id="a153e-107">The property must have the same name as the function.</span></span>

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="a153e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a153e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a153e-109">*атрибуты необязательного свойства*</span><span class="sxs-lookup"><span data-stu-id="a153e-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="a153e-110">Ноль или более атрибутов свойств.</span><span class="sxs-lookup"><span data-stu-id="a153e-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a153e-111">*Тип возвращаемого значения*</span><span class="sxs-lookup"><span data-stu-id="a153e-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a153e-112">Тип данных, возвращаемых удаленной процедурой.</span><span class="sxs-lookup"><span data-stu-id="a153e-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a153e-113">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="a153e-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a153e-114">Имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="a153e-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a153e-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="a153e-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="a153e-116">Ноль или более параметров для удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="a153e-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a153e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a153e-117">Remarks</span></span>

<span data-ttu-id="a153e-118">Функция с атрибутом propget также должна иметь в качестве последнего параметра тип указателя с **\[** [](out-idl.md) **\]** атрибутами out и **\[** [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a153e-118">A function that has the propget attribute should also have, as its last parameter, a pointer type with the **\[**[**out**](out-idl.md)**\]** and **\[**[**retval**](retval.md)**\]** attributes.</span></span> <span data-ttu-id="a153e-119">Если у последнего параметра нет \[ атрибутов out, \] то возвращаемое значение функции обрабатывается как \[ параметр out, retval \] .</span><span class="sxs-lookup"><span data-stu-id="a153e-119">If the last parameter does not have the \[out, retval\] attributes, the return value of the function is treated as an \[out, retval\] parameter.</span></span> <span data-ttu-id="a153e-120">Например, функция с прототипом</span><span class="sxs-lookup"><span data-stu-id="a153e-120">For example, a function with the prototype</span></span>

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

<span data-ttu-id="a153e-121">рассматривается как</span><span class="sxs-lookup"><span data-stu-id="a153e-121">is treated as</span></span>

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

<span data-ttu-id="a153e-122">Для функции можно указать не более одного параметра **\[ propget \]**, **\[** [**propput**](propput.md) **\]** и **\[** [**propputref**](propputref.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a153e-122">At most, one of **\[propget\]**, **\[**[**propput**](propput.md)**\]**, and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="a153e-123">Если атрибут **\[** [**LCID**](lcid.md) **\]** используется в списке параметров функции, содержащей параметр с **\[** [](propput.md) **\]** атрибутом propput, то параметр **\[ LCID \]** должен находиться в секундах до последней.</span><span class="sxs-lookup"><span data-stu-id="a153e-123">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[**[**propput**](propput.md)**\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="a153e-124">Флаги</span><span class="sxs-lookup"><span data-stu-id="a153e-124">Flags</span></span>

<span data-ttu-id="a153e-125">ВЫЗВАТЬ \_ пропертижет</span><span class="sxs-lookup"><span data-stu-id="a153e-125">INVOKE\_PROPERTYGET</span></span>

## <a name="examples"></a><span data-ttu-id="a153e-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="a153e-126">Examples</span></span>

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a><span data-ttu-id="a153e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a153e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a153e-128">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="a153e-128">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a153e-129">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="a153e-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a153e-130">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="a153e-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a153e-131">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="a153e-131">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="a153e-132">**retval**</span><span class="sxs-lookup"><span data-stu-id="a153e-132">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="a153e-133">**propput**</span><span class="sxs-lookup"><span data-stu-id="a153e-133">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="a153e-134">**propputref**</span><span class="sxs-lookup"><span data-stu-id="a153e-134">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="a153e-135">**типефлагс**</span><span class="sxs-lookup"><span data-stu-id="a153e-135">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 