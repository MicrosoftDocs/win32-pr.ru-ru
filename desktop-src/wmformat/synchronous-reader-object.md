---
title: Объект модуля синхронного чтения
description: Объект модуля синхронного чтения
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Пакет SDK для формата Windows Media, синхронные объекты чтения
- Расширенный формат систем (ASF), синхронные объекты чтения
- ASF (Расширенный системный формат), синхронные объекты чтения
- объекты, синхронные объекты чтения
- синхронные читатели, объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105700824"
---
# <a name="synchronous-reader-object"></a><span data-ttu-id="5cf51-108">Объект модуля синхронного чтения</span><span class="sxs-lookup"><span data-stu-id="5cf51-108">Synchronous Reader Object</span></span>

<span data-ttu-id="5cf51-109">Синхронный объект Reader используется для чтения цифровых файлов мультимедиа с помощью синхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="5cf51-109">The synchronous reader object is used to read digital media files by using synchronous calls.</span></span>

<span data-ttu-id="5cf51-110">Синхронный объект Reader создается функцией [**вмкреатесинкреадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), которая устанавливает указатель на интерфейс **ивмсинкреадер** .</span><span class="sxs-lookup"><span data-stu-id="5cf51-110">The synchronous reader object is created by the function [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), which sets a pointer to an **IWMSyncReader** interface.</span></span> <span data-ttu-id="5cf51-111">Другие интерфейсы, поддерживаемые синхронным интерфейсом чтения, можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="5cf51-111">The other interfaces supported by the synchronous reader interface can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="5cf51-112">Объект синхронного модуля чтения поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="5cf51-112">The following interfaces are supported by the synchronous reader object.</span></span>



| <span data-ttu-id="5cf51-113">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="5cf51-113">Interface</span></span>                                | <span data-ttu-id="5cf51-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5cf51-114">Description</span></span>                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cf51-115">**ивмхеадеринфо**</span><span class="sxs-lookup"><span data-stu-id="5cf51-115">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | <span data-ttu-id="5cf51-116">Задает и получает сведения о заголовке, такие как метаданные, [*маркеры*](wmformat-glossary.md)и т. д.</span><span class="sxs-lookup"><span data-stu-id="5cf51-116">Sets and retrieves header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                            |
| [<span data-ttu-id="5cf51-117">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="5cf51-117">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | <span data-ttu-id="5cf51-118">Перечисляет сведения о доступных кодеках.</span><span class="sxs-lookup"><span data-stu-id="5cf51-118">Enumerates the available codec information.</span></span> <span data-ttu-id="5cf51-119">Наследует все методы **ивмхеадеринфо**.</span><span class="sxs-lookup"><span data-stu-id="5cf51-119">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                      |
| [<span data-ttu-id="5cf51-120">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="5cf51-120">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | <span data-ttu-id="5cf51-121">Поддерживает крупные размеры атрибутов, дублирующиеся имена атрибутов и поддержку нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="5cf51-121">Supports large attribute sizes, duplicate attribute names, and multiple language support.</span></span> <span data-ttu-id="5cf51-122">Наследует все методы **ивмхеадеринфо** и **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="5cf51-122">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span> |
| [<span data-ttu-id="5cf51-123">**ивмпрофиле**</span><span class="sxs-lookup"><span data-stu-id="5cf51-123">**IWMProfile**</span></span>](iwmprofile.md)         | <span data-ttu-id="5cf51-124">Предоставляет доступ к сведениям о профиле файла Windows Media, загруженного в средство чтения.</span><span class="sxs-lookup"><span data-stu-id="5cf51-124">Provides access to the profile information of the Windows Media file loaded into the reader.</span></span>                                                                       |
| [<span data-ttu-id="5cf51-125">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="5cf51-125">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | <span data-ttu-id="5cf51-126">Возвращает глобальный уникальный идентификатор (GUID), если таковой имеется, связанный с профилем.</span><span class="sxs-lookup"><span data-stu-id="5cf51-126">Retrieves the globally unique identifier (GUID), if any, associated with the profile.</span></span> <span data-ttu-id="5cf51-127">Наследует все методы **ивмпрофиле**.</span><span class="sxs-lookup"><span data-stu-id="5cf51-127">Inherits all of the methods of **IWMProfile**.</span></span>                               |
| [<span data-ttu-id="5cf51-128">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="5cf51-128">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | <span data-ttu-id="5cf51-129">Поддерживает совместное использование пропускной способности и сведения о приоритизации потоков в профиле.</span><span class="sxs-lookup"><span data-stu-id="5cf51-129">Supports bandwidth sharing and stream prioritization information in the profile.</span></span> <span data-ttu-id="5cf51-130">Наследует все методы **ивмпрофиле** и **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="5cf51-130">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span>                |
| [<span data-ttu-id="5cf51-131">**ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="5cf51-131">**IWMSyncReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | <span data-ttu-id="5cf51-132">Предоставляет возможности синхронного чтения для цифровых файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5cf51-132">Provides synchronous reading capabilities for digital media files.</span></span>                                                                                                 |
| [<span data-ttu-id="5cf51-133">**IWMSyncReader2**</span><span class="sxs-lookup"><span data-stu-id="5cf51-133">**IWMSyncReader2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | <span data-ttu-id="5cf51-134">Обеспечивает поддержку поиска для SMPTE кодов времени и для выделения образцов вручную.</span><span class="sxs-lookup"><span data-stu-id="5cf51-134">Provides support for seeking to SMPTE time codes and for allocating samples manually.</span></span> <span data-ttu-id="5cf51-135">Наследует все методы **ивмсинкреадер**.</span><span class="sxs-lookup"><span data-stu-id="5cf51-135">Inherits all of the methods of **IWMSyncReader**.</span></span>                            |



 

## <a name="related-topics"></a><span data-ttu-id="5cf51-136">См. также</span><span class="sxs-lookup"><span data-stu-id="5cf51-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cf51-137">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="5cf51-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="5cf51-138">**Объект модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="5cf51-138">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="5cf51-139">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="5cf51-139">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




