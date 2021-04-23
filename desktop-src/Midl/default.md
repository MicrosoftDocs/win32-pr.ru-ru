---
title: default - атрибут
description: Атрибут \ Default \ указывает, что интерфейс или DISP, определенные в компонентном классе, представляют интерфейс программирования по умолчанию. Этот атрибут предназначен для использования в языках макросов.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- атрибут по умолчанию MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487585"
---
# <a name="default-attribute"></a><span data-ttu-id="cad49-105">default - атрибут</span><span class="sxs-lookup"><span data-stu-id="cad49-105">default attribute</span></span>

<span data-ttu-id="cad49-106">Атрибут **\[ по \] умолчанию** указывает, что [**интерфейс**](interface.md) или [**DISP**](dispinterface.md), определенный в [**компонентном классе**](coclass.md), представляет интерфейс программирования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cad49-106">The **\[default\]** attribute Indicates that the [**interface**](interface.md) or [**dispinterface**](dispinterface.md), defined within a [**coclass**](coclass.md), represents the default programmability interface.</span></span> <span data-ttu-id="cad49-107">Этот атрибут предназначен для использования в языках макросов.</span><span class="sxs-lookup"><span data-stu-id="cad49-107">This attribute is intended for use by macro languages.</span></span>

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a><span data-ttu-id="cad49-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cad49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cad49-109">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="cad49-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="cad49-110">Задает универсальный уникальный идентификационный номер для [**компонентного класса**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="cad49-110">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="cad49-111">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="cad49-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="cad49-112">Задает дополнительные атрибуты [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="cad49-112">Specifies additional [**coclass**](coclass.md) attributes.</span></span> <span data-ttu-id="cad49-113">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="cad49-113">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="cad49-114">*имя класса*</span><span class="sxs-lookup"><span data-stu-id="cad49-114">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cad49-115">Указывает имя, по которому другие программные компоненты могут ссылаться [**на этот компонент**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="cad49-115">Specifies the name by which other software components can reference this [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="cad49-116">*Необязательный атрибут-Interface-*</span><span class="sxs-lookup"><span data-stu-id="cad49-116">*optional-interface-attribute*</span></span> 
</dt> <dd>

<span data-ttu-id="cad49-117">**\[** [**Исходный**](source.md) **\]** атрибут, указывающий, что интерфейс или DISP-интерфейсы является исходящим, является единственным другим атрибутом, который можно использовать здесь.</span><span class="sxs-lookup"><span data-stu-id="cad49-117">The **\[**[**source**](source.md)**\]** attribute, which specifies that an interface or dispinterface is outgoing, is the only other attribute that can be used here.</span></span>

</dd> <dt>

<span data-ttu-id="cad49-118">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="cad49-118">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="cad49-119">Указывает имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cad49-119">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cad49-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cad49-120">Remarks</span></span>

<span data-ttu-id="cad49-121">[**Компонентный класс**](coclass.md) может иметь не более двух элементов **\[ по умолчанию \]** .</span><span class="sxs-lookup"><span data-stu-id="cad49-121">A [**coclass**](coclass.md) may have at most two **\[default\]** members.</span></span> <span data-ttu-id="cad49-122">Один представляет исходящий (исходный) интерфейс, а другой — входящий (приемник) интерфейс или DISP.</span><span class="sxs-lookup"><span data-stu-id="cad49-122">One represents the outgoing (source) interface or dispinterface, and the other represents the incoming (sink) interface or dispinterface.</span></span> <span data-ttu-id="cad49-123">Если атрибут **\[ по \] умолчанию** не указан ни для одного члена **класса coclass** или **котипа**, то первые исходящие и входящие члены, не имеющие **\[** атрибута [**Restricted**](restricted.md) , **\]** рассматриваются как значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cad49-123">If the **\[default\]** attribute is not specified for any member of the **coclass** or **cotype**, the first outgoing and incoming members that do not have the **\[**[**restricted**](restricted.md)**\]** attribute are treated as the defaults.</span></span>

### <a name="flags"></a><span data-ttu-id="cad49-124">Флаги</span><span class="sxs-lookup"><span data-stu-id="cad49-124">Flags</span></span>

<span data-ttu-id="cad49-125">ИМПЛТИПЕФЛАГ \_ фдефаулт</span><span class="sxs-lookup"><span data-stu-id="cad49-125">IMPLTYPEFLAG\_FDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="cad49-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="cad49-126">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a><span data-ttu-id="cad49-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cad49-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad49-128">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="cad49-128">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="cad49-129">типефлагс</span><span class="sxs-lookup"><span data-stu-id="cad49-129">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="cad49-130">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="cad49-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="cad49-131">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="cad49-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="cad49-132">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="cad49-132">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="cad49-133">**зона**</span><span class="sxs-lookup"><span data-stu-id="cad49-133">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="cad49-134">**источника**</span><span class="sxs-lookup"><span data-stu-id="cad49-134">**source**</span></span>](source.md)
</dt> </dl>

 

 