---
title: Ипропертистораже — изолированная реализация
description: Предоставляемая системой изолированная реализация IPropertySetStorage включает реализацию Ипропертистораже, интерфейс, считывающий и записывающий свойства в хранилище набора свойств.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- Ипропертистораже — изолированная реализация
- Ипропертистораже Стрктд STG, реализации, автономные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413131"
---
# <a name="ipropertystorage-stand-alone-implementation"></a><span data-ttu-id="d327e-105">Ипропертистораже — изолированная реализация</span><span class="sxs-lookup"><span data-stu-id="d327e-105">IPropertyStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="d327e-106">Предоставляемая системой изолированная реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) включает реализацию [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), интерфейс, считывающий и записывающий свойства в хранилище набора свойств.</span><span class="sxs-lookup"><span data-stu-id="d327e-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="d327e-107">Интерфейс **IPropertySetStorage** создает и открывает наборы свойств в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d327e-107">The **IPropertySetStorage** interface creates and opens property sets in a storage.</span></span> <span data-ttu-id="d327e-108">Интерфейсы [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) и [**иенумстатпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) также предоставляются в изолированной реализации.</span><span class="sxs-lookup"><span data-stu-id="d327e-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="d327e-109">Чтобы получить указатель на изолированную реализацию [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), вызовите функцию [**стгкреатепропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) , чтобы создать новый набор свойств или [**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , чтобы получить указатель интерфейса на существующем наборе свойств (или вызовите методы [**CREATE**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) или [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) в изолированной реализации [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ).</span><span class="sxs-lookup"><span data-stu-id="d327e-109">To get a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), call the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function to create a new property set or [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) to obtain the interface pointer on an existing property set (or call the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) or [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) stand-alone implementation).</span></span>

<span data-ttu-id="d327e-110">Изолированная реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) создает наборы свойств для любого объекта хранилища или потока, а не только для хранения составных файлов и потоков.</span><span class="sxs-lookup"><span data-stu-id="d327e-110">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creates property sets on any storage or stream object, not just on compound file storages and streams.</span></span> <span data-ttu-id="d327e-111">Изолированная реализация не зависит от составных файлов и может использоваться с любой реализацией структурированных хранилищ.</span><span class="sxs-lookup"><span data-stu-id="d327e-111">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="d327e-112">Дополнительные сведения о реализации составного файла этого интерфейса см. в разделе [ипропертистораже-составной реализации файла](ipropertystorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="d327e-112">For more information about the compound file implementation of this interface, see [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d327e-113">Назначение</span><span class="sxs-lookup"><span data-stu-id="d327e-113">When to Use</span></span>

<span data-ttu-id="d327e-114">Используйте [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) для управления свойствами в пределах одного набора свойств.</span><span class="sxs-lookup"><span data-stu-id="d327e-114">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) to manage properties within a single property set.</span></span> <span data-ttu-id="d327e-115">Его методы поддерживают чтение, запись и удаление обоих свойств, а также необязательные имена строк, которые могут быть связаны с идентификаторами свойств.</span><span class="sxs-lookup"><span data-stu-id="d327e-115">Its methods support reading, writing, and deleting both properties and the optional string names that can be associated with property IDs.</span></span> <span data-ttu-id="d327e-116">Другие методы поддерживают стандартные операции фиксации и отката хранилища.</span><span class="sxs-lookup"><span data-stu-id="d327e-116">Other methods support the standard commit and revert storage operations.</span></span> <span data-ttu-id="d327e-117">Существует также метод, который задает время, связанное с хранилищем свойств, и другой, который разрешает использовать присваивание CLSID для связывания другого кода, например кода пользовательского интерфейса, с набором свойств.</span><span class="sxs-lookup"><span data-stu-id="d327e-117">There is also a method that sets times associated with the property storage, and another that permits the assignment of a CLSID to be used to associate other code, such as user interface code, with the property set.</span></span> <span data-ttu-id="d327e-118">Метод [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) предоставляет указатель на изолированную реализацию [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), которая перечисляет свойства в наборе.</span><span class="sxs-lookup"><span data-stu-id="d327e-118">The [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) method supplies a pointer to the stand-alone implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), which enumerates the properties in the set.</span></span>

## <a name="version-0-and-version-1-property-set-formats"></a><span data-ttu-id="d327e-119">Форматы набора свойств версий 0 и 1</span><span class="sxs-lookup"><span data-stu-id="d327e-119">Version 0 and Version 1 Property Set Formats</span></span>

<span data-ttu-id="d327e-120">Изолированная реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) поддерживает свойства версии 0 и версии 1, устанавливая форматы сериализации.</span><span class="sxs-lookup"><span data-stu-id="d327e-120">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports both the version 0 and the version 1 property set serialization formats.</span></span> <span data-ttu-id="d327e-121">Дополнительные сведения см. в разделе [Свойства Сериализация набора свойств](version-0-vs--version-1-property-set-serialization.md).</span><span class="sxs-lookup"><span data-stu-id="d327e-121">For more information, see [Property Set Serialization](version-0-vs--version-1-property-set-serialization.md).</span></span> <span data-ttu-id="d327e-122">Наборы свойств создаются в формате версии 0 и остаются в этом формате, если не запрашиваются новые функции.</span><span class="sxs-lookup"><span data-stu-id="d327e-122">Property sets are created in version 0 format and remain in that format unless new features are requested.</span></span> <span data-ttu-id="d327e-123">В этот момент формат обновляется до версии 1.</span><span class="sxs-lookup"><span data-stu-id="d327e-123">At that time, the format is updated to version 1.</span></span>

<span data-ttu-id="d327e-124">Например, если набор свойств создается с \_ флагом пропсетфлаг по умолчанию, его формат имеет версию 0.</span><span class="sxs-lookup"><span data-stu-id="d327e-124">For example, if a property set is created with the PROPSETFLAG\_DEFAULT flag, its format is version 0.</span></span> <span data-ttu-id="d327e-125">При условии, что типы свойств, соответствующие формату версии 0, записываются и считываются из этого набора свойств, набор свойств остается в формате версии 0.</span><span class="sxs-lookup"><span data-stu-id="d327e-125">As long as property types that conform to the version 0 format are written to and read from that property set, the property set remains in version 0 format.</span></span> <span data-ttu-id="d327e-126">Если тип свойства версии 1 записывается в набор свойств, набор свойств автоматически обновляется до версии 1.</span><span class="sxs-lookup"><span data-stu-id="d327e-126">If a version 1 property type is written to the property set, the property set is automatically updated to version 1.</span></span> <span data-ttu-id="d327e-127">Впоследствии этот набор свойств больше не может быть прочитан реализациями, которые только понимают версию 0.</span><span class="sxs-lookup"><span data-stu-id="d327e-127">Subsequently, that property set can no longer be read by implementations that only understand version 0.</span></span>

## <a name="ipropertystorage-and-variant-types"></a><span data-ttu-id="d327e-128">Типы Ипропертистораже и Variant</span><span class="sxs-lookup"><span data-stu-id="d327e-128">IPropertyStorage and Variant Types</span></span>

<span data-ttu-id="d327e-129">Изолированная реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) не поддерживает варианты типов VT \_ Unknown или VT \_ Dispatch в элементе **VT** структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="d327e-129">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) does not support the variant types VT\_UNKNOWN or VT\_DISPATCH in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="d327e-130">В SafeArray поддерживаются следующие типы вариантов. Это значит, что эти значения можно комбинировать с \_ массивом VT в элементе **VT** структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="d327e-130">The following variant types are supported within a SafeArray; that is, these values can be combined with VT\_ARRAY in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>



<span data-ttu-id="d327e-131">Типы Variant, поддерживаемые в SafeArray путем реализации составного файла для [ **ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span><span class="sxs-lookup"><span data-stu-id="d327e-131">Variant types supported within SafeArray by compound file implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span></span>

<span data-ttu-id="d327e-132">VT \_ I1</span><span class="sxs-lookup"><span data-stu-id="d327e-132">VT\_I1</span></span>

<span data-ttu-id="d327e-133">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="d327e-133">VT\_UI1</span></span>

<span data-ttu-id="d327e-134">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="d327e-134">VT\_I2</span></span>

<span data-ttu-id="d327e-135">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="d327e-135">VT\_UI2</span></span>

<span data-ttu-id="d327e-136">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d327e-136">VT\_I4</span></span>

<span data-ttu-id="d327e-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="d327e-137">VT\_UI4</span></span>

<span data-ttu-id="d327e-138">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="d327e-138">VT\_INT</span></span>

<span data-ttu-id="d327e-139">VT \_ uint</span><span class="sxs-lookup"><span data-stu-id="d327e-139">VT\_UINT</span></span>

<span data-ttu-id="d327e-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="d327e-140">VT\_R4</span></span>

<span data-ttu-id="d327e-141">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="d327e-141">VT\_R8</span></span>

<span data-ttu-id="d327e-142">VT \_ CY</span><span class="sxs-lookup"><span data-stu-id="d327e-142">VT\_CY</span></span>

<span data-ttu-id="d327e-143">\_Дата VT</span><span class="sxs-lookup"><span data-stu-id="d327e-143">VT\_DATE</span></span>

<span data-ttu-id="d327e-144">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="d327e-144">VT\_BSTR</span></span>

<span data-ttu-id="d327e-145">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="d327e-145">VT\_BOOL</span></span>

<span data-ttu-id="d327e-146">VT \_ Decimal</span><span class="sxs-lookup"><span data-stu-id="d327e-146">VT\_DECIMAL</span></span>

<span data-ttu-id="d327e-147">\_Ошибка VT</span><span class="sxs-lookup"><span data-stu-id="d327e-147">VT\_ERROR</span></span>

<span data-ttu-id="d327e-148">\_вариант VT</span><span class="sxs-lookup"><span data-stu-id="d327e-148">VT\_VARIANT</span></span>

 



 

<span data-ttu-id="d327e-149">Когда VT \_ Variant сочетается с \_ массивом VT, сам массив SafeArray содержит структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="d327e-149">When VT\_VARIANT is combined with VT\_ARRAY, the SafeArray itself holds [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structures.</span></span> <span data-ttu-id="d327e-150">Тем не менее типы этих элементов должны быть взяты из предыдущего списка, не могут быть VT \_ и не могут включать \_ векторы VT, VT \_ или VT \_ ByRef.</span><span class="sxs-lookup"><span data-stu-id="d327e-150">However, the types of these elements must be taken from the preceding list, cannot be VT\_VARIANT, and cannot include the VT\_VECTOR, VT\_ARRAY, or VT\_BYREF indicators.</span></span>

## <a name="ipropertystorage-methods"></a><span data-ttu-id="d327e-151">Методы Ипропертистораже</span><span class="sxs-lookup"><span data-stu-id="d327e-151">IPropertyStorage Methods</span></span>

<span data-ttu-id="d327e-152">Изолированная реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) поддерживает следующие методы:</span><span class="sxs-lookup"><span data-stu-id="d327e-152">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports the following methods:</span></span>

<dl> <dt>

<span data-ttu-id="d327e-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**Ипропертистораже:: Реадмултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span><span class="sxs-lookup"><span data-stu-id="d327e-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-154">Считывает свойства, указанные в массиве *ргпспек* , и предоставляет значения всех допустимых свойств в массиве *ргвар* элементов [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="d327e-154">Reads the properties specified in the *rgpspec* array and supplies the values of all valid properties in the *rgvar* array of [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) elements.</span></span>

<span data-ttu-id="d327e-155">В предоставляемой системой изолированной реализации дублированные идентификаторы свойств, которые ссылаются на Stream-или Storage-Types, приводят к созданию нескольких вызовов метода [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) или [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , а успешное или неуспешное выполнение [**реадмултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) зависит от возможности реализации базового хранилища для предоставления общего доступа к открытым хранилищам.</span><span class="sxs-lookup"><span data-stu-id="d327e-155">In the system-provided, stand-alone implementation, duplicate property identifiers that refer to stream- or storage-types result in multiple calls to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) and the success or failure of [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depends on the underlying storage implementation's ability to share open storages.</span></span>

<span data-ttu-id="d327e-156">Кроме того, чтобы обеспечить поточно-ориентированную операцию, если одно и то же свойство Stream или Storage-value запрашивается несколько раз с помощью одного и того же указателя [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , открытие будет успешным или неудачным в зависимости от того, открыто ли свойство, а также от того, обрабатывает ли базовая файловая система множественное открытие потока или хранилища.</span><span class="sxs-lookup"><span data-stu-id="d327e-156">In addition, to ensure thread-safe operation if the same stream- or storage-valued property is requested multiple times through the same [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pointer, the open will succeed or fail depending on whether or not the property is already open and on whether the underlying file system handles multiple opens of a stream or storage.</span></span> <span data-ttu-id="d327e-157">Таким образом, операция [**реадмултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) для потока или свойства, возвращающего хранение, всегда приводит к вызову [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)или [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), передаче доступа ( \_ например, стгм ReadWrite) и общим значениям ( \_ например, стгм общего доступа \_ ), указанным при первоначальном открытии или создании набора свойств.</span><span class="sxs-lookup"><span data-stu-id="d327e-157">Thus, the [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) operation on a stream- or storage-valued property always results in a call to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream), or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passing the access (STGM\_READWRITE, for example) and share values (STGM\_SHARE\_EXCLUSIVE, for example) specified when the property set was originally opened or created.</span></span>

<span data-ttu-id="d327e-158">Если метод завершается ошибкой, значения, записанные в *ргвар* , \[ \] не определяются.</span><span class="sxs-lookup"><span data-stu-id="d327e-158">If the method fails, the values written to *rgvar*\[\] are undefined.</span></span> <span data-ttu-id="d327e-159">Если некоторые свойства, возвращающие поток или хранилище, успешно открыты, но перед завершением выполнения возникает ошибка, эти свойства должны быть освобождены до того, как метод возвратит значение.</span><span class="sxs-lookup"><span data-stu-id="d327e-159">If some stream- or storage-valued properties are opened successfully but an error occurs before execution is complete, these properties should be released before the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="d327e-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**Ипропертистораже:: Вритемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span><span class="sxs-lookup"><span data-stu-id="d327e-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-161">Записывает свойства, указанные в  \[ \] массиве ргпспек, присваивая им теги [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) и значения, указанные в *ргвар* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d327e-161">Writes the properties specified in the *rgpspec*\[\] array, assigning them the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) tags and values specified in *rgvar*\[\].</span></span> <span data-ttu-id="d327e-162">Свойства, которые уже существуют, присваиваются указанным значениям **пропвариант** , а свойства, которые в настоящее время не существуют, создаются.</span><span class="sxs-lookup"><span data-stu-id="d327e-162">Properties that already exist are assigned the specified **PROPVARIANT** values, and properties that do not currently exist are created.</span></span>

</dd> <dt>

<span data-ttu-id="d327e-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**Ипропертистораже::D Елетемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span><span class="sxs-lookup"><span data-stu-id="d327e-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-164">Удаляет свойства, указанные в параметре *ргпспек* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d327e-164">Deletes the properties specified in the *rgpspec*\[\].</span></span>

</dd> <dt>

<span data-ttu-id="d327e-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**Ипропертистораже:: Реадпропертинамес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span><span class="sxs-lookup"><span data-stu-id="d327e-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-166">Считывает существующие имена строк, связанные с идентификаторами свойств, указанными в  \[ \] массиве ргпропид.</span><span class="sxs-lookup"><span data-stu-id="d327e-166">Reads existing string names associated with the property IDs specified in the *rgpropid*\[\] array.</span></span>

</dd> <dt>

<span data-ttu-id="d327e-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**Ипропертистораже:: Вритепропертинамес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span><span class="sxs-lookup"><span data-stu-id="d327e-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-168">Присваивает строковые имена, указанные в массиве *рглпвстрнаме* , с идентификаторами свойств, указанными в массиве *ргпропид* .</span><span class="sxs-lookup"><span data-stu-id="d327e-168">Assigns string names specified in the *rglpwstrName* array to property IDs specified in the *rgpropid* array.</span></span>

</dd> <dt>

<span data-ttu-id="d327e-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**Ипропертистораже::D Елетепропертинамес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span><span class="sxs-lookup"><span data-stu-id="d327e-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::DeletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-170">Удаляет строки с идентификаторами свойств, указанными в массиве *ргпропид* , записывая **значение NULL** в имя свойства.</span><span class="sxs-lookup"><span data-stu-id="d327e-170">Deletes the string names of the property IDs specified in the *rgpropid* array by writing **NULL** to the property name.</span></span>

</dd> <dt>

<span data-ttu-id="d327e-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**Ипропертистораже:: Сеткласс**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="d327e-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-172">Задает **идентификатор CLSID** потока набора свойств.</span><span class="sxs-lookup"><span data-stu-id="d327e-172">Sets the **CLSID** of the property set stream.</span></span> <span data-ttu-id="d327e-173">В изолированной реализации задание идентификатора CLSID для непростого набора свойств (в котором могут содержаться свойства, возвращающие потоковые значения, как описано в [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) также задает идентификатор CLSID для базового подхранилища, чтобы его можно было получить с помощью вызова метода [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span><span class="sxs-lookup"><span data-stu-id="d327e-173">In the stand-alone implementation, setting the CLSID on a nonsimple property set (one that can contain storage- or stream-valued properties, as described in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) also sets the CLSID on the underlying substorage so that it can be obtained through a call to [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span></span>

</dd> <dt>

<span data-ttu-id="d327e-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**Ипропертистораже:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span><span class="sxs-lookup"><span data-stu-id="d327e-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-175">Для простых и непростых наборов свойств очищает образ памяти с дисковой подсистемой.</span><span class="sxs-lookup"><span data-stu-id="d327e-175">For both simple and nonsimple property sets, flushes the memory image to the disk subsystem.</span></span> <span data-ttu-id="d327e-176">Кроме того, для непростых наборов свойств в режиме транзакций этот метод вызывает [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) для набора свойств.</span><span class="sxs-lookup"><span data-stu-id="d327e-176">In addition, for nonsimple transacted-mode property sets, this method calls [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="d327e-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**Ипропертистораже:: revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span><span class="sxs-lookup"><span data-stu-id="d327e-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-178">Для непростых наборов свойств вызывает метод [**reopen**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) базового хранилища и повторно открывает поток "содержимое".</span><span class="sxs-lookup"><span data-stu-id="d327e-178">For nonsimple property sets only, calls the [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) method of the underlying storage and reopens the 'contents' stream.</span></span> <span data-ttu-id="d327e-179">Для простых наборов свойств возвращается только значение E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d327e-179">For simple property sets, only returns E\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="d327e-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**Ипропертистораже:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span><span class="sxs-lookup"><span data-stu-id="d327e-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-181">Создает объект перечислителя, который реализует [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), методы, которые могут быть вызваны для перечисления структур [**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , предоставляющих сведения о каждом свойстве в наборе.</span><span class="sxs-lookup"><span data-stu-id="d327e-181">Creates an enumerator object that implements [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), the methods of which can be called to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that provide information about each of the properties in the set.</span></span>

<span data-ttu-id="d327e-182">Эта реализация создает массив, в который считывается весь набор свойств и который может использоваться совместно при вызове [**иенумстатпропстг:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) .</span><span class="sxs-lookup"><span data-stu-id="d327e-182">This implementation creates an array into which the entire property set is read and which can be shared when [**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) is called.</span></span>

</dd> <dt>

<span data-ttu-id="d327e-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**Ипропертистораже:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span><span class="sxs-lookup"><span data-stu-id="d327e-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-184">Заполняет элементы структуры [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , которая содержит сведения о свойстве, заданном в целом.</span><span class="sxs-lookup"><span data-stu-id="d327e-184">Fills in the members of a [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structure, which contains information about the property set as a whole.</span></span> <span data-ttu-id="d327e-185">При возврате предоставляет указатель на структуру.</span><span class="sxs-lookup"><span data-stu-id="d327e-185">On return, supplies a pointer to the structure.</span></span>

<span data-ttu-id="d327e-186">Для непростых наборов хранения Эта реализация вызывает метод [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (или [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) для получения сведений из базового хранилища или потока.</span><span class="sxs-lookup"><span data-stu-id="d327e-186">For nonsimple storage sets, this implementation calls [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (or [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) to get the information from the underlying storage or stream.</span></span>

</dd> <dt>

<span data-ttu-id="d327e-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**Ипропертистораже:: Сеттимес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span><span class="sxs-lookup"><span data-stu-id="d327e-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span></span>
</dt> <dd>

<span data-ttu-id="d327e-188">Для непростых наборов свойств задает время, поддерживаемое базовым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="d327e-188">For nonsimple property sets only, sets the times supported by the underlying storage.</span></span> <span data-ttu-id="d327e-189">Эта реализация [**сеттимес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) вызывает метод [**IStorage:: сетелементтимес**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) базового хранилища, чтобы изменить время.</span><span class="sxs-lookup"><span data-stu-id="d327e-189">This implementation of [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) calls the [**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) method of the underlying storage to modify the times.</span></span> <span data-ttu-id="d327e-190">Он поддерживает время, поддерживаемое базовым методом, который может быть изменением времени, времени доступа или времени создания.</span><span class="sxs-lookup"><span data-stu-id="d327e-190">It supports the times supported by the underlying method which can be modification time, access time, or creation time.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d327e-191">См. также</span><span class="sxs-lookup"><span data-stu-id="d327e-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d327e-192">IPropertySetStorage — изолированная реализация</span><span class="sxs-lookup"><span data-stu-id="d327e-192">IPropertySetStorage-Stand-alone Implementation</span></span>](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="d327e-193">**ипропертистораже**</span><span class="sxs-lookup"><span data-stu-id="d327e-193">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="d327e-194">**IStorage:: Сетелементтимес**</span><span class="sxs-lookup"><span data-stu-id="d327e-194">**IStorage::SetElementTimes**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[<span data-ttu-id="d327e-195">**стгопенпропстг**</span><span class="sxs-lookup"><span data-stu-id="d327e-195">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="d327e-196">**стгкреатепропстг**</span><span class="sxs-lookup"><span data-stu-id="d327e-196">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="d327e-197">**стгкреатепропсетстг**</span><span class="sxs-lookup"><span data-stu-id="d327e-197">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 