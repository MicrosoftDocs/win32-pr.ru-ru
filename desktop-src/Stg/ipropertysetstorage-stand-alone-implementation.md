---
title: IPropertySetStorage — изолированная реализация
description: Предоставляемая системой изолированная реализация IPropertySetStorage включает реализацию как Ипропертистораже, так и IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Стрктд STG, реализации
- IPropertySetStorage Стрктд STG, реализации, автономные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070111"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a><span data-ttu-id="5baa4-105">IPropertySetStorage — изолированная реализация</span><span class="sxs-lookup"><span data-stu-id="5baa4-105">IPropertySetStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="5baa4-106">Предоставляемая системой изолированная реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) включает реализацию как [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , так и **IPropertySetStorage**. [**Ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) — это интерфейс, который считывает и записывает свойства в хранилище набора свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of both [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and **IPropertySetStorage**.[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) is the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="5baa4-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) — это интерфейс, который создает и открывает наборы свойств в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5baa4-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) is the interface that creates and opens property sets in a storage.</span></span> <span data-ttu-id="5baa4-108">Интерфейсы [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) и [**иенумстатпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) также предоставляются в изолированной реализации.</span><span class="sxs-lookup"><span data-stu-id="5baa4-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="5baa4-109">Чтобы использовать изолированную реализацию [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), сначала получите указатель на предоставляемую системой изолированную реализацию и свяжите предоставленную системой реализацию с объектом хранилища.</span><span class="sxs-lookup"><span data-stu-id="5baa4-109">To use the stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), first obtain a pointer to the system-provided, stand-alone implementation and associate the system-provided implementation with your storage object.</span></span> <span data-ttu-id="5baa4-110">Чтобы получить указатель на изолированную реализацию **IPropertySetStorage**, вызовите функцию [**стгкреатепропсетстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) и укажите параметр *пстораже* , указывающий объект хранилища, который будет содержать набор свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-110">To get a pointer to the stand-alone implementation of **IPropertySetStorage**, call the [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) function and provide the *pStorage* parameter specifying the storage object that will contain the property set.</span></span> <span data-ttu-id="5baa4-111">Эта функция предоставляет указатель на новый интерфейс **IPropertySetStorage** для указанного объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="5baa4-111">This function provides a pointer to the new **IPropertySetStorage** interface for the specified storage object.</span></span>

<span data-ttu-id="5baa4-112">Изолированная реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) создает наборы свойств для любого объекта хранилища, а не только для хранилищ составных файлов.</span><span class="sxs-lookup"><span data-stu-id="5baa4-112">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) creates property sets on any storage object, not just on compound file storages.</span></span> <span data-ttu-id="5baa4-113">Изолированная реализация не зависит от составных файлов и может использоваться с любой реализацией структурированных хранилищ.</span><span class="sxs-lookup"><span data-stu-id="5baa4-113">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="5baa4-114">Все ограничения на предоставляемые вызывающим объектом структурированные хранилища применяются к этой реализации наборов свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-114">Any restrictions on the caller-provided structured storages apply to this implementation of property sets.</span></span> <span data-ttu-id="5baa4-115">Например, если вы предоставляете хранилище в простом режиме для [**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), полученный **IPropertySetStorage** будет ограничен предоставленным [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).</span><span class="sxs-lookup"><span data-stu-id="5baa4-115">For example, if you provide a simple-mode storage to [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), the resulting **IPropertySetStorage** will be restricted by the supplied [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).</span></span>

<span data-ttu-id="5baa4-116">Дополнительные сведения о реализации составного файла этого интерфейса см. в разделе [IPropertySetStorage-составной реализации файла](ipropertysetstorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="5baa4-116">For more information about the compound file implementation of this interface, see the section [IPropertySetStorage-Compound File Implementation](ipropertysetstorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5baa4-117">Назначение</span><span class="sxs-lookup"><span data-stu-id="5baa4-117">When to Use</span></span>

<span data-ttu-id="5baa4-118">Вызывайте методы [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) для создания, открытия и удаления наборов свойств в любом структурированном хранилище.</span><span class="sxs-lookup"><span data-stu-id="5baa4-118">Call the methods of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) to create, open, and delete property sets in any structured storage.</span></span> <span data-ttu-id="5baa4-119">Существует также метод, который предоставляет указатель на перечислитель [**иенумстатпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , который можно использовать для перечисления наборов свойств в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5baa4-119">There is also a method that supplies a pointer to the [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) enumerator that can be used to enumerate the property sets in the storage.</span></span>

<span data-ttu-id="5baa4-120">Изолированная реализация также предоставляет вспомогательные функции [**стгкреатепропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) и [**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) в дополнение к методам [**CREATE**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) и [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) для создания и открытия наборов свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-120">The stand-alone implementation also provides the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) and [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) helper functions, in addition to the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods, to create and open property sets.</span></span> <span data-ttu-id="5baa4-121">Эти две функции добавляют поддержку \_ НЕбуферизованного значения пропсетфлаг, поэтому вы можете записывать изменения непосредственно в набор свойств вместо их буферизации в кэше.</span><span class="sxs-lookup"><span data-stu-id="5baa4-121">These two functions add support for the PROPSETFLAG\_UNBUFFERED value so you can write changes directly to the property set instead of buffering them in a cache.</span></span> <span data-ttu-id="5baa4-122">Дополнительные сведения см. в разделе [**константы пропсетфлаг**](propsetflag-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5baa4-122">For more information, see [**PROPSETFLAG Constants**](propsetflag-constants.md).</span></span>

## <a name="methods"></a><span data-ttu-id="5baa4-123">Методы</span><span class="sxs-lookup"><span data-stu-id="5baa4-123">Methods</span></span>

<span data-ttu-id="5baa4-124">Изолированная реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5baa4-124">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supports the following methods.</span></span>

<dl> <dt>

<span data-ttu-id="5baa4-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span><span class="sxs-lookup"><span data-stu-id="5baa4-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span></span>
</dt> <dd>

<span data-ttu-id="5baa4-126">Создает новое свойство, заданное в хранилище, и возвращает указатель на интерфейс [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-126">Creates a new property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="5baa4-127">Если вы планируете использовать значение без \_ буферизации пропсетфлаг, то вместо этого используйте функцию [**стгкреатепропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) , чтобы создать и открыть новый набор свойств и получить указатель на изолированную реализацию интерфейса [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-127">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function instead to create and open the new property set and to obtain a pointer to the stand-alone implementation for the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="5baa4-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span><span class="sxs-lookup"><span data-stu-id="5baa4-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span></span>
</dt> <dd>

<span data-ttu-id="5baa4-129">Открывает существующий набор свойств в хранилище и возвращает указатель на интерфейс [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-129">Opens an existing property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="5baa4-130">Если вы планируете использовать значение без \_ буферизации пропсетфлаг, используйте функцию [**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , чтобы получить указатель на изолированную реализацию [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) для указанного набора свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-130">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) function instead to obtain a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) on the specified property set.</span></span>

</dd> <dt>

<span data-ttu-id="5baa4-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D удалить**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span><span class="sxs-lookup"><span data-stu-id="5baa4-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::Delete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span></span>
</dt> <dd>

<span data-ttu-id="5baa4-132">Удаляет свойство, заданное в этом свойстве хранилища.</span><span class="sxs-lookup"><span data-stu-id="5baa4-132">Deletes a property set in this property set storage.</span></span>

</dd> <dt>

<span data-ttu-id="5baa4-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span><span class="sxs-lookup"><span data-stu-id="5baa4-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="5baa4-134">Создает объект, который можно использовать для перечисления структур [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) .</span><span class="sxs-lookup"><span data-stu-id="5baa4-134">Creates an object that can be used to enumerate [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures.</span></span> <span data-ttu-id="5baa4-135">Каждая структура **статпропсетстг** предоставляет данные об отдельном наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-135">Each **STATPROPSETSTG** structure provides data about a single property set.</span></span>

> [!Note]  
> <span data-ttu-id="5baa4-136">Набор свойств Документсуммаринформатион и Пользователяопределенные уникален в том, что в одном базовом потоке могут быть два раздела набора свойств.</span><span class="sxs-lookup"><span data-stu-id="5baa4-136">The DocumentSummaryInformation and UserDefined property set is unique in that it may have two property set sections in a single underlying stream.</span></span> <span data-ttu-id="5baa4-137">Дополнительные сведения см. в описании [наборов свойств документсуммаринформатион и пользователяопределенные](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="5baa4-137">For more information, see [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span></span>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="5baa4-138">См. также</span><span class="sxs-lookup"><span data-stu-id="5baa4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5baa4-139">Ипропертистораже — изолированная реализация</span><span class="sxs-lookup"><span data-stu-id="5baa4-139">IPropertyStorage-Stand-alone Implementation</span></span>](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="5baa4-140">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="5baa4-140">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[<span data-ttu-id="5baa4-141">**ипропертистораже**</span><span class="sxs-lookup"><span data-stu-id="5baa4-141">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="5baa4-142">**IStorage:: Енумелементс**</span><span class="sxs-lookup"><span data-stu-id="5baa4-142">**IStorage::EnumElements**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[<span data-ttu-id="5baa4-143">**Константы ПРОПСЕТФЛАГ**</span><span class="sxs-lookup"><span data-stu-id="5baa4-143">**PROPSETFLAG Constants**</span></span>](propsetflag-constants.md)
</dt> <dt>

[<span data-ttu-id="5baa4-144">**статпропсетстг**</span><span class="sxs-lookup"><span data-stu-id="5baa4-144">**STATPROPSETSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[<span data-ttu-id="5baa4-145">**стгкреатепропсетстг**</span><span class="sxs-lookup"><span data-stu-id="5baa4-145">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[<span data-ttu-id="5baa4-146">**стгкреатепропстг**</span><span class="sxs-lookup"><span data-stu-id="5baa4-146">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="5baa4-147">**стгопенпропстг**</span><span class="sxs-lookup"><span data-stu-id="5baa4-147">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="5baa4-148">**Константы СТГМ**</span><span class="sxs-lookup"><span data-stu-id="5baa4-148">**STGM Constants**</span></span>](stgm-constants.md)
</dt> </dl>

 

 