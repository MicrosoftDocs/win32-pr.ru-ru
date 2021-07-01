---
title: Функции языка ODL в MIDL
description: Атрибуты, ключевые слова, операторы и директивы языка описания объектов (ODL), которые являются частью MIDL.
ms.assetid: beca14a6-01c4-4605-b1c5-214d48a7f46a
keywords:
- MIDL и ODL MIDL, языковые функции
- ODL MIDL, в MIDL
- ODL MIDL, атрибуты
- ODL MIDL, ключевые слова
- ODL MIDL, инструкции
- ODL MIDL, директивы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db346a664ed7b8f7beeacfe73cc928a924befe10
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119789"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="ecf61-109">Функции языка ODL в MIDL</span><span class="sxs-lookup"><span data-stu-id="ecf61-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="ecf61-110">Средство Mktyplib.exe устарело.</span><span class="sxs-lookup"><span data-stu-id="ecf61-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="ecf61-111">Вместо этого используйте компилятор MIDL.</span><span class="sxs-lookup"><span data-stu-id="ecf61-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="ecf61-112">В следующих разделах перечислены атрибуты, ключевые слова, операторы и директивы языка описания объектов (ODL), которые теперь являются частью язык MIDL (MIDL):</span><span class="sxs-lookup"><span data-stu-id="ecf61-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="ecf61-113">Атрибуты ODL</span><span class="sxs-lookup"><span data-stu-id="ecf61-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="ecf61-114">Ключевые слова, инструкции и директивы ODL</span><span class="sxs-lookup"><span data-stu-id="ecf61-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="ecf61-115">Атрибуты ODL</span><span class="sxs-lookup"><span data-stu-id="ecf61-115">ODL Attributes</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-116">\[[**аппобжект**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-116">\[[**appobject**](appobject.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-117">\[[**привязываемых**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-117">\[[**bindable**](bindable.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-118">\[[**элемента**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-118">\[[**control**](control.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-119">\[[**параметры**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-119">\[[**default**](default.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-120">\[[**максимально**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-121">\[[**дисплайбинд**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-121">\[[**displaybind**](displaybind.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-122">\[[**dllname**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-122">\[[**dllname**](dllname-str-.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-123">\[[**двойной**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-123">\[[**dual**](dual.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-124">\[[**операции**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-124">\[[**entry**](entry.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-125">\[[**HelpContext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-125">\[[**helpcontext**](helpcontext.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-126">\[[**helpstring**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-126">\[[**helpstring**](helpstring.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-127">\[[**HelpFile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-127">\[[**helpfile**](helpfile.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-128">\[[**служеб**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-128">\[[**hidden**](hidden.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-129">\[[**удостоверения**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-129">\[[**id**](id.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-130">\[[**иммедиатебинд**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-130">\[[**immediatebind**](immediatebind.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-131">\[[**окне**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-131">\[[**in**](in.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-132">\[[**намного**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-132">\[[**lcid**](lcid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-133">\[[**обладателем**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-133">\[[**licensed**](licensed.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-134">\[[**nonextensible**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-134">\[[**nonextensible**](nonextensible.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-135">\[[**ODL**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-135">\[[**odl**](odl.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-136">\[[**oleautomation**](oleautomation.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-137">\[[**используемых**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-137">\[[**optional**](optional.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-138">\[[**заполняет**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-138">\[[**out**](out-idl.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-139">\[[**propget**](propget.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-140">\[[**propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-140">\[[**propput**](propput.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-141">\[[**propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-141">\[[**propputref**](propputref.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-142">\[[**закрытый**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-142">\[[**public**](public.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-143">\[[ **только для чтения**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-143">\[ [**readonly**](readonly.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-144">\[[**рекуестедит**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-144">\[[**requestedit**](requestedit.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-145">\[[**зона**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-145">\[[**restricted**](restricted.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-146">\[[**retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-146">\[[**retval**](retval.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-147">\[[**источника**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-147">\[[**source**](source.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-148">\[[**UUID**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-148">\[[**uuid**](uuid.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-149">[**аргумент**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-149">[**vararg**](vararg.md)\]</span></span>
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        <span data-ttu-id="ecf61-150">\[[**Версия**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-150">\[[**version**](version.md)\]</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="ecf61-151">Â</span><span class="sxs-lookup"><span data-stu-id="ecf61-151">Â</span></span>
    :::column-end:::
:::row-end:::

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="ecf61-152">Ключевые слова, инструкции и директивы ODL</span><span class="sxs-lookup"><span data-stu-id="ecf61-152">ODL Keywords, Statements, and Directives</span></span>

[<span data-ttu-id="ecf61-153">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="ecf61-153">**coclass**</span></span>](coclass.md)

[<span data-ttu-id="ecf61-154">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="ecf61-154">**dispinterface**</span></span>](dispinterface.md)

[<span data-ttu-id="ecf61-155">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="ecf61-155">**enum**</span></span>](enum.md)

<span data-ttu-id="ecf61-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="ecf61-156">\[[**importlib**](importlib.md)\]</span></span>

[<span data-ttu-id="ecf61-157">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="ecf61-157">**interface**</span></span>](interface.md)

[<span data-ttu-id="ecf61-158">**Библиотечная**</span><span class="sxs-lookup"><span data-stu-id="ecf61-158">**library**</span></span>](library.md)

[<span data-ttu-id="ecf61-159">**модуль**</span><span class="sxs-lookup"><span data-stu-id="ecf61-159">**module**</span></span>](module.md)

[<span data-ttu-id="ecf61-160">**struct**</span><span class="sxs-lookup"><span data-stu-id="ecf61-160">**struct**</span></span>](struct.md)

[<span data-ttu-id="ecf61-161">**определение**</span><span class="sxs-lookup"><span data-stu-id="ecf61-161">**typedef**</span></span>](typedef.md)

[<span data-ttu-id="ecf61-162">**наборов**</span><span class="sxs-lookup"><span data-stu-id="ecf61-162">**union**</span></span>](union.md)

<span data-ttu-id="ecf61-163">Сведения о том, как маршалировать типы OLE Automation, такие как **BSTR**, **Variant** и **SAFEARRAY**, см. в разделе [маршалирование типов данных OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="ecf61-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




