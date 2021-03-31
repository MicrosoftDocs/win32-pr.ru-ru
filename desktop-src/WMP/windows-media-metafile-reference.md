---
title: Справочник по метафайлу Windows Media
description: Справочник по метафайлу Windows Media
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Метафайлы Windows Media, Справочник
- Метафайлы, справочные материалы
- Справочник по метафайлам Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067938"
---
# <a name="windows-media-metafile-reference"></a><span data-ttu-id="ca8eb-106">Справочник по метафайлу Windows Media</span><span class="sxs-lookup"><span data-stu-id="ca8eb-106">Windows Media Metafile Reference</span></span>

<span data-ttu-id="ca8eb-107">Этот справочник документирует элементы и расширения имен файлов для метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-107">This reference documents elements and file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="ca8eb-108">Ссылка делится на следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-108">The reference is divided into the following sections.</span></span>



| <span data-ttu-id="ca8eb-109">Section</span><span class="sxs-lookup"><span data-stu-id="ca8eb-109">Section</span></span>                                                                                    | <span data-ttu-id="ca8eb-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ca8eb-110">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca8eb-111">Справочник по элементам метафайлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="ca8eb-111">Windows Media Metafile Elements Reference</span></span>](windows-media-metafile-elements-reference.md) | <span data-ttu-id="ca8eb-112">Документирует элементы метафайла, включая определения, атрибуты и их значения, а также особые условия, связанные с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-112">Documents metafile elements, including definitions, attributes and their values, and special conditions related to each element.</span></span> |
| [<span data-ttu-id="ca8eb-113">Расширения файлов</span><span class="sxs-lookup"><span data-stu-id="ca8eb-113">File Name Extensions</span></span>](file-name-extensions.md)                                           | <span data-ttu-id="ca8eb-114">Документирует расширения метафайлов имен файлов с правилами и рекомендациями по их использованию.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-114">Documents metafile file name extensions with rules and guidelines on their use.</span></span>                                                  |



 

<span data-ttu-id="ca8eb-115">Метафайлы Windows Media — это текстовые файлы, содержащие сведения о файловом потоке и его представлении.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-115">Windows Media metafiles are text files that provide information about a file stream and its presentation.</span></span> <span data-ttu-id="ca8eb-116">Метафайлы основаны на синтаксисе язык XML (XML) и состоят из различных элементов, похожих на XML, с их тегами и атрибутами.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-116">The metafiles are based on the Extensible Markup Language (XML) syntax, and are made up of various XML-like elements with their tags and attributes.</span></span> <span data-ttu-id="ca8eb-117">Каждый элемент определяет параметр или действие для потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-117">Each element defines a setting or action for streaming media.</span></span>

<span data-ttu-id="ca8eb-118">Для метафайлов доступно два набора тегов элементов.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-118">There are two sets of element tags available for metafiles.</span></span> <span data-ttu-id="ca8eb-119">В метафайлах на стороне клиента имеется один набор элементов, а для метафайлов на стороне сервера — другой набор элементов.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-119">Client-side metafiles have one set of elements, and server-side metafiles have another set of elements.</span></span>

<span data-ttu-id="ca8eb-120">Если тег элемента не содержит дочерних элементов (тех, которые изменяют или содержатся в другом элементе), то в конце открывающего тега вместо закрывающего тега можно использовать только один символ косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="ca8eb-120">If an element tag does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag in place of a closing tag.</span></span> <span data-ttu-id="ca8eb-121">Если дочерние элементы не отображаются между открывающим и закрывающим тегом элемента, они не являются дочерними элементами для этого элемента и не учитываются или вызывают ошибку в синтаксисе метафайла.</span><span class="sxs-lookup"><span data-stu-id="ca8eb-121">If child elements do not appear between the opening and closing tag for an element, they are not child elements for that element, and are ignored or cause an error in the syntax of the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca8eb-122">См. также</span><span class="sxs-lookup"><span data-stu-id="ca8eb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca8eb-123">**О метафайлах Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ca8eb-123">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> <dt>

[<span data-ttu-id="ca8eb-124">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ca8eb-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="ca8eb-125">**Метафайлы Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ca8eb-125">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




