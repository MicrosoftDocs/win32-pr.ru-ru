---
description: В этом разделе объясняется, как создавать и регистрировать обработчики свойств для работы с системой свойств Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Инициализация обработчиков свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264739"
---
# <a name="initializing-property-handlers"></a><span data-ttu-id="85068-103">Инициализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="85068-103">Initializing Property Handlers</span></span>

<span data-ttu-id="85068-104">В этом разделе объясняется, как создавать и регистрировать обработчики свойств для работы с системой свойств Windows.</span><span class="sxs-lookup"><span data-stu-id="85068-104">This topic explains how to create and register property handlers to work with the Windows property system.</span></span>

<span data-ttu-id="85068-105">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="85068-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="85068-106">Обработчики свойств</span><span class="sxs-lookup"><span data-stu-id="85068-106">Property Handlers</span></span>](#property-handlers)
-   [<span data-ttu-id="85068-107">Перед началом</span><span class="sxs-lookup"><span data-stu-id="85068-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="85068-108">Инициализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="85068-108">Initializing Property Handlers</span></span>](#initializing-property-handlers)
-   [<span data-ttu-id="85068-109">Хранилище свойств в памяти</span><span class="sxs-lookup"><span data-stu-id="85068-109">In-Memory Property Store</span></span>](#in-memory-property-store)
-   [<span data-ttu-id="85068-110">Работа с PROPVARIANT-Basedными значениями</span><span class="sxs-lookup"><span data-stu-id="85068-110">Dealing with PROPVARIANT-Based Values</span></span>](#dealing-with-propvariant-based-values)
-   [<span data-ttu-id="85068-111">Поддержка открытых метаданных</span><span class="sxs-lookup"><span data-stu-id="85068-111">Supporting Open Metadata</span></span>](#supporting-open-metadata)
-   [<span data-ttu-id="85068-112">Полнотекстовое содержимое</span><span class="sxs-lookup"><span data-stu-id="85068-112">Full-Text Contents</span></span>](#full-text-contents)
-   [<span data-ttu-id="85068-113">Предоставление значений для свойств</span><span class="sxs-lookup"><span data-stu-id="85068-113">Providing Values for Properties</span></span>](#providing-values-for-properties)
-   [<span data-ttu-id="85068-114">Запись обратных значений</span><span class="sxs-lookup"><span data-stu-id="85068-114">Writing Back Values</span></span>](#writing-back-values)
-   [<span data-ttu-id="85068-115">Реализация Ипропертисторекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="85068-115">Implementing IPropertyStoreCapabilities</span></span>](#implementing-ipropertystorecapabilities)
-   [<span data-ttu-id="85068-116">Регистрация и распространение обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="85068-116">Registering and Distributing Property Handlers</span></span>](#registering-and-distributing-property-handlers)
-   [<span data-ttu-id="85068-117">См. также</span><span class="sxs-lookup"><span data-stu-id="85068-117">Related topics</span></span>](#related-topics)

## <a name="property-handlers"></a><span data-ttu-id="85068-118">Обработчики свойств</span><span class="sxs-lookup"><span data-stu-id="85068-118">Property Handlers</span></span>

<span data-ttu-id="85068-119">Обработчики свойств являются ключевой частью системы свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-119">Property handlers are a crucial part of the property system.</span></span> <span data-ttu-id="85068-120">Они вызываются внутри процесса индексатором для чтения и индексирования значений свойств, а также вызываются проводником Windows в процессе чтения и записи значений свойств непосредственно в файлах.</span><span class="sxs-lookup"><span data-stu-id="85068-120">They are invoked in-process by the indexer to read and index property values, and are also invoked by Windows Explorer in-process to read and write property values directly in the files.</span></span> <span data-ttu-id="85068-121">Эти обработчики необходимо тщательно записать и протестировать, чтобы предотвратить снижение производительности или потери данных в затронутых файлах.</span><span class="sxs-lookup"><span data-stu-id="85068-121">These handlers need to be carefully written and tested to prevent degraded performance or the loss of data in the affected files.</span></span> <span data-ttu-id="85068-122">Дополнительные сведения о вопросах, связанных с индексатором, которые влияют на реализацию обработчика свойств, см. в разделе [Разработка обработчиков свойств для поиска Windows](../search/-search-3x-wds-extidx-propertyhandlers.md).</span><span class="sxs-lookup"><span data-stu-id="85068-122">For more information on indexer-specific considerations that affect property handler implementation, see [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span></span>

<span data-ttu-id="85068-123">В этом разделе рассматривается пример формата файлов на основе XML, описывающий рецепт с расширением имени файла. рецепт.</span><span class="sxs-lookup"><span data-stu-id="85068-123">This topic discusses a sample XML-based file format that describes a recipe with a .recipe file name extension.</span></span> <span data-ttu-id="85068-124">Расширение имени файла с расширением. рецепт регистрируется в собственном отдельном формате, не полагаясь на более универсальный формат XML-файла, обработчик которого использует вторичный поток для хранения свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-124">The .recipe file name extension is registered as its own distinct file format rather than relying on the more generic .xml file format, whose handler uses a secondary stream to store properties.</span></span> <span data-ttu-id="85068-125">Для типов файлов рекомендуется зарегистрировать уникальные расширения имен файлов.</span><span class="sxs-lookup"><span data-stu-id="85068-125">We recommend that you register unique file name extensions for your file types.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="85068-126">Перед началом</span><span class="sxs-lookup"><span data-stu-id="85068-126">Before You Begin</span></span>

<span data-ttu-id="85068-127">Обработчики свойств — это COM-объекты, создающие абстракцию [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) для определенного формата файла.</span><span class="sxs-lookup"><span data-stu-id="85068-127">Property handlers are COM objects that create the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abstraction for a specific file format.</span></span> <span data-ttu-id="85068-128">Они считывают (анализируют) и записывают этот формат файла способом, который соответствует его спецификации.</span><span class="sxs-lookup"><span data-stu-id="85068-128">They read (parse) and write this file format in a manner that conforms to its specification.</span></span> <span data-ttu-id="85068-129">Некоторые обработчики свойств выполняют свою работу на основе API-интерфейсов, которые имеют абстрактный доступ к конкретному формату файла.</span><span class="sxs-lookup"><span data-stu-id="85068-129">Some property handlers do their work based on APIs that abstract access to a specific file format.</span></span> <span data-ttu-id="85068-130">Перед разработкой обработчика свойств для формата файла необходимо понять, как хранятся свойства в формате файла, и как эти свойства (имена и значения) сопоставляются с абстракцией хранилища свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-130">Before you develop a property handler for your file format, you need to understand how your file format stores properties, and how those properties (names and values) are mapped into the property store abstraction.</span></span>

<span data-ttu-id="85068-131">При планировании реализации Помните, что обработчики свойств являются компонентами низкого уровня, загруженными в контексте таких процессов, как проводник, индексатор Windows Search и сторонние приложения, использующие модель программирования элементов оболочки.</span><span class="sxs-lookup"><span data-stu-id="85068-131">When planning your implementation, remember that property handlers are low-level components that are loaded in the context of processes like Windows Explorer, the Windows Search indexer, and third-party applications that use the Shell item programming model.</span></span> <span data-ttu-id="85068-132">В результате обработчики свойств не могут быть реализованы в управляемом коде и должны быть реализованы в C++.</span><span class="sxs-lookup"><span data-stu-id="85068-132">As a result, property handlers cannot be implemented in managed code, and should be implemented in C++.</span></span> <span data-ttu-id="85068-133">Если обработчик использует интерфейсы API или службы для выполнения своей работы, необходимо убедиться, что эти службы могут правильно работать в средах, где загружается обработчик свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-133">If your handler uses any APIs or services to do its work, you must ensure that those services can function properly in the environment(s) in which your property handler is loaded.</span></span>

> [!Note]  
> <span data-ttu-id="85068-134">Обработчики свойств всегда связаны с конкретными типами файлов. Таким же, если формат файла содержит свойства, требующие пользовательского обработчика свойств, всегда следует регистрировать уникальное расширение имени файла для каждого формата файла.</span><span class="sxs-lookup"><span data-stu-id="85068-134">Property handlers are always associated with specific file types; thus, if your file format contains properties that require a custom property handler, you should always register a unique file name extension for each file format.</span></span>

 

## <a name="initializing-property-handlers"></a><span data-ttu-id="85068-135">Инициализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="85068-135">Initializing Property Handlers</span></span>

<span data-ttu-id="85068-136">Прежде чем свойство будет использоваться системой, оно инициализируется путем вызова реализации [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span><span class="sxs-lookup"><span data-stu-id="85068-136">Before a property is used by the system, it is initialized by calling an implementation of [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span></span> <span data-ttu-id="85068-137">Обработчик свойства должен быть инициализирован путем того, что система присваивает ему поток, а не оставит это назначение реализации обработчика.</span><span class="sxs-lookup"><span data-stu-id="85068-137">The property handler should be initialized by having the system assign it a stream rather than leaving that assignment to the handler implementation.</span></span> <span data-ttu-id="85068-138">Этот метод инициализации обеспечивает следующие факторы:</span><span class="sxs-lookup"><span data-stu-id="85068-138">This method of initialization ensures the following things:</span></span>

-   <span data-ttu-id="85068-139">Обработчик свойств может выполняться в ограниченном процессе (важный компонент безопасности) без прав доступа для непосредственного чтения или записи файлов, а не доступа к их содержимому через поток.</span><span class="sxs-lookup"><span data-stu-id="85068-139">The property handler can run in a restricted process (an important security feature) without having access rights to directly read or write files, rather accessing their content through the stream.</span></span>
-   <span data-ttu-id="85068-140">Система может быть доверенной, чтобы правильно обрабатывать файл операционные блокировки, что является важной мерой надежности.</span><span class="sxs-lookup"><span data-stu-id="85068-140">The system can be trusted to handle the file oplocks correctly, which is an important reliability measure.</span></span>
-   <span data-ttu-id="85068-141">Система свойств предоставляет автоматически сохраняемую службу без дополнительных функций, необходимых для реализации обработчика свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-141">The property system provides an automatic safe saving service without any extra functionality required from the property handler implementation.</span></span> <span data-ttu-id="85068-142">Дополнительные сведения о потоках см. в разделе [запись обратных значений](#writing-back-values) .</span><span class="sxs-lookup"><span data-stu-id="85068-142">See the [Writing Back Values](#writing-back-values) section for more information about streams.</span></span>
-   <span data-ttu-id="85068-143">Использование [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) абстрагирует реализацию из сведений о файловой системе.</span><span class="sxs-lookup"><span data-stu-id="85068-143">Use of the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstracts your implementation from file system details.</span></span> <span data-ttu-id="85068-144">Это позволяет обработчику поддерживать инициализацию с помощью альтернативных хранилищ, например папки протокол FTP (FTP) или сжатого файла с расширением ZIP.</span><span class="sxs-lookup"><span data-stu-id="85068-144">This enables the handler to support initialization through alternative storages such as a File Transfer Protocol (FTP) folder or a compressed file with a .zip file name extension.</span></span>

<span data-ttu-id="85068-145">Бывают случаи, когда инициализация с помощью потоков невозможна.</span><span class="sxs-lookup"><span data-stu-id="85068-145">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="85068-146">В этих ситуациях существуют два дополнительных интерфейса, которые могут реализовать обработчики свойств: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) и [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span><span class="sxs-lookup"><span data-stu-id="85068-146">In those situations, there are two further interfaces that property handlers can implement: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) and [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span></span> <span data-ttu-id="85068-147">Если обработчик свойства не реализует [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), он должен отказаться от выполнения в изолированном процессе, в котором индексатор системы поместит его по умолчанию, если произошло изменение в потоке.</span><span class="sxs-lookup"><span data-stu-id="85068-147">If a property handler does not implement the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process into which the system indexer would place it by default if there were a change to the stream.</span></span> <span data-ttu-id="85068-148">Чтобы отказаться от этой функции, задайте следующее значение реестра.</span><span class="sxs-lookup"><span data-stu-id="85068-148">To opt out of this feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

<span data-ttu-id="85068-149">Однако гораздо лучше реализовать [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) и выполнить инициализацию на основе потока.</span><span class="sxs-lookup"><span data-stu-id="85068-149">However, it is far better to implement [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization.</span></span> <span data-ttu-id="85068-150">В результате ваш обработчик свойств будет более безопасным и надежным.</span><span class="sxs-lookup"><span data-stu-id="85068-150">Your property handler will be safer and more reliable as a result.</span></span> <span data-ttu-id="85068-151">Отключение изоляции процессов обычно предназначено только для устаревших обработчиков свойств и должно быть стренуауслио без какого-либо нового кода.</span><span class="sxs-lookup"><span data-stu-id="85068-151">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

<span data-ttu-id="85068-152">Чтобы подробно изучить реализацию обработчика свойств, рассмотрим следующий пример кода, который является реализацией [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="85068-152">To examine the implementation of a property handler in detail, look at the following code example, which is an implementation of [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span> <span data-ttu-id="85068-153">Обработчик инициализируется путем загрузки документа с рецептом на основе XML посредством указателя на соответствующий экземпляр [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) этого документа.</span><span class="sxs-lookup"><span data-stu-id="85068-153">The handler is initialized by loading an XML-based recipe document through a pointer to that document's associated [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) instance.</span></span> <span data-ttu-id="85068-154">Переменная **\_ спдоцеле** , используемая около конца примера кода, определена ранее в примере как Msxml2:: иксмлдомелементптр.</span><span class="sxs-lookup"><span data-stu-id="85068-154">The **\_spDocEle** variable used near the end of the code example is defined earlier in the sample as an MSXML2::IXMLDOMElementPtr.</span></span>

> [!Note]  
> <span data-ttu-id="85068-155">Следующий код и все последующие примеры кода взяты из примера обработчика рецептов, входящего в состав пакета средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="85068-155">The following and all subsequent code examples are taken from the recipe handler sample included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="85068-156">.</span><span class="sxs-lookup"><span data-stu-id="85068-156">.</span></span>

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



<span data-ttu-id="85068-157">Â</span><span class="sxs-lookup"><span data-stu-id="85068-157">Â</span></span> 

<span data-ttu-id="85068-158">После загрузки документа свойства, отображаемые в проводнике Windows, загружаются путем вызова защищенного метода **\_ LoadProperties** , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="85068-158">After the document itself is loaded, the properties to be displayed in Windows Explorer are loaded by calling the protected **\_LoadProperties** method, as illustrated in the following code example.</span></span> <span data-ttu-id="85068-159">Этот процесс подробно рассматривается в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="85068-159">This process is examined in detail in the next section.</span></span>


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



<span data-ttu-id="85068-160">Если поток доступен только для чтения, но параметр *грфмоде* содержит \_ флаг стгм ReadWrite, инициализация должна завершиться ошибкой и вернуть STG \_ E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="85068-160">If the stream is read-only but the *grfMode* parameter contains the STGM\_READWRITE flag, the initialization should fail and return STG\_E\_ACCESSDENIED.</span></span> <span data-ttu-id="85068-161">Без этой проверки проводник Windows отображает значения свойств как доступные для записи, даже если это не так, что приведет к путанице в работе конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="85068-161">Without this check, Windows Explorer shows the property values as writable even though they are not, leading to a confusing end-user experience.</span></span>

<span data-ttu-id="85068-162">Обработчик свойств инициализируется только один раз в течение своего времени существования.</span><span class="sxs-lookup"><span data-stu-id="85068-162">The property handler is initialized only once in its lifetime.</span></span> <span data-ttu-id="85068-163">Если запрашивается вторая инициализация, обработчик должен вернуть `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .</span><span class="sxs-lookup"><span data-stu-id="85068-163">If a second initialization is requested, the handler should return `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)`.</span></span>

## <a name="in-memory-property-store"></a><span data-ttu-id="85068-164">Хранилище свойств In-Memory</span><span class="sxs-lookup"><span data-stu-id="85068-164">In-Memory Property Store</span></span>

<span data-ttu-id="85068-165">Перед рассмотрением реализации **\_ LoadProperties** необходимо понять, какой массив **PropertyMap** используется в примере, чтобы сопоставлять свойства в XML-документе с существующими свойствами в системе свойств с помощью их значений PKEY.</span><span class="sxs-lookup"><span data-stu-id="85068-165">Before looking at the implementation of **\_LoadProperties**, you should understand the **PropertyMap** array used in the sample to map properties in the XML document to existing properties in the property system through their PKEY values.</span></span>

<span data-ttu-id="85068-166">Не следует предоставлять каждый элемент и атрибут в XML-файле в качестве свойства.</span><span class="sxs-lookup"><span data-stu-id="85068-166">You should not expose every element and attribute in the XML file as a property.</span></span> <span data-ttu-id="85068-167">Вместо этого следует выбирать только те, которые вы считаете полезными для конечных пользователей в организации их документов (в нашем примере это рецепты).</span><span class="sxs-lookup"><span data-stu-id="85068-167">Instead, select only those that you believe will be useful to end users in the organization of their documents (in this case, recipes).</span></span> <span data-ttu-id="85068-168">Это важная концепция, которую следует помнить при разработке обработчиков свойств: разница между сведениями, которые действительно удобно использовать для организационных сценариев, и сведениями, которые относятся к сведениям о файле и могут быть просмотрены путем открытия самого файла.</span><span class="sxs-lookup"><span data-stu-id="85068-168">This is an important concept to keep in mind as you develop your property handlers: the difference between information that is truly useful for organizational scenarios, and information that belongs to the details of your file and can be seen by opening the file itself.</span></span> <span data-ttu-id="85068-169">Свойства не предназначены для полного дублирования XML-файла.</span><span class="sxs-lookup"><span data-stu-id="85068-169">Properties are not intended to be a full duplication of an XML file.</span></span>


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



<span data-ttu-id="85068-170">Ниже приведена полная реализация метода **\_ LoadProperties** , вызываемого методом [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="85068-170">Here is the full implementation of the **\_LoadProperties** method called by [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



<span data-ttu-id="85068-171">Метод **\_ LoadProperties** вызывает вспомогательную функцию оболочки [**пскреатемеморипропертисторе**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) для создания хранилища свойств в памяти (кэша) для обрабатываемых свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-171">The **\_LoadProperties** method calls the Shell helper function [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create an in-memory property store (cache) for the handled properties.</span></span> <span data-ttu-id="85068-172">С помощью кэша изменения отправляются за вас.</span><span class="sxs-lookup"><span data-stu-id="85068-172">By using a cache, changes are tracked for you.</span></span> <span data-ttu-id="85068-173">Это освобождает от отслеживания изменения значения свойства в кэше, но еще не сохраненного в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="85068-173">This frees you from tracking whether a property value has been changed in the cache but not yet saved to persisted storage.</span></span> <span data-ttu-id="85068-174">Он также освобождает вас от ненужных сохраненных значений свойств, которые не были изменены.</span><span class="sxs-lookup"><span data-stu-id="85068-174">It also frees you from needlessly persisting property values that have not changed.</span></span>

<span data-ttu-id="85068-175">Метод **\_ LoadProperties** также вызывает **\_ Свойства LoadProperty** , реализация которого показана в следующем коде, один раз для каждого сопоставленного свойства.</span><span class="sxs-lookup"><span data-stu-id="85068-175">The **\_LoadProperties** method also calls **\_LoadProperty** whose implementation is illustrated in the following code) once for each mapped property.</span></span> <span data-ttu-id="85068-176">**\_ Свойства LoadProperty** получает значение свойства, как указано в элементе **PROPERTYMAP** в потоке XML, и назначает его кэшу в памяти посредством вызова [**ипропертисторекаче:: сетвалуеандстате**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span><span class="sxs-lookup"><span data-stu-id="85068-176">**\_LoadProperty** gets the value of the property as specified in the **PropertyMap** element in the XML stream and assigns it to the in-memory cache through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span></span> <span data-ttu-id="85068-177">\_Стандартный флаг PSC в вызове **ипропертисторекаче:: сетвалуеандстате** указывает, что значение свойства не было изменено со времени, когда оно было введено в кэш.</span><span class="sxs-lookup"><span data-stu-id="85068-177">The PSC\_NORMAL flag in the call to **IPropertyStoreCache::SetValueAndState** indicates that the property value has not been altered since the time it entered the cache.</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a><span data-ttu-id="85068-178">Работа с PROPVARIANT-Basedными значениями</span><span class="sxs-lookup"><span data-stu-id="85068-178">Dealing with PROPVARIANT-Based Values</span></span>

<span data-ttu-id="85068-179">В реализации **\_ Свойства LoadProperty** значение свойства указывается в виде [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="85068-179">In the implementation of **\_LoadProperty**, a property value is provided in the form of a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="85068-180">Набор интерфейсов API в пакете средств разработки программного обеспечения (SDK) предоставляется для преобразования из типов **пропвариант** в типы-примитивы, такие как **пвстр** или **int** .</span><span class="sxs-lookup"><span data-stu-id="85068-180">A set of APIs in the software development kit (SDK) is provided to convert from primitive types such as **PWSTR** or **int** to or from **PROPVARIANT** types.</span></span> <span data-ttu-id="85068-181">Эти API-интерфейсы находятся в Пропварутил. h.</span><span class="sxs-lookup"><span data-stu-id="85068-181">These APIs are found in Propvarutil.h.</span></span>

<span data-ttu-id="85068-182">Например, чтобы преобразовать [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) в строку, можно использовать [**пропварианттостринг**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) , как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="85068-182">For example, to convert a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to a string, you can use [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) as illustrated here.</span></span>


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



<span data-ttu-id="85068-183">Чтобы инициализировать ПРОПВАРИАНТ из строки, можно использовать [**инитпропвариантфромстринг**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span><span class="sxs-lookup"><span data-stu-id="85068-183">To initialize a PROPVARIANT from a string, you can use [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span></span>


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



<span data-ttu-id="85068-184">Как можно увидеть в любом из файлов рецептов, входящих в образец, в каждом файле может быть несколько ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="85068-184">As you can see in any of the recipe files included in the sample, there can be more than one keyword in each file.</span></span> <span data-ttu-id="85068-185">Для этого система свойств поддерживает строки с несколькими значениями, представленные в виде вектора строк (например, "VT \_ vector \| VT \_ ").</span><span class="sxs-lookup"><span data-stu-id="85068-185">To account for this, the property system supports multi-valued strings represented as a vector of strings (for instance "VT\_VECTOR \| VT\_LPWSTR").</span></span> <span data-ttu-id="85068-186">Метод **\_ лоадвекторпроперти** в примере использует векторные значения.</span><span class="sxs-lookup"><span data-stu-id="85068-186">The **\_LoadVectorProperty** method in the example uses vector-based values.</span></span>


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



<span data-ttu-id="85068-187">Если значение не существует в файле, не возвращайте ошибку.</span><span class="sxs-lookup"><span data-stu-id="85068-187">If a value does not exist in the file, do not return an error.</span></span> <span data-ttu-id="85068-188">Вместо этого задайте значение VT \_ Empty и возвратите **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="85068-188">Instead, set the value to VT\_EMPTY and return **S\_OK**.</span></span> <span data-ttu-id="85068-189">VT \_ Empty указывает, что значение свойства не существует.</span><span class="sxs-lookup"><span data-stu-id="85068-189">VT\_EMPTY indicates that the property value does not exist.</span></span>

## <a name="supporting-open-metadata"></a><span data-ttu-id="85068-190">Поддержка открытых метаданных</span><span class="sxs-lookup"><span data-stu-id="85068-190">Supporting Open Metadata</span></span>

<span data-ttu-id="85068-191">В этом примере используется формат файла на основе XML.</span><span class="sxs-lookup"><span data-stu-id="85068-191">This example uses an XML-based file format.</span></span> <span data-ttu-id="85068-192">Его схему можно расширить для поддержки свойств, которые не были рассмотрены во время девелопмет, например.</span><span class="sxs-lookup"><span data-stu-id="85068-192">Its schema can be extended to support properties that were not thought of during developmet, for example.</span></span> <span data-ttu-id="85068-193">Эта система называется открытыми метаданными.</span><span class="sxs-lookup"><span data-stu-id="85068-193">This system is known as open metadata.</span></span> <span data-ttu-id="85068-194">Этот пример расширяет систему свойств, создавая узел под элементом **рецепта** с именем **расширенных свойств**, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="85068-194">This example extends the property system by creating a node under the **Recipe** element called **ExtendedProperties**, as illustrated in the following code example.</span></span>


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



<span data-ttu-id="85068-195">Чтобы загрузить материализованные расширенные свойства во время инициализации, реализуйте метод **\_ лоадекстендедпропертиес** , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="85068-195">To load persisted extended properties during initialization, implement the **\_LoadExtendedProperties** method, as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



<span data-ttu-id="85068-196">Интерфейсы API сериализации, объявленные в Пропсис. h, используются для сериализации и десериализации типов [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) в большие двоичные объекты данных, а затем для сериализации этих больших двоичных объектов в строки, которые могут быть СОХРАНЕНЫ в XML, используются кодировка Base64.</span><span class="sxs-lookup"><span data-stu-id="85068-196">Serialization APIs declared in Propsys.h are used to serialize and deserialize [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types into blobs of data, and then Base64 encoding is used to serialize those blobs into strings that can be saved in the XML.</span></span> <span data-ttu-id="85068-197">Эти строки хранятся в атрибуте **енкодедвалуе** элемента **расширенных свойств** .</span><span class="sxs-lookup"><span data-stu-id="85068-197">These strings are stored in the **EncodedValue** attribute of the **ExtendedProperties** element.</span></span> <span data-ttu-id="85068-198">Следующий служебный метод, реализованный в файле util. cpp в примере, выполняет сериализацию.</span><span class="sxs-lookup"><span data-stu-id="85068-198">The following utility method, implemented in the sample's Util.cpp file, performs the serialization.</span></span> <span data-ttu-id="85068-199">Он начинается с вызова функции [**стгсериализепропвариант**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) для выполнения двоичной сериализации, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="85068-199">It begins with a call to the [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) function to perform the binary serialization, as illustrated in the following code example.</span></span>


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



<span data-ttu-id="85068-200">Затем функция [**криптбинаритостринг**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)в, объявленная в винкрипт. h, выполняет преобразование Base64.</span><span class="sxs-lookup"><span data-stu-id="85068-200">Next, the [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â function, declared in Wincrypt.h, performs the Base64 conversion.</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



<span data-ttu-id="85068-201">Функция **десериализепропвариантфромстринг** , также найденная в файле util. cpp, обращается к операции десериализации значений из XML-файла.</span><span class="sxs-lookup"><span data-stu-id="85068-201">The **DeserializePropVariantFromString** function, also found in Util.cpp, reverses the operation, deserializing values from the XML file.</span></span>

<span data-ttu-id="85068-202">Дополнительные сведения о поддержке открытых метаданных см. в разделе "типы файлов, поддерживающие открытые метаданные" раздела [типы файлов](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="85068-202">For information about support for open metadata, see "File Types that Support Open Metadata" in [File Types](../shell/fa-file-types.md).</span></span>

## <a name="full-text-contents"></a><span data-ttu-id="85068-203">Содержимое Full-Text</span><span class="sxs-lookup"><span data-stu-id="85068-203">Full-Text Contents</span></span>

<span data-ttu-id="85068-204">Обработчики свойств также могут упростить полнотекстовый поиск содержимого файла, и они являются простым способом предоставления этих функций, если формат файла не слишком сложен.</span><span class="sxs-lookup"><span data-stu-id="85068-204">Property handlers can also facilitate a full-text search of the file contents, and they are an easy way to provide that functionality if the file format is not overly complicated.</span></span> <span data-ttu-id="85068-205">Существует альтернативный, более эффективный способ предоставления полного текста файла с помощью реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="85068-205">There is an alternative, more powerful way to provide the full text of the file through the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface implementation.</span></span>

<span data-ttu-id="85068-206">В следующей таблице приведены преимущества каждого из подходов, использующих [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) или [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="85068-206">The following table summarizes the benefits of each approach using either [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>



| <span data-ttu-id="85068-207">Функция</span><span class="sxs-lookup"><span data-stu-id="85068-207">Capability</span></span>                                   | <span data-ttu-id="85068-208">IFilter</span><span class="sxs-lookup"><span data-stu-id="85068-208">IFilter</span></span>                      | <span data-ttu-id="85068-209">ипропертисторе</span><span class="sxs-lookup"><span data-stu-id="85068-209">IPropertyStore</span></span> |
|----------------------------------------------|------------------------------|----------------|
| <span data-ttu-id="85068-210">Разрешает ли обратную запись в файлы?</span><span class="sxs-lookup"><span data-stu-id="85068-210">Allows write back to files?</span></span>                  | <span data-ttu-id="85068-211">Нет</span><span class="sxs-lookup"><span data-stu-id="85068-211">No</span></span>                           | <span data-ttu-id="85068-212">Да</span><span class="sxs-lookup"><span data-stu-id="85068-212">Yes</span></span>            |
| <span data-ttu-id="85068-213">Предоставляет сочетание содержимого и свойств?</span><span class="sxs-lookup"><span data-stu-id="85068-213">Provides mix of content and properties?</span></span>      | <span data-ttu-id="85068-214">Да</span><span class="sxs-lookup"><span data-stu-id="85068-214">Yes</span></span>                          | <span data-ttu-id="85068-215">Да</span><span class="sxs-lookup"><span data-stu-id="85068-215">Yes</span></span>            |
| <span data-ttu-id="85068-216">Многоязычных?</span><span class="sxs-lookup"><span data-stu-id="85068-216">Multilingual?</span></span>                                | <span data-ttu-id="85068-217">Да</span><span class="sxs-lookup"><span data-stu-id="85068-217">Yes</span></span>                          | <span data-ttu-id="85068-218">Нет</span><span class="sxs-lookup"><span data-stu-id="85068-218">No</span></span>             |
| <span data-ttu-id="85068-219">MIME/Embedded?</span><span class="sxs-lookup"><span data-stu-id="85068-219">MIME/Embedded?</span></span>                               | <span data-ttu-id="85068-220">Да</span><span class="sxs-lookup"><span data-stu-id="85068-220">Yes</span></span>                          | <span data-ttu-id="85068-221">Нет</span><span class="sxs-lookup"><span data-stu-id="85068-221">No</span></span>             |
| <span data-ttu-id="85068-222">Границы текста?</span><span class="sxs-lookup"><span data-stu-id="85068-222">Text boundaries?</span></span>                             | <span data-ttu-id="85068-223">Предложение, абзац, глава</span><span class="sxs-lookup"><span data-stu-id="85068-223">Sentence, paragraph, chapter</span></span> | <span data-ttu-id="85068-224">Нет</span><span class="sxs-lookup"><span data-stu-id="85068-224">None</span></span>           |
| <span data-ttu-id="85068-225">Реализация, поддерживаемая для SPS/SQL Server?</span><span class="sxs-lookup"><span data-stu-id="85068-225">Implementation supported for SPS/SQL Server?</span></span> | <span data-ttu-id="85068-226">Да</span><span class="sxs-lookup"><span data-stu-id="85068-226">Yes</span></span>                          | <span data-ttu-id="85068-227">Нет</span><span class="sxs-lookup"><span data-stu-id="85068-227">No</span></span>             |
| <span data-ttu-id="85068-228">Реализация</span><span class="sxs-lookup"><span data-stu-id="85068-228">Implementation</span></span>                               | <span data-ttu-id="85068-229">Complex</span><span class="sxs-lookup"><span data-stu-id="85068-229">Complex</span></span>                      | <span data-ttu-id="85068-230">Простота</span><span class="sxs-lookup"><span data-stu-id="85068-230">Simple</span></span>         |



 

<span data-ttu-id="85068-231">В образце обработчика рецептов формат файла рецепта не имеет сложных требований, поэтому для поддержки полнотекстового выполнения реализован только [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="85068-231">In the recipe handler sample, the recipe file format does not have any complex requirements, so only [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) has been implemented for full-text support.</span></span> <span data-ttu-id="85068-232">Полнотекстовый поиск реализуется для XML-узлов, указанных в следующем массиве.</span><span class="sxs-lookup"><span data-stu-id="85068-232">Full-text search is implemented for the XML nodes named in the following array.</span></span>


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



<span data-ttu-id="85068-233">Система свойств содержит `System.Search.Contents` свойство (содержимое для \_ поиска PKEY \_ ), которое было создано для предоставления полнотекстового содержимого индексатору.</span><span class="sxs-lookup"><span data-stu-id="85068-233">The property system contains the `System.Search.Contents` (PKEY\_Search\_Contents) property, which was created to provide full-text content to the indexer.</span></span> <span data-ttu-id="85068-234">Значение этого свойства никогда не отображается непосредственно в пользовательском интерфейсе; текст из всех узлов XML, указанных в приведенном выше массиве, объединяется в одну строку.</span><span class="sxs-lookup"><span data-stu-id="85068-234">This property's value is never displayed directly in the UI; the text from all of the XML nodes named in the array above are concatenated into a single string.</span></span> <span data-ttu-id="85068-235">Затем эта строка предоставляется индексатору в качестве полнотекстового содержимого файла рецепта с помощью вызова [**ипропертисторекаче:: сетвалуеандстате**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="85068-235">That string is then provided to the indexer as the full-text content of the recipe file through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a><span data-ttu-id="85068-236">Предоставление значений для свойств</span><span class="sxs-lookup"><span data-stu-id="85068-236">Providing Values for Properties</span></span>

<span data-ttu-id="85068-237">При использовании для считывания значений обработчики свойств обычно вызываются по одной из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="85068-237">When used to read values, property handlers are usually invoked for one of the following reasons:</span></span>

-   <span data-ttu-id="85068-238">Для перечисления всех значений свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-238">To enumerate all property values.</span></span>
-   <span data-ttu-id="85068-239">Для получения значения определенного свойства.</span><span class="sxs-lookup"><span data-stu-id="85068-239">To get the value of a specific property.</span></span>

<span data-ttu-id="85068-240">Для перечисления обработчику свойств предлагается перечислить его свойства либо во время индексирования, либо когда диалоговое окно свойств запрашивает свойства, отображаемые в **другой** группе.</span><span class="sxs-lookup"><span data-stu-id="85068-240">For enumeration, a property handler is asked to enumerate its properties either during indexing or when the properties dialog box asks for properties to display in the **Other** group.</span></span> <span data-ttu-id="85068-241">Индексирование постоянно выполняется как фоновая операция.</span><span class="sxs-lookup"><span data-stu-id="85068-241">Indexing goes on constantly as a background operation.</span></span> <span data-ttu-id="85068-242">При каждом изменении файла индексатор уведомляется, и он повторно индексирует файл, запросив обработчику свойств перечислить его свойства.</span><span class="sxs-lookup"><span data-stu-id="85068-242">Whenever a file changes, the indexer is notified, and it re-indexes the file by asking the property handler to enumerate its properties.</span></span> <span data-ttu-id="85068-243">Поэтому очень важно, чтобы обработчики свойств были эффективно реализованы и возвращали значения свойств как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="85068-243">Therefore, it is critical that property handlers are implemented efficiently and return property values as quickly as possible.</span></span> <span data-ttu-id="85068-244">Перечислите все свойства, для которых имеются значения, точно так же, как и для любой коллекции, но не перечислите свойства, использующие вычисления с интенсивным использованием памяти или сетевые запросы, которые могут затруднить их получение.</span><span class="sxs-lookup"><span data-stu-id="85068-244">Enumerate all the properties for which you have values, just as you would for any collection, but do not enumerate properties that involve memory-intensive calculations or network requests that could make them slow to retrieve.</span></span>

<span data-ttu-id="85068-245">При написании обработчика свойств, как правило, необходимо рассмотреть два следующих набора свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-245">When writing a property handler, you usually need to consider the following two sets of properties.</span></span>

-   <span data-ttu-id="85068-246">Основные свойства. свойства, которые поддерживает собственный тип файлов.</span><span class="sxs-lookup"><span data-stu-id="85068-246">Primary properties: Properties that your file type supports natively.</span></span> <span data-ttu-id="85068-247">Например, обработчик свойств Photo для метаданных файла изображения (EXIF), который изначально поддерживает `System.Photo.FNumber` .</span><span class="sxs-lookup"><span data-stu-id="85068-247">For example, a photo property handler for Exchangeable Image File (EXIF) metadata natively supports `System.Photo.FNumber`.</span></span>
-   <span data-ttu-id="85068-248">Расширенные свойства: свойства, которые поддерживаются типом файлов как часть открытых метаданных.</span><span class="sxs-lookup"><span data-stu-id="85068-248">Extended properties: Properties that your file type supports as part of open metadata.</span></span>

<span data-ttu-id="85068-249">Поскольку в этом примере используется кэш в памяти, реализация методов [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) заключается в делегировании к этому кэшу, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="85068-249">Because the sample uses in-memory cache, implementing [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods is just a matter of delegating to that cache, as illustrated in the following code example.</span></span>


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



<span data-ttu-id="85068-250">Если вы решили не делегировать кэш в памяти, необходимо реализовать методы, чтобы обеспечить> следующем ожидаемом поведении:</span><span class="sxs-lookup"><span data-stu-id="85068-250">If you choose not to delegate to the in-memory cache, you must implement your methods to provide> the following expected behavior:</span></span>

-   <span data-ttu-id="85068-251">[**Ипропертисторе:: NOCOUNT**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): Если нет свойств, этот метод возвращает значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="85068-251">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): If there are no properties, this method returns **S\_OK**.</span></span>
-   <span data-ttu-id="85068-252">[**Ипропертисторе:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): Если *ипроп* больше или равно *Кпропс*, этот метод возвращает E \_ INVALIDARG, а структура, на которую указывает параметр *PKEY* , заполняется нулями.</span><span class="sxs-lookup"><span data-stu-id="85068-252">[**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): If *iProp* is greater than or equal to *cProps*, this method returns E\_INVALIDARG and the structure pointed to by the *pkey* parameter is filled with zeroes.</span></span>
-   <span data-ttu-id="85068-253">[**Ипропертисторе::**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) NOCOUNT и [**Ипропертисторе:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) отражает текущее состояние обработчика свойства.</span><span class="sxs-lookup"><span data-stu-id="85068-253">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflect the current state of the property handler.</span></span> <span data-ttu-id="85068-254">Если [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) добавляется в файл или удаляется из него с помощью [**Ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), эти два метода должны отражать это изменение при следующем вызове.</span><span class="sxs-lookup"><span data-stu-id="85068-254">If a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) is added to or removed from the file through [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), these two methods must reflect that change the next time they are called.</span></span>
-   <span data-ttu-id="85068-255">[**Ипропертисторе:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): Если этот метод запрашивает значение, которое не существует, то оно возвращает **\_ ОК** , а значение, сообщаемое как VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="85068-255">[**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): If this method is asked for a value that does not exist, it returns **S\_OK** with the value reported as VT\_EMPTY.</span></span>

## <a name="writing-back-values"></a><span data-ttu-id="85068-256">Запись обратных значений</span><span class="sxs-lookup"><span data-stu-id="85068-256">Writing Back Values</span></span>

<span data-ttu-id="85068-257">Когда обработчик свойств записывает значение свойства с помощью [**ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), он не записывает значение в файл до тех пор, пока не будет вызван [**Ипропертисторе:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="85068-257">When the property handler writes the value of a property using [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), it does not write the value to the file until [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) is called.</span></span> <span data-ttu-id="85068-258">Кэш в памяти может быть полезен при реализации этой схемы.</span><span class="sxs-lookup"><span data-stu-id="85068-258">The in-memory cache can be useful in implementing this scheme.</span></span> <span data-ttu-id="85068-259">В образце кода реализация **ипропертисторе:: SetValue** просто задает новое значение в кэше в памяти и устанавливает для этого свойства состояние "нет на PSC \_ ".</span><span class="sxs-lookup"><span data-stu-id="85068-259">In the sample code the **IPropertyStore::SetValue** implementation simply sets the new value in the in-memory cache and sets the state of that property to PSC\_DIRTY.</span></span>


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



<span data-ttu-id="85068-260">В любой реализации [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) ожидается следующее поведение из [**Ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="85068-260">In any [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, the following behavior is expected from [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span></span>

-   <span data-ttu-id="85068-261">Если свойство уже существует, устанавливается значение свойства.</span><span class="sxs-lookup"><span data-stu-id="85068-261">If the property already exists, the value of the property is set.</span></span>
-   <span data-ttu-id="85068-262">Если свойство не существует, добавляется новое свойство и задается его значение.</span><span class="sxs-lookup"><span data-stu-id="85068-262">If the property does not exist, the new property is added and its value set.</span></span>
-   <span data-ttu-id="85068-263">Если значение свойства не может быть сохранено точно так же, как это было задано (например, усечение из-за ограничений размера в формате файла), значение задается как можно больше, и \_ \_ возвращается усечение с усеченным значением.</span><span class="sxs-lookup"><span data-stu-id="85068-263">If the property value cannot be persisted at the same accuracy as given (for instance, truncation due to size limitations in the file format), the value is set as far as possible and INPLACE\_S\_TRUNCATED is returned.</span></span>
-   <span data-ttu-id="85068-264">Если свойство не поддерживается обработчиком свойств, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` возвращается значение.</span><span class="sxs-lookup"><span data-stu-id="85068-264">If the property is not supported by the property handler, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` is returned.</span></span>
-   <span data-ttu-id="85068-265">Если существует другая причина, по которой невозможно задать значение свойства, например блокировка файла или отсутствие прав на изменение через списки управления доступом (ACL), \_ возвращается STG E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="85068-265">If there is another reason that the property value cannot be set, such as the file being locked or lack of rights to edit through access control lists (ACLs), then STG\_E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="85068-266">Одним из основных преимуществ использования потоков в качестве примера является надежность.</span><span class="sxs-lookup"><span data-stu-id="85068-266">One major advantage of using streams, as the sample, is reliability.</span></span> <span data-ttu-id="85068-267">Обработчики свойств должны всегда учитывать, что они не могут оставить файл в нестабильном состоянии в случае катастрофического сбоя.</span><span class="sxs-lookup"><span data-stu-id="85068-267">Property handlers must always consider that they cannot leave a file in an inconsistent state in the case of a catastrophic failure.</span></span> <span data-ttu-id="85068-268">Из-за повреждения файлов пользователя следует избегать, и лучший способ сделать это — использовать механизм копирования при записи.</span><span class="sxs-lookup"><span data-stu-id="85068-268">Corrupting a user's files obviously should be avoided, and the best way to do this is with a "copy-on-write" mechanism.</span></span> <span data-ttu-id="85068-269">Если обработчик свойств использует поток для доступа к файлу, это поведение будет получено автоматически. система записывает любые изменения в поток, заменяя файл новой копией только во время операции фиксации.</span><span class="sxs-lookup"><span data-stu-id="85068-269">If your property handler uses a stream to access a file, you get this behavior automatically; the system writes any changes to the stream, replacing the file with the new copy only during the commit operation.</span></span>

<span data-ttu-id="85068-270">Чтобы переопределить это поведение и управлять процессом сохранения файлов вручную, можно отказаться от безопасного сохранения, задав значение Мануалсафесаве в записи реестра обработчика, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="85068-270">To override this behavior and control the file saving process manually, you can opt out of the safe save behavior by setting the ManualSafeSave value in your handler's registry entry as illustrated here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

<span data-ttu-id="85068-271">Если обработчик задает значение Мануалсафесаве, то поток, с помощью которого он инициализируется, не является транзакционным потоком (СТГМ \_ транзакционным).</span><span class="sxs-lookup"><span data-stu-id="85068-271">When a handler specifies the ManualSafeSave value, the stream with which it is initialized is not a transacted stream (STGM\_TRANSACTED).</span></span> <span data-ttu-id="85068-272">Сам обработчик должен реализовать функцию безопасного сохранения, чтобы убедиться, что файл не поврежден, если операция сохранения прервана.</span><span class="sxs-lookup"><span data-stu-id="85068-272">The handler itself must implement the safe save function to ensure that the file is not corrupted if the save operation is interrupted.</span></span> <span data-ttu-id="85068-273">Если обработчик реализует встроенную запись, он выполняет запись в поток, который ему передан.</span><span class="sxs-lookup"><span data-stu-id="85068-273">If the handler implements in-place writing, it will write to the stream that it is given.</span></span> <span data-ttu-id="85068-274">Если обработчик не поддерживает эту функцию, он должен получить поток для записи обновленной копии файла с помощью [**идестинатионстреамфактори:: жетдестинатионстреам**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span><span class="sxs-lookup"><span data-stu-id="85068-274">If the handler does not support this feature, then it must retrieve a stream with which to write the updated copy of the file using [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span></span> <span data-ttu-id="85068-275">После того как обработчик закончит запись, он должен вызвать [**ипропертисторе:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) для исходного потока, чтобы завершить операцию, и заменить содержимое исходного потока новой копией файла.</span><span class="sxs-lookup"><span data-stu-id="85068-275">After the handler is done writing, it should call [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) on the original stream to complete the operation, and replace the contents of the original stream with the new copy of the file.</span></span>

<span data-ttu-id="85068-276">Мануалсафесаве также является ситуацией по умолчанию, если обработчик не инициализируется потоком.</span><span class="sxs-lookup"><span data-stu-id="85068-276">ManualSafeSave is also the default situation if you do not initialize your handler with a stream.</span></span> <span data-ttu-id="85068-277">Без исходного потока для получения содержимого временного потока необходимо использовать [**реплацефиле**](/windows/win32/api/winbase/nf-winbase-replacefilea) для выполнения атомарной замены исходного файла.</span><span class="sxs-lookup"><span data-stu-id="85068-277">Without an original stream to receive the contents of the temporary stream, you must use [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) to perform an atomic replacement of the source file.</span></span>

<span data-ttu-id="85068-278">Большие форматы файлов, которые будут использоваться способом создания файлов, превышающих 1 МБ, должны реализовать поддержку записи свойств на месте; в противном случае поведение производительности не соответствует ожиданиям клиентов системы свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-278">Large file formats that will be used in a way that produces files greater than 1 MB should implement support for in-place property writing; otherwise, the performance behavior does not meet the expectations of clients of the property system.</span></span> <span data-ttu-id="85068-279">В этом сценарии время, необходимое для записи свойств, не должно зависеть от размера файла.</span><span class="sxs-lookup"><span data-stu-id="85068-279">In this scenario, the time required to write properties should not be affected by the file size.</span></span>

<span data-ttu-id="85068-280">Для очень больших файлов, например видеофайла размером 1 ГБ или более, требуется другое решение.</span><span class="sxs-lookup"><span data-stu-id="85068-280">For very large files, for example a video file of 1 GB or more, a different solution is required.</span></span> <span data-ttu-id="85068-281">Если в файле недостаточно места для выполнения записи на месте, обработчик может завершиться ошибкой, если объем пространства, зарезервированного для записи свойств на месте, был исчерпан.</span><span class="sxs-lookup"><span data-stu-id="85068-281">If there is not enough space in the file to perform in-place writing, the handler may fail the property update if the amount of space reserved for in-place property writing has been exhausted.</span></span> <span data-ttu-id="85068-282">Эта ошибка возникает во избежание низкой производительности от 2 ГБ операций ввода-вывода (1 для чтения, 1 для записи).</span><span class="sxs-lookup"><span data-stu-id="85068-282">This failure occurs to avoid poor performance arising from 2 GB of IO (1 to read, 1 to write).</span></span> <span data-ttu-id="85068-283">Из-за такого сбоя эти форматы файлов должны резервировать достаточно места для записи свойств на месте.</span><span class="sxs-lookup"><span data-stu-id="85068-283">Because of this potential failure, these file formats should reserve enough space for in-place property writing.</span></span>

<span data-ttu-id="85068-284">Если файл содержит достаточно места в заголовке для записи метаданных, и если запись этих метаданных не приводит к увеличению или уменьшению файла, то может быть полезно писать на месте.</span><span class="sxs-lookup"><span data-stu-id="85068-284">If the file has enough space in its header to write metadata, and if the writing of that metadata does not cause the file to grow or shrink, it might be safe to write in-place.</span></span> <span data-ttu-id="85068-285">В качестве отправной точки рекомендуется использовать 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="85068-285">We recommend 64 KB as a starting point.</span></span> <span data-ttu-id="85068-286">Написание на месте эквивалентно обработчику, запрашивающему Мануалсафесаве и вызывающему метод [**IStream:: Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) в реализации [**Ипропертисторе:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), и имеет гораздо более высокую производительность, чем копирование на запись.</span><span class="sxs-lookup"><span data-stu-id="85068-286">Writing in-place is equivalent to the handler asking for ManualSafeSave and calling [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in the implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), and has much better performance than copy-on-write.</span></span> <span data-ttu-id="85068-287">Если размер файла изменяется из-за изменения значения свойства, запись на месте не должна быть выполнена из-за возможного повреждения файла в случае аварийного завершения.</span><span class="sxs-lookup"><span data-stu-id="85068-287">If the file size changes due to property value changes, writing in-place should not be attempted because of the potential for a corrupted file in the event of an abnormal termination.</span></span>

> [!Note]  
> <span data-ttu-id="85068-288">Для повышения производительности рекомендуется использовать параметр Мануалсафесаве с обработчиками свойств, которые работают с файлами размером 100 КБ или больше.</span><span class="sxs-lookup"><span data-stu-id="85068-288">For performance reasons we recommend that the ManualSafeSave option be used with property handlers working with files that are 100 KB or larger.</span></span>

 

<span data-ttu-id="85068-289">Как показано в следующем примере реализации [**ипропертисторе:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), обработчик для мануалсафесаве регистрируется, чтобы проиллюстрировать параметр безопасного сохранения вручную.</span><span class="sxs-lookup"><span data-stu-id="85068-289">As illustrated in the following sample implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), the handler for ManualSafeSave is registered to illustrate the manual safe save option.</span></span> <span data-ttu-id="85068-290">Метод **\_ савекачетодом** записывает значения свойств, хранящиеся в кэше в памяти, в объект XMLdocument.</span><span class="sxs-lookup"><span data-stu-id="85068-290">The **\_SaveCacheToDom** method writes the property values stored in the in-memory cache to the XMLdocument object.</span></span>


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



<span data-ttu-id="85068-291">Затем спросите, поддерживает ли занное [**идестинатионстреамфактори**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span><span class="sxs-lookup"><span data-stu-id="85068-291">Next, ask whether the pecified supports [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span></span>


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



<span data-ttu-id="85068-292">Затем зафиксируйте исходный поток, который записывает данные обратно в исходный файл в безопасном режиме.</span><span class="sxs-lookup"><span data-stu-id="85068-292">Next, commit the original stream, which writes the data back to the original file in a safe manner.</span></span>


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



<span data-ttu-id="85068-293">Затем изучите реализацию **\_ савекачетодом** .</span><span class="sxs-lookup"><span data-stu-id="85068-293">Then examine the **\_SaveCacheToDom** implementation.</span></span>


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



<span data-ttu-id="85068-294">Затем получите количество свойств, хранящихся в кэше в памяти.</span><span class="sxs-lookup"><span data-stu-id="85068-294">Next, get the number of properties stored in the in-memory cache.</span></span>


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



<span data-ttu-id="85068-295">Теперь можно выполнить итерацию по свойствам, чтобы определить, изменилось ли значение свойства с момента его загрузки в память.</span><span class="sxs-lookup"><span data-stu-id="85068-295">Now iterate through the properties to determine whether the value of a property has been changed since it was loaded into memory.</span></span>


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



<span data-ttu-id="85068-296">Метод [**ипропертисторекаче::**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) WebMethod возвращает состояние свойства в кэше.</span><span class="sxs-lookup"><span data-stu-id="85068-296">The [**IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) method gets the state of the property in the cache.</span></span> <span data-ttu-id="85068-297">Флаг PSC \_ Dirty, заданный в реализации [**ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) , помечает свойство как измененное.</span><span class="sxs-lookup"><span data-stu-id="85068-297">The PSC\_DIRTY flag, which was set in the [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) implementation, marks a property as changed.</span></span>


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



<span data-ttu-id="85068-298">Сопоставьте свойство с XML-узлом, как указано в массиве **\_ ргпропертимап** .</span><span class="sxs-lookup"><span data-stu-id="85068-298">Map the property to the XML node as specified in the **eg\_rgPropertyMap** array.</span></span>


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



<span data-ttu-id="85068-299">Если свойство отсутствует в сопоставлении, это новое свойство, установленное проводником Windows.</span><span class="sxs-lookup"><span data-stu-id="85068-299">If a property is not in the map, it is a new property that was set by Windows Explorer.</span></span> <span data-ttu-id="85068-300">Так как поддерживаются открытые метаданные, сохраните новое свойство в разделе **РАСШИРЕННЫХ свойств** XML.</span><span class="sxs-lookup"><span data-stu-id="85068-300">Because open metadata is supported, save the new property in the **ExtendedProperties** section of the XML.</span></span>


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a><span data-ttu-id="85068-301">Реализация Ипропертисторекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="85068-301">Implementing IPropertyStoreCapabilities</span></span>

<span data-ttu-id="85068-302">[**Ипропертисторекапабилитиес**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) информирует пользовательский интерфейс оболочки о возможности редактирования определенного свойства в пользовательском интерфейсе оболочки.</span><span class="sxs-lookup"><span data-stu-id="85068-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informs the Shell UI whether a particular property can be edited in the Shell UI.</span></span> <span data-ttu-id="85068-303">Важно отметить, что это связано только с возможностью изменения свойства в пользовательском интерфейсе, а также в том, можно ли успешно вызвать метод [**ипропертисторе:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) для свойства.</span><span class="sxs-lookup"><span data-stu-id="85068-303">It is important to note that this relates only to the ability to edit the property in the UI, not whether you can successfully call [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) on the property.</span></span> <span data-ttu-id="85068-304">Свойство, провокес возвращаемое значение S \_ false из [**ипропертисторекапабилитиес:: испропертивритабле**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) , по-прежнему может быть настроено через приложение.</span><span class="sxs-lookup"><span data-stu-id="85068-304">A property that provokes a return value of S\_FALSE from [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) might still be capable of being set through an application.</span></span>


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



<span data-ttu-id="85068-305">[**Испропертивритабле**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) возвращает **" \_ ОК** ", чтобы указать, что конечным пользователям следует разрешить изменение свойства напрямую; \_Значение false указывает, что они не должны.</span><span class="sxs-lookup"><span data-stu-id="85068-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) returns **S\_OK** to indicate that end users should be allowed to edit the property directly; S\_FALSE indicates that they should not.</span></span> <span data-ttu-id="85068-306">\_Значение false может означать, что приложения отвечают за написание свойства, а не пользователей.</span><span class="sxs-lookup"><span data-stu-id="85068-306">S\_FALSE can mean that applications are responsible for writing the property, not users.</span></span> <span data-ttu-id="85068-307">Оболочка отключает редактирование элементов управления в соответствии с результатами вызовов этого метода.</span><span class="sxs-lookup"><span data-stu-id="85068-307">The Shell disables editing controls as appropriate based on the results of calls to this method.</span></span> <span data-ttu-id="85068-308">Предполагается, что обработчик, не реализующий [**ипропертисторекапабилитиес**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) , поддерживает открытые метаданные посредством поддержки записи любого свойства.</span><span class="sxs-lookup"><span data-stu-id="85068-308">A handler that does not implement [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) is assumed to support open metadata through support for the writing of any property.</span></span>

<span data-ttu-id="85068-309">При создании обработчика, который обрабатывает только свойства, доступные только для чтения, следует реализовать метод **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**иинитиализевиситем**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)или [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)), чтобы он возвращал STG \_ E \_ ACCESSDENIED при вызове с \_ флагом стгм ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="85068-309">If you are building a handler that handles only read-only properties, then you should implement your **Initialize** method ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem), or [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) so that it returns STG\_E\_ACCESSDENIED when called with the STGM\_READWRITE flag.</span></span>

<span data-ttu-id="85068-310">Для некоторых свойств атрибут [исиннате](./propdesc-schema-typeinfo.md) имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="85068-310">Some properties have their [isInnate](./propdesc-schema-typeinfo.md) attribute set to **true**.</span></span> <span data-ttu-id="85068-311">Свойства присущей имеют следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="85068-311">Innate properties have the following characteristics:</span></span>

-   <span data-ttu-id="85068-312">Свойство обычно вычисляется каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="85068-312">The property is usually calculated in some way.</span></span> <span data-ttu-id="85068-313">Например, `System.Image.BitDepth` вычисляется на основе самого изображения.</span><span class="sxs-lookup"><span data-stu-id="85068-313">For instance, `System.Image.BitDepth` is calculated from the image itself.</span></span>
-   <span data-ttu-id="85068-314">Изменение свойства не имеет смысла, не изменяя файл.</span><span class="sxs-lookup"><span data-stu-id="85068-314">Changing the property would not make sense without changing the file.</span></span> <span data-ttu-id="85068-315">Например, изменение `System.Image.Dimensions` не приведет к изменению размера изображения, поэтому нет смысла разрешать пользователю изменять его.</span><span class="sxs-lookup"><span data-stu-id="85068-315">For instance, changing `System.Image.Dimensions` would not resize the image, so it does not make sense to allow the user to change it.</span></span>
-   <span data-ttu-id="85068-316">В некоторых случаях эти свойства предоставляются системой автоматически.</span><span class="sxs-lookup"><span data-stu-id="85068-316">In some cases, these properties are provided automatically by the system.</span></span> <span data-ttu-id="85068-317">Примеры включают в себя `System.DateModified` , предоставляемые файловой системой, и `System.SharedWith` , основанные на том, кому предоставлен доступ к файлу.</span><span class="sxs-lookup"><span data-stu-id="85068-317">Examples include `System.DateModified`, which is provided by the file system, and `System.SharedWith`, which is based on who the user is sharing the file with.</span></span>

<span data-ttu-id="85068-318">Из-за этих характеристик свойства, помеченные как *исиннате* , предоставляются пользователю в пользовательском интерфейсе оболочки только в качестве свойств, доступных только для чтения.</span><span class="sxs-lookup"><span data-stu-id="85068-318">Due to these characteristics, properties marked as *IsInnate* are provided to the user in the Shell UI only as read-only properties.</span></span> <span data-ttu-id="85068-319">Если свойство помечено как *исиннате*, система свойств не сохраняет это свойство в обработчике свойств.</span><span class="sxs-lookup"><span data-stu-id="85068-319">If a property is marked as *IsInnate*, the property system does not store that property in the property handler.</span></span> <span data-ttu-id="85068-320">Поэтому обработчики свойств не требуют специального кода для учета этих свойств в своих реализациях.</span><span class="sxs-lookup"><span data-stu-id="85068-320">Therefore, property handlers do not need special code to account for these properties in their implementations.</span></span> <span data-ttu-id="85068-321">Если значение атрибута *исиннате* явно не указано для конкретного свойства, значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="85068-321">If the value of the *IsInnate* attribute is not explicitly stated for a particular property, the default value is **false**.</span></span>

## <a name="registering-and-distributing-property-handlers"></a><span data-ttu-id="85068-322">Регистрация и распространение обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="85068-322">Registering and Distributing Property Handlers</span></span>

<span data-ttu-id="85068-323">При реализации обработчика свойств необходимо зарегистрировать его и расширение имени файла, связанное с обработчиком.</span><span class="sxs-lookup"><span data-stu-id="85068-323">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="85068-324">Дополнительные сведения см. в разделе [Регистрация и распространение обработчиков свойств](./prophand-reg-dist.md).</span><span class="sxs-lookup"><span data-stu-id="85068-324">For more information, see [Registering and Distributing Property Handlers](./prophand-reg-dist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="85068-325">См. также</span><span class="sxs-lookup"><span data-stu-id="85068-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85068-326">Основные сведения о обработчиках свойств</span><span class="sxs-lookup"><span data-stu-id="85068-326">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="85068-327">Использование имен видов</span><span class="sxs-lookup"><span data-stu-id="85068-327">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="85068-328">Использование списков свойств</span><span class="sxs-lookup"><span data-stu-id="85068-328">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="85068-329">Регистрация и распространение обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="85068-329">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="85068-330">Рекомендации и вопросы и ответы по обработчикам свойств</span><span class="sxs-lookup"><span data-stu-id="85068-330">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
