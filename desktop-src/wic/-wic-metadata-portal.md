---
description: В этом разделе содержатся основные разделы, описывающие систему метаданных компонента Windows Imaging Component (WIC).
ms.assetid: 68f08f5a-eec6-4484-b901-dbe96c443a0d
title: Обработка метаданных изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475294acb6c5f6836409938fbaedf22306181f08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081148"
---
# <a name="processing-image-metadata"></a><span data-ttu-id="e599e-103">Обработка метаданных изображения</span><span class="sxs-lookup"><span data-stu-id="e599e-103">Processing Image Metadata</span></span>

<span data-ttu-id="e599e-104">В этом разделе содержатся основные разделы, описывающие систему метаданных компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="e599e-104">This section contains conceptual topics that describe the Windows Imaging Component (WIC) metadata system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e599e-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="e599e-105">In this section</span></span>



| <span data-ttu-id="e599e-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="e599e-106">Topic</span></span>                                                                                              | <span data-ttu-id="e599e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e599e-107">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e599e-108">Общие сведения о метаданных компонента WIC</span><span class="sxs-lookup"><span data-stu-id="e599e-108">WIC Metadata Overview</span></span>](-wic-about-metadata.md)<br/>                                        | <span data-ttu-id="e599e-109">В этом разделе представлены сведения о поддержке метаданных для создания образов, предоставляемых компонентом WIC.</span><span class="sxs-lookup"><span data-stu-id="e599e-109">This topic introduces the imaging metadata support provided by the WIC.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="e599e-110">Общие сведения о языке запросов метаданных</span><span class="sxs-lookup"><span data-stu-id="e599e-110">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)<br/>                | <span data-ttu-id="e599e-111">В этом разделе представлен язык запросов метаданных для WIC.</span><span class="sxs-lookup"><span data-stu-id="e599e-111">This topic introduces the metadata query language for WIC.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="e599e-112">Запросы метаданных встроенных форматов изображений</span><span class="sxs-lookup"><span data-stu-id="e599e-112">Native Image Format Metadata Queries</span></span>](-wic-native-image-format-metadata-queries.md)<br/>   | <span data-ttu-id="e599e-113">В этом разделе содержится обзор запросов на [языке запросов метаданных](-wic-codec-metadataquerylanguage.md) для чтения и записи метаданных, поддерживаемых изображениями в формате GIF, PNG, TIFF и JPEG.</span><span class="sxs-lookup"><span data-stu-id="e599e-113">This topic provides an overview of the [metadata query language](-wic-codec-metadataquerylanguage.md) queries for reading and writing metadata supported by GIF, PNG, TIFF and JPEG images.</span></span><br/>                                                                  |
| [<span data-ttu-id="e599e-114">Общие сведения о чтении и записи метаданных изображений</span><span class="sxs-lookup"><span data-stu-id="e599e-114">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)<br/> | <span data-ttu-id="e599e-115">В этом разделе приводятся общие сведения об использовании API-интерфейсов WIC для чтения и записи метаданных, внедренных в файлы изображений.</span><span class="sxs-lookup"><span data-stu-id="e599e-115">This topic provides an overview of how you can use the WIC APIs to read and write metadata that is embedded in image files.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="e599e-116">Общие сведения о расширяемости метаданных</span><span class="sxs-lookup"><span data-stu-id="e599e-116">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)<br/>                      | <span data-ttu-id="e599e-117">В этом разделе описываются требования к созданию пользовательских обработчиков метаданных для WIC, включая средства чтения и записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="e599e-117">This topic introduces the requirements for creating custom metadata handlers for the WIC, including both metadata readers and writers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="e599e-118">Общие сведения о разметке пользователей</span><span class="sxs-lookup"><span data-stu-id="e599e-118">People Tagging Overview</span></span>](-wic-people-tagging.md)<br/>                                      | <span data-ttu-id="e599e-119">В этом разделе рассказывается о новой схеме с расширенной платформой метаданных (XMP) и свойстве Photo [. photo. Пеопленамес](../properties/props-system-photo-peoplenames.md) Windows 7, которая позволяет размечать людей в цифровой фотографии.</span><span class="sxs-lookup"><span data-stu-id="e599e-119">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e599e-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="e599e-120">See Also</span></span>

[<span data-ttu-id="e599e-121">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="e599e-121">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="e599e-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="e599e-122">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="e599e-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="e599e-123">Samples</span></span>](-wic-samples.md)


 

 
