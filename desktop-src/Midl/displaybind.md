---
title: displaybind - атрибут
description: Атрибут \ дисплайбинд \ указывает свойство, которое должно быть отображено пользователю как связываемое.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- атрибут дисплайбинд MIDL
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790225"
---
# <a name="displaybind-attribute"></a><span data-ttu-id="abd9a-104">displaybind - атрибут</span><span class="sxs-lookup"><span data-stu-id="abd9a-104">displaybind attribute</span></span>

<span data-ttu-id="abd9a-105">Атрибут **\[ дисплайбинд \]** указывает свойство, которое должно быть отображено пользователю как связываемое.</span><span class="sxs-lookup"><span data-stu-id="abd9a-105">The **\[displaybind\]** attribute indicates a property that should be displayed to the user as bindable.</span></span>

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="abd9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="abd9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd9a-107">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="abd9a-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="abd9a-108">Указывает необязательный список атрибутов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="abd9a-108">Specifies an optional list of interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="abd9a-109">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="abd9a-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="abd9a-110">Имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="abd9a-110">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="abd9a-111">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="abd9a-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="abd9a-112">Задает список из одного или нескольких атрибутов, разделенных запятыми, которые применяются к типу возвращаемых функцией значений.</span><span class="sxs-lookup"><span data-stu-id="abd9a-112">Specifies a list of one or more attributes, separated by commas, that apply to the function-return type.</span></span>

</dd> <dt>

<span data-ttu-id="abd9a-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="abd9a-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="abd9a-114">Указывает тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="abd9a-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="abd9a-115">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="abd9a-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="abd9a-116">Указывает имя функции, к которой будет применен атрибут **\[ дисплайбинд \]** .</span><span class="sxs-lookup"><span data-stu-id="abd9a-116">Specifies the name of the function to which the **\[displaybind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="abd9a-117">*params*</span><span class="sxs-lookup"><span data-stu-id="abd9a-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="abd9a-118">Список параметров функции.</span><span class="sxs-lookup"><span data-stu-id="abd9a-118">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abd9a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abd9a-119">Remarks</span></span>

<span data-ttu-id="abd9a-120">Свойства, имеющие атрибут **\[ дисплайбинд \]** , также должны иметь атрибут **\[** [**BIND**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="abd9a-120">Properties that have the **\[displaybind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="abd9a-121">Объект может поддерживать привязку данных, но не имеет этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="abd9a-121">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="abd9a-122">Флаги</span><span class="sxs-lookup"><span data-stu-id="abd9a-122">Flags</span></span>

<span data-ttu-id="abd9a-123">ФУНКФЛАГ \_ фдисплайбинд, варфлаг \_ фдисплайбинд</span><span class="sxs-lookup"><span data-stu-id="abd9a-123">FUNCFLAG\_FDISPLAYBIND, VARFLAG\_FDISPLAYBIND</span></span>

## <a name="examples"></a><span data-ttu-id="abd9a-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="abd9a-124">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="abd9a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abd9a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd9a-126">**bindable**</span><span class="sxs-lookup"><span data-stu-id="abd9a-126">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="abd9a-127">типефлагс</span><span class="sxs-lookup"><span data-stu-id="abd9a-127">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="abd9a-128">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="abd9a-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="abd9a-129">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="abd9a-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="abd9a-130">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="abd9a-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 