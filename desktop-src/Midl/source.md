---
title: source - атрибут
description: Атрибут \ Source \ указывает, что член класса, свойства или метода является источником событий. Для члена класса coclass этот атрибут означает, что элемент вызывается, а не реализован.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- Исходный атрибут MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987385"
---
# <a name="source-attribute"></a><span data-ttu-id="7d6a1-105">source - атрибут</span><span class="sxs-lookup"><span data-stu-id="7d6a1-105">source attribute</span></span>

<span data-ttu-id="7d6a1-106">Атрибут **\[ source \]** указывает на то, что член [**класса**](coclass.md), свойства или метода является источником событий.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-106">The **\[source\]** attribute indicates that a member of a [**coclass**](coclass.md), property, or method is a source of events.</span></span> <span data-ttu-id="7d6a1-107">Для члена **класса coclass** этот атрибут означает, что элемент вызывается, а не реализован.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-107">For a member of a **coclass**, this attribute means that the member is called rather than implemented.</span></span>

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="7d6a1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d6a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6a1-109">*атрибуты coclass*</span><span class="sxs-lookup"><span data-stu-id="7d6a1-109">*coclass-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a1-110">Ноль или более атрибутов, которые будут применены к [**компонентному классу**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="7d6a1-110">Zero or more attributes that will be applied to the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d6a1-111">*имя класса*</span><span class="sxs-lookup"><span data-stu-id="7d6a1-111">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a1-112">Идентификатор имени [**компонентного класса**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="7d6a1-112">The name identifier of the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d6a1-113">*необязательные атрибуты*</span><span class="sxs-lookup"><span data-stu-id="7d6a1-113">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a1-114">Ноль или несколько атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-114">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="7d6a1-115">*оператор-тип*</span><span class="sxs-lookup"><span data-stu-id="7d6a1-115">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a1-116">Может быть [**интерфейсом**](interface.md) или [**DISP**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="7d6a1-116">Can be [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d6a1-117">*имя оператора*</span><span class="sxs-lookup"><span data-stu-id="7d6a1-117">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a1-118">Имя [**интерфейса**](interface.md) или [**DISP**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="7d6a1-118">The name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d6a1-119">*Object-Type*</span><span class="sxs-lookup"><span data-stu-id="7d6a1-119">*object-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a1-120">Тип объекта, возвращаемого методом.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-120">The type of the object that the method returns.</span></span> <span data-ttu-id="7d6a1-121">Этот объект является источником событий.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-121">This object is a source of events.</span></span>

</dd> <dt>

<span data-ttu-id="7d6a1-122">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="7d6a1-122">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a1-123">Имя метода в [**интерфейсе**](interface.md) или [**DISP**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="7d6a1-123">The name of a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d6a1-124">*список необязательных параметров*</span><span class="sxs-lookup"><span data-stu-id="7d6a1-124">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a1-125">Ноль или более параметров метода.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-125">Zero or more method parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d6a1-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d6a1-126">Remarks</span></span>

<span data-ttu-id="7d6a1-127">В свойстве или методе **\[ исходный \]** атрибут указывает, что член возвращает объект или вариант, являющийся источником событий.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-127">On a property or method, the **\[source\]** attribute indicates that the member returns an object or VARIANT that is a source of events.</span></span> <span data-ttu-id="7d6a1-128">Объект реализует **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="7d6a1-128">The object implements **IConnectionPointContainer**.</span></span>

### <a name="flags"></a><span data-ttu-id="7d6a1-129">Флаги</span><span class="sxs-lookup"><span data-stu-id="7d6a1-129">Flags</span></span>

<span data-ttu-id="7d6a1-130">ИМПЛТИПЕФЛАГ \_ фсаурце, \_ источник варфлаг, \_ источник функфлаг</span><span class="sxs-lookup"><span data-stu-id="7d6a1-130">IMPLTYPEFLAG\_FSOURCE, VARFLAG\_SOURCE, FUNCFLAG\_SOURCE</span></span>

## <a name="examples"></a><span data-ttu-id="7d6a1-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="7d6a1-131">Examples</span></span>

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a><span data-ttu-id="7d6a1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d6a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d6a1-133">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="7d6a1-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="7d6a1-134">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="7d6a1-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="7d6a1-135">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="7d6a1-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7d6a1-136">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="7d6a1-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="7d6a1-137">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="7d6a1-137">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7d6a1-138">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="7d6a1-138">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7d6a1-139">типефлагс</span><span class="sxs-lookup"><span data-stu-id="7d6a1-139">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 