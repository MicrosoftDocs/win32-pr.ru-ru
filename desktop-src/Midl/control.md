---
title: атрибут элемента управления
description: Атрибут \ Control \ определяет компонентный класс или библиотеку как элемент управления COM, из которого сайт контейнера будет наследовать дополнительные библиотеки типов или классы объектов компонентов.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- атрибут элемента управления MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789865"
---
# <a name="control-attribute"></a><span data-ttu-id="c9ff3-104">атрибут элемента управления</span><span class="sxs-lookup"><span data-stu-id="c9ff3-104">control attribute</span></span>

<span data-ttu-id="c9ff3-105">Атрибут **\[ Control \]** определяет компонентный [**класс**](coclass.md) или [**библиотеку**](library.md) как элемент управления COM, из которого сайт контейнера будет наследовать дополнительные библиотеки типов или классы объектов компонентов.</span><span class="sxs-lookup"><span data-stu-id="c9ff3-105">The **\[control\]** attribute identifies a [**coclass**](coclass.md) or [**library**](library.md) as a COM control, from which a container site will derive additional type libraries or component object classes.</span></span>

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a><span data-ttu-id="c9ff3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9ff3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ff3-107">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="c9ff3-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ff3-108">Указывает ноль или более атрибутов, применимых к оператору [**Library**](library.md) или [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="c9ff3-108">Specifies zero or more attributes that apply to the [**library**](library.md) or [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="c9ff3-109">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="c9ff3-109">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c9ff3-110">*lib-или-коclassname*</span><span class="sxs-lookup"><span data-stu-id="c9ff3-110">*lib-or-coclassname*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ff3-111">Указывает имя [**библиотеки**](library.md) или [**компонентного класса**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="c9ff3-111">Specifies the name of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9ff3-112">*вирус*</span><span class="sxs-lookup"><span data-stu-id="c9ff3-112">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ff3-113">Операторы MIDL, задающих члены [**библиотеки**](library.md) или [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="c9ff3-113">MIDL statements that specify the members of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9ff3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9ff3-114">Remarks</span></span>

<span data-ttu-id="c9ff3-115">Этот атрибут позволяет помечать библиотеки типов, описывающие элементы управления, так что они не будут отображаться в браузерах типов, предназначенных для невизуальных объектов.</span><span class="sxs-lookup"><span data-stu-id="c9ff3-115">This attribute allows you to mark type libraries that describe controls so they will not be displayed in type browsers intended for nonvisual objects.</span></span>

### <a name="flags"></a><span data-ttu-id="c9ff3-116">Флаги</span><span class="sxs-lookup"><span data-stu-id="c9ff3-116">Flags</span></span>

<span data-ttu-id="c9ff3-117">ТИПЕФЛАГ \_ фконтрол, либфлаг \_ фконтрол</span><span class="sxs-lookup"><span data-stu-id="c9ff3-117">TYPEFLAG\_FCONTROL, LIBFLAG\_FCONTROL</span></span>

## <a name="examples"></a><span data-ttu-id="c9ff3-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="c9ff3-118">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a><span data-ttu-id="c9ff3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9ff3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ff3-120">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="c9ff3-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c9ff3-121">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="c9ff3-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c9ff3-122">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="c9ff3-122">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="c9ff3-123">типефлагс</span><span class="sxs-lookup"><span data-stu-id="c9ff3-123">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="c9ff3-124">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="c9ff3-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="c9ff3-125">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="c9ff3-125">**library**</span></span>](library.md)
</dt> </dl>

 

 