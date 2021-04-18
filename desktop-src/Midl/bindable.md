---
title: bindable - атрибут
description: Атрибут \ BIND \ указывает, что свойство поддерживает привязку данных.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- атрибут с возможностью привязки MIDL
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681604"
---
# <a name="bindable-attribute"></a><span data-ttu-id="36e1c-104">bindable - атрибут</span><span class="sxs-lookup"><span data-stu-id="36e1c-104">bindable attribute</span></span>

<span data-ttu-id="36e1c-105">Атрибут **\[ BIND \]** указывает, что свойство поддерживает привязку данных.</span><span class="sxs-lookup"><span data-stu-id="36e1c-105">The **\[bindable\]** attribute indicates that the property supports data binding.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="36e1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36e1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36e1c-107">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="36e1c-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="36e1c-108">Задает список из нуля или нескольких атрибутов IDL, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="36e1c-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="36e1c-109">При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="36e1c-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="36e1c-110">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="36e1c-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="36e1c-111">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="36e1c-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="36e1c-112">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="36e1c-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="36e1c-113">Указывает ноль или более атрибутов, которые применяются к прототипу функции для свойства или метода в [**интерфейсе**](interface.md) или [**DISP**](dispinterface.md)-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="36e1c-113">Specifies zero or more attributes that apply to the function prototype for a property or a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span> <span data-ttu-id="36e1c-114">Допустимы следующие атрибуты: [**\[ helpString \]**](helpstring.md), [**\[ \] HelpContext**](helpcontext.md), [**\[ \] String**](string.md), [**\[ дефаултбинд \]**](defaultbind.md), [**\[ дисплайбинд \]**](displaybind.md), [**\[ иммедиатебинд \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ propputref \]**](propputref.md)и [**\[ vararg \]**](vararg.md).</span><span class="sxs-lookup"><span data-stu-id="36e1c-114">The following attributes are valid: [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[string\]**](string.md), [**\[defaultbind\]**](defaultbind.md), [**\[displaybind\]**](displaybind.md), [**\[immediatebind\]**](immediatebind.md), [**\[propget\]**](propget.md), [**\[propput\]**](propput.md), [**\[propputref\]**](propputref.md), and [**\[vararg\]**](vararg.md).</span></span> <span data-ttu-id="36e1c-115">Если указано **vararg** , последний параметр должен быть надежным массивом типа Variant.</span><span class="sxs-lookup"><span data-stu-id="36e1c-115">If **vararg** is specified, the last parameter must be a safe array of type VARIANT.</span></span> <span data-ttu-id="36e1c-116">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="36e1c-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="36e1c-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="36e1c-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="36e1c-118">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="36e1c-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="36e1c-119">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="36e1c-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="36e1c-120">Указывает имя функции, к которой будет применен атрибут, **\[ допускающий привязку \]** .</span><span class="sxs-lookup"><span data-stu-id="36e1c-120">Specifies the name of the function to which the **\[bindable\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="36e1c-121">*params*</span><span class="sxs-lookup"><span data-stu-id="36e1c-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="36e1c-122">Список параметров функции.</span><span class="sxs-lookup"><span data-stu-id="36e1c-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36e1c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36e1c-123">Remarks</span></span>

<span data-ttu-id="36e1c-124">Благодаря поддержке привязки данных атрибут **\[ BIND \]** позволяет клиенту получать уведомления при каждом изменении значения свойства.</span><span class="sxs-lookup"><span data-stu-id="36e1c-124">By supporting data binding, the **\[bindable\]** attribute allows the client to be notified whenever a property has changed value.</span></span> <span data-ttu-id="36e1c-125">(Если требуется, чтобы клиент получал уведомления об ожидающих изменениях свойства, используйте атрибут [**\[ рекуестедит \]**](requestedit.md) .)</span><span class="sxs-lookup"><span data-stu-id="36e1c-125">(If you want the client to be notified of impending changes to a property, use the [**\[requestedit\]**](requestedit.md) attribute.)</span></span>

<span data-ttu-id="36e1c-126">Поскольку атрибут, **\[ допускающий привязку \]** , ссылается на свойство в целом, его необходимо указывать везде, где определено свойство.</span><span class="sxs-lookup"><span data-stu-id="36e1c-126">Because the **\[bindable\]** attribute refers to the property as a whole, it must be specified wherever the property is defined.</span></span> <span data-ttu-id="36e1c-127">Поэтому необходимо указать атрибут как для функции доступа к свойствам, так и для функции настройки свойства.</span><span class="sxs-lookup"><span data-stu-id="36e1c-127">Therefore, you need to specify the attribute on both the property-accessing function and the property-setting function.</span></span>

### <a name="flags"></a><span data-ttu-id="36e1c-128">Флаги</span><span class="sxs-lookup"><span data-stu-id="36e1c-128">Flags</span></span>

<span data-ttu-id="36e1c-129">ФУНКФЛАГ \_ фбиндабле, варфлаг \_ фбиндабле</span><span class="sxs-lookup"><span data-stu-id="36e1c-129">FUNCFLAG\_FBINDABLE, VARFLAG\_FBINDABLE</span></span>

## <a name="examples"></a><span data-ttu-id="36e1c-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="36e1c-130">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="36e1c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36e1c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36e1c-132">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="36e1c-132">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="36e1c-133">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="36e1c-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="36e1c-134">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="36e1c-134">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="36e1c-135">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="36e1c-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="36e1c-136">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="36e1c-136">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="36e1c-137">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="36e1c-137">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="36e1c-138">**immediatebind**</span><span class="sxs-lookup"><span data-stu-id="36e1c-138">**immediatebind**</span></span>](immediatebind.md)
</dt> <dt>

[<span data-ttu-id="36e1c-139">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="36e1c-139">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="36e1c-140">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="36e1c-140">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="36e1c-141">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="36e1c-141">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="36e1c-142">**propget**</span><span class="sxs-lookup"><span data-stu-id="36e1c-142">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="36e1c-143">**propput**</span><span class="sxs-lookup"><span data-stu-id="36e1c-143">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="36e1c-144">**propputref**</span><span class="sxs-lookup"><span data-stu-id="36e1c-144">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="36e1c-145">**requestedit**</span><span class="sxs-lookup"><span data-stu-id="36e1c-145">**requestedit**</span></span>](requestedit.md)
</dt> <dt>

[<span data-ttu-id="36e1c-146">**Строка**</span><span class="sxs-lookup"><span data-stu-id="36e1c-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="36e1c-147">типефлагс</span><span class="sxs-lookup"><span data-stu-id="36e1c-147">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="36e1c-148">**vararg**</span><span class="sxs-lookup"><span data-stu-id="36e1c-148">**vararg**</span></span>](vararg.md)
</dt> </dl>

 

 