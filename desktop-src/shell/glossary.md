---
description: Страница глоссария
ROBOTS: NOINDEX, NOFOLLOW
title: Глоссарий оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345395"
---
# <a name="shell-glossary"></a><span data-ttu-id="893bb-103">Глоссарий оболочки</span><span class="sxs-lookup"><span data-stu-id="893bb-103">Shell Glossary</span></span>

## <a name="a"></a><span data-ttu-id="893bb-104">Объект</span><span class="sxs-lookup"><span data-stu-id="893bb-104">A</span></span>

<dl> <dt>

<span data-ttu-id="893bb-105">**связке**</span><span class="sxs-lookup"><span data-stu-id="893bb-105">**association**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-106">Сопоставление расширения имени файла (например,. mp3) или протокола (например, HTTP) с программным идентификатором (ProgID).</span><span class="sxs-lookup"><span data-stu-id="893bb-106">A mapping of a file name extension (for example, .mp3) or protocol (for example, http) to a programmatic identifier (ProgID).</span></span> <span data-ttu-id="893bb-107">Это сопоставление хранится в реестре в качестве параметра для отдельного пользователя с резервом на компьютере.</span><span class="sxs-lookup"><span data-stu-id="893bb-107">This mapping is stored in the registry as a per-user setting with a per-computer fallback.</span></span> <span data-ttu-id="893bb-108">Приложения, участвующие в системе по умолчанию, устанавливают сопоставление сопоставления для расширения имени файла или протокола, чтобы указывать на ключи ProgID, которыми они владеют.</span><span class="sxs-lookup"><span data-stu-id="893bb-108">Applications that participate in the Default Programs system set the association mapping for the file name extension or protocol to point to the ProgID keys that they own.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-109">**массив ассоциаций**</span><span class="sxs-lookup"><span data-stu-id="893bb-109">**association array**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-110">Упорядоченный список расположений реестра, используемых для хранения сведений о типе элемента, включая обработчики, глаголы и другие атрибуты, такие как значок и отображаемое имя типа.</span><span class="sxs-lookup"><span data-stu-id="893bb-110">An ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="893bb-111">Например, файл. jpg имеет следующий массив ассоциаций в системе Windows по умолчанию: "HKCR \\ жпгфиле", "HKCR \\ системфилеассоЦиатионс \\ . jpg", "HKCR \\ системфилеассоЦиатионс \\ Image", "HKCR \\ \* ", "HKCR \\ аллфилесистемобжектс".</span><span class="sxs-lookup"><span data-stu-id="893bb-111">For example, a .jpg file has the following association array on a default Windows system: "HKCR\\jpgfile", "HKCR\\SystemFileAssociations\\.jpg", "HKCR\\SystemFileAssociations\\image", "HKCR\\\*", "HKCR\\AllFileSystemObjects".</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="893bb-112">B</span><span class="sxs-lookup"><span data-stu-id="893bb-112">B</span></span>

<dl> <dt>

<span data-ttu-id="893bb-113">**bind**</span><span class="sxs-lookup"><span data-stu-id="893bb-113">**bind**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-114">Для загрузки или связывания кода с данными.</span><span class="sxs-lookup"><span data-stu-id="893bb-114">To load or associate code with data.</span></span> <span data-ttu-id="893bb-115">Например, обработчик может быть связан с источником данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-115">For example, a handler may be associated with a Shell data source.</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="893bb-116">C</span><span class="sxs-lookup"><span data-stu-id="893bb-116">C</span></span>

<dl> <dt>

<span data-ttu-id="893bb-117">**каноническое имя**</span><span class="sxs-lookup"><span data-stu-id="893bb-117">**canonical name**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-118">Уникальное имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="893bb-118">The unique name of a resource.</span></span> <span data-ttu-id="893bb-119">Каноническое значение означает "в соответствии с правилами".</span><span class="sxs-lookup"><span data-stu-id="893bb-119">Canonical means "according to the rules."</span></span> <span data-ttu-id="893bb-120">См. также: каноническое имя команды.</span><span class="sxs-lookup"><span data-stu-id="893bb-120">See also: canonical verb name.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-121">**каноническое имя команды**</span><span class="sxs-lookup"><span data-stu-id="893bb-121">**canonical verb name**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-122">Имя, не зависящее от языка, которое можно использовать программно для ссылки на команду, независимо от локализованной строки в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="893bb-122">A language-neutral name that can be used programmatically to refer to a verb, regardless of the localized string in the user interface.</span></span> <span data-ttu-id="893bb-123">См. также: каноническое имя, команда.</span><span class="sxs-lookup"><span data-stu-id="893bb-123">See also: canonical name, verb.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-124">**container**</span><span class="sxs-lookup"><span data-stu-id="893bb-124">**container**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-125">Тип элемента оболочки, который может содержать другие элементы.</span><span class="sxs-lookup"><span data-stu-id="893bb-125">A type of Shell item that can contain other items.</span></span> <span data-ttu-id="893bb-126">Элементы в контейнере предоставляются пространству имен оболочки с помощью источника данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-126">Items in a container are exposed to the Shell namespace by using a Shell data source.</span></span> <span data-ttu-id="893bb-127">К примерам относятся папки, диски, сетевые серверы и сжатые файлы с расширением ZIP.</span><span class="sxs-lookup"><span data-stu-id="893bb-127">Examples include folders, drives, network servers, and compressed files with a .zip file name extension.</span></span> <span data-ttu-id="893bb-128">См. также: источник данных оболочки, папка, элемент оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-128">See also: Shell data source, folder, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-129">**content**</span><span class="sxs-lookup"><span data-stu-id="893bb-129">**content**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-130">Текст и свойства, связанные с элементом оболочки или источником содержимого, который может быть проиндексирован.</span><span class="sxs-lookup"><span data-stu-id="893bb-130">Text and properties associated with a Shell item or a content source that can be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-131">**Источник содержимого**</span><span class="sxs-lookup"><span data-stu-id="893bb-131">**content source**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-132">Элемент, к которому может получить доступ индексатор.</span><span class="sxs-lookup"><span data-stu-id="893bb-132">An item that can be accessed by the indexer.</span></span> <span data-ttu-id="893bb-133">Источники содержимого можно адресации по URL-адресу и предоставлены индексатору с помощью обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="893bb-133">Content sources are addressable by a URL and are provided to the indexer by a protocol handler.</span></span> <span data-ttu-id="893bb-134">К примерам относятся: файлы и папки файловой системы, элементы и папки Microsoft Outlook, записи базы данных и сохраненные элементы Microsoft SharePoint.</span><span class="sxs-lookup"><span data-stu-id="893bb-134">Examples include: file system files and folders, Microsoft Outlook items and folders, database records, and Microsoft SharePoint stored items.</span></span> <span data-ttu-id="893bb-135">Источник содержимого может быть представлен как элементы оболочки путем реализации источника данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-135">A content source can be exposed as Shell items by implementing a Shell data source.</span></span> <span data-ttu-id="893bb-136">См. также: содержимое, элемент оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-136">See also: content, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-137">**content view** (представление содержимого)</span><span class="sxs-lookup"><span data-stu-id="893bb-137">**content view**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-138">Представление в проводнике Windows (предлагается в Windows 7 и более поздних версиях), которое отображает наиболее релевантное содержимое для каждого элемента в списке на основе расширения имени файла или сопоставления типа.</span><span class="sxs-lookup"><span data-stu-id="893bb-138">A view in Windows Explorer (offered in Windows 7 and later) that displays the most relevant content for each item in the list based on its file name extension or Kind association.</span></span> <span data-ttu-id="893bb-139">В представлении содержимого используется логика изменения размера, которая удаляет свойства при уменьшении размера окна, чтобы гарантировать, что наиболее важные свойства остаются видимыми для чтения.</span><span class="sxs-lookup"><span data-stu-id="893bb-139">Content view uses a resizing logic that drops properties when the window size decreases to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="893bb-140">См. также: шаблон макета, вид, Ассоциация типа.</span><span class="sxs-lookup"><span data-stu-id="893bb-140">See also: layout pattern, Kind, Kind association.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-141">**режим просмотра содержимого**</span><span class="sxs-lookup"><span data-stu-id="893bb-141">**content view mode**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-142">См. определение для: представление содержимого.</span><span class="sxs-lookup"><span data-stu-id="893bb-142">See definition for: content view.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-143">**контекстное меню**</span><span class="sxs-lookup"><span data-stu-id="893bb-143">**context menu**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-144">Этот термин иногда используется для обозначения контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="893bb-144">This term is sometimes used to mean shortcut menu.</span></span> <span data-ttu-id="893bb-145">См. определение для: контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="893bb-145">See definition for: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-146">**Обработчик контекстного меню**</span><span class="sxs-lookup"><span data-stu-id="893bb-146">**context menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-147">Этот термин иногда используется для обозначения обработчика контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="893bb-147">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="893bb-148">См. определение для: обработчик контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="893bb-148">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="893bb-149">D</span><span class="sxs-lookup"><span data-stu-id="893bb-149">D</span></span>

<dl> <dt>

<span data-ttu-id="893bb-150">**обработчик объектов данных**</span><span class="sxs-lookup"><span data-stu-id="893bb-150">**data object handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-151">Обработчик, предоставляющий дополнительные форматы буфера обмена для объекта данных (IDataObject) элемента.</span><span class="sxs-lookup"><span data-stu-id="893bb-151">A handler that provides additional clipboard formats for the data object (IDataObject) of an item.</span></span> <span data-ttu-id="893bb-152">Объекты данных используются в сценариях перетаскивания и копирования и вставки.</span><span class="sxs-lookup"><span data-stu-id="893bb-152">Data objects are used in drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-153">**Источник данных**</span><span class="sxs-lookup"><span data-stu-id="893bb-153">**data source**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-154">Этот термин иногда используется для обозначения хранилища данных или источника данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-154">This term is sometimes used to mean data store or Shell data source.</span></span> <span data-ttu-id="893bb-155">См. определение для: хранилище данных, источник данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-155">See definition for: data store, Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-156">**хранилище данных**</span><span class="sxs-lookup"><span data-stu-id="893bb-156">**data store**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-157">Репозиторий данных.</span><span class="sxs-lookup"><span data-stu-id="893bb-157">A repository of data.</span></span> <span data-ttu-id="893bb-158">Хранилище данных может быть предоставлено модели программирования оболочки в качестве контейнера с помощью источника данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-158">A data store can be exposed to the Shell programming model as a container using a Shell data source.</span></span> <span data-ttu-id="893bb-159">Элементы в хранилище данных могут индексироваться системой поиска Windows с помощью обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="893bb-159">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-160">**Композиция рабочего стола**</span><span class="sxs-lookup"><span data-stu-id="893bb-160">**desktop composition**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-161">Функция Windows Vista, позволяющая рисовать отдельные окна в видеопамяти вне экрана, а не непосредственно на основном устройстве отображения.</span><span class="sxs-lookup"><span data-stu-id="893bb-161">A Windows Vista feature that enables individual windows to be drawn to off-screen surfaces in video memory instead of the being drawn directly to the primary display device.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-162">**document**</span><span class="sxs-lookup"><span data-stu-id="893bb-162">**document**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-163">Элемент оболочки, содержащий текст, для которого может быть реализован интерфейс IFilter.</span><span class="sxs-lookup"><span data-stu-id="893bb-163">A Shell item that contains text, and for which the IFilter interface could be implemented.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-164">**удалить обработчик**</span><span class="sxs-lookup"><span data-stu-id="893bb-164">**drop handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-165">Обработчик, который разрешает определенный тип элемента для поддержки сценариев перетаскивания и копирования и вставки.</span><span class="sxs-lookup"><span data-stu-id="893bb-165">A handler that enables a particular item type to support drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-166">**Целевой объект перетаскивания**</span><span class="sxs-lookup"><span data-stu-id="893bb-166">**drop target**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-167">Объект данных, который перетаскивается и удаляется в файл.</span><span class="sxs-lookup"><span data-stu-id="893bb-167">A data object that is dragged and dropped onto a file.</span></span> <span data-ttu-id="893bb-168">См. также: обработчик данных, обработчик Drop.</span><span class="sxs-lookup"><span data-stu-id="893bb-168">See also: data handler, drop handler.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-169">**Динамическая команда**</span><span class="sxs-lookup"><span data-stu-id="893bb-169">**dynamic verb**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-170">Команда, зависящая от состояния элемента оболочки или системы; внешний вид элемента зависит от состояния и требует, чтобы исполняемый код определил, отображается ли элемент.</span><span class="sxs-lookup"><span data-stu-id="893bb-170">A verb that depends on the state of a Shell item or of the system; the appearance of the item is state based and requires that the executing code determine whether the item should appear.</span></span> <span data-ttu-id="893bb-171">См. также: обработчик контекстного меню, статическая команда, команда.</span><span class="sxs-lookup"><span data-stu-id="893bb-171">See also: shortcut menu handler, static verb, verb.</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="893bb-172">E</span><span class="sxs-lookup"><span data-stu-id="893bb-172">E</span></span>

<dl> <dt>

<span data-ttu-id="893bb-173">**Команда обозревателя**</span><span class="sxs-lookup"><span data-stu-id="893bb-173">**Explorer command**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-174">Объект, который можно представить в виде кнопки в верхней части окна проводника Windows, предоставляющей функциональные возможности для элементов и контейнеров в этом окне.</span><span class="sxs-lookup"><span data-stu-id="893bb-174">An object that can be presented as a button near the top of the Windows Explorer window that provides functionality for items and containers in that window.</span></span> <span data-ttu-id="893bb-175">Источник данных оболочки предоставляет командные объекты проводника Windows для определенного элемента контейнера.</span><span class="sxs-lookup"><span data-stu-id="893bb-175">A Shell data source provides the Windows Explorer command objects for a particular container item.</span></span> <span data-ttu-id="893bb-176">Команды иногда используются в качестве глаголов.</span><span class="sxs-lookup"><span data-stu-id="893bb-176">Commands are sometimes used as verbs.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="893bb-177">C</span><span class="sxs-lookup"><span data-stu-id="893bb-177">F</span></span>

<dl> <dt>

<span data-ttu-id="893bb-178">**Сопоставление файлов**</span><span class="sxs-lookup"><span data-stu-id="893bb-178">**file association**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-179">См. определение для: сопоставление типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-179">See definition for: file type association.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-180">**формат файла**</span><span class="sxs-lookup"><span data-stu-id="893bb-180">**file format**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-181">Формат данных, хранящихся в файле с задокументированной спецификацией формата.</span><span class="sxs-lookup"><span data-stu-id="893bb-181">A format for data stored in a file that has a documented format specification.</span></span> <span data-ttu-id="893bb-182">К примерам относятся OLE Докфиле, OPC, XML, ZIP и другие хорошо известные спецификации формата файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-182">Examples include OLE DocFile, OPC, XML, ZIP and other well known file format specifications.</span></span> <span data-ttu-id="893bb-183">Создатели типов файлов обычно используют существующий формат файлов в качестве базиса для нового типа файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-183">File type creators generally use an existing file format as the basis of a new file type.</span></span> <span data-ttu-id="893bb-184">Формат файла может быть просто определением, для которого не создается экземпляр типа файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-184">A file format can be simply a definition that is not instantiated as a file type.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-185">**обработчик формата файла**</span><span class="sxs-lookup"><span data-stu-id="893bb-185">**file format handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-186">Этот термин является синонимом обработчика типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-186">This term is a synonym for file type handler.</span></span> <span data-ttu-id="893bb-187">См. определение для: обработчика типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-187">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-188">**расширение имени файла**</span><span class="sxs-lookup"><span data-stu-id="893bb-188">**file name extension**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-189">Основным индикатором типа файла для элементов файловой системы является часть имени файла, следующая за конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="893bb-189">The primary indicator of a file type for file system items, it is the portion of the file name that follows the final dot.</span></span> <span data-ttu-id="893bb-190">Расширение имени файла не может содержать пробелы или символы, отличные от ASCII, и применяется только к файлам (не папкам).</span><span class="sxs-lookup"><span data-stu-id="893bb-190">The file name extension cannot contain spaces or non-ASCII characters and applies only to files (not folders).</span></span> <span data-ttu-id="893bb-191">Расширения имен файлов сравниваются с помощью функции сравнения, которая не чувствительна к регистру или языку.</span><span class="sxs-lookup"><span data-stu-id="893bb-191">File name extensions are compared using a comparison function that is not sensitive to case or locale.</span></span> <span data-ttu-id="893bb-192">См. также: формат файла, тип файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-192">See also: file format, file type.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-193">**Тип файла**</span><span class="sxs-lookup"><span data-stu-id="893bb-193">**file type**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-194">Определенное значение расширения имени файла, например ". htm" или ". jpg", которое определяет класс файлов того же типа и имеет общий набор ассоциаций.</span><span class="sxs-lookup"><span data-stu-id="893bb-194">A particular file name extension value, like ".htm" or ".jpg", that defines a class of files that are of the same type and have a common set of associations.</span></span> <span data-ttu-id="893bb-195">См. также: вид, сопоставление типов файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-195">See also: Kind, file type association.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-196">**сопоставление типов файлов**</span><span class="sxs-lookup"><span data-stu-id="893bb-196">**file type association**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-197">Для конкретного расширения имени файла элементы массива ассоциаций, определяющие, где можно зарегистрировать обработчики и другие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="893bb-197">For a particular file name extension, the association array elements that define where handlers and other attributes can be registered.</span></span> <span data-ttu-id="893bb-198">См. также: массив ассоциаций, тип файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-198">See also: association array, file type.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-199">**Настройка типа файла**</span><span class="sxs-lookup"><span data-stu-id="893bb-199">**file type customization**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-200">Ассоциация, позволяющая оболочке настраивать тип файла в оболочке.</span><span class="sxs-lookup"><span data-stu-id="893bb-200">An association that enables Shell to customize how Shell treats a file type.</span></span> <span data-ttu-id="893bb-201">К настройкам типов файлов относятся: указание приложения, используемого для открытия файла при двойном щелчке, Добавление команд в контекстное меню для типа файла, задание пользовательского значка, указание типа содержимого MIME для связи с типом файла, указание воспринимаемого типа и указание одного или нескольких приложений, связанных с типом файла, с помощью диалогового окна "Открыть с помощью".</span><span class="sxs-lookup"><span data-stu-id="893bb-201">File type customizations include: specifying the application used to open the file when double-clicked, adding commands to the shortcut menu for a file type, specifying a custom icon, specifying a MIME content type to associate with a file type, specifying a perceived type, and specifying one or more applications associated by file type with the Open With dialog box.</span></span> <span data-ttu-id="893bb-202">См. также: PerceivedType.</span><span class="sxs-lookup"><span data-stu-id="893bb-202">See also: PerceivedType.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-203">**обработчик типа файла**</span><span class="sxs-lookup"><span data-stu-id="893bb-203">**file type handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-204">Обработчик, зарегистрированный для типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-204">A handler registered for a file type.</span></span> <span data-ttu-id="893bb-205">См. также: обработчик.</span><span class="sxs-lookup"><span data-stu-id="893bb-205">See also: handler.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-206">**Folder**</span><span class="sxs-lookup"><span data-stu-id="893bb-206">**folder**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-207">См. определение для: Container.</span><span class="sxs-lookup"><span data-stu-id="893bb-207">See definition for: container.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-208">**полный ПИДЛ**</span><span class="sxs-lookup"><span data-stu-id="893bb-208">**full PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-209">ПИДЛ, который однозначно описывает объект относительно папки рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="893bb-209">A PIDL that uniquely describes an object relative to the desktop folder.</span></span>

</dd> </dl>

## <a name="h"></a><span data-ttu-id="893bb-210">H</span><span class="sxs-lookup"><span data-stu-id="893bb-210">H</span></span>

<dl> <dt>

<span data-ttu-id="893bb-211">**обработке**</span><span class="sxs-lookup"><span data-stu-id="893bb-211">**handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-212">COM-объект, предоставляющий функциональные возможности для элемента оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-212">A COM object that provides functionality for a Shell item.</span></span> <span data-ttu-id="893bb-213">Большинство источников данных оболочки предлагают расширяемую систему для привязки обработчиков к элементам.</span><span class="sxs-lookup"><span data-stu-id="893bb-213">Most Shell data sources offer an extensible system for binding handlers to items.</span></span> <span data-ttu-id="893bb-214">Например, папка «файловая система» использует систему взаимосвязей для поиска обработчиков определенного типа файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-214">For example, the file system folder uses the association system to look up the handlers for a particular file type.</span></span> <span data-ttu-id="893bb-215">См. также: сопоставление файлов, тип файла, Настройка типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-215">See also: file association, file type, file type customization.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="893bb-216">I</span><span class="sxs-lookup"><span data-stu-id="893bb-216">I</span></span>

<dl> <dt>

<span data-ttu-id="893bb-217">**обработчик значков**</span><span class="sxs-lookup"><span data-stu-id="893bb-217">**icon handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-218">Обработчик, предоставляющий сведения, необходимые для создания и кэширования значка элемента.</span><span class="sxs-lookup"><span data-stu-id="893bb-218">A handler that provides the information needed to generate and cache an icon for an item.</span></span> <span data-ttu-id="893bb-219">Хранилище данных файловой системы поддерживает загрузку обработчика значков для элемента на основе типа файла, позволяя этому обработчику предоставлять значок, используемый для всех экземпляров этого типа файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-219">The file system data store supports loading an icon handler for an item based on the file type, enabling that handler to provide an icon that is used for all instances of that file type.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-220">**обработчик подсказки**</span><span class="sxs-lookup"><span data-stu-id="893bb-220">**infotip handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-221">Обработчик, который предоставляет всплывающий текст, когда пользователь наводит указатель мыши на объект пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="893bb-221">A handler that provides pop-up text when the user hovers the mouse pointer over a user interface object.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-222">**Item**</span><span class="sxs-lookup"><span data-stu-id="893bb-222">**item**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-223">См. определение для: элемент оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-223">See definition for: Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-224">**класс Item**</span><span class="sxs-lookup"><span data-stu-id="893bb-224">**item class**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-225">См. определение для: тип файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-225">See definition for: file type.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-226">**список идентификаторов элементов**</span><span class="sxs-lookup"><span data-stu-id="893bb-226">**item identifier list**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-227">Последовательность из одной или нескольких структур ШИТЕМИД, которые однозначно определяют объект относительно некоторого корневого объекта.</span><span class="sxs-lookup"><span data-stu-id="893bb-227">Sequence of one or more SHITEMID structures that uniquely defines an object relative to some root object.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="893bb-228">K</span><span class="sxs-lookup"><span data-stu-id="893bb-228">K</span></span>

<dl> <dt>

<span data-ttu-id="893bb-229">**Вид**</span><span class="sxs-lookup"><span data-stu-id="893bb-229">**Kind**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-230">Свойство, которое предоставляет понятное имя пользователя и может быть связано со списком свойств и шаблоном макета.</span><span class="sxs-lookup"><span data-stu-id="893bb-230">A property that provides a user-friendly Kind name, and can be associated with a list of properties and a layout pattern.</span></span> <span data-ttu-id="893bb-231">В Windows Vista появился вид, чтобы выразить более понятное представление типа файлов, которое было определено как многозначное строковое свойство (канонические строковые значения), поэтому у вас может быть значение вида "Audio; Video" или "Link; Document".</span><span class="sxs-lookup"><span data-stu-id="893bb-231">Kind was introduced in Windows Vista to express a more end-user friendly notion of file type and it was defined to be a multi-value string property (canonical string values), thus you can have an "audio;video" or "link;document" Kind value.</span></span> <span data-ttu-id="893bb-232">Некоторые понятные имена пользователей уже связаны со свойствами и шаблонами макета.</span><span class="sxs-lookup"><span data-stu-id="893bb-232">Some user-friendly Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="893bb-233">Например, элементы, связанные с видом. рисунок и элементы, связанные с Kind.Docумент, отображают различные свойства, даже если они находятся в одном и том же представлении.</span><span class="sxs-lookup"><span data-stu-id="893bb-233">For example, items associated with Kind.Picture and items associated with Kind.Document display different properties even when they are in the same view.</span></span> <span data-ttu-id="893bb-234">Каждый вид элемента может быть связан с одним из четырех уникальных шаблонов макета, определяющих количество свойств, отображаемых для каждого элемента и их макета.</span><span class="sxs-lookup"><span data-stu-id="893bb-234">Each item Kind can be associated with one of four unique layout patterns that define the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="893bb-235">См. также: тип связи, представление содержимого, шаблон макета.</span><span class="sxs-lookup"><span data-stu-id="893bb-235">See also: Kind association, content view, layout pattern.</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="893bb-236">L</span><span class="sxs-lookup"><span data-stu-id="893bb-236">L</span></span>

<dl> <dt>

<span data-ttu-id="893bb-237">**шаблон макета**</span><span class="sxs-lookup"><span data-stu-id="893bb-237">**layout pattern**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-238">Одно из нескольких упорядочений для отображения свойств.</span><span class="sxs-lookup"><span data-stu-id="893bb-238">One of several arrangements for displaying properties.</span></span> <span data-ttu-id="893bb-239">В Windows 7 и более поздних версиях при регистрации нового типа файлов можно использовать представление содержимого для регистрации пользовательского списка свойств и шаблона макета для типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-239">In Windows 7 and later, when you are registering a new file type, you can use the content view to register a custom property list and layout pattern for your file type.</span></span> <span data-ttu-id="893bb-240">Можно выбрать один из четырех различных шаблонов макета: Alpha (для результатов поиска документов, содержащих фрагменты кода), бета-версия (для результатов поиска по электронной почте с фрагментами кода), гамма (аналогична альфа-каналу, но с двунаправленным макетом вместо четырех) и Дельта (для отображения многих более коротких свойств, таких как музыка и изображения).</span><span class="sxs-lookup"><span data-stu-id="893bb-240">You can choose from four different layout patterns: Alpha (for document search results that contain code snippets), Beta (for email search results with code snippets), Gamma (similar to Alpha but with a two-line layout instead of four), and Delta (for showing many shorter properties, such as with music and pictures).</span></span> <span data-ttu-id="893bb-241">См. также: представление содержимого, вид, сопоставление типа.</span><span class="sxs-lookup"><span data-stu-id="893bb-241">See also: content view, Kind, Kind association.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="893bb-242">M</span><span class="sxs-lookup"><span data-stu-id="893bb-242">M</span></span>

<dl> <dt>

<span data-ttu-id="893bb-243">**обработчик метаданных**</span><span class="sxs-lookup"><span data-stu-id="893bb-243">**metadata handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-244">Этот термин иногда используется для обозначения обработчика свойств.</span><span class="sxs-lookup"><span data-stu-id="893bb-244">This term is sometimes used to mean property handler.</span></span> <span data-ttu-id="893bb-245">См. Определение обработчика свойства:.</span><span class="sxs-lookup"><span data-stu-id="893bb-245">See definition for: property handler.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="893bb-246">Нет</span><span class="sxs-lookup"><span data-stu-id="893bb-246">N</span></span>

<dl> <dt>

<span data-ttu-id="893bb-247">**расширение пространства имен**</span><span class="sxs-lookup"><span data-stu-id="893bb-247">**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-248">См. определение для: Shell Data Source.</span><span class="sxs-lookup"><span data-stu-id="893bb-248">See definition for: Shell data source.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="893bb-249">O</span><span class="sxs-lookup"><span data-stu-id="893bb-249">O</span></span>

<dl> <dt>

<span data-ttu-id="893bb-250">**Связывание объектов и внедрение базы данных (OLE DB)**</span><span class="sxs-lookup"><span data-stu-id="893bb-250">**Object Linking and Embedding Database (OLE DB)**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-251">Стандартный набор интерфейсов, предоставляющий разнородный доступ к разнородным источникам информации, находящимся в любом месте, например файловые системы, папки электронной почты и базы данных.</span><span class="sxs-lookup"><span data-stu-id="893bb-251">A standard set of interfaces that provides heterogeneous access to disparate sources of information located anywhere, such as file systems, email folders, and databases.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-252">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="893bb-252">**OLE DB**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-253">См. определение для: связывание объектов и внедрение базы данных.</span><span class="sxs-lookup"><span data-stu-id="893bb-253">See definition for: Object Linking and Embedding Database.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="893bb-254">С</span><span class="sxs-lookup"><span data-stu-id="893bb-254">P</span></span>

<dl> <dt>

<span data-ttu-id="893bb-255">**PerceivedType**</span><span class="sxs-lookup"><span data-stu-id="893bb-255">**PerceivedType**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-256">Обширная категория типов форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-256">A broad category of file format types.</span></span> <span data-ttu-id="893bb-257">PerceivedType был впервые появился в Windows XP и поддерживает ограниченный набор известных типов файлов (например, Image, Text, Audio и сжатый тип файлов).</span><span class="sxs-lookup"><span data-stu-id="893bb-257">PerceivedType was introduced in Windows XP, and supports a limited set of known file types (examples include Image, Text, Audio, and Compressed file types).</span></span> <span data-ttu-id="893bb-258">Типы файлов, как правило, общедоступные типы файлов, также могут иметь воспринимаемый тип.</span><span class="sxs-lookup"><span data-stu-id="893bb-258">File types, generally public file types, can also have a perceived type.</span></span> <span data-ttu-id="893bb-259">Например, типы файлов изображений BMP, PNG, JPG и GIF также имеют воспринимаемый тип Image.</span><span class="sxs-lookup"><span data-stu-id="893bb-259">For example, the image file types .bmp, .png, .jpg, and .gif are also of the perceived type, image.</span></span> <span data-ttu-id="893bb-260">На уровне программирования PerceivedType выражается целым числом.</span><span class="sxs-lookup"><span data-stu-id="893bb-260">At the programming layer, PerceivedType is expressed as an integer.</span></span> <span data-ttu-id="893bb-261">Поскольку существует код, использующий Kind и PerceivedType, владельцы форматов файлов должны зарегистрировать оба.</span><span class="sxs-lookup"><span data-stu-id="893bb-261">Because there is code that uses Kind and PerceivedType, file format owners must register both.</span></span> <span data-ttu-id="893bb-262">Например, "Воспроизвести все" зависит от PerceivedType.</span><span class="sxs-lookup"><span data-stu-id="893bb-262">For example "play all" depends on PerceivedType.</span></span> <span data-ttu-id="893bb-263">См. также: тип файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-263">See also: file type.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-264">**обработчик просмотра**</span><span class="sxs-lookup"><span data-stu-id="893bb-264">**preview handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-265">Обработчик, который быстро создает доступное только для чтения упрощенное представление элемента оболочки, отображаемого в панели предварительного просмотра проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="893bb-265">A handler that quickly produces a read-only, simplified view of the Shell item to be displayed in the Windows Explorer preview pane.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-266">**обработчик свойства**</span><span class="sxs-lookup"><span data-stu-id="893bb-266">**property handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-267">Обработчик, который преобразует данные, хранящиеся в файле, в структурированную схему, которая распознается и может быть доступна в проводнике Windows, Windows Search и других приложениях.</span><span class="sxs-lookup"><span data-stu-id="893bb-267">A handler that translates data stored in a file into a structured schema that is recognized by and can be accessed by Windows Explorer, Windows Search, and other applications.</span></span> <span data-ttu-id="893bb-268">Затем эти системы могут взаимодействовать с обработчиком свойств для записи и чтения свойств в файле и из него.</span><span class="sxs-lookup"><span data-stu-id="893bb-268">These systems can then interact with the property handler to write and read properties to and from the file.</span></span> <span data-ttu-id="893bb-269">Переведенные данные включают в себя представление Details, инфотипс, область сведений, страницы свойств и т. д.</span><span class="sxs-lookup"><span data-stu-id="893bb-269">The translated data includes details view, infotips, details pane, property pages, and so forth.</span></span> <span data-ttu-id="893bb-270">Каждый обработчик свойств связан с определенным типом файла, определяемым расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-270">Each property handler is associated with a particular file type, identified by the file name extension.</span></span> <span data-ttu-id="893bb-271">См. также: система свойств.</span><span class="sxs-lookup"><span data-stu-id="893bb-271">See also: property system.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-272">**обработчик страницы свойств**</span><span class="sxs-lookup"><span data-stu-id="893bb-272">**property sheet handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-273">Обработчик, который используется для создания настраиваемых страниц свойств с изображениями и элементами управления пользовательского интерфейса, которые допускают пользовательское взаимодействие с типом файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-273">A handler that is used to create custom property sheets with UI pictures and controls that permit custom interaction with a file type.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-274">**система свойств**</span><span class="sxs-lookup"><span data-stu-id="893bb-274">**property system**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-275">Расширяемая система чтения и записи определений данных, использующая свойства, реализованные как пары "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="893bb-275">An extensible read/write system of data definitions that uses properties implemented as name-value pairs.</span></span> <span data-ttu-id="893bb-276">См. также: обработчик свойств, элемент оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-276">See also: property handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-277">**значение свойства**</span><span class="sxs-lookup"><span data-stu-id="893bb-277">**property value**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-278">Значение, связанное с именем свойства для элемента оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-278">A value associated with a property name for a Shell item.</span></span> <span data-ttu-id="893bb-279">Например, «автор», «размер» и «Дата съемки» — свойства.</span><span class="sxs-lookup"><span data-stu-id="893bb-279">For example, "Author", "Size", and "Date Taken" are properties.</span></span> <span data-ttu-id="893bb-280">Значения свойств выражаются в виде структуры ПРОПВАРИАНТ.</span><span class="sxs-lookup"><span data-stu-id="893bb-280">Property values are expressed as a PROPVARIANT structure.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-281">**обработчик протокола**</span><span class="sxs-lookup"><span data-stu-id="893bb-281">**protocol handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-282">Обработчик, обращающийся к источникам содержимого и предоставляющий объект Иурлакцессор для указанного протокола и URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="893bb-282">A handler that accesses content sources and provides an IUrlAccessor object for a specified protocol and URL.</span></span> <span data-ttu-id="893bb-283">Обработчики протоколов расширяют функциональные возможности поиска Windows и могут предоставлять уведомления об изменениях индексаторам.</span><span class="sxs-lookup"><span data-stu-id="893bb-283">Protocol handlers extend Windows Search functionality, and may provide change notifications to indexers.</span></span> <span data-ttu-id="893bb-284">Для индексирования конкретных типов хранилищ данных требуются разные обработчики протокола.</span><span class="sxs-lookup"><span data-stu-id="893bb-284">Different protocol handlers are required to index specific types of data stores.</span></span> <span data-ttu-id="893bb-285">Чтобы обеспечить разумное взаимодействие с пользователем, необходимо также предоставить источник данных оболочки для хранилища данных в дополнение к реализации обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="893bb-285">To provide a reasonable user experience, you must also provide a Shell data source for the data store in addition to implementing your protocol handler.</span></span> <span data-ttu-id="893bb-286">Обработчик протокола предоставляет элементы в хранилище данных индексатору, а источник данных оболочки предоставляет элементы в хранилище данных оболочке.</span><span class="sxs-lookup"><span data-stu-id="893bb-286">The protocol handler exposes the items in the data store to the indexer, while the Shell data source exposes the items in the data store to the Shell.</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="893bb-287">R</span><span class="sxs-lookup"><span data-stu-id="893bb-287">R</span></span>

<dl> <dt>

<span data-ttu-id="893bb-288">**относительные ПИДЛ**</span><span class="sxs-lookup"><span data-stu-id="893bb-288">**relative PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-289">Объект ПИДЛ, который относится к определенному корневому объекту в пространстве имен оболочки, отличном от папки рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="893bb-289">A PIDL that is relative to some root object in the shell namespace other than the desktop folder.</span></span> <span data-ttu-id="893bb-290">Обычно это родительская папка элемента.</span><span class="sxs-lookup"><span data-stu-id="893bb-290">This is commonly the parent folder of the item.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="893bb-291">S</span><span class="sxs-lookup"><span data-stu-id="893bb-291">S</span></span>

<dl> <dt>

<span data-ttu-id="893bb-292">**Источник данных оболочки**</span><span class="sxs-lookup"><span data-stu-id="893bb-292">**Shell data source**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-293">Компонент, используемый для расширения пространства имен оболочки и предоставления элементов в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="893bb-293">A component that is used to extend the Shell namespace and expose items in a data store.</span></span> <span data-ttu-id="893bb-294">В прошлом источник данных оболочки назывался расширением пространства имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-294">In the past, the Shell data source was referred to as the Shell namespace extension.</span></span> <span data-ttu-id="893bb-295">См. также: контейнер, обработчик, элемент оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-295">See also: container, handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-296">**Расширение оболочки**</span><span class="sxs-lookup"><span data-stu-id="893bb-296">**Shell extension**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-297">Этот термин иногда используется для обозначения обработчика типов файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-297">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="893bb-298">См. определение для: обработчика типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-298">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-299">**Обработчик расширения оболочки**</span><span class="sxs-lookup"><span data-stu-id="893bb-299">**Shell extension handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-300">Этот термин иногда используется для обозначения обработчика типов файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-300">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="893bb-301">См. определение для: обработчика типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-301">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-302">**Обработчик оболочки**</span><span class="sxs-lookup"><span data-stu-id="893bb-302">**Shell handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-303">Этот термин иногда используется для обозначения обработчика типов файлов.</span><span class="sxs-lookup"><span data-stu-id="893bb-303">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="893bb-304">См. определение для: обработчика типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-304">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-305">**Элемент оболочки**</span><span class="sxs-lookup"><span data-stu-id="893bb-305">**Shell item**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-306">Один фрагмент содержимого.</span><span class="sxs-lookup"><span data-stu-id="893bb-306">A single piece of content.</span></span> <span data-ttu-id="893bb-307">Некоторые элементы оболочки являются источниками содержимого, а некоторые — нет.</span><span class="sxs-lookup"><span data-stu-id="893bb-307">Some Shell items are content sources, and some are not.</span></span> <span data-ttu-id="893bb-308">Папка — это источник содержимого, например, но не файл. jpg.</span><span class="sxs-lookup"><span data-stu-id="893bb-308">A folder is a content source, for example, but a .jpg file is not.</span></span> <span data-ttu-id="893bb-309">Обработчики типов файлов предоставляют элементы оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-309">File type handlers expose Shell items.</span></span> <span data-ttu-id="893bb-310">В некоторых контекстах "элемент" используется для различения контейнеров от неконтейнерных.</span><span class="sxs-lookup"><span data-stu-id="893bb-310">In some contexts "item" is used to distinguish containers from noncontainers.</span></span> <span data-ttu-id="893bb-311">См. также: контейнер, источник содержимого, обработчик типа файла.</span><span class="sxs-lookup"><span data-stu-id="893bb-311">See also: container, content source, file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-312">**Расширение пространства имен оболочки**</span><span class="sxs-lookup"><span data-stu-id="893bb-312">**Shell namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-313">Этот термин иногда используется для обозначения источника данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-313">This term is sometimes used to mean Shell data source.</span></span> <span data-ttu-id="893bb-314">См. определение для: Shell Data Source.</span><span class="sxs-lookup"><span data-stu-id="893bb-314">See definition for: Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-315">**контекстное меню**</span><span class="sxs-lookup"><span data-stu-id="893bb-315">**shortcut menu**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-316">Пользовательский интерфейс, используемый для представления коллекции команд, связанных с элементом пользовательского интерфейса, например файла или папки.</span><span class="sxs-lookup"><span data-stu-id="893bb-316">A user interface that is used to present a collection of verbs associated with a user interface element, such as a file or folder.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-317">**Обработчик контекстного меню**</span><span class="sxs-lookup"><span data-stu-id="893bb-317">**Shortcut menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-318">Обработчик, добавляющий глаголы для элемента или элементов.</span><span class="sxs-lookup"><span data-stu-id="893bb-318">A handler that adds verbs for an item or items.</span></span> <span data-ttu-id="893bb-319">Эти команды обычно отображаются в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="893bb-319">These verbs are commonly displayed in a shortcut menu.</span></span> <span data-ttu-id="893bb-320">См. также: контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="893bb-320">See also: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-321">**простая ПИДЛ**</span><span class="sxs-lookup"><span data-stu-id="893bb-321">**simple PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-322">ПИДЛ, который анализируется без проверки диска.</span><span class="sxs-lookup"><span data-stu-id="893bb-322">A PIDL that is parsed without disk verification.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-323">**Статическая команда**</span><span class="sxs-lookup"><span data-stu-id="893bb-323">**static verb**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-324">Команда, которая применяется к элементу оболочки без необходимости проверять текущее состояние элемента или системы.</span><span class="sxs-lookup"><span data-stu-id="893bb-324">A verb that applies to a Shell item without needing to inspect the current state of an item or system.</span></span> <span data-ttu-id="893bb-325">Статическая команда основана на статической регистрации связанных элементов элемента и не изменяется.</span><span class="sxs-lookup"><span data-stu-id="893bb-325">A static verb is based on a static registration of the associated elements of an item, and does not change.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="893bb-326">T</span><span class="sxs-lookup"><span data-stu-id="893bb-326">T</span></span>

<dl> <dt>

<span data-ttu-id="893bb-327">**обработчик эскизов**</span><span class="sxs-lookup"><span data-stu-id="893bb-327">**thumbnail handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-328">Обработчик, предоставляющий статическое изображение для представления элемента оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-328">A handler that provides a static image to represent a Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-329">**Поставщик эскизов**</span><span class="sxs-lookup"><span data-stu-id="893bb-329">**thumbnail provider**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-330">Этот термин иногда используется для обозначения обработчика эскиза.</span><span class="sxs-lookup"><span data-stu-id="893bb-330">This term is sometimes used to mean thumbnail handler.</span></span> <span data-ttu-id="893bb-331">См. определение для: обработчик эскизов.</span><span class="sxs-lookup"><span data-stu-id="893bb-331">See definition for: thumbnail handler.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="893bb-332">U</span><span class="sxs-lookup"><span data-stu-id="893bb-332">U</span></span>

<dl> <dt>

<span data-ttu-id="893bb-333">**Понятное имя пользователя**</span><span class="sxs-lookup"><span data-stu-id="893bb-333">**user friendly kind name**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-334">См. определение для: Kind.</span><span class="sxs-lookup"><span data-stu-id="893bb-334">See definition for: Kind.</span></span>

</dd> </dl>

## <a name="v"></a><span data-ttu-id="893bb-335">V</span><span class="sxs-lookup"><span data-stu-id="893bb-335">V</span></span>

<dl> <dt>

<span data-ttu-id="893bb-336">**Команда**</span><span class="sxs-lookup"><span data-stu-id="893bb-336">**verb**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-337">Отдельное действие, которое может быть вызвано элементом оболочки.</span><span class="sxs-lookup"><span data-stu-id="893bb-337">An individual action that can be called by a Shell item.</span></span> <span data-ttu-id="893bb-338">Примеры: Open и Print.</span><span class="sxs-lookup"><span data-stu-id="893bb-338">Examples include open and print.</span></span> <span data-ttu-id="893bb-339">Команды иногда называют командами или задачами.</span><span class="sxs-lookup"><span data-stu-id="893bb-339">Verbs are sometimes referred to as commands or tasks.</span></span> <span data-ttu-id="893bb-340">См. также: Динамическая команда, обработчик контекстного меню, статическая команда.</span><span class="sxs-lookup"><span data-stu-id="893bb-340">See also: dynamic verb, shortcut menu handler, static verb.</span></span>

</dd> <dt>

<span data-ttu-id="893bb-341">**обработчик команд**</span><span class="sxs-lookup"><span data-stu-id="893bb-341">**verb handler**</span></span>
</dt> <dd>

<span data-ttu-id="893bb-342">Этот термин иногда используется для обозначения обработчика контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="893bb-342">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="893bb-343">См. определение для: обработчик контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="893bb-343">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

 

 



