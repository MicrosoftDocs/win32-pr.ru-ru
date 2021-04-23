---
title: restricted - атрибут
description: Атрибут \ Restricted указывает, что библиотека, или член модуля, интерфейса или DISP, не может вызываться произвольным образом.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- ограниченный атрибут MIDL
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412895"
---
# <a name="restricted-attribute"></a><span data-ttu-id="84b92-104">restricted - атрибут</span><span class="sxs-lookup"><span data-stu-id="84b92-104">restricted attribute</span></span>

<span data-ttu-id="84b92-105">Атрибут **\[ Restricted \]** указывает, что библиотеку, член модуля, интерфейса или disp-интерфейсов, нельзя вызывать произвольным образом.</span><span class="sxs-lookup"><span data-stu-id="84b92-105">The **\[restricted\]** attribute specifies that a library, or member of a module, interface, or dispinterface cannot be called arbitrarily.</span></span>

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a><span data-ttu-id="84b92-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84b92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84b92-107">*другие атрибуты*</span><span class="sxs-lookup"><span data-stu-id="84b92-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="84b92-108">Ноль или несколько атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="84b92-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="84b92-109">*оператор-тип*</span><span class="sxs-lookup"><span data-stu-id="84b92-109">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="84b92-110">Один из следующих: [**Библиотека**](library.md), [**модуль**](module.md), [**интерфейс**](interface.md), [**DISP**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="84b92-110">One of the following: [**library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="84b92-111">*имя оператора*</span><span class="sxs-lookup"><span data-stu-id="84b92-111">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="84b92-112">Идентификатор, по которому программное обеспечение ссылается на эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="84b92-112">The identifier by which the software refers to this statement.</span></span>

</dd> <dt>

<span data-ttu-id="84b92-113">*вирус*</span><span class="sxs-lookup"><span data-stu-id="84b92-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="84b92-114">Языковые элементы MIDL, определяющие содержимое этой инструкции.</span><span class="sxs-lookup"><span data-stu-id="84b92-114">MIDL language elements that define the contents of this statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84b92-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84b92-115">Remarks</span></span>

<span data-ttu-id="84b92-116">Этот атрибут позволяет управлять доступом к элементам интерфейсов, библиотек, модулей и диспетчерских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="84b92-116">This attribute enables you to control access to elements of interfaces, libraries, modules, and dispinterfaces.</span></span> <span data-ttu-id="84b92-117">Например, это может препятствовать тому, что элемент данных будет использоваться программистом макроса.</span><span class="sxs-lookup"><span data-stu-id="84b92-117">For example, it can prevent a data item from being used by a macro programmer.</span></span> <span data-ttu-id="84b92-118">Этот атрибут можно применить к члену [**класса coclass**](coclass.md), независимо от того, является ли элемент DISP или интерфейсом, и независимо от того, является ли элемент приемником (входящим) или источником (исходящим).</span><span class="sxs-lookup"><span data-stu-id="84b92-118">You can apply this attribute to a member of a [**coclass**](coclass.md), independent of whether the member is a dispinterface or interface, and independent of whether the member is a sink (incoming) or source (outgoing).</span></span> <span data-ttu-id="84b92-119">Член **coclass** не может иметь как **\[ ограниченный \]** атрибут, так и атрибуты **\[ по умолчанию \]** .</span><span class="sxs-lookup"><span data-stu-id="84b92-119">A member of a **coclass** cannot have both the **\[restricted\]** and **\[default\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="84b92-120">Флаги</span><span class="sxs-lookup"><span data-stu-id="84b92-120">Flags</span></span>

<span data-ttu-id="84b92-121">ИМПЛТИПЕФЛАГ \_ фрестриктед, функфлаг \_ фрестриктед</span><span class="sxs-lookup"><span data-stu-id="84b92-121">IMPLTYPEFLAG\_FRESTRICTED, FUNCFLAG\_FRESTRICTED</span></span>

## <a name="examples"></a><span data-ttu-id="84b92-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="84b92-122">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a><span data-ttu-id="84b92-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84b92-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b92-124">типефлагс</span><span class="sxs-lookup"><span data-stu-id="84b92-124">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="84b92-125">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="84b92-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="84b92-126">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="84b92-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="84b92-127">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="84b92-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="84b92-128">**модуль**</span><span class="sxs-lookup"><span data-stu-id="84b92-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="84b92-129">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="84b92-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="84b92-130">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="84b92-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="84b92-131">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="84b92-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 