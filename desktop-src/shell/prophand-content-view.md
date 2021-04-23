---
description: В этом разделе описывается новое представление в проводнике Windows, называемое представлением содержимого, которое отображает наиболее релевантное содержимое для каждого элемента.
title: Представление содержимого по типу или виду файла
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814840"
---
# <a name="content-view-by-file-type-or-kind"></a><span data-ttu-id="00305-103">Представление содержимого по типу или виду файла</span><span class="sxs-lookup"><span data-stu-id="00305-103">Content View By File Type or Kind</span></span>

<span data-ttu-id="00305-104">В этом разделе описывается новое представление в проводнике Windows, называемое представлением содержимого, которое отображает наиболее релевантное содержимое для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="00305-104">This topic describes a new view in Windows Explorer, called the Content view, that displays the most relevant content for each item.</span></span> <span data-ttu-id="00305-105">С помощью набора разделов реестра элементы могут определять список свойств и макет, используемый оболочкой для представления содержимого.</span><span class="sxs-lookup"><span data-stu-id="00305-105">Using a set of registry keys, items can define a property list and a layout that the Shell uses for Content view.</span></span> <span data-ttu-id="00305-106">Оболочка извлекает разделы реестра с помощью [массива ассоциаций](fa-perceivedtypes.md)элемента.</span><span class="sxs-lookup"><span data-stu-id="00305-106">The Shell retrieves the registry keys by using the item's [association array](fa-perceivedtypes.md).</span></span>

## <a name="how-does-the-content-view-work"></a><span data-ttu-id="00305-107">Как работает представление содержимого?</span><span class="sxs-lookup"><span data-stu-id="00305-107">How Does the Content View Work?</span></span>

<span data-ttu-id="00305-108">В Windows 7 и более поздних версиях в представлении содержимого используется логика изменения размера, при которой удаляются свойства при уменьшении размера окна, чтобы гарантировать, что наиболее важные свойства остаются видимыми для чтения.</span><span class="sxs-lookup"><span data-stu-id="00305-108">In Windows 7 and later, the Content view uses a resizing logic that drops properties when the window size decreases, to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="00305-109">На следующем снимке экрана показано представление содержимого результатов поиска, содержащих музыку, рисунки и документы.</span><span class="sxs-lookup"><span data-stu-id="00305-109">The following screen shot illustrates the Content view of search results containing music, pictures, and documents.</span></span>

![представление содержимого результатов поиска, содержащих музыку, изображения и документы](images/content-view/contentviewsearchresults.png)

<span data-ttu-id="00305-111">Некоторые источники данных оболочки используют представление содержимого по умолчанию, но пользователи могут выбрать представление содержимого, нажав кнопку **View Control (Просмотр элемента управления** ) в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="00305-111">Some Shell data sources use Content view by default, but users can select the Content view by clicking the **View Control** button in Windows Explorer.</span></span> <span data-ttu-id="00305-112">Источник данных оболочки расширяет пространство имен оболочки и предоставляет элементы в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="00305-112">A Shell data source extends the Shell namespace and exposes items in a data store.</span></span> <span data-ttu-id="00305-113">Элементы в хранилище данных могут индексироваться системой поиска Windows с помощью обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="00305-113">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

## <a name="how-to-implement-the-content-view"></a><span data-ttu-id="00305-114">Реализация представления содержимого</span><span class="sxs-lookup"><span data-stu-id="00305-114">How to Implement the Content View</span></span>

<span data-ttu-id="00305-115">При регистрации нового [типа файла](fa-file-types.md) или [обработчика протокола](../search/-search-3x-wds-extidx-prot-implementing.md)можно воспользоваться представлением содержимого, используя один из двух различных подходов.</span><span class="sxs-lookup"><span data-stu-id="00305-115">When registering a new [file type](fa-file-types.md) or [protocol handler](../search/-search-3x-wds-extidx-prot-implementing.md), you can take advantage of the Content view by using either of two different approaches.</span></span> <span data-ttu-id="00305-116">Вы можете использовать существующий набор свойств и шаблон макета или создать собственное сочетание.</span><span class="sxs-lookup"><span data-stu-id="00305-116">You can use an existing set of properties and layout pattern, or you can create your own combination.</span></span>

<span data-ttu-id="00305-117">С помощью записи реестра можно связать тип файла или элемент с предопределенным [видом](../properties/building-property-handlers-user-friendly-kind-names.md), который представляет собой свойство, которое можно представить как категорию содержимого.</span><span class="sxs-lookup"><span data-stu-id="00305-117">You can use a registry entry to associate your file type or item with a predefined [Kind](../properties/building-property-handlers-user-friendly-kind-names.md), which is a property that you can think of as a content category.</span></span> <span data-ttu-id="00305-118">Связав тип файла или элемент с определенными типами, вы автоматически наследуете шаблоны макета представления содержимого этого вида и списки свойств.</span><span class="sxs-lookup"><span data-stu-id="00305-118">By associating your file type or item with certain of these Kinds, you automatically inherit that Kind's Content view layout patterns and property lists.</span></span> <span data-ttu-id="00305-119">Windows определяет шаблоны макета представления содержимого и списки свойств для следующих типов: документы, электронная почта, папка, музыка, рисунки и универсальные.</span><span class="sxs-lookup"><span data-stu-id="00305-119">Windows defines Content view layout patterns and property lists for the following Kinds: documents, email, folder, music, picture, and generic.</span></span> <span data-ttu-id="00305-120">Этот тип ассоциации рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="00305-120">This type of association is encouraged.</span></span> <span data-ttu-id="00305-121">Она позволяет обеспечить единообразный процесс, который пользователь ожидает для похожих элементов.</span><span class="sxs-lookup"><span data-stu-id="00305-121">It lets you provide the consistent experience that a user expects for similar items.</span></span>

<span data-ttu-id="00305-122">Дополнительные сведения см. в статьях [типы файлов](fa-file-types.md) и [имена](../properties/building-property-handlers-user-friendly-kind-names.md) типов и [Регистрация уникального набора свойств представления содержимого и шаблона макета для типа файла или элемента](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span><span class="sxs-lookup"><span data-stu-id="00305-122">For more information, see [File Types](fa-file-types.md) and [Kind Names](../properties/building-property-handlers-user-friendly-kind-names.md) and [How To Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00305-123">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="00305-123">Additional Resources</span></span>

-   <span data-ttu-id="00305-124">Справочную документацию по свойствам см. в разделе [System. Kind](../properties/props-system-kind.md)и [System. киндтекст](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="00305-124">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>
-   <span data-ttu-id="00305-125">Справочную документацию по Проплист см. в разделе [System. проплист. контентвиевмодефорбровсе](../properties/props-system-proplist-contentviewmodeforbrowse.md)и [System. проплист. контентвиевмодефорсеарч](../properties/props-system-proplist-contentviewmodeforsearch.md).</span><span class="sxs-lookup"><span data-stu-id="00305-125">For PropList reference documentation, see [System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md), and [System.PropList.ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00305-126">См. также</span><span class="sxs-lookup"><span data-stu-id="00305-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00305-127">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="00305-127">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="00305-128">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="00305-128">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="00305-129">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="00305-129">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="00305-130">Средство проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="00305-130">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="00305-131">Обработчики типов файлов</span><span class="sxs-lookup"><span data-stu-id="00305-131">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="00305-132">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="00305-132">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="00305-133">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="00305-133">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="00305-134">Массивы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="00305-134">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
