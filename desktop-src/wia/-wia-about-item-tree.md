---
description: В Windows Vista существенно изменилось дерево элементов для загрузки изображений (WIA).
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Сведения о дереве элементов IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909875"
---
# <a name="about-the-iwiaitem2-item-tree"></a><span data-ttu-id="9db96-103">Сведения о дереве элементов IWiaItem2</span><span class="sxs-lookup"><span data-stu-id="9db96-103">About the IWiaItem2 Item Tree</span></span>

<span data-ttu-id="9db96-104">В Windows Vista существенно изменилось дерево элементов для загрузки изображений (WIA).</span><span class="sxs-lookup"><span data-stu-id="9db96-104">With Windows Vista, the Windows Image Acquisition (WIA) item tree has changed significantly.</span></span> <span data-ttu-id="9db96-105">Элементы [**IWiaItem2**](-wia-iwiaitem2.md) используются для представления атрибутов устройства и данных устройства.</span><span class="sxs-lookup"><span data-stu-id="9db96-105">[**IWiaItem2**](-wia-iwiaitem2.md) items are used to represent device attributes and device data.</span></span> <span data-ttu-id="9db96-106">Приложения для работы с образами видят устройство для получения изображений (WIA) 2,0 в виде иерархического дерева элементов с корневым элементом, представляющим само устройство, и дочерними элементами, представляющими такие элементы, как программируемые источники данных, изображения или папки, содержащие изображения.</span><span class="sxs-lookup"><span data-stu-id="9db96-106">Imaging applications see a Windows Image Acquisition (WIA) 2.0 device as a hierarchical tree of items, with the root item representing the device itself and the child items representing things like programmable data sources, images, or folders that contain images.</span></span>

-   [<span data-ttu-id="9db96-107">Элементы приложения</span><span class="sxs-lookup"><span data-stu-id="9db96-107">Application Items</span></span>](#application-items)
-   [<span data-ttu-id="9db96-108">Флаги элементов</span><span class="sxs-lookup"><span data-stu-id="9db96-108">Item Flags</span></span>](#item-flags)
-   [<span data-ttu-id="9db96-109">Категории элементов</span><span class="sxs-lookup"><span data-stu-id="9db96-109">Item Categories</span></span>](#item-categories)
-   [<span data-ttu-id="9db96-110">Корневой элемент</span><span class="sxs-lookup"><span data-stu-id="9db96-110">Root Item</span></span>](#root-item)
-   [<span data-ttu-id="9db96-111">Элемент данных</span><span class="sxs-lookup"><span data-stu-id="9db96-111">Data Item</span></span>](#data-item)
-   [<span data-ttu-id="9db96-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9db96-112">Related topics</span></span>](#related-topics)

## <a name="application-items"></a><span data-ttu-id="9db96-113">Элементы приложения</span><span class="sxs-lookup"><span data-stu-id="9db96-113">Application Items</span></span>

<span data-ttu-id="9db96-114">Дерево элементов WIA 2,0, которое может видеть приложение, отличается от дерева, созданного и обслуживаемого WIA 2,0 минидривер.</span><span class="sxs-lookup"><span data-stu-id="9db96-114">The WIA 2.0 item tree that an application can see is separate from the tree created and maintained by a WIA 2.0 minidriver.</span></span> <span data-ttu-id="9db96-115">Когда минидривер создает дерево, служба WIA 2,0 использует это дерево элементов WIA 2,0 в качестве инструкции по созданию копии дерева, которую можно просматривать с помощью приложений для работы с образами.</span><span class="sxs-lookup"><span data-stu-id="9db96-115">When a minidriver creates a tree, the WIA 2.0 service uses this WIA 2.0 item tree as a guide to create a copy of the tree that can be viewed by imaging applications.</span></span> <span data-ttu-id="9db96-116">Элементы в скопированном дереве называются элементами *приложения* .</span><span class="sxs-lookup"><span data-stu-id="9db96-116">Items in the copied tree are called *application* items.</span></span> <span data-ttu-id="9db96-117">Элементы в дереве, созданном минидривер, называются элементами *драйвера* .</span><span class="sxs-lookup"><span data-stu-id="9db96-117">Items in the tree created by a minidriver are called *driver* items.</span></span>

<span data-ttu-id="9db96-118">Элемент WIA может представлять программируемый источник данных для устройства подачи документов сканера или данные, хранящиеся на этом устройстве.</span><span class="sxs-lookup"><span data-stu-id="9db96-118">A WIA item can represent a programmable data source for a scanner's document feeder or the data stored on that device.</span></span> <span data-ttu-id="9db96-119">Устройство WIA должно быть разделено на отдельные элементы, описывающие различные данные, создаваемые этим устройством.</span><span class="sxs-lookup"><span data-stu-id="9db96-119">A WIA device should be divided into individual items that describe different data produced by that device.</span></span>

<span data-ttu-id="9db96-120">Например, сканер WIA, поддерживающий сканирование для планшетов и сканирования веб-каналов документов, может быть разделен на два дочерних элемента.</span><span class="sxs-lookup"><span data-stu-id="9db96-120">For example, a WIA scanner that supports both flatbed scanning and document feeder scanning might be divided into two child items.</span></span> <span data-ttu-id="9db96-121">Один представляет функцию сканирования на планшете, а другая — функцию сканирования устройства подачи документов.</span><span class="sxs-lookup"><span data-stu-id="9db96-121">One represents the flatbed scanning functionality and the other represents the document feeder scanning functionality.</span></span>

<span data-ttu-id="9db96-122">Несколько образов, представленных на сканере для планшетов и сканированных одновременно, можно поместить в одну папку.</span><span class="sxs-lookup"><span data-stu-id="9db96-122">Multiple images laid out on a flatbed scanner and scanned at the same time can be placed in one folder.</span></span> <span data-ttu-id="9db96-123">С помощью фильтра сегментации ([**ивиасегментатионфилтер**](-wia-iwiasegmentationfilter.md)) каждое изображение или подобласть можно создать как дочерний элемент папки.</span><span class="sxs-lookup"><span data-stu-id="9db96-123">Using the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), each image or subregion can then be created as a child item of the folder.</span></span>

<span data-ttu-id="9db96-124">Дерево WIA для устройства камеры, в котором хранятся фотографии («пленка»), можно разделить на элементы, представляющие папки, вложенные папки и фотографии.</span><span class="sxs-lookup"><span data-stu-id="9db96-124">The WIA tree for a camera device that stores photos ("Film") can be divided into items that represent folders, subfolders, and photos.</span></span>

## <a name="item-flags"></a><span data-ttu-id="9db96-125">Флаги элементов</span><span class="sxs-lookup"><span data-stu-id="9db96-125">Item Flags</span></span>

<span data-ttu-id="9db96-126">Флаги элементов WIA помогают классифицировать содержимое или поддерживаемое поведение конкретного элемента WIA.</span><span class="sxs-lookup"><span data-stu-id="9db96-126">WIA item flags help classify the content or supported behavior of a particular WIA item.</span></span> <span data-ttu-id="9db96-127">Флаги элементов WIA делятся на две группы.</span><span class="sxs-lookup"><span data-stu-id="9db96-127">WIA item flags fall into two groups.</span></span>

1.  <span data-ttu-id="9db96-128">Флаги состояния элемента сообщают о текущем состоянии элемента WIA, например [**виаитемтипедисконнектед**](-wia-wia-item-type-flags.md), **виаитемтипеделетед** и т. д.</span><span class="sxs-lookup"><span data-stu-id="9db96-128">Item status flags report the current state of the WIA item, for example, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, and so forth.</span></span>
2.  <span data-ttu-id="9db96-129">Флаги представления и использования данных элемента сообщают о данных, которые элемент WIA представляет или может создать при передаче.</span><span class="sxs-lookup"><span data-stu-id="9db96-129">Item data representation/usage flags report the data that the WIA item represents or can produce if transferred.</span></span> <span data-ttu-id="9db96-130">Например, [**виаитемтипеимаже**](-wia-wia-item-type-flags.md) является флагом представления данных, сообщающим приложению, что данные, связанные с текущим элементом WIA, являются данными изображения и должны иметь свойства данных изображения.</span><span class="sxs-lookup"><span data-stu-id="9db96-130">For example, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) is a data representation flag that tells the application the data associated with the current WIA item is image data and should have image data properties.</span></span> <span data-ttu-id="9db96-131">**WIA \_ \_ \_ Флаги элементов IPA** — это флаг использования элемента, который сообщает приложению, что элемент WIA является настраиваемым и соответствует набору предварительно определенных правил конфигурации на [**основе \_ \_ \_ категории элемента WIA IPA**](-wia-wiaitempropcommonitem.md) и что конфигурация может изменить результат для каждой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="9db96-131">**WIA\_IPA\_ITEM\_FLAGS** is an item usage flag that tells the application that the WIA item is configurable and follows a set of predefined configuration rules based on the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) and that the configuration can possibly change the result for each data transfer.</span></span> <span data-ttu-id="9db96-132">(Дополнительные сведения об определениях категорий см. в разделе категории элементов [категорий](#item-categories) товаров.)</span><span class="sxs-lookup"><span data-stu-id="9db96-132">(For more information about category definitions, see [Item Categories](#item-categories) item categories.)</span></span>

<span data-ttu-id="9db96-133">На следующем рисунке показан пример дерева элементов WIA и различные флаги, которые могут быть связаны с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="9db96-133">The following graphic shows an example of a WIA item tree and the various flags that might be associated with each item.</span></span>

![Примеры флагов элементов для элементов в дереве](images/scannertree1.jpg)

## <a name="item-categories"></a><span data-ttu-id="9db96-135">Категории элементов</span><span class="sxs-lookup"><span data-stu-id="9db96-135">Item Categories</span></span>

<span data-ttu-id="9db96-136">Элементы WIA группируются в категории с помощью значений [**свойств \_ \_ \_ категории элемента WIA IPA**](-wia-wiaitempropcommonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="9db96-136">WIA items are grouped into categories using the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) property values.</span></span> <span data-ttu-id="9db96-137">Эти категории определяют способ обработки или использования элемента WIA.</span><span class="sxs-lookup"><span data-stu-id="9db96-137">These categories define how a WIA item is to be treated or used.</span></span> <span data-ttu-id="9db96-138">Например, если элемент представляет готовый файл ( \_ Файл «Категория WIA \_ завершена» \_ ), приложение WIA должно предположить, что данные статичны и расположены на устройстве.</span><span class="sxs-lookup"><span data-stu-id="9db96-138">For example, if the item represents a finished file (WIA\_CATEGORY\_FINISHED\_FILE), a WIA application should assume that the data is static and located on the device.</span></span> <span data-ttu-id="9db96-139">Если элемент представляет поток- \_ \_ контейнер (податчик категории WIA), приложение должно содержать необходимые свойства устройства подачи документов и действовать как устройство подачи документов.</span><span class="sxs-lookup"><span data-stu-id="9db96-139">If the item represents a feeder (WIA\_CATEGORY\_FEEDER), the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span>

<span data-ttu-id="9db96-140">Ниже перечислены категории, определяемые WIA.</span><span class="sxs-lookup"><span data-stu-id="9db96-140">The categories defined by WIA are:</span></span>

-   <span data-ttu-id="9db96-141">\_Автоматическая категория \_ WIA</span><span class="sxs-lookup"><span data-stu-id="9db96-141">WIA\_CATEGORY\_AUTO</span></span>
-   <span data-ttu-id="9db96-142">\_податчик категории WIA \_</span><span class="sxs-lookup"><span data-stu-id="9db96-142">WIA\_CATEGORY\_FEEDER</span></span>
-   <span data-ttu-id="9db96-143">\_пленка для категории WIA \_</span><span class="sxs-lookup"><span data-stu-id="9db96-143">WIA\_CATEGORY\_FILM</span></span>
-   <span data-ttu-id="9db96-144">файл, в котором \_ Категория WIA \_ завершена \_</span><span class="sxs-lookup"><span data-stu-id="9db96-144">WIA\_CATEGORY\_FINISHED\_FILE</span></span>
-   <span data-ttu-id="9db96-145">\_стекло категории \_ WIA</span><span class="sxs-lookup"><span data-stu-id="9db96-145">WIA\_CATEGORY\_FLATBED</span></span>

<span data-ttu-id="9db96-146">Например, для элемента сканера WIA могут быть заданы [**\_ \_ \_ Флаги IPA элементов**](-wia-wiaitempropcommonitem.md) для [**виаитемтипеимаже**](-wia-wia-item-type-flags.md), **виаитемтипетрансфер** и **виаитемтипепрограммабледатасаурце**, а для свойства **WIA \_ IPA \_ элемента \_ Category** задано значение WIA категории "планшетный" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9db96-146">For example, a scanner's flatbed item may have the [**WIA\_IPA\_ITEM\_FLAGS**](-wia-wiaitempropcommonitem.md) set to [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer**, and **WiaItemTypeProgrammableDataSource**, and the **WIA\_IPA\_ITEM\_CATEGORY** property set to WIA\_CATEGORY\_FLATBED.</span></span>

<span data-ttu-id="9db96-147">В следующей таблице показано группирование категорий WIA с помощью флагов элементов и элементов WIA.</span><span class="sxs-lookup"><span data-stu-id="9db96-147">The following table shows WIA category grouping with item flags and WIA items.</span></span> <span data-ttu-id="9db96-148">Эта таблица не включает полный список флагов элементов WIA, определенных WIA.</span><span class="sxs-lookup"><span data-stu-id="9db96-148">This table does not include a full list of the WIA item flags defined by WIA.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9db96-149">Категория WIA</span><span class="sxs-lookup"><span data-stu-id="9db96-149">WIA Category</span></span></th>
<th><span data-ttu-id="9db96-150">Допустимые флаги элемента WIA</span><span class="sxs-lookup"><span data-stu-id="9db96-150">Valid WIA Item Flags</span></span></th>
<th><span data-ttu-id="9db96-151">Набор свойств WIA</span><span class="sxs-lookup"><span data-stu-id="9db96-151">WIA Property Set</span></span></th>
<th><span data-ttu-id="9db96-152">Элементы WIA</span><span class="sxs-lookup"><span data-stu-id="9db96-152">WIA Items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9db96-153">WIA_CATEGORY_AUTO</span><span class="sxs-lookup"><span data-stu-id="9db96-153">WIA_CATEGORY_AUTO</span></span></td>
<td><ul>
<li><span data-ttu-id="9db96-154"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипепрограммабледатасаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="9db96-155"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипеимаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9db96-156"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипетрансфер</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="9db96-157"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипефиле</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="9db96-158">Набор свойств включает автоматические настроенные свойства сканера.</span><span class="sxs-lookup"><span data-stu-id="9db96-158">Property set includes auto-configured scanner properties.</span></span></td>
<td><span data-ttu-id="9db96-159">Автоэлемент WIA, представляющий автоматическую настройку параметров сканирования сканера.</span><span class="sxs-lookup"><span data-stu-id="9db96-159">WIA auto item that represents the scanner's auto-configured scanning settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9db96-160">WIA_CATEGORY_FEEDER</span><span class="sxs-lookup"><span data-stu-id="9db96-160">WIA_CATEGORY_FEEDER</span></span></td>
<td><ul>
<li><span data-ttu-id="9db96-161"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипепрограммабледатасаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="9db96-162"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипеимаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9db96-163"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипедокумент</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="9db96-164"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипетрансфер</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="9db96-165"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипефолдер</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="9db96-166">Набор свойств включает свойства элемента управления сканера веб-канала (обычно это набор свойств, связанных с изображениями и документами).</span><span class="sxs-lookup"><span data-stu-id="9db96-166">Property set includes feeder scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="9db96-167">Элементы податчика WIA, включая дочерние элементы, представляющие переднюю и заднюю страницы документа.</span><span class="sxs-lookup"><span data-stu-id="9db96-167">WIA Feeder items, including child items that represent the front and back pages of a document.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9db96-168">WIA_CATEGORY_FILM</span><span class="sxs-lookup"><span data-stu-id="9db96-168">WIA_CATEGORY_FILM</span></span></td>
<td><ul>
<li><span data-ttu-id="9db96-169"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипепрограммабледатасаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="9db96-170"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипеимаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9db96-171"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипетрансфер</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="9db96-172"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипефолдер</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="9db96-173">Набор свойств включает свойства элемента управления "сканер пленки" (обычно это набор свойств Image и Document).</span><span class="sxs-lookup"><span data-stu-id="9db96-173">Property set includes film scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="9db96-174">Элементы пленки WIA, включая дочерние элементы, представляющие отдельные кадры сканирования.</span><span class="sxs-lookup"><span data-stu-id="9db96-174">WIA Film items, including child items that represent the individual scanning frames.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9db96-175">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="9db96-175">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><ul>
<li><span data-ttu-id="9db96-176"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипефолдер</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
<li><span data-ttu-id="9db96-177"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипеимаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9db96-178"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипеаудио</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span></span></li>
<li><span data-ttu-id="9db96-179"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипевидео</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span></span></li>
<li><span data-ttu-id="9db96-180"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипедокумент</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="9db96-181"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипетрансфер</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="9db96-182">Свойство, заданное для этого элемента, зависит от сообщаемого типа элемента.</span><span class="sxs-lookup"><span data-stu-id="9db96-182">The property set on this item depends on the item type reported.</span></span> <span data-ttu-id="9db96-183">Например, <a href="-wia-wia-item-type-flags.md"><strong>виаитемтипеимаже</strong></a> должен включать некоторые свойства элементов изображения, например бит на пиксель и т. д.</span><span class="sxs-lookup"><span data-stu-id="9db96-183">For example, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> should include some image item properties, like bits per pixel and so forth.</span></span></td>
<td><span data-ttu-id="9db96-184">Элементы хранения WIA, включая дочерние элементы, представляющие завершенное содержимое файла (файлы данных, такие как JPEG, HTML, TXT и т. д.).</span><span class="sxs-lookup"><span data-stu-id="9db96-184">WIA storage items, including child items that represent finished file content (data files like JPEG, HTML, TXT, and so forth).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9db96-185">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="9db96-185">WIA_CATEGORY_FLATBED</span></span></td>
<td><ul>
<li><span data-ttu-id="9db96-186"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипепрограммабледатасаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="9db96-187"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипеимаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="9db96-188"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипедокумент</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="9db96-189"><a href="-wia-wia-item-type-flags.md"><strong>виаитемтипетрансфер</strong></a></span><span class="sxs-lookup"><span data-stu-id="9db96-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="9db96-190"><a href="-wia-wia-item-type-flags.md"><strong>Виаитемтипефолдер</strong></a>— может присутствовать, если сканер поддерживает сканирование нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="9db96-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>—may be present if the scanner supports multi-item scanning.</span></span></li>
<li><span data-ttu-id="9db96-191"><a href="-wia-wia-item-type-flags.md"><strong>Виаитемтипеженератед</strong></a>— может присутствовать, если приложение создает элемент WIA во время сеанса сканирования нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="9db96-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>—may be present if the application generates a WIA item during a multi-item scanning session.</span></span></li>
</ul></td>
<td><span data-ttu-id="9db96-192">Набор свойств включает свойства элемента управления "планшетный сканер" (обычно это набор свойств, связанных с изображениями и документами).</span><span class="sxs-lookup"><span data-stu-id="9db96-192">The property set includes flatbed scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="9db96-193">Планшетные элементы WIA, включая дочерние элементы, которые представляют регионы, сканируемые на планшете сканера Платен.</span><span class="sxs-lookup"><span data-stu-id="9db96-193">WIA flatbed items, including child items that represent regions being scanned on the scanner's flatbed platen.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9db96-194">На следующем рисунке показан пример дерева элементов WIA и различных категорий, которые могут быть связаны с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="9db96-194">The following graphic shows an example of a WIA item tree and the various categories that might be associated with each item.</span></span>

![Примеры категорий элементов для элементов в дереве](images/scannertree2.jpg)

## <a name="root-item"></a><span data-ttu-id="9db96-196">Корневой элемент</span><span class="sxs-lookup"><span data-stu-id="9db96-196">Root Item</span></span>

<span data-ttu-id="9db96-197">Корневой элемент WIA — это элемент папки, помеченный флагами [**виаитемтиперут**](-wia-wia-item-type-flags.md) и **виаитемтипедевице** , который представляет само устройство.</span><span class="sxs-lookup"><span data-stu-id="9db96-197">A WIA root item is a folder item marked with [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) and **WiaItemTypeDevice** flags that represents the device itself.</span></span> <span data-ttu-id="9db96-198">Он содержит такие атрибуты устройства, как изготовитель, имя устройства и атрибуты драйвера, такие как версия драйвера и идентификатор класса пользовательского интерфейса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="9db96-198">It contains device attributes like manufacturer, device name, and driver attributes like driver version and user interface class identifier (CLSID).</span></span> <span data-ttu-id="9db96-199">Приложения для работы с образами получают корневой элемент дерева элементов WIA путем вызова метода [**IWiaDevMgr2:: креатедевице**](-wia-iwiadevmgr2-createdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="9db96-199">Imaging applications get the root to the WIA item tree by calling [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) method.</span></span> <span data-ttu-id="9db96-200">Приложение использует корневой элемент для получения доступа к отдельным дочерним элементам WIA путем перечисления дерева (см. [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span><span class="sxs-lookup"><span data-stu-id="9db96-200">The application uses the root item to gain access to the individual child WIA items by enumerating the tree (see [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span></span>

## <a name="data-item"></a><span data-ttu-id="9db96-201">Data Item</span><span class="sxs-lookup"><span data-stu-id="9db96-201">Data Item</span></span>

<span data-ttu-id="9db96-202">Любой элемент, который можно использовать для перемещения данных, считается элементом данных.</span><span class="sxs-lookup"><span data-stu-id="9db96-202">Any item that can be use to transfer data is considered a data item.</span></span> <span data-ttu-id="9db96-203">Сюда входят элементы, помеченные флагом [**виаитемтипепрограммабледатасаурце**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="9db96-203">This includes items marked with the [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) flag.</span></span>

<span data-ttu-id="9db96-204">Элементы папок и элементы, не являющиеся элементами папки, могут предоставлять возможность передачи данных с помощью флага [**виаитемтипетрансфер**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="9db96-204">Folder items and nonfolder items can expose the ability to transfer data by being marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag.</span></span> <span data-ttu-id="9db96-205">Любой элемент с установленным флагом должен предоставлять следующие свойства элемента WIA:</span><span class="sxs-lookup"><span data-stu-id="9db96-205">Any item with this flag set has to provide the following WIA item properties:</span></span>

-   [<span data-ttu-id="9db96-206">**\_ \_ права доступа WIA \_ IPA**</span><span class="sxs-lookup"><span data-stu-id="9db96-206">**WIA\_IPA\_ACCESS\_RIGHTS**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9db96-207">**\_ \_ размер элемента IPA \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="9db96-207">**WIA\_IPA\_ITEM\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9db96-208">**\_ \_ Размер буфера IPA \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="9db96-208">**WIA\_IPA\_BUFFER\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9db96-209">**\_формат IPA \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="9db96-209">**WIA\_IPA\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9db96-210">**\_ \_ предпочтительный формат IPA WIA \_**</span><span class="sxs-lookup"><span data-stu-id="9db96-210">**WIA\_IPA\_PREFERRED\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9db96-211">**WIA \_ IPA \_ тимед**</span><span class="sxs-lookup"><span data-stu-id="9db96-211">**WIA\_IPA\_TYMED**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="9db96-212">**\_ \_ расширение файла WIA \_ IPA**</span><span class="sxs-lookup"><span data-stu-id="9db96-212">**WIA\_IPA\_FILENAME\_EXTENSION**</span></span>](-wia-wiaitempropcommonitem.md)

<span data-ttu-id="9db96-213">Программируемые элементы источника данных, помеченные флагом [**виаитемтипетрансфер**](-wia-wia-item-type-flags.md) , также должны указывать набор свойств, требуемых для элемента данных.</span><span class="sxs-lookup"><span data-stu-id="9db96-213">Programmable data source items marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag must also supply the data item required property set.</span></span>

<span data-ttu-id="9db96-214">Элементы данных WIA могут иметь дополнительные свойства в зависимости от настроек флага элемента.</span><span class="sxs-lookup"><span data-stu-id="9db96-214">WIA data items may have additional properties depending on the item's flag settings.</span></span> <span data-ttu-id="9db96-215">Например, элементы WIA, помеченные флагом [**виаитемтипеимаже**](-wia-wia-item-type-flags.md) , должны иметь свойства сведений, специфичные для изображения, такие как [**WIA \_ IPA \_ Depth**](-wia-wiaitempropcommonitem.md) и **WIA \_ IPA \_ число \_ \_ строк**.</span><span class="sxs-lookup"><span data-stu-id="9db96-215">For example, WIA items marked with the [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) flag should have image specific information properties, like [**WIA\_IPA\_DEPTH**](-wia-wiaitempropcommonitem.md) and **WIA\_IPA\_NUMBER\_OF\_LINES**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9db96-216">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9db96-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9db96-217">**Reference**</span><span class="sxs-lookup"><span data-stu-id="9db96-217">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9db96-218">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="9db96-218">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="9db96-219">**IEnumWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="9db96-219">**IEnumWiaItem2**</span></span>](-wia-ienumwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="9db96-220">**IWiaDevMgr2**</span><span class="sxs-lookup"><span data-stu-id="9db96-220">**IWiaDevMgr2**</span></span>](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



