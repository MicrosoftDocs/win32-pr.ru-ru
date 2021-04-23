---
description: Несколько форматов файлов изображений позволяют хранить метаданные вместе с изображением.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Константы тега свойства Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985204"
---
# <a name="image-property-tag-constants"></a><span data-ttu-id="438e1-103">Константы тега свойства Image</span><span class="sxs-lookup"><span data-stu-id="438e1-103">Image Property Tag Constants</span></span>

<span data-ttu-id="438e1-104">Несколько форматов файлов изображений позволяют хранить метаданные вместе с изображением.</span><span class="sxs-lookup"><span data-stu-id="438e1-104">Several image file formats enable you to store metadata along with an image.</span></span> <span data-ttu-id="438e1-105">Метаданные — это сведения о изображении, например заголовок, ширина, модель камеры и исполнитель.</span><span class="sxs-lookup"><span data-stu-id="438e1-105">Metadata is information about an image, for example, title, width, camera model, and artist.</span></span> <span data-ttu-id="438e1-106">Windows GDI+ обеспечивает единообразный способ хранения и извлечения метаданных из файлов изображений в формате TIFF, JPEG, PNG и файлов обмена изображениями (EXIF).</span><span class="sxs-lookup"><span data-stu-id="438e1-106">Windows GDI+ provides a uniform way of storing and retrieving metadata from image files in the Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG), and Exchangeable Image File (EXIF) formats.</span></span>

<span data-ttu-id="438e1-107">В GDI+ фрагмент метаданных называется *элементом свойства*, а отдельный элемент свойства идентифицируется с помощью числовой константы, называемой *тегом свойства*.</span><span class="sxs-lookup"><span data-stu-id="438e1-107">In GDI+, a piece of metadata is called a *property item*, and an individual property item is identified by a numerical constant called a *property tag*.</span></span> <span data-ttu-id="438e1-108">Метаданные можно хранить и извлекать путем вызова методов [**Image:: сетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) и [**Image:: жетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , и вам не нужно беспокоиться о том, как конкретный формат файлов сохраняет эти метаданные.</span><span class="sxs-lookup"><span data-stu-id="438e1-108">You can store and retrieve metadata by calling the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) and [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned with the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="438e1-109">В следующих разделах перечислены и описаны элементы свойств, поддерживаемые GDI+.</span><span class="sxs-lookup"><span data-stu-id="438e1-109">The following topics list and describe the property items supported by GDI+.</span></span> <span data-ttu-id="438e1-110">Описания являются краткими и общими, поэтому они применяются к различным форматам файлов.</span><span class="sxs-lookup"><span data-stu-id="438e1-110">The descriptions are brief and general so that they apply to a variety of file formats.</span></span> <span data-ttu-id="438e1-111">Подробное описание использования элемента свойства в определенном формате файла см. в спецификации для этого формата файла.</span><span class="sxs-lookup"><span data-stu-id="438e1-111">For a detailed description of how a property item is used in a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="438e1-112">Ссылки на несколько спецификаций формата файла см. в разделе [спецификации формата файла изображения](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="438e1-112">For links to several file format specifications, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span> <span data-ttu-id="438e1-113">Дополнительные сведения о метаданных см. в разделе [чтение и запись метаданных](-gdiplus-reading-and-writing-metadata-use.md) и [**констант типа тега свойства Image**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="438e1-113">For more information about metadata, see [Reading and Writing Metadata](-gdiplus-reading-and-writing-metadata-use.md) and [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span>

-   [<span data-ttu-id="438e1-114">Теги свойств в числовом порядке</span><span class="sxs-lookup"><span data-stu-id="438e1-114">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [<span data-ttu-id="438e1-115">Теги свойств в алфавитном порядке</span><span class="sxs-lookup"><span data-stu-id="438e1-115">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [<span data-ttu-id="438e1-116">Описания элементов свойств</span><span class="sxs-lookup"><span data-stu-id="438e1-116">Property Item Descriptions</span></span>](-gdiplus-constant-property-item-descriptions.md)

 

 



