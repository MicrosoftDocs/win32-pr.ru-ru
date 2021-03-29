---
description: Чтобы гарантировать, что данные индексируются и правильно отображаются для пользователя во время поиска, необходимо реализовать оболочки хранилища данных (также известные как расширения пространства имен оболочки) и обработчики типов файлов (также называемые расширениями оболочки, обработчиками расширений или обработчиками расширений оболочки).
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Добавление значков, предварительных версий и контекстных меню
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540735"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a><span data-ttu-id="73e9b-103">Добавление значков, предварительных версий и контекстных меню</span><span class="sxs-lookup"><span data-stu-id="73e9b-103">Adding Icons, Previews and Shortcut Menus</span></span>

<span data-ttu-id="73e9b-104">Чтобы гарантировать, что данные индексируются и правильно отображаются для пользователя во время поиска, необходимо реализовать оболочки хранилища данных (также известные как [расширения пространства имен оболочки](../shell/nse-works.md)) и обработчики типов файлов (также называемые расширениями оболочки, [обработчиками расширений](../shell/handlers.md)или обработчиками расширений оболочки).</span><span class="sxs-lookup"><span data-stu-id="73e9b-104">To ensure that your data is indexed and presented correctly to the user during searches, you need to implement Shell data stores (also known as [Shell Namespace Extensions](../shell/nse-works.md)), and file type handlers (also known as Shell extensions, [extension handlers](../shell/handlers.md), or Shell extension handlers).</span></span>

<span data-ttu-id="73e9b-105">В этом разделе описываются следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="73e9b-105">This topic describes the following interfaces:</span></span>

-   [<span data-ttu-id="73e9b-106">Реализация обработчиков типов файлов</span><span class="sxs-lookup"><span data-stu-id="73e9b-106">Implementing File Type Handlers</span></span>](#implementing-file-type-handlers)
    -   [<span data-ttu-id="73e9b-107">IPersist</span><span class="sxs-lookup"><span data-stu-id="73e9b-107">IPersist</span></span>](#ipersist)
    -   [<span data-ttu-id="73e9b-108">иперсистфолдер</span><span class="sxs-lookup"><span data-stu-id="73e9b-108">IPersistFolder</span></span>](#ipersistfolder)
    -   [<span data-ttu-id="73e9b-109">ишеллфолдер</span><span class="sxs-lookup"><span data-stu-id="73e9b-109">IShellFolder</span></span>](#ishellfolder)
    -   [<span data-ttu-id="73e9b-110">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="73e9b-110">IContextMenu</span></span>](#icontextmenu)
    -   [<span data-ttu-id="73e9b-111">иекстрактикон</span><span class="sxs-lookup"><span data-stu-id="73e9b-111">IExtractIcon</span></span>](#iextracticon)
    -   [<span data-ttu-id="73e9b-112">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="73e9b-112">IPreviewHandler</span></span>](#ipreviewhandler)
-   [<span data-ttu-id="73e9b-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="73e9b-113">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="73e9b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="73e9b-114">Related topics</span></span>](#related-topics)

## <a name="implementing-file-type-handlers"></a><span data-ttu-id="73e9b-115">Реализация обработчиков типов файлов</span><span class="sxs-lookup"><span data-stu-id="73e9b-115">Implementing File Type Handlers</span></span>

<span data-ttu-id="73e9b-116">Эти расширения оболочки или обработчики типов файлов предоставляют пользователям следующие возможности оболочки:</span><span class="sxs-lookup"><span data-stu-id="73e9b-116">These Shell extensions or file type handlers provide your users with the following Shell experiences:</span></span>

-   <span data-ttu-id="73e9b-117">В представлении результатов отображается конкретный значок для типа элемента.</span><span class="sxs-lookup"><span data-stu-id="73e9b-117">The results view displays a specific icon for your item type.</span></span>
-   <span data-ttu-id="73e9b-118">В представлении результатов отображается предварительный просмотр элемента, когда пользователь выбирает элемент.</span><span class="sxs-lookup"><span data-stu-id="73e9b-118">The results view displays a preview of the item when the user selects the item.</span></span>
-   <span data-ttu-id="73e9b-119">Пользователи могут дважды щелкнуть элемент, чтобы инициировать такие события, как открытие файла.</span><span class="sxs-lookup"><span data-stu-id="73e9b-119">Users can double-click items to initiate events such as opening the file.</span></span>
-   <span data-ttu-id="73e9b-120">Пользователи могут щелкнуть правой кнопкой мыши элемент, чтобы открыть контекстное меню (контекст).</span><span class="sxs-lookup"><span data-stu-id="73e9b-120">Users can right-click items to access a shortcut (context) menu.</span></span>
-   <span data-ttu-id="73e9b-121">Пользователи могут перетаскивать элементы.</span><span class="sxs-lookup"><span data-stu-id="73e9b-121">Users can drag-and-drop items.</span></span>

<span data-ttu-id="73e9b-122">Как и все объекты COM, обработчики типов файлов должны реализовывать интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) и фабрику классов.</span><span class="sxs-lookup"><span data-stu-id="73e9b-122">Like all Component Object Model (COM) objects, file type handlers must implement an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a class factory.</span></span>

<span data-ttu-id="73e9b-123">В Windows XP или более ранних версиях обработчики должны также реализовать:</span><span class="sxs-lookup"><span data-stu-id="73e9b-123">In Windows XP or earlier, handlers should also implement:</span></span>

-   <span data-ttu-id="73e9b-124">Либо [интерфейс IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span><span class="sxs-lookup"><span data-stu-id="73e9b-124">Either [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span></span>
-   <span data-ttu-id="73e9b-125">Или [интерфейс ишеллекстинит](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span><span class="sxs-lookup"><span data-stu-id="73e9b-125">Or [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span></span>

<span data-ttu-id="73e9b-126">В Windows Vista интерфейс [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) и [интерфейс ишеллекстинит](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) были заменены следующими тремя интерфейсами для инициализации обработчика с помощью оболочки:</span><span class="sxs-lookup"><span data-stu-id="73e9b-126">In Windows Vista, [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) were replaced by the following three interfaces for Shell to initialize the handler:</span></span>

-   [<span data-ttu-id="73e9b-127">Интерфейс IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="73e9b-127">IInitializeWithStream Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="73e9b-128">Интерфейс Иинитиализевиситем</span><span class="sxs-lookup"><span data-stu-id="73e9b-128">IInitializeWithItem Interface</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="73e9b-129">Интерфейс IInitializeWithFile</span><span class="sxs-lookup"><span data-stu-id="73e9b-129">IInitializeWithFile Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="73e9b-130">Чтобы обеспечить разумное взаимодействие с пользователем, необходимо предоставить обработчику протокола хранилище данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="73e9b-130">To provide a reasonable user experience you must provide a Shell data store with your protocol handler.</span></span> <span data-ttu-id="73e9b-131">Это хранилище данных затем служит "фабрикой" для обработчиков значков, обработчиков контекстного меню, обработчиков предварительного просмотра и т. д.</span><span class="sxs-lookup"><span data-stu-id="73e9b-131">That data store then serves as the "factory" for icon handlers, shortcut menu handlers, preview handlers, and so forth.</span></span> <span data-ttu-id="73e9b-132">[Интерфейс ишеллфолдер](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)требует минимальных реализаций [интерфейса IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist) и [интерфейса иперсистфолдер](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) , а для [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) и [иекстрактикон](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)требуется минимальная реализация интерфейса ишеллфолдер.</span><span class="sxs-lookup"><span data-stu-id="73e9b-132">Minimal implementations of [IPersist Interface](/windows/desktop/api/objidl/nn-objidl-ipersist) and [IPersistFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) are required by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), and a minimal implementation of IShellFolder Interface is required for the [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) and [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span></span>

> [!Note]  
> <span data-ttu-id="73e9b-133">Для **IPersist**, **иперсистфолдер** и **ишеллфолдер** должен быть реализован один и тот же идентификатор класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="73e9b-133">The same class identifier (CLSID) should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="73e9b-134">Дополнительные сведения о создании хранилища данных оболочки для поддержки обработчика протокола см. в разделе [реализация базовых интерфейсов объекта папки](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73e9b-134">For more information about creating a Shell data store to support a protocol handler, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

### <a name="ipersist"></a><span data-ttu-id="73e9b-135">IPersist</span><span class="sxs-lookup"><span data-stu-id="73e9b-135">IPersist</span></span>

<span data-ttu-id="73e9b-136">Интерфейс **IPersist** определяет единственный метод- **ClassID**, который предназначен для предоставления идентификатора CLSID объекта, который может храниться в системе постоянно.</span><span class="sxs-lookup"><span data-stu-id="73e9b-136">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="73e9b-137">Метод</span><span class="sxs-lookup"><span data-stu-id="73e9b-137">Method</span></span>     | <span data-ttu-id="73e9b-138">Описание</span><span class="sxs-lookup"><span data-stu-id="73e9b-138">Description</span></span>                                      |
|------------|--------------------------------------------------|
| <span data-ttu-id="73e9b-139">GetClassID</span><span class="sxs-lookup"><span data-stu-id="73e9b-139">GetClassID</span></span> | <span data-ttu-id="73e9b-140">Возвращает идентификатор CLSID объекта хранилища данных оболочки.</span><span class="sxs-lookup"><span data-stu-id="73e9b-140">Returns the CLSID of the Shell data store object</span></span> |



 

### <a name="ipersistfolder"></a><span data-ttu-id="73e9b-141">иперсистфолдер</span><span class="sxs-lookup"><span data-stu-id="73e9b-141">IPersistFolder</span></span>

<span data-ttu-id="73e9b-142">Интерфейс **иперсистфолдер** используется для инициализации объектов папки оболочки.</span><span class="sxs-lookup"><span data-stu-id="73e9b-142">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="73e9b-143">Реализация этого интерфейса, производного от **IPersist**, заключается в том, как папка сообщается, где она находится в пространстве имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="73e9b-143">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span> <span data-ttu-id="73e9b-144">Этот интерфейс не используется напрямую.</span><span class="sxs-lookup"><span data-stu-id="73e9b-144">You do not use this interface directly.</span></span> <span data-ttu-id="73e9b-145">Он используется реализацией файловой системы [метода ишеллфолдер:: биндтубжект](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) при инициализации объекта папки оболочки.</span><span class="sxs-lookup"><span data-stu-id="73e9b-145">It is used by the file system implementation of [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) when it initializes a Shell folder object.</span></span>



| <span data-ttu-id="73e9b-146">Метод</span><span class="sxs-lookup"><span data-stu-id="73e9b-146">Method</span></span>     | <span data-ttu-id="73e9b-147">Описание</span><span class="sxs-lookup"><span data-stu-id="73e9b-147">Description</span></span>                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e9b-148">Инициализация</span><span class="sxs-lookup"><span data-stu-id="73e9b-148">Initialize</span></span> | <span data-ttu-id="73e9b-149">Указывает объекту папки оболочки инициализировать себя на основе переданных и возвратов \_ ОК</span><span class="sxs-lookup"><span data-stu-id="73e9b-149">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

### <a name="ishellfolder"></a><span data-ttu-id="73e9b-150">ишеллфолдер</span><span class="sxs-lookup"><span data-stu-id="73e9b-150">IShellFolder</span></span>

<span data-ttu-id="73e9b-151">Интерфейс [ишеллфолдер](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) используется для управления папками, а частичная реализация необходима, чтобы интерфейсы значков и контекста, реализованные для обработчика протокола, были корректно работать в пользовательском интерфейсе Windows Search Results.</span><span class="sxs-lookup"><span data-stu-id="73e9b-151">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Search results user interface.</span></span> <span data-ttu-id="73e9b-152">Большинство необходимых функциональных возможностей предоставляется с помощью метода **жетуиобжектоф** .</span><span class="sxs-lookup"><span data-stu-id="73e9b-152">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="73e9b-153">Этот метод позволяет надстройке запрашивать интерфейсы **иекстрактикон** и **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="73e9b-153">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="73e9b-154">Интерфейс [ишеллфолдер](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) использует PIDL вместо URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="73e9b-154">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="73e9b-155">В отличие от требований к полному хранилищу данных оболочки, надстройки могут использовать простую структуру IDL, содержащую только URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="73e9b-155">In contrast to the requirements of a complete Shell data store, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="73e9b-156">Должны быть реализованы следующие методы [интерфейса ишеллфолдер](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="73e9b-156">The following methods of [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) must be implemented.</span></span> <span data-ttu-id="73e9b-157">Для пяти этих методов требуется минимальная реализация.</span><span class="sxs-lookup"><span data-stu-id="73e9b-157">Five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="73e9b-158">Метод</span><span class="sxs-lookup"><span data-stu-id="73e9b-158">Method</span></span>           | <span data-ttu-id="73e9b-159">Описание</span><span class="sxs-lookup"><span data-stu-id="73e9b-159">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e9b-160">биндтубжект</span><span class="sxs-lookup"><span data-stu-id="73e9b-160">BindToObject</span></span>     | <span data-ttu-id="73e9b-161">Возвращает E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="73e9b-161">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="73e9b-162">биндтостораже</span><span class="sxs-lookup"><span data-stu-id="73e9b-162">BindToStorage</span></span>    | <span data-ttu-id="73e9b-163">Возвращает E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="73e9b-163">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="73e9b-164">креатевиевобжект</span><span class="sxs-lookup"><span data-stu-id="73e9b-164">CreateViewObject</span></span> | <span data-ttu-id="73e9b-165">Возвращает E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="73e9b-165">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="73e9b-166">сетнамеоф</span><span class="sxs-lookup"><span data-stu-id="73e9b-166">SetNameOf</span></span>        | <span data-ttu-id="73e9b-167">Возвращает E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="73e9b-167">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="73e9b-168">парседисплайнаме</span><span class="sxs-lookup"><span data-stu-id="73e9b-168">ParseDisplayName</span></span> | <span data-ttu-id="73e9b-169">Преобразует URL-адрес в структуру ПИДЛ</span><span class="sxs-lookup"><span data-stu-id="73e9b-169">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="73e9b-170">компареидс</span><span class="sxs-lookup"><span data-stu-id="73e9b-170">CompareIDs</span></span>       | <span data-ttu-id="73e9b-171">Сравнивает два значения ПИДЛ</span><span class="sxs-lookup"><span data-stu-id="73e9b-171">Compares two PIDL values</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="73e9b-172">жетдисплайнамеоф</span><span class="sxs-lookup"><span data-stu-id="73e9b-172">GetDisplayNameOf</span></span> | <span data-ttu-id="73e9b-173">Возвращает URL-адрес для ПИДЛ</span><span class="sxs-lookup"><span data-stu-id="73e9b-173">Returns the URL for a PIDL</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="73e9b-174">жетуиобжектоф</span><span class="sxs-lookup"><span data-stu-id="73e9b-174">GetUIObjectOf</span></span>    | <span data-ttu-id="73e9b-175">Этот метод аналогичен [методу IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="73e9b-175">This method is similar to the [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="73e9b-176">Если запрошен значок, вызывающий объект запрашивает IID \_ иекстрактикон; если контекстное меню запрашивается, вызывающий объект запрашивает IID \_ IContextMenu</span><span class="sxs-lookup"><span data-stu-id="73e9b-176">If an icon is requested, the caller requests the IID\_IExtractIcon; if a shortcut menu is requested, the caller requests the IID\_IContextMenu</span></span> |



 

<span data-ttu-id="73e9b-177">**Ишеллфолдер** не используется для перечисления папок.</span><span class="sxs-lookup"><span data-stu-id="73e9b-177">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="73e9b-178">Это означает, что отображаемое имя папки будет физическим URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="73e9b-178">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="73e9b-179">Это может измениться в будущем.</span><span class="sxs-lookup"><span data-stu-id="73e9b-179">This may change in the future.</span></span>

### <a name="icontextmenu"></a><span data-ttu-id="73e9b-180">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="73e9b-180">IContextMenu</span></span>

<span data-ttu-id="73e9b-181">Когда Windows Search отображает результаты для пользователя, пользователь может щелкнуть правой кнопкой мыши элемент и увидеть контекстное меню, определенное интерфейсом **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="73e9b-181">When Windows Search displays results to the user, the user can right-click an item and see a shortcut menu defined by your **IContextMenu** interface.</span></span> <span data-ttu-id="73e9b-182">Контекстные меню также называются контекстными меню.</span><span class="sxs-lookup"><span data-stu-id="73e9b-182">Shortcut menus are also known as context menus.</span></span>

<span data-ttu-id="73e9b-183">Действие по умолчанию в контекстном меню — это то же действие, которое предпринимается при двойном щелчке элемента.</span><span class="sxs-lookup"><span data-stu-id="73e9b-183">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="73e9b-184">При отсутствии соответствующих интерфейсов **ишеллфолдер** или **IContextMenu** для элемента поведение по умолчанию для события двойного щелчка заключается в передаче URL-адреса в качестве аргумента функции [функции ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="73e9b-184">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the [ShellExecute Function](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function.</span></span>

<span data-ttu-id="73e9b-185">Дополнительные сведения о создании обработчиков контекстного меню см. в разделе Создание обработчиков [контекстного меню](../shell/context-menu-handlers.md) , а [Пример: расширения оболочки для обработчиков протоколов](-search-3x-wds-ph-ui-samplecode.md) для образца кода.</span><span class="sxs-lookup"><span data-stu-id="73e9b-185">Refer to [Creating Context Menu Handlers](../shell/context-menu-handlers.md) for more information on creating shortcut menu handlers, and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="iextracticon"></a><span data-ttu-id="73e9b-186">иекстрактикон</span><span class="sxs-lookup"><span data-stu-id="73e9b-186">IExtractIcon</span></span>

<span data-ttu-id="73e9b-187">**Иекстрактикон** извлекает значок пользовательского интерфейса службы поиска Windows на основе URL-адреса в Пидл, предоставленного обработчиком протокола.</span><span class="sxs-lookup"><span data-stu-id="73e9b-187">**IExtractIcon** retrieves an icon for the Windows Search user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

<span data-ttu-id="73e9b-188">Дополнительные сведения о создании обработчиков значков и примеров см. в разделе [Создание](../shell/how-to-create-icon-handlers.md) обработчиков значков для [обработчиков протокола](-search-3x-wds-ph-ui-samplecode.md) для образца кода.</span><span class="sxs-lookup"><span data-stu-id="73e9b-188">Refer to [Creating Icon Handlers](../shell/how-to-create-icon-handlers.md) for more information on creating icon handlers and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="ipreviewhandler"></a><span data-ttu-id="73e9b-189">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="73e9b-189">IPreviewHandler</span></span>

<span data-ttu-id="73e9b-190">[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) отображает расширенный предварительный просмотр выбранного элемента в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="73e9b-190">The [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) renders a rich preview of a selected item in Windows Explorer.</span></span> <span data-ttu-id="73e9b-191">Предварительные версии доступны в Windows Search 4,0 или в Windows Vista с Windows Desktop Search 3. x.</span><span class="sxs-lookup"><span data-stu-id="73e9b-191">Previews are available in Windows Search 4.0, or in Windows Vista with Windows Desktop Search 3.x.</span></span>

<span data-ttu-id="73e9b-192">Чтобы создать пользовательский обработчик просмотра, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="73e9b-192">To create a custom preview handler:</span></span>

1.  <span data-ttu-id="73e9b-193">Реализуйте [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) , который принимает [IStream](/windows/win32/api/objidl/nn-objidl-istream), следуя рекомендациям, предоставленным в [обработчиках просмотра](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="73e9b-193">Implement an [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) that takes an [IStream](/windows/win32/api/objidl/nn-objidl-istream), following the guidelines provided in [Preview Handlers](../shell/preview-handlers.md).</span></span>
2.  <span data-ttu-id="73e9b-194">Зарегистрируйте обработчик просмотра:</span><span class="sxs-lookup"><span data-stu-id="73e9b-194">Register your preview handler:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  <span data-ttu-id="73e9b-195">Выполните следующие два действия, чтобы реализовать папку оболочки для URL-адреса:</span><span class="sxs-lookup"><span data-stu-id="73e9b-195">Complete the following two steps to implement a Shell folder for your URL:</span></span>
    1.  <span data-ttu-id="73e9b-196">В [методе ишеллфолдер:: жетуиобжектоф](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof)обработайте [икуеряссоЦиатионс](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) и верните свое сопоставление для элементов оболочки, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="73e9b-196">In [IShellFolder::GetUIObjectOf Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), handle [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) and return your association for your Shell items, as shown in the following code sample.</span></span>

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  <span data-ttu-id="73e9b-197">После того как оболочка запросит папку оболочки для потока данных для инициализации обработчика просмотра, перейдите к методу [метода ишеллфолдер:: биндтубжект](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) , обработайте IID \_ IStream и верните в URL-адрес [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="73e9b-197">After the Shell queries your Shell folder for the data stream to initialize the preview handler, go to your [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) method, handle IID\_IStream and return an [IStream](/windows/win32/api/objidl/nn-objidl-istream) to your URL.</span></span>

<span data-ttu-id="73e9b-198">Чтобы повторно использовать существующий обработчик просмотра для типа файлов, выполните следующие два действия.</span><span class="sxs-lookup"><span data-stu-id="73e9b-198">To reuse an existing preview handler for your file type, follow these two steps:</span></span>

1.  <span data-ttu-id="73e9b-199">Зарегистрируйте этот обработчик просмотра для своего типа файлов, используя идентификатор CLSID существующего обработчика просмотра вместо <\_ \_> PreviewHandler GUID.</span><span class="sxs-lookup"><span data-stu-id="73e9b-199">Register that preview handler for your file type using the CLSID of the existing preview handler in place of <Your\_PreviewHandler\_GUID>.</span></span>
2.  <span data-ttu-id="73e9b-200">Реализуйте папку оболочки.</span><span class="sxs-lookup"><span data-stu-id="73e9b-200">Implement a Shell folder.</span></span>

<span data-ttu-id="73e9b-201">Дополнительные сведения о создании обработчиков просмотра см. в разделе [обработчики](../shell/preview-handlers.md) [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) и Preview.</span><span class="sxs-lookup"><span data-stu-id="73e9b-201">For more information on creating preview handlers, see [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73e9b-202">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="73e9b-202">Additional Resources</span></span>

-   <span data-ttu-id="73e9b-203">Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="73e9b-203">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="73e9b-204">Сведения о создании обработчиков см. в статьях [Регистрация расширений оболочки](../shell/reg-shell-exts.md), [Создание обработчиков расширений оболочки](../shell/handlers.md), [контекстное меню](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [расширения пространства имен оболочки](../shell/nse-works.md) и [обработчики просмотра](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="73e9b-204">For information about creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [Shell Namespace Extensions](../shell/nse-works.md) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="73e9b-205">См. также</span><span class="sxs-lookup"><span data-stu-id="73e9b-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="73e9b-206">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="73e9b-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="73e9b-207">Разработка обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="73e9b-207">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="73e9b-208">Основные сведения о обработчиках протоколов</span><span class="sxs-lookup"><span data-stu-id="73e9b-208">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="73e9b-209">Уведомление индекса изменений</span><span class="sxs-lookup"><span data-stu-id="73e9b-209">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="73e9b-210">Пример кода: расширения оболочки для обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="73e9b-210">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="73e9b-211">Установка и регистрация обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="73e9b-211">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="73e9b-212">Создание соединителя поиска для обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="73e9b-212">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="73e9b-213">Обработчики протокола отладки</span><span class="sxs-lookup"><span data-stu-id="73e9b-213">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
