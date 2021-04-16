---
title: hidden - атрибут
description: Атрибут \ Hidden \ указывает, что элемент существует, но не должен отображаться в браузере, ориентированном на пользователей.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- скрытый атрибут MIDL
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650334"
---
# <a name="hidden-attribute"></a><span data-ttu-id="5875f-104">hidden - атрибут</span><span class="sxs-lookup"><span data-stu-id="5875f-104">hidden attribute</span></span>

<span data-ttu-id="5875f-105">Атрибут **\[ Hidden \]** указывает, что элемент существует, но не должен отображаться в браузере, ориентированном на пользователей.</span><span class="sxs-lookup"><span data-stu-id="5875f-105">The **\[hidden\]** attribute indicates that the item exists but should not be displayed in a user-oriented browser.</span></span>

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="5875f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5875f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5875f-107">*другие атрибуты*</span><span class="sxs-lookup"><span data-stu-id="5875f-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="5875f-108">Ноль или несколько необязательных атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="5875f-108">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="5875f-109">*дерев*</span><span class="sxs-lookup"><span data-stu-id="5875f-109">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="5875f-110">Одна из следующих директив: [**компонент coclass**](coclass.md), [**DISP**](dispinterface.md), [**интерфейс**](interface.md)или [**Библиотека**](library.md).</span><span class="sxs-lookup"><span data-stu-id="5875f-110">One of the following directives: [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), or [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="5875f-111">*имя элемента*</span><span class="sxs-lookup"><span data-stu-id="5875f-111">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5875f-112">Имя, которое другие программные компоненты могут использовать для отделения текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="5875f-112">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="5875f-113">*вирус*</span><span class="sxs-lookup"><span data-stu-id="5875f-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="5875f-114">Указывает инструкции, которые составляют определение элемента.</span><span class="sxs-lookup"><span data-stu-id="5875f-114">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="5875f-115">*тип функции*</span><span class="sxs-lookup"><span data-stu-id="5875f-115">*function-type*</span></span> 
</dt> <dd>

<span data-ttu-id="5875f-116">Тип возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="5875f-116">Return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="5875f-117">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="5875f-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5875f-118">Имя, используемое для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="5875f-118">Name used for invoking the function.</span></span>

</dd> <dt>

<span data-ttu-id="5875f-119">*список необязательных параметров*</span><span class="sxs-lookup"><span data-stu-id="5875f-119">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5875f-120">Ноль или более параметров функции.</span><span class="sxs-lookup"><span data-stu-id="5875f-120">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5875f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5875f-121">Remarks</span></span>

<span data-ttu-id="5875f-122">Атрибут **\[ Hidden \]** позволяет удалять члены интерфейса (путем экранирования их из дальнейшего использования), сохраняя совместимость с существующим кодом.</span><span class="sxs-lookup"><span data-stu-id="5875f-122">The **\[hidden\]** attribute allows you to remove members from your interface (by shielding them from further use) while maintaining compatibility with existing code.</span></span> <span data-ttu-id="5875f-123">Атрибут **\[ Hidden \]** можно использовать для свойств, методов и операторов [**coclass**](coclass.md), [**DISP**](dispinterface.md), [**Interface**](interface.md)и [**Library**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="5875f-123">You can use the **\[hidden\]** attribute on properties, methods, and the [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), and [**library**](library.md) statements.</span></span>

<span data-ttu-id="5875f-124">При указании для библиотеки атрибут **\[ Hidden \]** предотвращает отображение всей библиотеки.</span><span class="sxs-lookup"><span data-stu-id="5875f-124">When specified for a library, the **\[hidden\]** attribute prevents the entire library from being displayed.</span></span> <span data-ttu-id="5875f-125">Этот режим предназначен для использования с элементами управления.</span><span class="sxs-lookup"><span data-stu-id="5875f-125">This usage is intended for use with controls.</span></span> <span data-ttu-id="5875f-126">Узлы должны создать новую библиотеку типов, инкапсулирующую элемент управления с расширенными свойствами.</span><span class="sxs-lookup"><span data-stu-id="5875f-126">Hosts need to create a new type library that wraps the control with extended properties.</span></span>

### <a name="flags"></a><span data-ttu-id="5875f-127">Флаги</span><span class="sxs-lookup"><span data-stu-id="5875f-127">Flags</span></span>

<span data-ttu-id="5875f-128">ВАРФЛАГ \_ фхидден, функфлаг \_ ФХИДДЕН, типефлаг \_ фхидден</span><span class="sxs-lookup"><span data-stu-id="5875f-128">VARFLAG\_FHIDDEN, FUNCFLAG\_FHIDDEN, TYPEFLAG\_FHIDDEN</span></span>

## <a name="examples"></a><span data-ttu-id="5875f-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="5875f-129">Examples</span></span>

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="5875f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5875f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5875f-131">типефлагс</span><span class="sxs-lookup"><span data-stu-id="5875f-131">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="5875f-132">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="5875f-132">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="5875f-133">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="5875f-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="5875f-134">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="5875f-134">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="5875f-135">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="5875f-135">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="5875f-136">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="5875f-136">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="5875f-137">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="5875f-137">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5875f-138">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="5875f-138">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 