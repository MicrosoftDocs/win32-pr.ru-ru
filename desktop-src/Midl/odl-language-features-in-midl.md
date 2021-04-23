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
ms.openlocfilehash: 49e525322eb185e38303b387dc4aa0007322e713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888967"
---
# <a name="odl-language-features-in-midl"></a><span data-ttu-id="01914-109">Функции языка ODL в MIDL</span><span class="sxs-lookup"><span data-stu-id="01914-109">ODL Language Features in MIDL</span></span>

> [!Note]  
> <span data-ttu-id="01914-110">Средство Mktyplib.exe устарело.</span><span class="sxs-lookup"><span data-stu-id="01914-110">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="01914-111">Вместо этого используйте компилятор MIDL.</span><span class="sxs-lookup"><span data-stu-id="01914-111">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="01914-112">В следующих разделах перечислены атрибуты, ключевые слова, операторы и директивы языка описания объектов (ODL), которые теперь являются частью язык MIDL (MIDL):</span><span class="sxs-lookup"><span data-stu-id="01914-112">The following topics list the Object Description Language (ODL) attributes, keywords, statements, and directives that are now part of the Microsoft Interface Definition Language (MIDL):</span></span>

-   [<span data-ttu-id="01914-113">Атрибуты ODL</span><span class="sxs-lookup"><span data-stu-id="01914-113">ODL Attributes</span></span>](#odl-attributes)
-   [<span data-ttu-id="01914-114">Ключевые слова, инструкции и директивы ODL</span><span class="sxs-lookup"><span data-stu-id="01914-114">ODL Keywords, Statements, and Directives</span></span>](#odl-keywords-statements-and-directives)

## <a name="odl-attributes"></a><span data-ttu-id="01914-115">Атрибуты ODL</span><span class="sxs-lookup"><span data-stu-id="01914-115">ODL Attributes</span></span>



|                                            |                                        |
|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="01914-116">\[[**аппобжект**](appobject.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-116">\[[**appobject**](appobject.md)\]</span></span>         | <span data-ttu-id="01914-117">\[[**привязываемых**](bindable.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-117">\[[**bindable**](bindable.md)\]</span></span>       |
| <span data-ttu-id="01914-118">\[[**элемента**](control.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-118">\[[**control**](control.md)\]</span></span>             | <span data-ttu-id="01914-119">\[[**параметры**](default.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-119">\[[**default**](default.md)\]</span></span>         |
| <span data-ttu-id="01914-120">\[[**максимально**](defaultvalue.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-120">\[[**defaultvalue**](defaultvalue.md)\]</span></span>   | <span data-ttu-id="01914-121">\[[**дисплайбинд**](displaybind.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-121">\[[**displaybind**](displaybind.md)\]</span></span> |
| <span data-ttu-id="01914-122">\[[**dllname**](dllname-str-.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-122">\[[**dllname**](dllname-str-.md)\]</span></span>        | <span data-ttu-id="01914-123">\[[**двойной**](dual.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-123">\[[**dual**](dual.md)\]</span></span>               |
| <span data-ttu-id="01914-124">\[[**операции**](entry.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-124">\[[**entry**](entry.md)\]</span></span>                 | <span data-ttu-id="01914-125">\[[**HelpContext**](helpcontext.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-125">\[[**helpcontext**](helpcontext.md)\]</span></span> |
| <span data-ttu-id="01914-126">\[[**helpstring**](helpstring.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-126">\[[**helpstring**](helpstring.md)\]</span></span>       | <span data-ttu-id="01914-127">\[[**HelpFile**](helpfile.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-127">\[[**helpfile**](helpfile.md)\]</span></span>       |
| <span data-ttu-id="01914-128">\[[**служеб**](hidden.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-128">\[[**hidden**](hidden.md)\]</span></span>               | <span data-ttu-id="01914-129">\[[**удостоверения**](id.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-129">\[[**id**](id.md)\]</span></span>                   |
| <span data-ttu-id="01914-130">\[[**иммедиатебинд**](immediatebind.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-130">\[[**immediatebind**](immediatebind.md)\]</span></span> | <span data-ttu-id="01914-131">\[[**окне**](in.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-131">\[[**in**](in.md)\]</span></span>                   |
| <span data-ttu-id="01914-132">\[[**намного**](lcid.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-132">\[[**lcid**](lcid.md)\]</span></span>                   | <span data-ttu-id="01914-133">\[[**обладателем**](licensed.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-133">\[[**licensed**](licensed.md)\]</span></span>       |
| <span data-ttu-id="01914-134">\[[**nonextensible**](nonextensible.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-134">\[[**nonextensible**](nonextensible.md)\]</span></span> | <span data-ttu-id="01914-135">\[[**ODL**](odl.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-135">\[[**odl**](odl.md)\]</span></span>                 |
| <span data-ttu-id="01914-136">\[[**oleautomation**](oleautomation.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-136">\[[**oleautomation**](oleautomation.md)\]</span></span> | <span data-ttu-id="01914-137">\[[**используемых**](optional.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-137">\[[**optional**](optional.md)\]</span></span>       |
| <span data-ttu-id="01914-138">\[[**заполняет**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-138">\[[**out**](out-idl.md)\]</span></span>                 | <span data-ttu-id="01914-139">\[[**propget**](propget.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-139">\[[**propget**](propget.md)\]</span></span>         |
| <span data-ttu-id="01914-140">\[[**propput**](propput.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-140">\[[**propput**](propput.md)\]</span></span>             | <span data-ttu-id="01914-141">\[[**propputref**](propputref.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-141">\[[**propputref**](propputref.md)\]</span></span>   |
| <span data-ttu-id="01914-142">\[[**закрытый**](public.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-142">\[[**public**](public.md)\]</span></span>               | <span data-ttu-id="01914-143">\[[ **только для чтения**](readonly.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-143">\[ [**readonly**](readonly.md)\]</span></span>      |
| <span data-ttu-id="01914-144">\[[**рекуестедит**](requestedit.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-144">\[[**requestedit**](requestedit.md)\]</span></span>     | <span data-ttu-id="01914-145">\[[**зона**](restricted.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-145">\[[**restricted**](restricted.md)\]</span></span>   |
| <span data-ttu-id="01914-146">\[[**retval**](retval.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-146">\[[**retval**](retval.md)\]</span></span>               | <span data-ttu-id="01914-147">\[[**источника**](source.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-147">\[[**source**](source.md)\]</span></span>           |
| <span data-ttu-id="01914-148">\[[**UUID**](uuid.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-148">\[[**uuid**](uuid.md)\]</span></span>                   | <span data-ttu-id="01914-149">[**аргумент**](vararg.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-149">[**vararg**](vararg.md)\]</span></span>             |
| <span data-ttu-id="01914-150">\[[**Версия**](version.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-150">\[[**version**](version.md)\]</span></span>             | <span data-ttu-id="01914-151">Â</span><span class="sxs-lookup"><span data-stu-id="01914-151">Â</span></span>                                      |



 

## <a name="odl-keywords-statements-and-directives"></a><span data-ttu-id="01914-152">Ключевые слова, инструкции и директивы ODL</span><span class="sxs-lookup"><span data-stu-id="01914-152">ODL Keywords, Statements, and Directives</span></span>



|                                        |
|----------------------------------------|
| [<span data-ttu-id="01914-153">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="01914-153">**coclass**</span></span>](coclass.md)             |
| [<span data-ttu-id="01914-154">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="01914-154">**dispinterface**</span></span>](dispinterface.md) |
| [<span data-ttu-id="01914-155">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="01914-155">**enum**</span></span>](enum.md)                   |
| <span data-ttu-id="01914-156">\[[**importlib**](importlib.md)\]</span><span class="sxs-lookup"><span data-stu-id="01914-156">\[[**importlib**](importlib.md)\]</span></span>     |
| [<span data-ttu-id="01914-157">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="01914-157">**interface**</span></span>](interface.md)         |
| [<span data-ttu-id="01914-158">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="01914-158">**library**</span></span>](library.md)             |
| [<span data-ttu-id="01914-159">**модуль**</span><span class="sxs-lookup"><span data-stu-id="01914-159">**module**</span></span>](module.md)               |
| [<span data-ttu-id="01914-160">**struct**</span><span class="sxs-lookup"><span data-stu-id="01914-160">**struct**</span></span>](struct.md)               |
| [<span data-ttu-id="01914-161">**определение**</span><span class="sxs-lookup"><span data-stu-id="01914-161">**typedef**</span></span>](typedef.md)             |
| [<span data-ttu-id="01914-162">**наборов**</span><span class="sxs-lookup"><span data-stu-id="01914-162">**union**</span></span>](union.md)                 |



 

<span data-ttu-id="01914-163">Сведения о том, как маршалировать типы OLE Automation, такие как **BSTR**, **Variant** и **SAFEARRAY**, см. в разделе [маршалирование типов данных OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="01914-163">For information on how to marshal OLE Automation types, such as **BSTR**, **VARIANT**, and **SAFEARRAY**, see [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




