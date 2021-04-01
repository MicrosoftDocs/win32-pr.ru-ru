---
title: dispinterface - атрибут
description: Оператор DISP определяет набор свойств и методов, для которых можно вызвать вызов IDispatch.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- интерфейс MIDL с атрибутом DISP
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890617"
---
# <a name="dispinterface-attribute"></a><span data-ttu-id="3757d-104">dispinterface - атрибут</span><span class="sxs-lookup"><span data-stu-id="3757d-104">dispinterface attribute</span></span>

<span data-ttu-id="3757d-105">Оператор **DISP** определяет набор свойств и методов, для которых можно вызвать **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="3757d-105">The **dispinterface** statement defines a set of properties and methods on which you can call **IDispatch::Invoke**.</span></span> <span data-ttu-id="3757d-106">Диспетчерский интерфейс может быть определен путем явного перечисления набора поддерживаемых методов и свойств (синтаксис 1) или путем перечисления одного интерфейса (синтаксис 2).</span><span class="sxs-lookup"><span data-stu-id="3757d-106">A dispinterface may be defined by explicitly listing the set of supported methods and properties (Syntax 1), or by listing a single interface (Syntax 2).</span></span>

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a><span data-ttu-id="3757d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3757d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3757d-108">*attributes*</span><span class="sxs-lookup"><span data-stu-id="3757d-108">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="3757d-109">Задает атрибуты, которые применяются ко всему **интерфейсу**.</span><span class="sxs-lookup"><span data-stu-id="3757d-109">Specifies attributes that apply to the entire **dispinterface**.</span></span> <span data-ttu-id="3757d-110">Принимаются следующие атрибуты: **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**unextensible**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** и **\[** [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="3757d-110">The following attributes are accepted: **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**nonextensible**](nonextensible.md)**\]**, **\[**[**oleautomation**](oleautomation.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="3757d-111">*имя disp-интерфейса*</span><span class="sxs-lookup"><span data-stu-id="3757d-111">*dispinterface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3757d-112">Имя, по которому **диспетчерский интерфейс** известен в библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="3757d-112">The name by which the **dispinterface** is known in the type library.</span></span> <span data-ttu-id="3757d-113">Это имя должно быть уникальным в пределах библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="3757d-113">This name must be unique within the type library.</span></span>

</dd> <dt>

<span data-ttu-id="3757d-114">*список свойств*</span><span class="sxs-lookup"><span data-stu-id="3757d-114">*property-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3757d-115">(Синтаксис 1) Необязательный список свойств, поддерживаемых объектом, объявленный в виде переменных.</span><span class="sxs-lookup"><span data-stu-id="3757d-115">(Syntax 1) An optional list of properties supported by the object, declared in the form of variables.</span></span> <span data-ttu-id="3757d-116">Это краткая форма для объявления функций свойств в списке методов.</span><span class="sxs-lookup"><span data-stu-id="3757d-116">This is the short form for declaring the property functions in the methods list.</span></span> <span data-ttu-id="3757d-117">Дополнительные сведения см. в разделе комментариев.</span><span class="sxs-lookup"><span data-stu-id="3757d-117">See the comments section for details.</span></span>

</dd> <dt>

<span data-ttu-id="3757d-118">*список методов*</span><span class="sxs-lookup"><span data-stu-id="3757d-118">*method-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3757d-119">(Синтаксис 1) Список, состоящий из прототипа функции для каждого метода и свойства в **DISP-интерфейсе**.</span><span class="sxs-lookup"><span data-stu-id="3757d-119">(Syntax 1) A list comprising a function prototype for each method and property in the **dispinterface**.</span></span> <span data-ttu-id="3757d-120">В *меслист* может использоваться любое количество определений функций.</span><span class="sxs-lookup"><span data-stu-id="3757d-120">Any number of function definitions can appear in *methlist*.</span></span> <span data-ttu-id="3757d-121">Функция в *меслист* имеет следующую форму:</span><span class="sxs-lookup"><span data-stu-id="3757d-121">A function in *methlist* has the following form:</span></span>

<span data-ttu-id="3757d-122">**\[  атрибуты \]** *ReturnType меснаме Type paramName ***(*** params \* \* *);**</span><span class="sxs-lookup"><span data-stu-id="3757d-122">**\[***attributes***\]** *returntype methname type paramname ***(*** params\*\*\*);*\*</span></span>

<span data-ttu-id="3757d-123">Следующие атрибуты принимаются для метода в **DISP-интерфейсе**: **\[ helpString \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** , **\[** [**propputref**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** и **\[** [**vararg**](vararg.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="3757d-123">The following attributes are accepted on a method in a **dispinterface**: **\[helpstring\]**, **\[helpcontext\]**, **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]**, **\[**[**propputref**](propputref.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**vararg**](vararg.md)**\]**.</span></span> <span data-ttu-id="3757d-124">Если указано **\[ \] vararg** , последний параметр должен быть надежным массивом типа **Variant** .</span><span class="sxs-lookup"><span data-stu-id="3757d-124">If **\[vararg\]** is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="3757d-125">Список параметров представляет собой список с разделителями-запятыми, каждый элемент которого имеет следующую форму:</span><span class="sxs-lookup"><span data-stu-id="3757d-125">The parameter list is a comma-delimited list, each element of which has the following form:</span></span>

<span data-ttu-id="3757d-126">**\[***атрибута***\]**</span><span class="sxs-lookup"><span data-stu-id="3757d-126">**\[***attributes***\]**</span></span>

<span data-ttu-id="3757d-127">*Тип* может быть любым объявленным или встроенным типом или указателем на любой тип.</span><span class="sxs-lookup"><span data-stu-id="3757d-127">The *type* can be any declared or built-in type, or a pointer to any type.</span></span> <span data-ttu-id="3757d-128">Атрибуты в параметрах:</span><span class="sxs-lookup"><span data-stu-id="3757d-128">Attributes on parameters are:</span></span>

<span data-ttu-id="3757d-129">**\[**[**в**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**необязательный**](optional.md) **\]** , **\[ строка \]**</span><span class="sxs-lookup"><span data-stu-id="3757d-129">**\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]**, **\[**[**optional**](optional.md)**\]**, **\[string\]**</span></span>

</dd> <dt>

<span data-ttu-id="3757d-130">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="3757d-130">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3757d-131">(Синтаксис 2) Имя интерфейса, объявляемого как интерфейс IDispatch.</span><span class="sxs-lookup"><span data-stu-id="3757d-131">(Syntax 2) The name of the interface to declare as an IDispatch interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3757d-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3757d-132">Remarks</span></span>

<span data-ttu-id="3757d-133">Компилятор MIDL принимает следующий порядок параметров (слева направо):</span><span class="sxs-lookup"><span data-stu-id="3757d-133">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="3757d-134">Обязательные параметры (параметры, у которых нет \[ DefaultValue \] или \[ необязательных \] атрибутов);</span><span class="sxs-lookup"><span data-stu-id="3757d-134">Required parameters (parameters that do not have the \[defaultvalue\] or \[optional\] attributes),</span></span>
2.  <span data-ttu-id="3757d-135">необязательные параметры с \[ атрибутом DefaultValue или без него \]</span><span class="sxs-lookup"><span data-stu-id="3757d-135">optional parameters with or without the \[defaultvalue\] attribute,</span></span>
3.  <span data-ttu-id="3757d-136">параметры с \[ необязательным \] атрибутом и без \[ \] атрибута DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="3757d-136">parameters with the \[optional\] attribute and without the \[defaultvalue\] attribute,</span></span>
4.  <span data-ttu-id="3757d-137">\[параметр [**LCID**](lcid.md) \] , если он есть,</span><span class="sxs-lookup"><span data-stu-id="3757d-137">\[ [**lcid**](lcid.md)\] parameter, if any,</span></span>
5.  <span data-ttu-id="3757d-138">\[[**retval**](retval.md) \] параметр</span><span class="sxs-lookup"><span data-stu-id="3757d-138">\[ [**retval**](retval.md)\] parameter</span></span>

<span data-ttu-id="3757d-139">Функции методов задаются точно так же, как описано на странице Справочник по [**модулю**](module.md) , за исключением того, что \[ атрибут [**entry**](entry.md) \] не разрешен.</span><span class="sxs-lookup"><span data-stu-id="3757d-139">Method functions are specified exactly as described in the reference page for [**module**](module.md) except that the \[ [**entry**](entry.md)\] attribute is not allowed.</span></span> <span data-ttu-id="3757d-140">Обратите внимание, что STDOLE32. TLB (СТДОЛЕ. TLB в 16-разрядных системах) необходимо импортировать, так как **диспетчерский интерфейс** наследует от IDispatch.</span><span class="sxs-lookup"><span data-stu-id="3757d-140">Note that STDOLE32.TLB (STDOLE.TLB on 16-bit systems) must be imported, because a **dispinterface** inherits from IDispatch.</span></span>

<span data-ttu-id="3757d-141">Свойства можно объявлять в списках свойств или методов.</span><span class="sxs-lookup"><span data-stu-id="3757d-141">You can declare properties in either the properties or methods lists.</span></span> <span data-ttu-id="3757d-142">Объявление свойств в списке свойств не указывает тип доступа, который поддерживает свойство (т. е. Get, WHERE или путреф).</span><span class="sxs-lookup"><span data-stu-id="3757d-142">Declaring properties in the properties list does not indicate the type of access the property supports (that is, get, put, or putref).</span></span> <span data-ttu-id="3757d-143">Укажите атрибут \[ [**ReadOnly**](readonly.md) \] для свойств, которые не поддерживают размещение или путреф.</span><span class="sxs-lookup"><span data-stu-id="3757d-143">Specify the \[ [**readonly**](readonly.md)\] attribute for properties that don't support put or putref.</span></span> <span data-ttu-id="3757d-144">При объявлении функций свойств в списке методов функции для одного свойства имеют одинаковый идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3757d-144">If you declare the property functions in the methods list, functions for one property all have the same identifier.</span></span>

<span data-ttu-id="3757d-145">При использовании первого синтаксиса требуются Теги Properties: и.</span><span class="sxs-lookup"><span data-stu-id="3757d-145">Using the first syntax, the properties: and methods: tags are required.</span></span> <span data-ttu-id="3757d-146">Атрибут \[ [**ID**](id.md) \] также требуется для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="3757d-146">The \[ [**id**](id.md)\] attribute is also required on each member.</span></span> <span data-ttu-id="3757d-147">Пример:</span><span class="sxs-lookup"><span data-stu-id="3757d-147">For example:</span></span>

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

<span data-ttu-id="3757d-148">В отличие от членов интерфейса, члены disp-интерфейсов не могут использовать атрибут [**retval**](retval.md) для возврата значения в дополнение к коду ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="3757d-148">Unlike interface members, dispinterface members cannot use the [**retval**](retval.md) attribute to return a value in addition to an HRESULT error code.</span></span> <span data-ttu-id="3757d-149">Атрибут \[ [**LCID**](lcid.md) \] также является недопустимым для disp-интерфейсов, так как IDispatch:: Invoke передает код языка.</span><span class="sxs-lookup"><span data-stu-id="3757d-149">The \[ [**lcid**](lcid.md)\] attribute is likewise invalid for dispinterfaces, because IDispatch::Invoke passes an LCID.</span></span> <span data-ttu-id="3757d-150">Однако можно повторно объявить интерфейс, использующий эти атрибуты.</span><span class="sxs-lookup"><span data-stu-id="3757d-150">However, it is possible to redeclare an interface that uses these attributes.</span></span>

<span data-ttu-id="3757d-151">С помощью второго синтаксиса интерфейсы, поддерживающие IDispatch и объявленные ранее в скрипте ODL, могут быть повторно объявлены как интерфейсы IDispatch следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3757d-151">Using the second syntax, interfaces that support IDispatch and are declared earlier in an ODL script can be redeclared as IDispatch interfaces as follows:</span></span>

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

<span data-ttu-id="3757d-152">В предыдущем примере объявляются все члены Hello и все члены, которые Привет наследуют как поддерживающие IDispatch.</span><span class="sxs-lookup"><span data-stu-id="3757d-152">The preceding example declares all the members of hello and all the members that hello inherits as supporting IDispatch.</span></span> <span data-ttu-id="3757d-153">В этом случае, если аргумент Hello был объявлен ранее \[ с \] элементами LCID и \[ retval \] , которые возвращали HRESULTS, MkTypLib будет удалять каждый \[ \] параметр LCID и тип возвращаемого значения HRESULT, а вместо этого помечать возвращаемый тип как \[ \] параметр retval.</span><span class="sxs-lookup"><span data-stu-id="3757d-153">In this case, if hello were declared earlier with \[lcid\] and \[retval\] members that returned HRESULTs, MkTypLib would remove each \[lcid\] parameter and HRESULT return type, and instead mark the return type as that of the \[retval\] parameter.</span></span>

> [!Note]  
> <span data-ttu-id="3757d-154">Средство Mktyplib.exe устарело.</span><span class="sxs-lookup"><span data-stu-id="3757d-154">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="3757d-155">Вместо этого используйте компилятор MIDL.</span><span class="sxs-lookup"><span data-stu-id="3757d-155">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="3757d-156">Свойства и методы disp-интерфейса не являются частью таблицы VTBL.</span><span class="sxs-lookup"><span data-stu-id="3757d-156">The properties and methods of a dispinterface are not part of the VTBL of the dispinterface.</span></span> <span data-ttu-id="3757d-157">Следовательно, [креатестддиспатч](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) и [диспинвоке](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) нельзя использовать для реализации IDispatch:: Invoke.</span><span class="sxs-lookup"><span data-stu-id="3757d-157">Consequently, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) and [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) cannot be used to implement IDispatch::Invoke.</span></span> <span data-ttu-id="3757d-158">Диспетчерский интерфейс используется, когда приложению необходимо предоставить доступ к существующим функциям, не относящимся к VTBL, с помощью службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3757d-158">The dispinterface is used when an application needs to expose existing non-VTBL functions through Automation.</span></span> <span data-ttu-id="3757d-159">Эти приложения могут реализовать IDispatch:: Invoke путем проверки параметра Диспидмембер и непосредственного вызова соответствующей функции.</span><span class="sxs-lookup"><span data-stu-id="3757d-159">These applications can implement IDispatch::Invoke by examining the dispidMember parameter and directly calling the corresponding function.</span></span>

## <a name="examples"></a><span data-ttu-id="3757d-160">Примеры</span><span class="sxs-lookup"><span data-stu-id="3757d-160">Examples</span></span>

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="3757d-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3757d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3757d-162">**bindable**</span><span class="sxs-lookup"><span data-stu-id="3757d-162">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="3757d-163">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="3757d-163">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="3757d-164">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="3757d-164">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="3757d-165">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="3757d-165">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="3757d-166">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="3757d-166">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="3757d-167">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="3757d-167">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="3757d-168">**служеб**</span><span class="sxs-lookup"><span data-stu-id="3757d-168">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="3757d-169">**окне**</span><span class="sxs-lookup"><span data-stu-id="3757d-169">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="3757d-170">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="3757d-170">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="3757d-171">типефлагс</span><span class="sxs-lookup"><span data-stu-id="3757d-171">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="3757d-172">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="3757d-172">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3757d-173">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="3757d-173">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3757d-174">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="3757d-174">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="3757d-175">**используемых**</span><span class="sxs-lookup"><span data-stu-id="3757d-175">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="3757d-176">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="3757d-176">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="3757d-177">**nonextensible**</span><span class="sxs-lookup"><span data-stu-id="3757d-177">**nonextensible**</span></span>](nonextensible.md)
</dt> <dt>

[<span data-ttu-id="3757d-178">**propget**</span><span class="sxs-lookup"><span data-stu-id="3757d-178">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="3757d-179">**propput**</span><span class="sxs-lookup"><span data-stu-id="3757d-179">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="3757d-180">**propputref**</span><span class="sxs-lookup"><span data-stu-id="3757d-180">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="3757d-181">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="3757d-181">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="3757d-182">**зона**</span><span class="sxs-lookup"><span data-stu-id="3757d-182">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="3757d-183">**Строка**</span><span class="sxs-lookup"><span data-stu-id="3757d-183">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="3757d-184">**UUID**</span><span class="sxs-lookup"><span data-stu-id="3757d-184">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="3757d-185">**vararg**</span><span class="sxs-lookup"><span data-stu-id="3757d-185">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="3757d-186">**Версия**</span><span class="sxs-lookup"><span data-stu-id="3757d-186">**version**</span></span>](version.md)
</dt> </dl>

 

 