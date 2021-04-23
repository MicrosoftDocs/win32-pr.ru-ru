---
description: В этом разделе описывается использование интерфейсов уровня страницы, обеспечивающих доступ к содержимому страницы в OM-модели XPS.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Работа с интерфейсами страниц OM в XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693236"
---
# <a name="working-with-xps-om-page-interfaces"></a><span data-ttu-id="111c9-103">Работа с интерфейсами страниц OM в XPS</span><span class="sxs-lookup"><span data-stu-id="111c9-103">Working with XPS OM Page Interfaces</span></span>

<span data-ttu-id="111c9-104">В этом разделе описывается использование интерфейсов уровня страницы, обеспечивающих доступ к содержимому страницы в OM-модели XPS.</span><span class="sxs-lookup"><span data-stu-id="111c9-104">This topic describes how to use the page-level interfaces that provide access to the contents of a page in an XPS OM.</span></span>



| <span data-ttu-id="111c9-105">Имя интерфейса</span><span class="sxs-lookup"><span data-stu-id="111c9-105">Interface name</span></span>                                                                                                                                                                              | <span data-ttu-id="111c9-106">Логические дочерние интерфейсы</span><span class="sxs-lookup"><span data-stu-id="111c9-106">Logical child interfaces</span></span>                                                                                                                                                                                            | <span data-ttu-id="111c9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="111c9-107">Description</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="111c9-108">**икспсомпаже**</span><span class="sxs-lookup"><span data-stu-id="111c9-108">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [<span data-ttu-id="111c9-109">**икспсомканвас**</span><span class="sxs-lookup"><span data-stu-id="111c9-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="111c9-110">**икспсомглифс**</span><span class="sxs-lookup"><span data-stu-id="111c9-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="111c9-111">**икспсомпас**</span><span class="sxs-lookup"><span data-stu-id="111c9-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | <span data-ttu-id="111c9-112">Корневой объект содержимого страницы.</span><span class="sxs-lookup"><span data-stu-id="111c9-112">The root object of the page contents.</span></span><br/> <span data-ttu-id="111c9-113">Этот объект представляет часть документа.</span><span class="sxs-lookup"><span data-stu-id="111c9-113">This object represents a document part.</span></span><br/>                                                |
| [<span data-ttu-id="111c9-114">**икспсомшареабле**</span><span class="sxs-lookup"><span data-stu-id="111c9-114">**IXpsOMShareable**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [<span data-ttu-id="111c9-115">**икспсомвисуал**</span><span class="sxs-lookup"><span data-stu-id="111c9-115">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [<span data-ttu-id="111c9-116">**икспсомматрикстрансформ**</span><span class="sxs-lookup"><span data-stu-id="111c9-116">**IXpsOMMatrixTransform**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [<span data-ttu-id="111c9-117">**икспсомжеометри**</span><span class="sxs-lookup"><span data-stu-id="111c9-117">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [<span data-ttu-id="111c9-118">**икспсомбруш**</span><span class="sxs-lookup"><span data-stu-id="111c9-118">**IXpsOMBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | <span data-ttu-id="111c9-119">Интерфейсы, производные от интерфейса [**икспсомшареабле**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) , могут храниться в словаре ресурсов и использоваться совместно.</span><span class="sxs-lookup"><span data-stu-id="111c9-119">Interfaces that derive from the [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) interface can be stored in a resource dictionary and shared.</span></span><br/> |
| [<span data-ttu-id="111c9-120">**икспсомремотедиктионариресаурце**</span><span class="sxs-lookup"><span data-stu-id="111c9-120">**IXpsOMRemoteDictionaryResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [<span data-ttu-id="111c9-121">**икспсомремотедиктионариресаурцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="111c9-121">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [<span data-ttu-id="111c9-122">**икспсомдиктионари**</span><span class="sxs-lookup"><span data-stu-id="111c9-122">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | <span data-ttu-id="111c9-123">Содержит словарь ресурсов.</span><span class="sxs-lookup"><span data-stu-id="111c9-123">Contains a resource dictionary.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="111c9-124">**икспсомдиктионари**</span><span class="sxs-lookup"><span data-stu-id="111c9-124">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | <span data-ttu-id="111c9-125">Нет</span><span class="sxs-lookup"><span data-stu-id="111c9-125">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="111c9-126">Ссылается на ресурсы, совместно используемые другими объектами.</span><span class="sxs-lookup"><span data-stu-id="111c9-126">References the resources that are shared by other objects.</span></span><br/>                                                                              |
| [<span data-ttu-id="111c9-127">**икспсомсторифрагментсресаурце**</span><span class="sxs-lookup"><span data-stu-id="111c9-127">**IXpsOMStoryFragmentsResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | <span data-ttu-id="111c9-128">Нет</span><span class="sxs-lookup"><span data-stu-id="111c9-128">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="111c9-129">Предоставляет доступ к содержимому потока ресурсов Сторифрагментс части документа.</span><span class="sxs-lookup"><span data-stu-id="111c9-129">Provides access to the content of the resource stream of the StoryFragments part of the document.</span></span><br/>                                       |



 

## <a name="related-topics"></a><span data-ttu-id="111c9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="111c9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="111c9-131">**Интерфейс Икспсомдиктионари**</span><span class="sxs-lookup"><span data-stu-id="111c9-131">**IXpsOMDictionary Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[<span data-ttu-id="111c9-132">**икспсомдокументструктурересаурце**</span><span class="sxs-lookup"><span data-stu-id="111c9-132">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[<span data-ttu-id="111c9-133">**Интерфейс Икспсомпаже**</span><span class="sxs-lookup"><span data-stu-id="111c9-133">**IXpsOMPage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="111c9-134">**Интерфейс Икспсомремотедиктионариресаурце**</span><span class="sxs-lookup"><span data-stu-id="111c9-134">**IXpsOMRemoteDictionaryResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[<span data-ttu-id="111c9-135">**Интерфейс Икспсомремотедиктионариресаурцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="111c9-135">**IXpsOMRemoteDictionaryResourceCollection Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[<span data-ttu-id="111c9-136">**Интерфейс Икспсомсторифрагментсресаурце**</span><span class="sxs-lookup"><span data-stu-id="111c9-136">**IXpsOMStoryFragmentsResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




