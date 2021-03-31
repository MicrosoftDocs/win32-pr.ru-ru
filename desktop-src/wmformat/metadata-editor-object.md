---
title: Объект редактора метаданных
description: Объект редактора метаданных
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Пакет SDK для формата Windows Media, объекты редактора метаданных
- Расширенный системный формат (ASF), объекты редактора метаданных
- ASF (Расширенный системный формат), объекты редактора метаданных
- объекты, объекты редактора метаданных
- объекты редактора метаданных, сведения
- метаданные, объекты редактора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789222"
---
# <a name="metadata-editor-object"></a><span data-ttu-id="8e571-109">Объект редактора метаданных</span><span class="sxs-lookup"><span data-stu-id="8e571-109">Metadata Editor Object</span></span>

<span data-ttu-id="8e571-110">Объект редактора метаданных используется для изменения сведений, хранящихся в разделе заголовка ASF-файлов.</span><span class="sxs-lookup"><span data-stu-id="8e571-110">The metadata editor object is used to edit information stored in the header section of ASF files.</span></span> <span data-ttu-id="8e571-111">Наиболее распространенными объектами, которыми управляет этот объект, являются атрибуты метаданных.</span><span class="sxs-lookup"><span data-stu-id="8e571-111">The most common things manipulated by this object are metadata attributes.</span></span> <span data-ttu-id="8e571-112">Кроме того, редактор метаданных работает с [*маркерами*](wmformat-glossary.md) и командами сценариев.</span><span class="sxs-lookup"><span data-stu-id="8e571-112">Additionally, the metadata editor deals with [*markers*](wmformat-glossary.md) and script commands.</span></span> <span data-ttu-id="8e571-113">Единственный раз, когда нужно использовать редактор метаданных, является необходимость изменения заголовка существующего файла без его воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8e571-113">The only time you need to use the metadata editor is when you want to edit the header of an existing file without playing it.</span></span>

<span data-ttu-id="8e571-114">Объект редактора метаданных создается функцией [**вмкреатидитор**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), которая устанавливает указатель на интерфейс **ивмметадатаедитор** .</span><span class="sxs-lookup"><span data-stu-id="8e571-114">The metadata editor object is created by the function [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), which sets a pointer to an **IWMMetadataEditor** interface.</span></span> <span data-ttu-id="8e571-115">Другие интерфейсы объекта редактора метаданных можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="8e571-115">The other interfaces of the metadata editor object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="8e571-116">Объект редактора метаданных поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8e571-116">The following interfaces are supported by the metadata editor object.</span></span>



| <span data-ttu-id="8e571-117">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="8e571-117">Interface</span></span>                                        | <span data-ttu-id="8e571-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8e571-118">Description</span></span>                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e571-119">**ивмдрмедитор**</span><span class="sxs-lookup"><span data-stu-id="8e571-119">**IWMDRMEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | <span data-ttu-id="8e571-120">Позволяет изменять приложения для проверки свойств [*DRM*](wmformat-glossary.md) файла ASF без каких бы то ни было прав на воспроизведение защищенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="8e571-120">Enables editing applications to examine the [*DRM*](wmformat-glossary.md) properties of an ASF file without having any rights to play the protected content.</span></span> |
| [<span data-ttu-id="8e571-121">**ивмхеадеринфо**</span><span class="sxs-lookup"><span data-stu-id="8e571-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="8e571-122">Управляет атрибутами, маркерами и командами скриптов в заголовке.</span><span class="sxs-lookup"><span data-stu-id="8e571-122">Manipulates attributes, markers, and script commands in the header.</span></span>                                                                                                                                    |
| [<span data-ttu-id="8e571-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="8e571-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | <span data-ttu-id="8e571-124">Извлекает сведения о кодека.</span><span class="sxs-lookup"><span data-stu-id="8e571-124">Retrieves codec information.</span></span> <span data-ttu-id="8e571-125">Наследует все методы **ивмхеадеринфо**.</span><span class="sxs-lookup"><span data-stu-id="8e571-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                                                         |
| [<span data-ttu-id="8e571-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="8e571-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | <span data-ttu-id="8e571-127">Обеспечивает расширенную поддержку атрибутов, включая крупные атрибуты, несколько языков и дублирующиеся имена атрибутов.</span><span class="sxs-lookup"><span data-stu-id="8e571-127">Provides advanced support for attributes, including large attributes, multiple languages, and duplicate attribute names.</span></span> <span data-ttu-id="8e571-128">Наследует все методы **ивмхеадеринфо** и **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="8e571-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>      |
| [<span data-ttu-id="8e571-129">**ивмметадатаедитор**</span><span class="sxs-lookup"><span data-stu-id="8e571-129">**IWMMetadataEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | <span data-ttu-id="8e571-130">Открывает, закрывает и сохраняет изменения в заголовке файла ASF.</span><span class="sxs-lookup"><span data-stu-id="8e571-130">Opens, closes, and saves changes to the header of an ASF file.</span></span>                                                                                                                                         |
| [<span data-ttu-id="8e571-131">**IWMMetadataEditor2**</span><span class="sxs-lookup"><span data-stu-id="8e571-131">**IWMMetadataEditor2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | <span data-ttu-id="8e571-132">Открытие файла ASF для редактирования заголовков с использованием нескольких параметров доступа к файлам и общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8e571-132">Opens an ASF file for header editing with multiple file access and sharing options.</span></span> <span data-ttu-id="8e571-133">Наследует все методы **ивмметадатаедитор**.</span><span class="sxs-lookup"><span data-stu-id="8e571-133">Inherits all of the methods of **IWMMetadataEditor**.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="8e571-134">См. также</span><span class="sxs-lookup"><span data-stu-id="8e571-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e571-135">**Метки**</span><span class="sxs-lookup"><span data-stu-id="8e571-135">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="8e571-136">**Метаданные**</span><span class="sxs-lookup"><span data-stu-id="8e571-136">**Metadata**</span></span>](metadata.md)
</dt> <dt>

[<span data-ttu-id="8e571-137">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="8e571-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="8e571-138">**Команды скриптов**</span><span class="sxs-lookup"><span data-stu-id="8e571-138">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="8e571-139">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="8e571-139">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




