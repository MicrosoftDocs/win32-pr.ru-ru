---
description: Реализация Ивикметадатаблоккреадер
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Реализация Ивикметадатаблоккреадер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910167"
---
# <a name="implementing-iwicmetadatablockreader"></a><span data-ttu-id="36582-103">Реализация Ивикметадатаблоккреадер</span><span class="sxs-lookup"><span data-stu-id="36582-103">Implementing IWICMetadataBlockReader</span></span>

## <a name="iwicmetadatablockreader"></a><span data-ttu-id="36582-104">ивикметадатаблоккреадер</span><span class="sxs-lookup"><span data-stu-id="36582-104">IWICMetadataBlockReader</span></span>

<span data-ttu-id="36582-105">В образе часто существует несколько блоков метаданных, каждый из которых предоставляет различные типы данных в различных форматах.</span><span class="sxs-lookup"><span data-stu-id="36582-105">Multiple blocks of metadata often exist within an image, each exposing different types of information in different formats.</span></span> <span data-ttu-id="36582-106">В модели компонента обработки изображений Windows (WIC) обработчики метаданных — это отдельные компоненты, которые, как и декодеры, обнаруживаются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="36582-106">In the Windows Imaging Component (WIC) model, metadata handlers are distinct components that, like decoders, are discoverable at run time.</span></span> <span data-ttu-id="36582-107">Каждый формат метаданных имеет отдельный обработчик, и каждый из этих обработчиков метаданных можно использовать с любым форматом изображения, поддерживающим формат метаданных, который он обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="36582-107">Each metadata format has a separate handler, and each of these metadata handlers can be used with any image format that supports the metadata format it handles.</span></span> <span data-ttu-id="36582-108">Таким образом, если формат изображения поддерживает EXIF, XMP, IPTC или другой формат, можно воспользоваться стандартными обработчиками метаданных для этих форматов, поставляемых с WIC, и вам не нужно писать собственный.</span><span class="sxs-lookup"><span data-stu-id="36582-108">Therefore, if your image format supports EXIF, XMP, IPTC, or another format, you can take advantage of the standard metadata handlers for these formats that ship with WIC, and you do not need to write your own.</span></span> <span data-ttu-id="36582-109">Конечно, при создании нового формата метаданных необходимо написать для него обработчик метаданных, который будет обнаружен и вызван во время выполнения точно так же, как стандартные.</span><span class="sxs-lookup"><span data-stu-id="36582-109">Of course, if you create a new metadata format, you must write a metadata handler for it, which will be discovered and invoked at run time just as the standard ones are.</span></span>

> [!Note]  
> <span data-ttu-id="36582-110">Если формат изображения основан на формате TIFF или в контейнере JPEG, то не нужно писать какие-либо обработчики метаданных (если не разработать новый или собственный формат метаданных).</span><span class="sxs-lookup"><span data-stu-id="36582-110">If your image format is based on a Tagged Image File Format (TIFF) or JPEG container, you won’t need to write any metadata handlers (unless you develop a new or proprietary metadata format).</span></span> <span data-ttu-id="36582-111">В контейнерах TIFF и JPEG блоки метаданных находятся в IFD, а каждый контейнер имеет отдельную структуру IFD.</span><span class="sxs-lookup"><span data-stu-id="36582-111">In TIFF and JPEG containers, blocks of metadata are located within IFDs, and each container has a different IFD structure.</span></span> <span data-ttu-id="36582-112">WIC предоставляет обработчики IFD для обоих форматов контейнеров, которые переходят по структуре IFD и делегируют стандартные обработчики метаданных для доступа к метаданным в них.</span><span class="sxs-lookup"><span data-stu-id="36582-112">WIC provides IFD handlers for both of these container formats that navigate the IFD structure and delegate to the standard metadata handlers to access the metadata within them.</span></span> <span data-ttu-id="36582-113">Таким образом, если ваш формат изображения основан на любом из этих контейнеров, можно автоматически воспользоваться преимуществами обработчиков WIC IFD.</span><span class="sxs-lookup"><span data-stu-id="36582-113">So, if your image format is based on either of these containers, you can automatically take advantage of the WIC IFD handlers.</span></span> <span data-ttu-id="36582-114">Однако если у вас есть собственный формат контейнера, имеющий собственную уникальную структуру метаданных верхнего уровня, необходимо написать обработчик, который может перемещаться по структуре верхнего уровня и делегировать их соответствующим обработчикам метаданных, как и обработчики IFD.)</span><span class="sxs-lookup"><span data-stu-id="36582-114">However, if you have a proprietary container format that has its own unique top-level metadata structure, you must write a handler that can navigate that top-level structure and delegate to the appropriate metadata handlers, just like the IFD handlers do.)</span></span>

 

<span data-ttu-id="36582-115">Аналогичным образом WIC предоставляет уровень абстракции для приложений, которые позволяют им работать со всеми форматами изображений таким же образом через согласованный набор интерфейсов, WIC обеспечивает уровень абстракции для авторов кодеков в отношении форматов метаданных.</span><span class="sxs-lookup"><span data-stu-id="36582-115">The same way WIC provides a layer of abstraction for applications that allows them to work with all image formats in the same way through a consistent set of interfaces, WIC provides a layer of abstraction for codec authors with regard to metadata formats.</span></span> <span data-ttu-id="36582-116">Как отмечалось ранее, авторы кодека, как правило, не нуждаются в непосредственной работе с различными форматами метаданных, которые могут присутствовать в образе.</span><span class="sxs-lookup"><span data-stu-id="36582-116">As noted previously, codec authors generally do not need to work directly with the various metadata formats that may be present in an image.</span></span> <span data-ttu-id="36582-117">Однако каждый автор кодека отвечает за предоставление способа перечисления блоков метаданных, чтобы можно было обнаружить и создать для каждого блока соответствующий обработчик метаданных.</span><span class="sxs-lookup"><span data-stu-id="36582-117">However, every codec author is responsible for providing a way to enumerate the blocks of metadata so an appropriate metadata handler can be discovered and instantiated for each block.</span></span>

<span data-ttu-id="36582-118">Этот интерфейс необходимо реализовать в классе декодирования на уровне кадров.</span><span class="sxs-lookup"><span data-stu-id="36582-118">You must implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="36582-119">Также может потребоваться реализовать его на классе декодера уровня контейнера, если формат изображения предоставляет глобальные метаданные за пределами отдельных кадров изображения.</span><span class="sxs-lookup"><span data-stu-id="36582-119">You may also need to implement it on your container-level decoder class if your image format exposes global metadata outside of any individual image frames.</span></span>

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [<span data-ttu-id="36582-120">жетконтаинерформат</span><span class="sxs-lookup"><span data-stu-id="36582-120">GetContainerFormat</span></span>](#getcontainerformat)
-   [<span data-ttu-id="36582-121">GetCount</span><span class="sxs-lookup"><span data-stu-id="36582-121">GetCount</span></span>](#getcount)
-   [<span data-ttu-id="36582-122">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="36582-122">GetEnumerator</span></span>](#getenumerator)
-   [<span data-ttu-id="36582-123">жетреадербиндекс</span><span class="sxs-lookup"><span data-stu-id="36582-123">GetReaderByIndex</span></span>](#getreaderbyindex)

### <a name="getcontainerformat"></a><span data-ttu-id="36582-124">жетконтаинерформат</span><span class="sxs-lookup"><span data-stu-id="36582-124">GetContainerFormat</span></span>

<span data-ttu-id="36582-125">[**Жетконтаинерформат**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) совпадает с методом [Жетконтаинерформат](-wic-imp-iwicbitmapdecoder.md) для [реализации ивикбитмапдекодер](-wic-imp-iwicbitmapdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="36582-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) is the same as the [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) method on [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span></span>

### <a name="getcount"></a><span data-ttu-id="36582-126">GetCount</span><span class="sxs-lookup"><span data-stu-id="36582-126">GetCount</span></span>

<span data-ttu-id="36582-127">Функция [**NOCOUNT**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) возвращает количество блоков метаданных верхнего уровня, связанных с кадром.</span><span class="sxs-lookup"><span data-stu-id="36582-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) returns the number of top-level metadata blocks associated with the frame.</span></span>

### <a name="getenumerator"></a><span data-ttu-id="36582-128">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="36582-128">GetEnumerator</span></span>

<span data-ttu-id="36582-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) Возвращает перечислитель, который вызывающий может использовать для перечисления блоков метаданных в кадре и чтения их метаданных.</span><span class="sxs-lookup"><span data-stu-id="36582-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) returns an enumerator that the caller can use to enumerate over the metadata blocks in the frame and read their metadata.</span></span> <span data-ttu-id="36582-130">Чтобы реализовать этот метод, необходимо создать модуль чтения метаданных для каждого блока метаданных и реализовать объект перечисления, который перечисляет коллекцию модулей чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="36582-130">To implement this method, you need to create a metadata reader for each block of metadata, and implement an enumeration object that enumerates over the collection of metadata readers.</span></span> <span data-ttu-id="36582-131">Объект перечисления должен реализовывать [иенумункновн](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) , чтобы его можно было привести к иенумункновн при возврате в параметр *ппиенумметадата* .</span><span class="sxs-lookup"><span data-stu-id="36582-131">The enumeration object must implement [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) so you can cast it to IEnumUnknown when you return it in the *ppIEnumMetadata* parameter.</span></span>

<span data-ttu-id="36582-132">При реализации объекта перечисления можно создать все средства чтения метаданных при первом создании объекта [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) или при создании объекта перечисления, или же вы можете создать их неактивно внутри реализации метода [Иенумункновн:: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) .</span><span class="sxs-lookup"><span data-stu-id="36582-132">When implementing the enumeration object, you can create all the metadata readers when you first create the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object or when you first create the enumeration object, or you can create them lazily inside the implementation of the [IEnumUnknown::Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) method.</span></span> <span data-ttu-id="36582-133">Во многих случаях более эффективно создавать их с отложенным созданием, но в следующем примере все средства чтения блокировок создаются в конструкторе для экономии пространства.</span><span class="sxs-lookup"><span data-stu-id="36582-133">In many cases, it’s more efficient to create them lazily but, in the following example, the block readers are all created in the constructor to save space.</span></span>


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



<span data-ttu-id="36582-134">Для создания модулей чтения метаданных используется метод [**креатеметадатареадерфромконтаинер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) .</span><span class="sxs-lookup"><span data-stu-id="36582-134">To create the metadata readers, you use the [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) method.</span></span> <span data-ttu-id="36582-135">При вызове этого метода вы передаете идентификатор GUID формата контейнера в параметре *гуидконтаинерформат* .</span><span class="sxs-lookup"><span data-stu-id="36582-135">When invoking this method, you pass in the GUID of the container format in the *guidContainerFormat* parameter.</span></span> <span data-ttu-id="36582-136">Если у вас есть предпочтение поставщика для читателя метаданных, можно передать идентификатор GUID предпочтительного поставщика в параметре *пгуидвендор* .</span><span class="sxs-lookup"><span data-stu-id="36582-136">If you have a preference of vendor for a metadata reader, you can pass the GUID of your preferred vendor in the *pGuidVendor* parameter.</span></span> <span data-ttu-id="36582-137">Например, если компания записывает обработчики метаданных и вы хотите использовать собственный при наличии, можно передать идентификатор GUID поставщика.</span><span class="sxs-lookup"><span data-stu-id="36582-137">For example, if your company writes metadata handlers, and you want to use your own if present, you can pass in your vendor GUID.</span></span> <span data-ttu-id="36582-138">В большинстве случаев необходимо просто передать **значение NULL** и позволить системе выбрать соответствующий модуль чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="36582-138">In most cases, you would just pass **NULL**, and let the system select the appropriate metadata reader.</span></span> <span data-ttu-id="36582-139">Если вы запрашиваете конкретного поставщика и у него есть средство чтения метаданных на компьютере, то компонент WIC возвратит читателя этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="36582-139">If you do request a specific vendor, and that vendor does have a metadata reader installed on the computer, WIC will return that vendor’s reader.</span></span> <span data-ttu-id="36582-140">Однако если запрошенному поставщику не назначен модуль чтения метаданных на компьютере и имеется соответствующий модуль чтения метаданных, этот модуль чтения будет возвращен, даже если он не является предпочтительным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="36582-140">However, if the requested vendor does not have a metadata reader installed on the computer, and if there is an appropriate metadata reader available, that reader will be returned even though it is not from the preferred vendor.</span></span> <span data-ttu-id="36582-141">Если на компьютере нет средства чтения метаданных для типа метаданных в блоке, фабрика компонентов вернет неизвестный обработчик метаданных, который будет обрабатывать блок метаданных как большой двоичный объект (BLOB) и десериализовать блок метаданных из файла без каких-либо попыток их синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="36582-141">If there is no metadata reader on the computer for the type of metadata in the block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB), and will deserialize the block of metadata from the file without any attempt at parsing it.</span></span>

<span data-ttu-id="36582-142">Для параметра *двоптионс* выполните операцию или между соответствующим [**Викперсистоптионс**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) с соответствующим [**викметадатакреатионоптионс**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions).</span><span class="sxs-lookup"><span data-stu-id="36582-142">For the *dwOptions* parameter, perform an OR operation between the appropriate [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) with the appropriate [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions).</span></span> <span data-ttu-id="36582-143">**Викперсистоптионс** описывает, как располагается контейнер. По умолчанию используется прямой порядок байтов.</span><span class="sxs-lookup"><span data-stu-id="36582-143">The **WICPersistOptions** describe how your container is laid out. Little-endian is the default.</span></span>

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

<span data-ttu-id="36582-144">[**Викметадатакреатионоптионс**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) укажите, нужно ли вернуть ункновнметадатахандлер, если на компьютере не найден модуль чтения метаданных, который может считывать формат метаданных определенного блока.</span><span class="sxs-lookup"><span data-stu-id="36582-144">The [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) specify whether you want to get back the UnknownMetadataHandler if no metadata reader is found on the machine that can read the metadata format of a particular block.</span></span> <span data-ttu-id="36582-145">**Викметадатакреатионалловункновн** используется по умолчанию, и всегда следует разрешать создание ункновнметадтатахандлер.</span><span class="sxs-lookup"><span data-stu-id="36582-145">**WICMetadataCreationAllowUnknown** is the default, and you should always allow creation of the UnknownMetadtataHandler.</span></span> <span data-ttu-id="36582-146">Ункновнметадатахандлер обрабатывает нераспознанные метаданные как большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="36582-146">The UnknownMetadataHandler treats unrecognized metadata as a BLOB.</span></span> <span data-ttu-id="36582-147">Он не может выполнить синтаксический анализ, но он записывает его в поток как большой двоичный объект и сохраняет его без изменений при обратной записи в поток во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="36582-147">It cannot parse it, but it writes it out into the stream as a BLOB, and persists it intact when it’s written back to the stream during encoding.</span></span> <span data-ttu-id="36582-148">Это позволяет обезопасить создание обработчиков метаданных для собственных метаданных или форматов метаданных, которые не поставляются с системой.</span><span class="sxs-lookup"><span data-stu-id="36582-148">This makes it safe to create metadata handlers for proprietary metadata or metadata formats that don’t ship with the system.</span></span> <span data-ttu-id="36582-149">Так как метаданные сохраняются без изменений, даже если на компьютере, который его распознает, нет обработчика, то при последующей установке соответствующего обработчика метаданных метаданные по-прежнему будут доступны для чтения.</span><span class="sxs-lookup"><span data-stu-id="36582-149">Because metadata is preserved intact, even if no handler is present on the computer that recognizes it, when an appropriate metadata handler is later installed, the metadata will still be there and can be read.</span></span> <span data-ttu-id="36582-150">Если вы не разрешаете создание Ункновнметадатахандлер, альтернативой является отмена или перезапись нераспознанных метаданных.</span><span class="sxs-lookup"><span data-stu-id="36582-150">If you don’t allow creation of the UnknownMetadataHandler, the alternative is discarding or overwriting unrecognized metadata.</span></span> <span data-ttu-id="36582-151">Это форма потери данных.</span><span class="sxs-lookup"><span data-stu-id="36582-151">This is a form of data loss.</span></span>

> [!Note]  
> <span data-ttu-id="36582-152">При написании собственного обработчика метаданных для частных метаданных никогда не следует включать ссылки на что-либо за пределы самого блока метаданных.</span><span class="sxs-lookup"><span data-stu-id="36582-152">If you write your own metadata handler for proprietary metadata, you should never include references to anything outside the metadata block itself.</span></span> <span data-ttu-id="36582-153">Несмотря на то, что Ункновнметадатахандлер сохраняет метаданные без изменений, метаданные перемещаются при редактировании файлов, а все ссылки на что-либо за пределами собственного блока больше не будут действительными в этом случае.</span><span class="sxs-lookup"><span data-stu-id="36582-153">Even though the UnknownMetadataHandler preserves metadata intact, metadata does get moved when files are edited, and any references to anything outside its own block will no longer be valid when this happens.</span></span>

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

<span data-ttu-id="36582-154">Параметр *пистреам* — это фактический поток, декодированный.</span><span class="sxs-lookup"><span data-stu-id="36582-154">The *pIStream* parameter is the actual stream that you are decoding.</span></span> <span data-ttu-id="36582-155">Перед передачей в поток следует перейти к началу блока метаданных, для которого запрашивается читатель.</span><span class="sxs-lookup"><span data-stu-id="36582-155">Before passing in the stream, you should seek to the beginning of the metadata block for which you’re requesting a reader.</span></span> <span data-ttu-id="36582-156">Соответствующий модуль чтения метаданных для блока метаданных в текущей позиции в [IStream](/windows/desktop/api/objidl/nn-objidl-istream) будет возвращен в параметре *ппиреадер* .</span><span class="sxs-lookup"><span data-stu-id="36582-156">The appropriate metadata reader for the metadata block at the current position in the [IStream](/windows/desktop/api/objidl/nn-objidl-istream) will be returned in the *ppiReader* parameter.</span></span>

### <a name="getreaderbyindex"></a><span data-ttu-id="36582-157">жетреадербиндекс</span><span class="sxs-lookup"><span data-stu-id="36582-157">GetReaderByIndex</span></span>

<span data-ttu-id="36582-158">[**Жетреадербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) возвращает модуль чтения метаданных по запрошенному индексу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="36582-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) returns the metadata reader at the requested index in the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36582-159">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="36582-159">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="36582-160">**Reference**</span><span class="sxs-lookup"><span data-stu-id="36582-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="36582-161">**ивикметадатаблоккреадер**</span><span class="sxs-lookup"><span data-stu-id="36582-161">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="36582-162">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="36582-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="36582-163">Реализация IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="36582-163">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="36582-164">Реализация Ивикбитмапсаурцетрансформ</span><span class="sxs-lookup"><span data-stu-id="36582-164">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="36582-165">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="36582-165">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="36582-166">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="36582-166">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
