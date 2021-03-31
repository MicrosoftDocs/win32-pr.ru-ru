---
title: defaultbind - атрибут
description: Атрибут \ дефаултбинд \ указывает единственное, связываемое свойство, которое лучше соответствует объекту.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- атрибут дефаултбинд MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069977"
---
# <a name="defaultbind-attribute"></a><span data-ttu-id="fb3d3-104">defaultbind - атрибут</span><span class="sxs-lookup"><span data-stu-id="fb3d3-104">defaultbind attribute</span></span>

<span data-ttu-id="fb3d3-105">Атрибут **\[ дефаултбинд \]** указывает единственное, связываемое свойство, которое лучше соответствует объекту.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-105">The **\[defaultbind\]** attribute indicates the single, bindable property that best represents the object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="fb3d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb3d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3d3-107">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="fb3d3-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3d3-108">Указывает список из одного или нескольких атрибутов, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="fb3d3-109">При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="fb3d3-110">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="fb3d3-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3d3-111">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="fb3d3-112">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="fb3d3-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3d3-113">Указывает список из одного или нескольких атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-113">Specifies a list of one or more attributes that apply to the function.</span></span> <span data-ttu-id="fb3d3-114">При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-114">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="fb3d3-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="fb3d3-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3d3-116">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="fb3d3-117">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="fb3d3-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3d3-118">Указывает имя функции, к которой будет применен атрибут **\[ дефаултбинд \]** .</span><span class="sxs-lookup"><span data-stu-id="fb3d3-118">Specifies the name of the function to which the **\[defaultbind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="fb3d3-119">*params*</span><span class="sxs-lookup"><span data-stu-id="fb3d3-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3d3-120">Список параметров функции.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb3d3-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb3d3-121">Remarks</span></span>

<span data-ttu-id="fb3d3-122">Свойства, имеющие атрибут **\[ дефаултбинд \]** , также должны иметь атрибут **\[** [**BIND**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fb3d3-122">Properties that have the **\[defaultbind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="fb3d3-123">Только одно свойство в интерфейсе или DISP может иметь атрибут **\[ дефаултбинд \]** .</span><span class="sxs-lookup"><span data-stu-id="fb3d3-123">Only one property in an interface or dispinterface can have the **\[defaultbind\]** attribute.</span></span>

<span data-ttu-id="fb3d3-124">Этот атрибут используется контейнерами, содержащими пользовательскую модель привязки к объекту, а не привязку к свойству объекта.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-124">This attribute is used by containers that have a user model involving binding to an object rather than binding to a property of an object.</span></span> <span data-ttu-id="fb3d3-125">Объект может поддерживать привязку данных, но не имеет этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-125">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="fb3d3-126">Флаги</span><span class="sxs-lookup"><span data-stu-id="fb3d3-126">Flags</span></span>

<span data-ttu-id="fb3d3-127">ФУНКФЛАГ \_ фдефаултбинд, варфлаг \_ фдефаултбинд</span><span class="sxs-lookup"><span data-stu-id="fb3d3-127">FUNCFLAG\_FDEFAULTBIND, VARFLAG\_FDEFAULTBIND</span></span>

## <a name="examples"></a><span data-ttu-id="fb3d3-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="fb3d3-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="fb3d3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb3d3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3d3-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="fb3d3-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="fb3d3-131">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="fb3d3-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="fb3d3-132">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="fb3d3-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="fb3d3-133">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="fb3d3-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="fb3d3-134">типефлагс</span><span class="sxs-lookup"><span data-stu-id="fb3d3-134">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 