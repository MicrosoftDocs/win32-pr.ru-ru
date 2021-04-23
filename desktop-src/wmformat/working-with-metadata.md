---
title: Работа с метаданными
description: Работа с метаданными
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media Format SDK, общие сведения о метаданных
- Улучшенный системный формат (ASF), общие сведения о метаданных
- ASF (Расширенный системный формат), общие сведения о метаданных
- метаданные, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104412707"
---
# <a name="working-with-metadata"></a><span data-ttu-id="58d3d-107">Работа с метаданными</span><span class="sxs-lookup"><span data-stu-id="58d3d-107">Working with Metadata</span></span>

<span data-ttu-id="58d3d-108">Поддержка метаданных обеспечивается объектом модуля записи, объектами чтения и синхронным модулем чтения, а также объектом редактора метаданных.</span><span class="sxs-lookup"><span data-stu-id="58d3d-108">Metadata support is provided by the writer object, the reader and synchronous reader objects, and the metadata editor object.</span></span> <span data-ttu-id="58d3d-109">Общие сведения о метаданных см. в разделе [метаданные](metadata.md).</span><span class="sxs-lookup"><span data-stu-id="58d3d-109">For general information about metadata, see [Metadata](metadata.md).</span></span> <span data-ttu-id="58d3d-110">Сведения о функциях, поддерживающих метаданные в пакете SDK формата Windows Media, см. в разделе [функции метаданных](metadata-features.md).</span><span class="sxs-lookup"><span data-stu-id="58d3d-110">For information about the features supporting metadata in the Windows Media Format SDK, see [Metadata Features](metadata-features.md).</span></span>

<span data-ttu-id="58d3d-111">Интерфейс для редактирования метаданных — [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), который можно получить, вызвав метод **QueryInterface** любого интерфейса в одном из объектов, перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="58d3d-111">The interface for metadata editing is [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), which you can obtain by calling the **QueryInterface** method of any interface in one of the objects listed above.</span></span> <span data-ttu-id="58d3d-112">**IWMHeaderInfo3** наследует методы [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) и [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span><span class="sxs-lookup"><span data-stu-id="58d3d-112">**IWMHeaderInfo3** inherits the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span></span> <span data-ttu-id="58d3d-113">Методы **IWMHeaderInfo3** , имеющие дело с атрибутами метаданных, представляют разные подходы к доступу к метаданным, чем используются методами **ивмхеадеринфо**.</span><span class="sxs-lookup"><span data-stu-id="58d3d-113">The methods of **IWMHeaderInfo3** that deal with metadata attributes represent a different approach to accessing metadata than that used by the methods of **IWMHeaderInfo**.</span></span> <span data-ttu-id="58d3d-114">Следует всегда использовать новые методы.</span><span class="sxs-lookup"><span data-stu-id="58d3d-114">You should always use the newer methods.</span></span>

<span data-ttu-id="58d3d-115">Метаданные в ASF-файле идентифицируются по индексу и номеру потока.</span><span class="sxs-lookup"><span data-stu-id="58d3d-115">Metadata in an ASF file is identified by an index and a stream number.</span></span> <span data-ttu-id="58d3d-116">Атрибутам уровня файла присваивается номер потока 0.</span><span class="sxs-lookup"><span data-stu-id="58d3d-116">File-level attributes are assigned a stream number of 0.</span></span> <span data-ttu-id="58d3d-117">В предыдущих версиях пакета SDK для формата Windows Media атрибуты можно было идентифицировать по имени.</span><span class="sxs-lookup"><span data-stu-id="58d3d-117">In previous versions of the Windows Media Format SDK, attributes could be identified by name.</span></span> <span data-ttu-id="58d3d-118">Однако, поскольку теперь можно дублировать имена атрибутов в потоке, это становится невозможным.</span><span class="sxs-lookup"><span data-stu-id="58d3d-118">However, because you can now duplicate attribute names within a stream, this is no longer possible.</span></span> <span data-ttu-id="58d3d-119">Вместо этого можно получить все индексы, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="58d3d-119">Instead, you can retrieve all the indexes matching a name.</span></span> <span data-ttu-id="58d3d-120">Дополнительные сведения см. в разделе [Получение атрибутов метаданных](retrieving-metadata-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="58d3d-120">For more information, see [Retrieving Metadata Attributes](retrieving-metadata-attributes.md).</span></span>

<span data-ttu-id="58d3d-121">Чтобы быстро найти атрибуты, можно использовать специальный номер потока, 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="58d3d-121">To aid in finding attributes quickly, you can use a special stream number, 0xFFFF.</span></span> <span data-ttu-id="58d3d-122">Используйте этот номер потока, чтобы указать файл в целом, а не конкретный поток или атрибуты уровня файла.</span><span class="sxs-lookup"><span data-stu-id="58d3d-122">Use this stream number to identify the file as a whole, rather than a specific stream or the file-level attributes.</span></span> <span data-ttu-id="58d3d-123">Объекты пакета SDK Windows Media Format поддерживают отдельные индексы для каждого потока и для атрибутов уровня файла.</span><span class="sxs-lookup"><span data-stu-id="58d3d-123">The objects of the Windows Media Format SDK maintain separate indexes for each stream and for the file-level attributes.</span></span> <span data-ttu-id="58d3d-124">При использовании Stream 0xFFFF индексы отличаются от используемых при указании конкретного потока.</span><span class="sxs-lookup"><span data-stu-id="58d3d-124">When using stream 0xFFFF, the indexes are different from those you use when specifying a specific stream.</span></span> <span data-ttu-id="58d3d-125">Например, атрибут с индексом 0 для потока 0 не будет совпадать с атрибутом, который является индексом 0 для Stream 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="58d3d-125">For example, the attribute that is index 0 for stream 0 will not be the same as the attribute that is index 0 for stream 0xFFFF.</span></span>

<span data-ttu-id="58d3d-126">В следующих разделах более подробно описывается использование метаданных.</span><span class="sxs-lookup"><span data-stu-id="58d3d-126">The following sections describe the use of metadata in greater detail.</span></span>



| <span data-ttu-id="58d3d-127">Section</span><span class="sxs-lookup"><span data-stu-id="58d3d-127">Section</span></span>                                                                    | <span data-ttu-id="58d3d-128">Описание</span><span class="sxs-lookup"><span data-stu-id="58d3d-128">Description</span></span>                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="58d3d-129">Получение атрибутов метаданных</span><span class="sxs-lookup"><span data-stu-id="58d3d-129">Retrieving Metadata Attributes</span></span>](retrieving-metadata-attributes.md)       | <span data-ttu-id="58d3d-130">Описывает, как считывать атрибуты метаданных из заголовка файла.</span><span class="sxs-lookup"><span data-stu-id="58d3d-130">Describes how to read metadata attributes from a file header.</span></span>                     |
| [<span data-ttu-id="58d3d-131">Задание атрибутов метаданных</span><span class="sxs-lookup"><span data-stu-id="58d3d-131">Setting Metadata Attributes</span></span>](setting-metadata-attributes.md)             | <span data-ttu-id="58d3d-132">Описывает, как добавлять новые атрибуты метаданных в заголовок файла.</span><span class="sxs-lookup"><span data-stu-id="58d3d-132">Describes how to add new metadata attributes to a file header.</span></span>                    |
| [<span data-ttu-id="58d3d-133">Изменение атрибутов метаданных</span><span class="sxs-lookup"><span data-stu-id="58d3d-133">Editing Metadata Attributes</span></span>](editing-metadata-attributes.md)             | <span data-ttu-id="58d3d-134">Описывает, как изменить существующие атрибуты метаданных.</span><span class="sxs-lookup"><span data-stu-id="58d3d-134">Describes how to edit existing metadata attributes.</span></span>                               |
| [<span data-ttu-id="58d3d-135">Удаление атрибутов метаданных</span><span class="sxs-lookup"><span data-stu-id="58d3d-135">Removing Metadata Attributes</span></span>](removing-metadata-attributes.md)           | <span data-ttu-id="58d3d-136">Описывает, как удалить существующие атрибуты метаданных.</span><span class="sxs-lookup"><span data-stu-id="58d3d-136">Describes how to remove existing metadata attributes.</span></span>                             |
| [<span data-ttu-id="58d3d-137">Использование сложных атрибутов метаданных</span><span class="sxs-lookup"><span data-stu-id="58d3d-137">Using Complex Metadata Attributes</span></span>](using-complex-metadata-attributes.md) | <span data-ttu-id="58d3d-138">Описывает работу с атрибутами, значения которых представлены структурами.</span><span class="sxs-lookup"><span data-stu-id="58d3d-138">Describes how to work with attributes whose values are represented by structures.</span></span> |



 

<span data-ttu-id="58d3d-139">В некоторых примерах приложений показано, как извлекать и изменять метаданные.</span><span class="sxs-lookup"><span data-stu-id="58d3d-139">Several of the sample applications show how to retrieve and edit metadata.</span></span> <span data-ttu-id="58d3d-140">В частности, см. пример Метадатаедит, который входит в версии C++ и C#.</span><span class="sxs-lookup"><span data-stu-id="58d3d-140">In particular, see the MetadataEdit sample, which comes in both C++ and C# versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58d3d-141">См. также</span><span class="sxs-lookup"><span data-stu-id="58d3d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58d3d-142">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="58d3d-142">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="58d3d-143">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="58d3d-143">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="58d3d-144">**Примеры приложений**</span><span class="sxs-lookup"><span data-stu-id="58d3d-144">**Sample Applications**</span></span>](sample-applications.md)
</dt> </dl>

 

 




