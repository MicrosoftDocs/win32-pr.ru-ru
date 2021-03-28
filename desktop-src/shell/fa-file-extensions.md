---
description: Регистрация типа файла — это первый шаг в создании сопоставления файлов, что делает этот тип файлов &\# 0034; известный&\# 0034; в оболочке. Однако без обработчиков типов файлов оболочка не может предоставить пользователю сведения о файле и о нем.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Обработчики типов файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897134"
---
# <a name="file-type-handlers"></a><span data-ttu-id="3e45c-104">Обработчики типов файлов</span><span class="sxs-lookup"><span data-stu-id="3e45c-104">File Type Handlers</span></span>

<span data-ttu-id="3e45c-105">[Регистрация типа файла](fa-how-work.md) — это первый шаг в создании сопоставления файлов, что делает этот тип файлов "известным" оболочке.</span><span class="sxs-lookup"><span data-stu-id="3e45c-105">[Registering a file type](fa-how-work.md) is the first step in creating a file association, which makes that file type "known" to the Shell.</span></span> <span data-ttu-id="3e45c-106">Однако без обработчиков типов файлов оболочка не может предоставить пользователю сведения о файле и о нем.</span><span class="sxs-lookup"><span data-stu-id="3e45c-106">However, without file type handlers, the Shell is unable to expose information to the user from and about the file.</span></span>

<span data-ttu-id="3e45c-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3e45c-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="3e45c-108">Создание типа файла, известного оболочке</span><span class="sxs-lookup"><span data-stu-id="3e45c-108">Make a File Type Known to Shell</span></span>](#make-a-file-type-known-to-shell)
-   [<span data-ttu-id="3e45c-109">Описания обработчика типов файлов</span><span class="sxs-lookup"><span data-stu-id="3e45c-109">File Type Handler Descriptions</span></span>](#file-type-handler-descriptions)
-   [<span data-ttu-id="3e45c-110">См. также</span><span class="sxs-lookup"><span data-stu-id="3e45c-110">Related topics</span></span>](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a><span data-ttu-id="3e45c-111">Создание типа файла, известного оболочке</span><span class="sxs-lookup"><span data-stu-id="3e45c-111">Make a File Type Known to Shell</span></span>

<span data-ttu-id="3e45c-112">На следующем снимке экрана проводника Windows файл изображения выглядит так: в библиотеке **изображений** оболочки и связан только с приложением Paint.</span><span class="sxs-lookup"><span data-stu-id="3e45c-112">In the following screen shot of Windows Explorer, the image file Desert.known appears in the Shell **Pictures** library, and is associated only with the Paint application.</span></span>

![снимок экрана с браузером открытие изображения без типа файлов](images/file-assoc/fileassoc-filetypehandler.png)

<span data-ttu-id="3e45c-114">На предыдущем снимке экрана отсутствуют следующие функциональные возможности, включенные обработчиком типов файлов:</span><span class="sxs-lookup"><span data-stu-id="3e45c-114">The Desert.known file in the preceding screen shot lacks the following functionality that is enabled by a file type handler:</span></span>

-   <span data-ttu-id="3e45c-115">Эскиз или предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="3e45c-115">Thumbnail or preview</span></span>
-   <span data-ttu-id="3e45c-116">Команды, относящиеся к образу, в контекстном меню, например:</span><span class="sxs-lookup"><span data-stu-id="3e45c-116">Image-specific verbs in the shortcut menu, such as:</span></span>
    -   <span data-ttu-id="3e45c-117">Повернуть предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="3e45c-117">Rotate Preview</span></span>
    -   <span data-ttu-id="3e45c-118">Задать как фон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="3e45c-118">Set as Desktop Background</span></span>
    -   <span data-ttu-id="3e45c-119">Печать</span><span class="sxs-lookup"><span data-stu-id="3e45c-119">Print</span></span>
-   <span data-ttu-id="3e45c-120">Свойства, относящиеся к конкретному образу, в области **сведений** , например:</span><span class="sxs-lookup"><span data-stu-id="3e45c-120">Image-specific properties in the **Details** pane, such as:</span></span>
    -   <span data-ttu-id="3e45c-121">Дата съемки</span><span class="sxs-lookup"><span data-stu-id="3e45c-121">Date Taken</span></span>
    -   <span data-ttu-id="3e45c-122">Tags</span><span class="sxs-lookup"><span data-stu-id="3e45c-122">Tags</span></span>
    -   <span data-ttu-id="3e45c-123">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="3e45c-123">Rating</span></span>
-   <span data-ttu-id="3e45c-124">Индексирование текста файла</span><span class="sxs-lookup"><span data-stu-id="3e45c-124">Indexing of file text</span></span>

<span data-ttu-id="3e45c-125">На следующем снимке экрана один и тот же файл («во. известный») имеет расширение JPG, то есть зарегистрированный тип файла, который имеет связанные обработчики типов файлов, поэтому отображаются эскизы и другие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e45c-125">In the following screen shot, the same file (Desert.known) has the .jpg extension, which is a registered file type that has associated file type handlers, so a thumbnail image and more properties are shown.</span></span>

![изображение с зарегистрированным типом файла и обработчиком типов связанных файлов](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a><span data-ttu-id="3e45c-127">Описания обработчика типов файлов</span><span class="sxs-lookup"><span data-stu-id="3e45c-127">File Type Handler Descriptions</span></span>

<span data-ttu-id="3e45c-128">Функциональные возможности, предоставляемые каждым обработчиком типов файлов, перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3e45c-128">The functionality provided by each file type handler is listed in the following table:</span></span>



| <span data-ttu-id="3e45c-129">Обработчик</span><span class="sxs-lookup"><span data-stu-id="3e45c-129">Handler</span></span>                                                      | <span data-ttu-id="3e45c-130">Описание</span><span class="sxs-lookup"><span data-stu-id="3e45c-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e45c-131">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="3e45c-131">Shortcut menu</span></span>](context-menu-handlers.md)                   | <span data-ttu-id="3e45c-132">Обработчик контекстного меню, иногда называемый обработчиком контекстного меню, является обработчиком типа файлов, добавляющим команды в существующее контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="3e45c-132">A shortcut menu handler, sometimes referred to as a context menu handler, is a file type handler that adds commands to an existing context menu.</span></span> <span data-ttu-id="3e45c-133">Эти обработчики связаны с определенным типом файла и вызываются каждый раз, когда отображается контекстное меню для элемента типа файла.</span><span class="sxs-lookup"><span data-stu-id="3e45c-133">These handlers are associated with a particular file type and are called any time a context menu is displayed for a member of the file type.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="3e45c-134">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="3e45c-134">Thumbnail</span></span>](thumbnail-providers.md)                         | <span data-ttu-id="3e45c-135">Обработчик, предоставляющий изображение для представления элемента оболочки.</span><span class="sxs-lookup"><span data-stu-id="3e45c-135">A handler that provides an image to represent a Shell item.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="3e45c-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="3e45c-136">Property</span></span>](../properties/building-property-handlers-properties.md) | <span data-ttu-id="3e45c-137">Обработчик свойства, предоставляющий доступ к свойствам элемента для поиска Windows, проводнику Windows и другим приложениям, которым требуется доступ к свойствам.</span><span class="sxs-lookup"><span data-stu-id="3e45c-137">A property handler that provides access to item properties for Windows Search, the Windows Explorer and other applications that need to access properties.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="3e45c-138">Предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="3e45c-138">Preview</span></span>](preview-handlers.md)                              | <span data-ttu-id="3e45c-139">Обработчик, который быстро создает доступное только для чтения упрощенное представление элемента, отображаемого в панели предварительного просмотра проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="3e45c-139">A handler that quickly produces a read-only, simplified view of the item to be displayed in the Windows Explorer preview pane.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="3e45c-140">Фильтры</span><span class="sxs-lookup"><span data-stu-id="3e45c-140">Filters</span></span>](../search/-search-3x-wds-extidx-filters.md)              | <span data-ttu-id="3e45c-141">Фильтр, реализация интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , который сканирует документы для текста и свойств (также называемых атрибутами).</span><span class="sxs-lookup"><span data-stu-id="3e45c-141">A filter, an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface, that scans documents for text and properties (also called attributes).</span></span> <span data-ttu-id="3e45c-142">Он извлекает фрагменты текста из этих документов, отфильтровывая внедренное форматирование и сохраняет информацию о положении текста.</span><span class="sxs-lookup"><span data-stu-id="3e45c-142">It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text.</span></span> <span data-ttu-id="3e45c-143">Он также извлекает фрагменты значений, которые являются свойствами всего документа или строго определенных частей документа.</span><span class="sxs-lookup"><span data-stu-id="3e45c-143">It also extracts chunks of values, which are properties of an entire document or of well defined parts of a document.</span></span> <span data-ttu-id="3e45c-144">**IFilter** предоставляет основу для создания приложений более высокого уровня, таких как индексаторы документов и средства просмотра, независимые от приложений.</span><span class="sxs-lookup"><span data-stu-id="3e45c-144">**IFilter** provides the foundation for building higher-level applications such as document indexers and application-independent viewers.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3e45c-145">См. также</span><span class="sxs-lookup"><span data-stu-id="3e45c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e45c-146">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="3e45c-146">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="3e45c-147">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="3e45c-147">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="3e45c-148">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="3e45c-148">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="3e45c-149">Представление содержимого по типу или виду файла</span><span class="sxs-lookup"><span data-stu-id="3e45c-149">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="3e45c-150">Средство проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="3e45c-150">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="3e45c-151">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="3e45c-151">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="3e45c-152">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="3e45c-152">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="3e45c-153">Массивы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="3e45c-153">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
