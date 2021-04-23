---
description: Реализация Ивикметадатаблокквритер
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Реализация Ивикметадатаблокквритер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547050"
---
# <a name="implementing-iwicmetadatablockwriter"></a><span data-ttu-id="597a7-103">Реализация Ивикметадатаблокквритер</span><span class="sxs-lookup"><span data-stu-id="597a7-103">Implementing IWICMetadataBlockWriter</span></span>

## <a name="iwicmetadatablockwriter"></a><span data-ttu-id="597a7-104">ивикметадатаблокквритер</span><span class="sxs-lookup"><span data-stu-id="597a7-104">IWICMetadataBlockWriter</span></span>

-   [<span data-ttu-id="597a7-105">инитиализефромблоккреадер</span><span class="sxs-lookup"><span data-stu-id="597a7-105">InitializeFromBlockReader</span></span>](#initializefromblockreader)
-   [<span data-ttu-id="597a7-106">жетвритербиндекс</span><span class="sxs-lookup"><span data-stu-id="597a7-106">GetWriterByIndex</span></span>](#getwriterbyindex)
-   [<span data-ttu-id="597a7-107">аддвритер</span><span class="sxs-lookup"><span data-stu-id="597a7-107">AddWriter</span></span>](#addwriter)
-   [<span data-ttu-id="597a7-108">сетвритербиндекс</span><span class="sxs-lookup"><span data-stu-id="597a7-108">SetWriterByIndex</span></span>](#setwriterbyindex)
-   [<span data-ttu-id="597a7-109">ремовевритербиндекс</span><span class="sxs-lookup"><span data-stu-id="597a7-109">RemoveWriterByIndex</span></span>](#removewriterbyindex)

<span data-ttu-id="597a7-110">Класс кодирования на уровне кадров реализует этот интерфейс для предоставления всех блоков метаданных и запроса соответствующего модуля записи метаданных для каждого блока.</span><span class="sxs-lookup"><span data-stu-id="597a7-110">The frame-level encoding class implements this interface to expose all the metadata blocks and request the appropriate metadata writer for each block.</span></span> <span data-ttu-id="597a7-111">Если формат изображения поддерживает глобальные метаданные вне отдельных фреймов, следует также реализовать этот интерфейс в классе кодировщика уровня контейнера.</span><span class="sxs-lookup"><span data-stu-id="597a7-111">If your image format supports global metadata, outside of any individual frame, you should also implement this interface on the container-level encoder class.</span></span> <span data-ttu-id="597a7-112">Более подробное описание обработчиков метаданных см. в разделе [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) в разделе Реализация декодера WIC-Enabled.</span><span class="sxs-lookup"><span data-stu-id="597a7-112">For a more detailed discussion of metadata handlers, refer to the section on the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the section on Implementing a WIC-Enabled Decoder.</span></span>

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a><span data-ttu-id="597a7-113">инитиализефромблоккреадер</span><span class="sxs-lookup"><span data-stu-id="597a7-113">InitializeFromBlockReader</span></span>

<span data-ttu-id="597a7-114">[**Инитиализефромблоккреадер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) использует [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) для инициализации модуля записи блока.</span><span class="sxs-lookup"><span data-stu-id="597a7-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) uses an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) to initialize the block writer.</span></span> <span data-ttu-id="597a7-115">**Ивикметадатаблоккреадер** можно получить из декодера, который декодирует образ.</span><span class="sxs-lookup"><span data-stu-id="597a7-115">You can get the **IWICMetadataBlockReader** from the decoder that decoded the image.</span></span>


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



<span data-ttu-id="597a7-116">Поскольку инициализация [**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) с помощью [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) создает экземпляр модуля записи метаданных для каждого модуля чтения метаданных, предоставляемого объектом **ивикметадатаблоккреадер** , приложению не нужно явным образом запрашивать модуль записи для каждого блока метаданных.</span><span class="sxs-lookup"><span data-stu-id="597a7-116">Because initializing the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) with an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instantiates a metadata writer for each metadata reader exposed by the **IWICMetadataBlockReader** object, the application doesn’t have to explicitly request a writer for each block of metadata.</span></span>

### <a name="getwriterbyindex"></a><span data-ttu-id="597a7-117">жетвритербиндекс</span><span class="sxs-lookup"><span data-stu-id="597a7-117">GetWriterByIndex</span></span>

<span data-ttu-id="597a7-118">[**Жетвритербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) возвращает объект [**ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) для n-го блока метаданных, где n — это значение, передаваемое в параметре *ниндекс* .</span><span class="sxs-lookup"><span data-stu-id="597a7-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) returns the [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) object for the nth metadata block, where n is the value passed in the *nIndex* parameter.</span></span> <span data-ttu-id="597a7-119">Если нет зарегистрированного модуля записи метаданных, который может обрабатывать тип метаданных в блоке n, фабрика компонентов вернет неизвестный обработчик метаданных, который будет обрабатывать блок метаданных как большой двоичный объект (BLOB).</span><span class="sxs-lookup"><span data-stu-id="597a7-119">If there is no metadata writer registered that can handle the type of metadata in the nth block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB).</span></span> <span data-ttu-id="597a7-120">Она будет сериализована как битовый поток без попытки его анализа.</span><span class="sxs-lookup"><span data-stu-id="597a7-120">It will serialize it out as a bit stream without attempting to parse it.</span></span>

### <a name="addwriter"></a><span data-ttu-id="597a7-121">аддвритер</span><span class="sxs-lookup"><span data-stu-id="597a7-121">AddWriter</span></span>

<span data-ttu-id="597a7-122">[**Аддвритер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) позволяет вызывающему объекту добавить новый модуль записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="597a7-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) allows a caller to add a new metadata writer.</span></span> <span data-ttu-id="597a7-123">Это необходимо, если приложению требуется добавить метаданные другого формата, чем любой из существующих блоков метаданных.</span><span class="sxs-lookup"><span data-stu-id="597a7-123">This is required if an application wants to add metadata of a different format than any of the existing metadata blocks.</span></span> <span data-ttu-id="597a7-124">Например, приложению может потребоваться добавить некоторые метаданные XMP.</span><span class="sxs-lookup"><span data-stu-id="597a7-124">For example, an application may want to add some XMP metadata.</span></span> <span data-ttu-id="597a7-125">Если существующего блока метаданных XMP нет, приложение должно создать экземпляр модуля записи метаданных XMP и использовать метод **аддвритер** , чтобы включить его в коллекцию модулей записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="597a7-125">If there is no existing XMP metadata block, the application must instantiate an XMP metadata writer and use the **AddWriter** method to include it in the collection of metadata writers.</span></span>

### <a name="setwriterbyindex"></a><span data-ttu-id="597a7-126">сетвритербиндекс</span><span class="sxs-lookup"><span data-stu-id="597a7-126">SetWriterByIndex</span></span>

<span data-ttu-id="597a7-127">[**Сетвритербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) используется для добавления модуля записи метаданных в указанный индекс в коллекции.</span><span class="sxs-lookup"><span data-stu-id="597a7-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) is used to add a metadata writer at a specific index in the collection.</span></span> <span data-ttu-id="597a7-128">Если в этом индексе уже существует модуль записи метаданных, новый элемент должен заменить его.</span><span class="sxs-lookup"><span data-stu-id="597a7-128">If a metadata writer is currently exists at that index, the new one should replace it.</span></span>

### <a name="removewriterbyindex"></a><span data-ttu-id="597a7-129">ремовевритербиндекс</span><span class="sxs-lookup"><span data-stu-id="597a7-129">RemoveWriterByIndex</span></span>

<span data-ttu-id="597a7-130">[**Ремовевритербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) используется для удаления модуля записи метаданных из коллекции.</span><span class="sxs-lookup"><span data-stu-id="597a7-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) is used to remove a metadata writer from the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="597a7-131">См. также</span><span class="sxs-lookup"><span data-stu-id="597a7-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="597a7-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="597a7-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="597a7-133">Реализация Ивикбитмапфраминкоде</span><span class="sxs-lookup"><span data-stu-id="597a7-133">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="597a7-134">Установка и регистрация КОДЕка</span><span class="sxs-lookup"><span data-stu-id="597a7-134">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="597a7-135">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="597a7-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="597a7-136">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="597a7-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



