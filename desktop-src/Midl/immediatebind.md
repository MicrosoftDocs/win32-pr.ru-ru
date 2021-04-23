---
title: immediatebind - атрибут
description: Атрибут \ иммедиатебинд \ указывает, что база данных будет уведомлена сразу обо всех изменениях свойства объекта, привязанного к данным.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- атрибут иммедиатебинд MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260479"
---
# <a name="immediatebind-attribute"></a><span data-ttu-id="9376a-104">immediatebind - атрибут</span><span class="sxs-lookup"><span data-stu-id="9376a-104">immediatebind attribute</span></span>

<span data-ttu-id="9376a-105">Атрибут **\[ иммедиатебинд \]** указывает, что база данных будет уведомлена сразу обо всех изменениях свойства объекта, привязанного к данным.</span><span class="sxs-lookup"><span data-stu-id="9376a-105">The **\[immediatebind\]** attribute indicates that the database will be notified immediately of all changes to a property of a data-bound object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="9376a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9376a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9376a-107">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="9376a-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9376a-108">Указывает список из одного или нескольких атрибутов, которые применяются к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="9376a-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="9376a-109">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="9376a-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9376a-110">Указывает имя [**интерфейса**](interface.md) или [**DISP**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="9376a-110">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="9376a-111">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="9376a-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9376a-112">Ноль или более атрибутов функций.</span><span class="sxs-lookup"><span data-stu-id="9376a-112">Zero or more function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="9376a-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="9376a-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="9376a-114">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="9376a-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="9376a-115">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="9376a-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9376a-116">Указывает имя функции в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="9376a-116">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="9376a-117">*params*</span><span class="sxs-lookup"><span data-stu-id="9376a-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="9376a-118">Ноль или более параметров функции.</span><span class="sxs-lookup"><span data-stu-id="9376a-118">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9376a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9376a-119">Remarks</span></span>

<span data-ttu-id="9376a-120">Атрибут **\[ иммедиатебинд \]** позволяет элементам управления различать свойства, которые должны уведомлять базу данных о каждом изменении, и те, которые не имеют.</span><span class="sxs-lookup"><span data-stu-id="9376a-120">The **\[immediatebind\]** attribute allows controls to differentiate between properties that need to notify the database of every change, and those that do not.</span></span> <span data-ttu-id="9376a-121">Например, каждое изменение элемента управления CheckBox должно быть немедленно отправлено в базовую базу данных, даже если элемент управления не потерял фокус.</span><span class="sxs-lookup"><span data-stu-id="9376a-121">For example, every change to a checkbox control should be sent to the underlying database immediately, even if the control has not lost the focus.</span></span> <span data-ttu-id="9376a-122">Однако для элемента управления ListBox изменение происходит при выделении другого выделения.</span><span class="sxs-lookup"><span data-stu-id="9376a-122">However, for a listbox control, a change occurs whenever a different selection is highlighted.</span></span> <span data-ttu-id="9376a-123">Уведомление базы данных об изменении до того, как элемент управления теряет фокус, будет неэффективным и ненужным.</span><span class="sxs-lookup"><span data-stu-id="9376a-123">Notifying the database of a change before the control loses focus would be inefficient and unnecessary.</span></span> <span data-ttu-id="9376a-124">Атрибут **\[ иммедиатебинд \]** позволяет указать, установив бит иммедиатебинд, отдельные свойства формы, изменения которых следует сообщить немедленно.</span><span class="sxs-lookup"><span data-stu-id="9376a-124">The **\[immediatebind\]** attribute allows you to specify, by setting the ImmediateBind bit, individual properties on a form whose changes should be reported immediately.</span></span>

<span data-ttu-id="9376a-125">Свойства, имеющие атрибут **\[ иммедиатебинд \]** , также должны иметь атрибут **\[** [**BIND**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="9376a-125">Properties that have the **\[immediatebind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="9376a-126">Флаги</span><span class="sxs-lookup"><span data-stu-id="9376a-126">Flags</span></span>

<span data-ttu-id="9376a-127">ФУНКФЛАГ \_ фиммедиатебинд, варфлаг \_ фиммедиатебинд</span><span class="sxs-lookup"><span data-stu-id="9376a-127">FUNCFLAG\_FIMMEDIATEBIND, VARFLAG\_FIMMEDIATEBIND</span></span>

## <a name="examples"></a><span data-ttu-id="9376a-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="9376a-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="9376a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9376a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9376a-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="9376a-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="9376a-131">**типефлагс**</span><span class="sxs-lookup"><span data-stu-id="9376a-131">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="9376a-132">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="9376a-132">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="9376a-133">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="9376a-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="9376a-134">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="9376a-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="9376a-135">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="9376a-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="9376a-136">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="9376a-136">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 