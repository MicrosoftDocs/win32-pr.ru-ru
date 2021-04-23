---
title: Компоненты метаданных
description: Метаданные используются в файлах ASF для описания содержимого и свойств файла.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media Format SDK, функции метаданных
- Windows Media Format SDK, функции
- Расширенный системный формат (ASF), функции метаданных
- ASF (Расширенный системный формат), функции метаданных
- Расширенный формат систем (ASF), функции
- ASF (Расширенный системный формат), функции
- метаданные, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104412699"
---
# <a name="metadata-features"></a><span data-ttu-id="3e43d-110">Компоненты метаданных</span><span class="sxs-lookup"><span data-stu-id="3e43d-110">Metadata Features</span></span>

<span data-ttu-id="3e43d-111">Метаданные используются в файлах ASF для описания содержимого и свойств файла.</span><span class="sxs-lookup"><span data-stu-id="3e43d-111">Metadata is used in ASF files to describe file contents and properties.</span></span> <span data-ttu-id="3e43d-112">Все создаваемые файлы ASF должны содержать соответствующие метаданные.</span><span class="sxs-lookup"><span data-stu-id="3e43d-112">All ASF files you create should include appropriate metadata.</span></span> <span data-ttu-id="3e43d-113">(Общие сведения см. в разделе [метаданные](metadata.md).) Пакет SDK для формата Windows Media включает поддержку редактирования метаданных с помощью объекта Writer, объекта редактора метаданных, а также объектов чтения и синхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="3e43d-113">(For an overview, see [Metadata](metadata.md).) The Windows Media Format SDK includes support for metadata editing through the writer object, the metadata editor object, and both the reader and synchronous reader objects.</span></span> <span data-ttu-id="3e43d-114">Включена собственная поддержка для широкого спектра атрибутов метаданных.</span><span class="sxs-lookup"><span data-stu-id="3e43d-114">Native support for a wide variety of metadata attributes is included.</span></span> <span data-ttu-id="3e43d-115">Список предопределенных атрибутов см. в разделе [атрибуты](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="3e43d-115">See [Attributes](attributes.md) for a list of the predefined attributes.</span></span>

<span data-ttu-id="3e43d-116">Поддержка метаданных, обеспечиваемая различными объектами пакета SDK Windows Media Format, является гибкой и мощной.</span><span class="sxs-lookup"><span data-stu-id="3e43d-116">The metadata support provided by the various objects of the Windows Media Format SDK is flexible and powerful.</span></span> <span data-ttu-id="3e43d-117">Основные функции метаданных приведены в следующем списке:</span><span class="sxs-lookup"><span data-stu-id="3e43d-117">The main metadata features are summarized in the following list:</span></span>

-   <span data-ttu-id="3e43d-118">Гибкий размер атрибута.</span><span class="sxs-lookup"><span data-stu-id="3e43d-118">Flexible attribute size.</span></span> <span data-ttu-id="3e43d-119">Атрибуты метаданных имеют неограниченный размер.</span><span class="sxs-lookup"><span data-stu-id="3e43d-119">Metadata attributes are not limited in size.</span></span>
-   <span data-ttu-id="3e43d-120">Атрибуты уровня потока.</span><span class="sxs-lookup"><span data-stu-id="3e43d-120">Stream-level attributes.</span></span> <span data-ttu-id="3e43d-121">Метаданные в ASF-файлах могут быть назначены файлу целиком или определенному потоку.</span><span class="sxs-lookup"><span data-stu-id="3e43d-121">Metadata in ASF files can be assigned to the file as a whole, or to a particular stream.</span></span>
-   <span data-ttu-id="3e43d-122">Дублирующиеся атрибуты.</span><span class="sxs-lookup"><span data-stu-id="3e43d-122">Duplicated attributes.</span></span> <span data-ttu-id="3e43d-123">Именованный атрибут может использоваться несколько раз в одном файле.</span><span class="sxs-lookup"><span data-stu-id="3e43d-123">A named attribute can be used multiple times in the same file.</span></span> <span data-ttu-id="3e43d-124">Эта функция относится к конкретному использованию при назначении описательных атрибутов содержимого.</span><span class="sxs-lookup"><span data-stu-id="3e43d-124">This feature is of particular use when assigning content descriptive attributes.</span></span> <span data-ttu-id="3e43d-125">Например, песня может иметь несколько авторов, каждая из которых требует наличия отдельного атрибута **Author** в файле.</span><span class="sxs-lookup"><span data-stu-id="3e43d-125">For example, a song may have several authors, each requiring a separate **Author** attribute in the file.</span></span>
-   <span data-ttu-id="3e43d-126">Несколько языков.</span><span class="sxs-lookup"><span data-stu-id="3e43d-126">Multiple languages.</span></span> <span data-ttu-id="3e43d-127">С каждым атрибутом связан язык.</span><span class="sxs-lookup"><span data-stu-id="3e43d-127">Every attribute has a language associated with it.</span></span> <span data-ttu-id="3e43d-128">Можно задать поддерживаемые языки, а затем назначить их каждому создаваемому атрибуту.</span><span class="sxs-lookup"><span data-stu-id="3e43d-128">You can set the supported languages and then assign one to each attribute you write.</span></span> <span data-ttu-id="3e43d-129">Так как вы можете дублировать атрибуты, можно предоставить наиболее важные атрибуты на нескольких языках для достижения более крупной аудитории.</span><span class="sxs-lookup"><span data-stu-id="3e43d-129">Because you can duplicate attributes, you can provide the most important attributes in several languages to reach a larger audience.</span></span> <span data-ttu-id="3e43d-130">Если язык не указан, будет использоваться язык по умолчанию (полученный из операционной системы компьютера, на котором выполняется приложение).</span><span class="sxs-lookup"><span data-stu-id="3e43d-130">If you do not specify a language, the default language (obtained from the operating system of the computer running your application) will be used.</span></span>
-   <span data-ttu-id="3e43d-131">Сложные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="3e43d-131">Complex attributes.</span></span> <span data-ttu-id="3e43d-132">Некоторые предопределенные атрибуты поддерживают структурированные данные.</span><span class="sxs-lookup"><span data-stu-id="3e43d-132">Some of the predefined attributes support structured data.</span></span> <span data-ttu-id="3e43d-133">Для этих атрибутов тип данных является двоичным, но значением является структура, определенная в этом пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="3e43d-133">For these attributes, the data type is binary, but the value is a structure defined in this SDK.</span></span>

<span data-ttu-id="3e43d-134">В следующих разделах обсуждаются другие поддерживаемые функции метаданных.</span><span class="sxs-lookup"><span data-stu-id="3e43d-134">The following topics discuss the other supported metadata features.</span></span>



| <span data-ttu-id="3e43d-135">Раздел</span><span class="sxs-lookup"><span data-stu-id="3e43d-135">Topic</span></span>                                  | <span data-ttu-id="3e43d-136">Описание</span><span class="sxs-lookup"><span data-stu-id="3e43d-136">Description</span></span>                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e43d-137">Поддержка ID3</span><span class="sxs-lookup"><span data-stu-id="3e43d-137">ID3 Support</span></span>](id3.md)                 | <span data-ttu-id="3e43d-138">Обсуждается поддержка кадров ID3 с помощью объектов пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="3e43d-138">Discusses the support for ID3 frames using the objects of the Windows Media Format SDK.</span></span> |
| [<span data-ttu-id="3e43d-139">Пользовательские метаданные</span><span class="sxs-lookup"><span data-stu-id="3e43d-139">Custom Metadata</span></span>](custom-metadata.md) | <span data-ttu-id="3e43d-140">Обсуждаются последствия использования пользовательских метаданных.</span><span class="sxs-lookup"><span data-stu-id="3e43d-140">Discusses the implications of using custom metadata.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="3e43d-141">См. также</span><span class="sxs-lookup"><span data-stu-id="3e43d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e43d-142">**Компоненты**</span><span class="sxs-lookup"><span data-stu-id="3e43d-142">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="3e43d-143">**Интерфейс Ивмхеадеринфо**</span><span class="sxs-lookup"><span data-stu-id="3e43d-143">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="3e43d-144">**Интерфейс IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="3e43d-144">**IWMHeaderInfo2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[<span data-ttu-id="3e43d-145">**Интерфейс IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="3e43d-145">**IWMHeaderInfo3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[<span data-ttu-id="3e43d-146">**Метаданные**</span><span class="sxs-lookup"><span data-stu-id="3e43d-146">**Metadata**</span></span>](metadata.md)
</dt> </dl>

 

 




