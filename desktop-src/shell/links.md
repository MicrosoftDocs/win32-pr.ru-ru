---
description: Ссылка на оболочку — это объект данных, который содержит сведения, используемые для доступа к другому объекту в пространстве имен оболочки&\# 8212, то есть любой объект, видимый в проводнике Windows.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Ссылки оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327bcb425f998bcc2a4c0714118d4461ded253ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265089"
---
# <a name="shell-links"></a><span data-ttu-id="5529e-103">Ссылки оболочки</span><span class="sxs-lookup"><span data-stu-id="5529e-103">Shell Links</span></span>

<span data-ttu-id="5529e-104">*Ссылка на оболочку* — это объект данных, который содержит сведения, используемые для доступа к другому объекту в пространстве имен оболочки, т. е. любой объект, видимый в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="5529e-104">A *Shell link* is a data object that contains information used to access another object in the Shell's namespace—that is, any object visible through Windows Explorer.</span></span> <span data-ttu-id="5529e-105">К типам объектов, к которым можно получить доступ через ссылки оболочки, относятся файлы, папки, диски и принтеры.</span><span class="sxs-lookup"><span data-stu-id="5529e-105">The types of objects that can be accessed through Shell links include files, folders, disk drives, and printers.</span></span> <span data-ttu-id="5529e-106">Ссылка на оболочку позволяет пользователю или приложению получить доступ к объекту из любого места в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5529e-106">A Shell link allows a user or an application to access an object from anywhere in the namespace.</span></span> <span data-ttu-id="5529e-107">Пользователю или приложению не нужно знать текущее имя и расположение объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-107">The user or application does not need to know the current name and location of the object.</span></span>

-   [<span data-ttu-id="5529e-108">О связях оболочки</span><span class="sxs-lookup"><span data-stu-id="5529e-108">About Shell Links</span></span>](#about-shell-links)
    -   [<span data-ttu-id="5529e-109">Разрешение ссылок</span><span class="sxs-lookup"><span data-stu-id="5529e-109">Link Resolution</span></span>](#link-resolution)
    -   [<span data-ttu-id="5529e-110">Файлы ссылок</span><span class="sxs-lookup"><span data-stu-id="5529e-110">Link Files</span></span>](#link-files)
    -   [<span data-ttu-id="5529e-111">Идентификаторы элементов и списки идентификаторов</span><span class="sxs-lookup"><span data-stu-id="5529e-111">Item Identifiers and Identifier Lists</span></span>](#item-identifiers-and-identifier-lists)
-   [<span data-ttu-id="5529e-112">Использование ссылок оболочки</span><span class="sxs-lookup"><span data-stu-id="5529e-112">Using Shell Links</span></span>](#using-shell-links)
    -   [<span data-ttu-id="5529e-113">Создание ярлыка и ярлыка папки для файла</span><span class="sxs-lookup"><span data-stu-id="5529e-113">Creating a Shortcut and a Folder Shortcut to a File</span></span>](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [<span data-ttu-id="5529e-114">Разрешение ярлыка</span><span class="sxs-lookup"><span data-stu-id="5529e-114">Resolving a Shortcut</span></span>](#resolving-a-shortcut)
    -   [<span data-ttu-id="5529e-115">Создание ярлыка для нефайлового объекта</span><span class="sxs-lookup"><span data-stu-id="5529e-115">Creating a Shortcut to a Nonfile Object</span></span>](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a><span data-ttu-id="5529e-116">О связях оболочки</span><span class="sxs-lookup"><span data-stu-id="5529e-116">About Shell Links</span></span>

<span data-ttu-id="5529e-117">Пользователь создает ссылку на оболочку, выбрав команду **создать ярлык** в контекстном меню объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-117">The user creates a Shell link by choosing the **Create Shortcut** command from an object's shortcut menu.</span></span> <span data-ttu-id="5529e-118">Система автоматически создает значок для связи с оболочкой, комбинируя значок объекта с маленькой стрелкой (называемой системным значком перекрытия ссылок), который отображается в левом нижнем углу значка.</span><span class="sxs-lookup"><span data-stu-id="5529e-118">The system automatically creates an icon for the Shell link by combining the object's icon with a small arrow (known as the system-defined link overlay icon) that appears in the lower left corner of the icon.</span></span> <span data-ttu-id="5529e-119">Ссылка на оболочку, имеющую значок, называется ярлыком; Однако термины «ссылка» и «ярлык оболочки» часто используются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="5529e-119">A Shell link that has an icon is called a shortcut; however, the terms Shell link and shortcut are often used interchangeably.</span></span> <span data-ttu-id="5529e-120">Как правило, пользователь создает ярлыки для быстрого доступа к объектам, хранящимся во вложенных папках или в общих папках на других компьютерах.</span><span class="sxs-lookup"><span data-stu-id="5529e-120">Typically, the user creates shortcuts to gain quick access to objects stored in subfolders or in shared folders on other computers.</span></span> <span data-ttu-id="5529e-121">Например, пользователь может создать ярлык для документа Microsoft Word, который находится во вложенной папке, и поместить значок ярлыка на Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="5529e-121">For example, a user can create a shortcut to a Microsoft Word document that is located in a subfolder and place the shortcut icon on the desktop.</span></span> <span data-ttu-id="5529e-122">Затем пользователь может открыть документ, дважды щелкнув значок ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-122">The user can then open the document by double-clicking the shortcut icon.</span></span> <span data-ttu-id="5529e-123">Если документ перемещается или переименовывается после создания ярлыка, система попытается обновить ярлык при следующем выборе пользователем.</span><span class="sxs-lookup"><span data-stu-id="5529e-123">If the document is moved or renamed after the shortcut is created, the system will attempt to update the shortcut the next time the user selects it.</span></span>

<span data-ttu-id="5529e-124">Приложения также могут создавать и использовать ссылки и ярлыки оболочки.</span><span class="sxs-lookup"><span data-stu-id="5529e-124">Applications can also create and use Shell links and shortcuts.</span></span> <span data-ttu-id="5529e-125">Например, приложение для обработки текста может создать ссылку оболочки для реализации списка недавно использовавшихся документов.</span><span class="sxs-lookup"><span data-stu-id="5529e-125">For example, a word processing application might create a Shell link to implement a list of the most recently used documents.</span></span> <span data-ttu-id="5529e-126">Приложение создает ссылку оболочки с помощью интерфейса [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) для создания объекта связи оболочки.</span><span class="sxs-lookup"><span data-stu-id="5529e-126">An application creates a Shell link by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface to create a Shell link object.</span></span> <span data-ttu-id="5529e-127">Приложение использует интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) или [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) для хранения объекта в файле или потоке.</span><span class="sxs-lookup"><span data-stu-id="5529e-127">The application uses the [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to store the object in a file or stream.</span></span>

> [!Note]  
> <span data-ttu-id="5529e-128">Нельзя использовать [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) для создания ссылки на URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5529e-128">You cannot use [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) to create a link to a URL.</span></span>

 

<span data-ttu-id="5529e-129">В этом обзоре описывается интерфейс [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) и объясняется, как с его помощью создавать и разрешать ссылки оболочки из приложения на основе Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="5529e-129">This overview describes the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface and explains how to use it to create and resolve Shell links from within a Microsoft Win32-based application.</span></span> <span data-ttu-id="5529e-130">Так как структура ссылок оболочки основана на модели COM, необходимо ознакомиться с основными понятиями программирования COM и OLE перед чтением этого обзора.</span><span class="sxs-lookup"><span data-stu-id="5529e-130">Because the design of Shell links is based on the OLE Component Object Model (COM), you should be familiar with the basic concepts of COM and OLE programming before reading this overview.</span></span>

### <a name="link-resolution"></a><span data-ttu-id="5529e-131">Разрешение ссылок</span><span class="sxs-lookup"><span data-stu-id="5529e-131">Link Resolution</span></span>

<span data-ttu-id="5529e-132">Если пользователь создает ярлык для объекта, а имя или расположение объекта позднее изменилось, система автоматически выполняет шаги по обновлению или разрешению, если при следующем выборе пользователя он будет выполнен в следующий раз.</span><span class="sxs-lookup"><span data-stu-id="5529e-132">If a user creates a shortcut to an object and the name or location of the object is later changed, the system automatically takes steps to update, or resolve, the shortcut the next time the user selects it.</span></span> <span data-ttu-id="5529e-133">Однако если приложение создает ссылку оболочки и сохраняет ее в потоке, система не пытается автоматически разрешить эту ссылку.</span><span class="sxs-lookup"><span data-stu-id="5529e-133">However, if an application creates a Shell link and stores it in a stream, the system does not automatically attempt to resolve the link.</span></span> <span data-ttu-id="5529e-134">Приложение должно разрешить ссылку, вызвав метод [**ишелллинк:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) .</span><span class="sxs-lookup"><span data-stu-id="5529e-134">The application must resolve the link by calling the [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) method.</span></span>

<span data-ttu-id="5529e-135">При создании ссылки на оболочку система сохраняет сведения о ссылке.</span><span class="sxs-lookup"><span data-stu-id="5529e-135">When a Shell link is created, the system saves information about the link.</span></span> <span data-ttu-id="5529e-136">При разрешении ссылки — либо автоматически, либо с помощью вызова [**ишелллинк:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) — система сначала извлекает путь, связанный со ссылкой оболочки, используя указатель на список идентификаторов для ссылки оболочки.</span><span class="sxs-lookup"><span data-stu-id="5529e-136">When resolving a link—either automatically or with an [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) call—the system first retrieves the path associated with the Shell link by using a pointer to the Shell link's identifier list.</span></span> <span data-ttu-id="5529e-137">Дополнительные сведения о списке идентификаторов см. в разделе [идентификаторы элементов и списки идентификаторов](#item-identifiers-and-identifier-lists).</span><span class="sxs-lookup"><span data-stu-id="5529e-137">For more information about the identifier list, see [Item Identifiers and Identifier Lists](#item-identifiers-and-identifier-lists).</span></span> <span data-ttu-id="5529e-138">Система выполняет поиск связанного объекта в этом пути и, если находит объект, разрешает ссылку.</span><span class="sxs-lookup"><span data-stu-id="5529e-138">The system searches for the associated object in that path and, if it finds the object, resolves the link.</span></span> <span data-ttu-id="5529e-139">Если система не может найти объект, то она вызывается в [службе DLT,](../fileio/distributed-link-tracking-and-object-identifiers.md) если она доступна, чтобы найти объект.</span><span class="sxs-lookup"><span data-stu-id="5529e-139">If the system cannot find the object, it calls on the [Distributed Link Tracking and Object Identifiers](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT) service, if available, to locate the object.</span></span> <span data-ttu-id="5529e-140">Если служба DLT недоступна или не может найти объект, система ищет в одном каталоге объект с тем же временем создания файла и атрибутами, но с другим именем.</span><span class="sxs-lookup"><span data-stu-id="5529e-140">If the DLT service is not available or cannot find the object, the system looks in the same directory for an object with the same file creation time and attributes but with a different name.</span></span> <span data-ttu-id="5529e-141">Этот тип поиска разрешает ссылку на объект, который был переименован.</span><span class="sxs-lookup"><span data-stu-id="5529e-141">This type of search resolves a link to an object that has been renamed.</span></span>

<span data-ttu-id="5529e-142">Если система по-прежнему не может найти объект, она выполняет поиск по каталогам, рабочему столу и локальным томам, выполняя рекурсивный просмотр дерева каталогов для объекта с тем же именем или временем создания.</span><span class="sxs-lookup"><span data-stu-id="5529e-142">If the system still cannot find the object, it searches the directories, the desktop, and local volumes, looking recursively though the directory tree for an object with either the same name or creation time.</span></span> <span data-ttu-id="5529e-143">Если система по-прежнему не находит совпадения, отображается диалоговое окно с запросом на ввод расположения.</span><span class="sxs-lookup"><span data-stu-id="5529e-143">If the system still does not find a match, it displays a dialog box prompting the user for a location.</span></span> <span data-ttu-id="5529e-144">Приложение может подавлять диалоговое окно, указывая значение **однообъективных зеркальных \_ без \_ пользовательского интерфейса** в вызове [**ишелллинк:: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span><span class="sxs-lookup"><span data-stu-id="5529e-144">An application can suppress the dialog box by specifying the **SLR\_NO\_UI** value in a call to [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span>

### <a name="initialization-of-the-component-object-library"></a><span data-ttu-id="5529e-145">Инициализация библиотеки объектов компонентов</span><span class="sxs-lookup"><span data-stu-id="5529e-145">Initialization of the Component Object Library</span></span>

<span data-ttu-id="5529e-146">Прежде чем приложение сможет создавать и разрешать ярлыки, оно должно инициализировать библиотеку объектов компонентов, вызвав функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) .</span><span class="sxs-lookup"><span data-stu-id="5529e-146">Before an application can create and resolve shortcuts, it must initialize the component object library by calling the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function.</span></span> <span data-ttu-id="5529e-147">Для каждого вызова **CoInitialize** требуется соответствующий вызов функции [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , которую приложение должно вызывать при завершении.</span><span class="sxs-lookup"><span data-stu-id="5529e-147">Each call to **CoInitialize** requires a corresponding call to the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function, which an application should call when it terminates.</span></span> <span data-ttu-id="5529e-148">Вызов **CoUninitialize** гарантирует, что приложение не завершит работу до получения всех его ожидающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="5529e-148">The call to **CoUninitialize** ensures that the application does not terminate until it has received all of its pending messages.</span></span>

### <a name="location-independent-names"></a><span data-ttu-id="5529e-149">Имена Location-Independent</span><span class="sxs-lookup"><span data-stu-id="5529e-149">Location-Independent Names</span></span>

<span data-ttu-id="5529e-150">Система предоставляет независимые от расположения имена для ссылок оболочки на объекты, хранящиеся в общих папках.</span><span class="sxs-lookup"><span data-stu-id="5529e-150">The system provides location-independent names for Shell links to objects stored in shared folders.</span></span> <span data-ttu-id="5529e-151">Если объект хранится локально, система предоставляет локальный путь и имя файла для объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-151">If the object is stored locally, the system provides the local path and file name for the object.</span></span> <span data-ttu-id="5529e-152">Если объект хранится удаленно, система предоставляет имя сетевого ресурса в формате UNC для объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-152">If the object is stored remotely, the system provides a Universal Naming Convention (UNC) network resource name for the object.</span></span> <span data-ttu-id="5529e-153">Так как система предоставляет имена, независимые от расположения, ссылка на оболочку может служить универсальным именем для файла, который можно передать на другие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="5529e-153">Because the system provides location-independent names, a Shell link can serve as a universal name for a file that can be transferred to other computers.</span></span>

### <a name="link-files"></a><span data-ttu-id="5529e-154">Файлы ссылок</span><span class="sxs-lookup"><span data-stu-id="5529e-154">Link Files</span></span>

<span data-ttu-id="5529e-155">Когда пользователь создает ярлык для объекта, выбрав команду **создать ярлык** в контекстном меню объекта, Windows хранит сведения, необходимые для доступа к объекту в файле ссылки — двоичный файл с расширением LNK.</span><span class="sxs-lookup"><span data-stu-id="5529e-155">When the user creates a shortcut to an object by choosing the **Create Shortcut** command from the object's shortcut menu, Windows stores the information it needs to access the object in a link file—a binary file that has the .lnk file name extension.</span></span> <span data-ttu-id="5529e-156">Файл ссылки содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="5529e-156">A link file contains the following information:</span></span>

-   <span data-ttu-id="5529e-157">Расположение (путь) объекта, на который ссылается ярлык (этот объект называется соответствующим объектом).</span><span class="sxs-lookup"><span data-stu-id="5529e-157">The location (path) of the object referenced by the shortcut (called the corresponding object).</span></span>
-   <span data-ttu-id="5529e-158">Рабочий каталог соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-158">The working directory of the corresponding object.</span></span>
-   <span data-ttu-id="5529e-159">Список аргументов, передаваемых системой соответствующему объекту при активации метода [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) для ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-159">The list of arguments that the system passes to the corresponding object when the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method is activated for the shortcut.</span></span>
-   <span data-ttu-id="5529e-160">Команда отображения, используемая для задания начального состояния отображения соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-160">The show command used to set the initial show state of the corresponding object.</span></span> <span data-ttu-id="5529e-161">Это одно из значений SW, \_ описанных в разделе [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).</span><span class="sxs-lookup"><span data-stu-id="5529e-161">This is one of the SW\_ values described in [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).</span></span>
-   <span data-ttu-id="5529e-162">Расположение (путь и индекс) значка ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-162">The location (path and index) of the shortcut's icon.</span></span>
-   <span data-ttu-id="5529e-163">Строка описания ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-163">The shortcut's description string.</span></span>
-   <span data-ttu-id="5529e-164">Сочетание клавиш для ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-164">The keyboard shortcut for the shortcut.</span></span>

<span data-ttu-id="5529e-165">При удалении файла ссылки соответствующий объект не изменяется.</span><span class="sxs-lookup"><span data-stu-id="5529e-165">When a link file is deleted, the corresponding object is not affected.</span></span>

<span data-ttu-id="5529e-166">При создании ярлыка для другого ярлыка система просто копирует файл ссылки, а не создает новый файл ссылки.</span><span class="sxs-lookup"><span data-stu-id="5529e-166">If you create a shortcut to another shortcut, the system simply copies the link file rather than creating a new link file.</span></span> <span data-ttu-id="5529e-167">В этом случае сочетания клавиш не будут зависеть друг от друга.</span><span class="sxs-lookup"><span data-stu-id="5529e-167">In this case, the shortcuts will not be independent of each other.</span></span>

<span data-ttu-id="5529e-168">Приложение может зарегистрировать расширение имени файла в качестве типа файла ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-168">An application can register a file name extension as a shortcut file type.</span></span> <span data-ttu-id="5529e-169">Если файл имеет расширение, зарегистрированное в качестве типа файла ярлыка, система автоматически добавляет к значку файла значок перекрытия ссылок, определенный системой (маленькая стрелка).</span><span class="sxs-lookup"><span data-stu-id="5529e-169">If a file has a file name extension that has been registered as a shortcut file type, the system automatically adds the system-defined link overlay icon (a small arrow) to the file's icon.</span></span> <span data-ttu-id="5529e-170">Чтобы зарегистрировать расширение имени файла в качестве типа ярлыка, необходимо добавить значение в реестре для расширения имени файла, как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="5529e-170">To register a file name extension as a shortcut file type, you must add the IsShortcut value to the registry description of the file name extension, as shown in the example below.</span></span> <span data-ttu-id="5529e-171">Обратите внимание, что оболочку необходимо перезапустить, чтобы значок оверлея вступил в силу.</span><span class="sxs-lookup"><span data-stu-id="5529e-171">Note that the Shell must be restarted for the overlay icon to take effect.</span></span> <span data-ttu-id="5529e-172">У "a" нет значения данных.</span><span class="sxs-lookup"><span data-stu-id="5529e-172">IsShortcut has no data value.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a><span data-ttu-id="5529e-173">Имена ярлыков</span><span class="sxs-lookup"><span data-stu-id="5529e-173">Shortcut names</span></span>

<span data-ttu-id="5529e-174">Имя ярлыка, представляющее собой строку, которая отображается под значком оболочки, фактически является именем файла самого ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-174">The shortcut's name, which is a string that appears below the Shell link icon, is actually the file name of the shortcut itself.</span></span> <span data-ttu-id="5529e-175">Пользователь может изменить строку описания, выбрав ее и введя новую строку.</span><span class="sxs-lookup"><span data-stu-id="5529e-175">The user can edit the description string by selecting it and entering a new string.</span></span>

### <a name="location-of-shortcuts-in-the-namespace"></a><span data-ttu-id="5529e-176">Расположение ярлыков в пространстве имен</span><span class="sxs-lookup"><span data-stu-id="5529e-176">Location of shortcuts in the namespace</span></span>

<span data-ttu-id="5529e-177">Ярлык может находиться на рабочем столе или в любом месте пространства имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="5529e-177">A shortcut can exist on the desktop or anywhere in the Shell's namespace.</span></span> <span data-ttu-id="5529e-178">Аналогичным образом объект, связанный с ярлыком, также может существовать в любом месте пространства имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="5529e-178">Similarly, the object that is associated with the shortcut can also exist anywhere in the Shell's namespace.</span></span> <span data-ttu-id="5529e-179">Приложение может использовать метод [**ишелллинк:: сетпас**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) , чтобы задать путь и имя файла для связанного объекта, а также метод [**ишелллинк::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) GetObject для получения текущего пути и имени файла для объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-179">An application can use the [**IShellLink::SetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) method to set the path and file name for the associated object, and the [**IShellLink::GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) method to retrieve the current path and file name for the object.</span></span>

### <a name="shortcut-working-directory"></a><span data-ttu-id="5529e-180">Ярлык рабочего каталога</span><span class="sxs-lookup"><span data-stu-id="5529e-180">Shortcut working directory</span></span>

<span data-ttu-id="5529e-181">Рабочий каталог — это каталог, в котором соответствующий объект ярлыка загружает или хранит файлы, когда пользователь не определяет конкретный каталог.</span><span class="sxs-lookup"><span data-stu-id="5529e-181">The working directory is the directory where the corresponding object of a shortcut loads or stores files when the user does not identify a specific directory.</span></span> <span data-ttu-id="5529e-182">Файл ссылки содержит имя рабочего каталога для соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-182">A link file contains the name of the working directory for the corresponding object.</span></span> <span data-ttu-id="5529e-183">Приложение может задать имя рабочего каталога для соответствующего объекта с помощью метода [**ишелллинк:: сетворкингдиректори**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) и может получить имя текущего рабочего каталога для соответствующего объекта с помощью метода [**Ишелллинк:: жетворкингдиректори**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) .</span><span class="sxs-lookup"><span data-stu-id="5529e-183">An application can set the name of the working directory for the corresponding object by using the [**IShellLink::SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) method and can retrieve the name of the current working directory for the corresponding object by using the [**IShellLink::GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) method.</span></span>

### <a name="shortcut-command-line-arguments"></a><span data-ttu-id="5529e-184">Аргументы командной строки ярлыка</span><span class="sxs-lookup"><span data-stu-id="5529e-184">Shortcut command-line arguments</span></span>

<span data-ttu-id="5529e-185">Файл ссылки содержит аргументы командной строки, которые оболочка передает в соответствующий объект, когда пользователь выбирает ссылку.</span><span class="sxs-lookup"><span data-stu-id="5529e-185">A link file contains command-line arguments that the Shell passes to the corresponding object when the user selects the link.</span></span> <span data-ttu-id="5529e-186">Приложение может задать аргументы командной строки для ярлыка с помощью метода [**ишелллинк:: сетаргументс**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) .</span><span class="sxs-lookup"><span data-stu-id="5529e-186">An application can set the command-line arguments for a shortcut by using the [**IShellLink::SetArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) method.</span></span> <span data-ttu-id="5529e-187">Можно задать аргументы командной строки, если соответствующее приложение, такое как компоновщик или компилятор, принимает специальные флаги в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="5529e-187">It is useful to set command-line arguments when the corresponding application, such as a linker or compiler, takes special flags as arguments.</span></span> <span data-ttu-id="5529e-188">Приложение может извлекать аргументы командной строки из ярлыка с помощью метода [**ишелллинк::-Arguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) .</span><span class="sxs-lookup"><span data-stu-id="5529e-188">An application can retrieve the command-line arguments from a shortcut by using the [**IShellLink::GetArguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) method.</span></span>

### <a name="shortcut-show-commands"></a><span data-ttu-id="5529e-189">Команды быстрого показа</span><span class="sxs-lookup"><span data-stu-id="5529e-189">Shortcut show commands</span></span>

<span data-ttu-id="5529e-190">Когда пользователь дважды щелкает ярлык, система запускает приложение, связанное с соответствующим объектом, и устанавливает начальное отображение состояния приложения на основе команды показ, заданной с помощью ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-190">When the user double-clicks a shortcut, the system starts the application associated with the corresponding object and sets the initial show state of the application based on the show command specified by the shortcut.</span></span> <span data-ttu-id="5529e-191">Команда отображения может иметь любое из значений SW, \_ входящих в описание функции [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="5529e-191">The show command can be any of the SW\_ values included in the description of the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span> <span data-ttu-id="5529e-192">Приложение может задать команду отображения для ярлыка с помощью метода [**ишелллинк:: сетшовкмд**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) , а также получить команду Current-шоу с помощью метода [**Ишелллинк:: жетшовкмд**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) .</span><span class="sxs-lookup"><span data-stu-id="5529e-192">An application can set the show command for a shortcut by using the [**IShellLink::SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) method and can retrieve the current show command by using the [**IShellLink::GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) method.</span></span>

### <a name="shortcut-icons"></a><span data-ttu-id="5529e-193">Значки ярлыков</span><span class="sxs-lookup"><span data-stu-id="5529e-193">Shortcut icons</span></span>

<span data-ttu-id="5529e-194">Как и другие объекты оболочки, ярлык имеет значок.</span><span class="sxs-lookup"><span data-stu-id="5529e-194">Like other Shell objects, a shortcut has an icon.</span></span> <span data-ttu-id="5529e-195">Пользователь обращается к объекту, связанному с ярлыком, дважды щелкнув значок ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-195">The user accesses the object associated with a shortcut by double-clicking the shortcut's icon.</span></span> <span data-ttu-id="5529e-196">Когда система создает значок для ярлыка, он использует точечный рисунок соответствующего объекта и добавляет в нижний левый угол значок перекрытия ссылок, определенный системой (маленькая стрелка).</span><span class="sxs-lookup"><span data-stu-id="5529e-196">When the system creates an icon for a shortcut, it uses the bitmap of the corresponding object and adds the system-defined link overlay icon (a small arrow) to the lower left corner.</span></span> <span data-ttu-id="5529e-197">Приложение может задать расположение (путь и индекс) значка ярлыка с помощью метода [**ишелллинк:: сетиконлокатион**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) .</span><span class="sxs-lookup"><span data-stu-id="5529e-197">An application can set the location (path and index) of a shortcut's icon by using the [**IShellLink::SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) method.</span></span> <span data-ttu-id="5529e-198">Приложение может извлечь это расположение с помощью метода [**ишелллинк:: жетиконлокатион**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) .</span><span class="sxs-lookup"><span data-stu-id="5529e-198">An application can retrieve this location by using the [**IShellLink::GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) method.</span></span>

### <a name="shortcut-descriptions"></a><span data-ttu-id="5529e-199">Описания ярлыков</span><span class="sxs-lookup"><span data-stu-id="5529e-199">Shortcut descriptions</span></span>

<span data-ttu-id="5529e-200">Сочетания клавиш имеют описания, но пользователь не видит их.</span><span class="sxs-lookup"><span data-stu-id="5529e-200">Shortcuts have descriptions, but the user never sees them.</span></span> <span data-ttu-id="5529e-201">Приложение может использовать описание для хранения любой текстовой информации.</span><span class="sxs-lookup"><span data-stu-id="5529e-201">An application can use a description to store any text information.</span></span> <span data-ttu-id="5529e-202">Описания задаются с помощью метода [**ишелллинк:: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) и извлекаются с помощью метода [**ишелллинк:: «Description**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) ».</span><span class="sxs-lookup"><span data-stu-id="5529e-202">Descriptions are set using the [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) method and retrieved using the [**IShellLink::GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) method.</span></span>

### <a name="shortcut-keyboard-shortcuts"></a><span data-ttu-id="5529e-203">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="5529e-203">Shortcut Keyboard Shortcuts</span></span>

<span data-ttu-id="5529e-204">С объектом ярлыка может быть связано сочетание клавиш.</span><span class="sxs-lookup"><span data-stu-id="5529e-204">A shortcut object can have a keyboard shortcut associated with it.</span></span> <span data-ttu-id="5529e-205">Сочетания клавиш позволяют пользователю нажать сочетание клавиш, чтобы активировать ярлык.</span><span class="sxs-lookup"><span data-stu-id="5529e-205">Keyboard shortcuts allow a user to press a combination of keys to activate a shortcut.</span></span> <span data-ttu-id="5529e-206">Приложение может задать сочетание клавиш для ярлыка с помощью метода [**ишелллинк:: сесоткэй**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) и может получить текущее сочетание клавиш с помощью метода [**ишелллинк::-горячих**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) .</span><span class="sxs-lookup"><span data-stu-id="5529e-206">An application can set the keyboard shortcut for a shortcut by using the [**IShellLink::SetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) method and can retrieve the current keyboard shortcut by using the [**IShellLink::GetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) method.</span></span>

### <a name="item-identifiers-and-identifier-lists"></a><span data-ttu-id="5529e-207">Идентификаторы элементов и списки идентификаторов</span><span class="sxs-lookup"><span data-stu-id="5529e-207">Item Identifiers and Identifier Lists</span></span>

<span data-ttu-id="5529e-208">Оболочка использует идентификаторы объектов в пространстве имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="5529e-208">The Shell uses object identifiers within the Shell's namespace.</span></span> <span data-ttu-id="5529e-209">Все объекты, видимые в оболочке (файлы, каталоги, серверы, рабочие группы и т. д.), имеют уникальные идентификаторы между объектами в их родительской папке.</span><span class="sxs-lookup"><span data-stu-id="5529e-209">All objects visible in the Shell (files, directories, servers, workgroups, and so on) have unique identifiers among the objects within their parent folder.</span></span> <span data-ttu-id="5529e-210">Эти идентификаторы называются идентификаторами элементов и имеют тип данных [**шитемид**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , как определено в файле заголовка штипес. h.</span><span class="sxs-lookup"><span data-stu-id="5529e-210">These identifiers are called item identifiers, and they have the [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) data type as defined in the Shtypes.h header file.</span></span> <span data-ttu-id="5529e-211">Идентификатор элемента — это байтовый поток переменной длины, который содержит сведения, определяющие объект в папке.</span><span class="sxs-lookup"><span data-stu-id="5529e-211">An item identifier is a variable-length byte stream that contains information that identifies an object within a folder.</span></span> <span data-ttu-id="5529e-212">Только создатель идентификатора элемента знает содержимое и формат идентификатора.</span><span class="sxs-lookup"><span data-stu-id="5529e-212">Only the creator of an item identifier knows the content and format of the identifier.</span></span> <span data-ttu-id="5529e-213">Единственная часть идентификатора элемента, используемая оболочкой, — первые два байта, которые указывают размер идентификатора.</span><span class="sxs-lookup"><span data-stu-id="5529e-213">The only part of an item identifier that the Shell uses is the first two bytes, which specify the size of the identifier.</span></span>

<span data-ttu-id="5529e-214">Каждая родительская папка имеет собственный идентификатор элемента, который идентифицирует его в собственной родительской папке.</span><span class="sxs-lookup"><span data-stu-id="5529e-214">Each parent folder has its own item identifier that identifies it within its own parent folder.</span></span> <span data-ttu-id="5529e-215">Таким образом, любой объект оболочки может быть однозначно идентифицирован списком идентификаторов элементов.</span><span class="sxs-lookup"><span data-stu-id="5529e-215">Thus, any Shell object can be uniquely identified by a list of item identifiers.</span></span> <span data-ttu-id="5529e-216">В родительской папке хранится список идентификаторов элементов, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="5529e-216">A parent folder keeps a list of identifiers for the items it contains.</span></span> <span data-ttu-id="5529e-217">Список имеет тип данных [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) .</span><span class="sxs-lookup"><span data-stu-id="5529e-217">The list has the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) data type.</span></span> <span data-ttu-id="5529e-218">Списки идентификаторов элементов выделяются оболочкой и могут передаваться через интерфейсы оболочки, такие как [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).</span><span class="sxs-lookup"><span data-stu-id="5529e-218">Item identifier lists are allocated by the Shell and may be passed across Shell interfaces, such as [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).</span></span> <span data-ttu-id="5529e-219">Важно помнить, что каждый идентификатор в списке идентификаторов элементов имеет смысл только в контексте родительской папки.</span><span class="sxs-lookup"><span data-stu-id="5529e-219">It is important to remember that each identifier in an item identifier list is only meaningful within the context of its parent folder.</span></span>

<span data-ttu-id="5529e-220">Приложение может задать список идентификаторов элементов ярлыка с помощью метода [**ишелллинк:: сетидлист**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) .</span><span class="sxs-lookup"><span data-stu-id="5529e-220">An application can set a shortcut's item identifier list by using the [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) method.</span></span> <span data-ttu-id="5529e-221">Этот метод полезен при задании ярлыка для объекта, который не является файлом, например принтером или диском.</span><span class="sxs-lookup"><span data-stu-id="5529e-221">This method is useful when setting a shortcut to an object that is not a file, such as a printer or disk drive.</span></span> <span data-ttu-id="5529e-222">Приложение может получить список идентификаторов элементов ярлыка с помощью метода [**ишелллинк:: жетидлист**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) .</span><span class="sxs-lookup"><span data-stu-id="5529e-222">An application can retrieve a shortcut's item identifier list by using the [**IShellLink::GetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) method.</span></span>

## <a name="using-shell-links"></a><span data-ttu-id="5529e-223">Использование ссылок оболочки</span><span class="sxs-lookup"><span data-stu-id="5529e-223">Using Shell Links</span></span>

<span data-ttu-id="5529e-224">В этом разделе содержатся примеры, демонстрирующие создание и разрешение ярлыков в приложениях на основе Win32.</span><span class="sxs-lookup"><span data-stu-id="5529e-224">This section contains examples that demonstrate how to create and resolve shortcuts from within a Win32-based application.</span></span> <span data-ttu-id="5529e-225">В этом разделе предполагается, что вы знакомы с программированием Win32, C++ и OLE COM.</span><span class="sxs-lookup"><span data-stu-id="5529e-225">This section assumes you are familiar with Win32, C++, and OLE COM programming.</span></span>

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a><span data-ttu-id="5529e-226">Создание ярлыка и ярлыка папки для файла</span><span class="sxs-lookup"><span data-stu-id="5529e-226">Creating a Shortcut and a Folder Shortcut to a File</span></span>

<span data-ttu-id="5529e-227">Пример функции Креателинк в следующем примере создает ярлык.</span><span class="sxs-lookup"><span data-stu-id="5529e-227">The CreateLink sample function in the following example creates a shortcut.</span></span> <span data-ttu-id="5529e-228">Параметры включают указатель на имя файла, с которым выполняется ссылка, указатель на имя создаваемого ярлыка и указатель на описание ссылки.</span><span class="sxs-lookup"><span data-stu-id="5529e-228">The parameters include a pointer to the name of the file to link to, a pointer to the name of the shortcut that you are creating, and a pointer to the description of the link.</span></span> <span data-ttu-id="5529e-229">Описание состоит из строки "ярлык **имени файла**", где **имя** файла — это имя файла, с которым необходимо создать ссылку.</span><span class="sxs-lookup"><span data-stu-id="5529e-229">The description consists of the string, "Shortcut to **file name**," where **file name** is the name of the file to link to.</span></span>

<span data-ttu-id="5529e-230">Чтобы создать ярлык папки с помощью образца функции Креателинк, вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с помощью CLSID \_ фолдершорткут вместо CLSID \_ шелллинк (CLSID \_ фолдершорткут поддерживает ишелллинк).</span><span class="sxs-lookup"><span data-stu-id="5529e-230">To create a folder shortcut using the CreateLink sample function, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) using CLSID\_FolderShortcut, instead of CLSID\_ShellLink (CLSID\_FolderShortcut supports IShellLink).</span></span> <span data-ttu-id="5529e-231">Весь остальной код остается прежним.</span><span class="sxs-lookup"><span data-stu-id="5529e-231">All other code remains the same.</span></span>

<span data-ttu-id="5529e-232">Поскольку Креателинк вызывает функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , предполагается, что функция [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) уже была вызвана.</span><span class="sxs-lookup"><span data-stu-id="5529e-232">Because CreateLink calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, it is assumed that the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function has already been called.</span></span> <span data-ttu-id="5529e-233">Креателинк использует интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) для сохранения ярлыка и интерфейса [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) для хранения имени и описания файла.</span><span class="sxs-lookup"><span data-stu-id="5529e-233">CreateLink uses the [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface to save the shortcut and the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface to store the file name and description.</span></span>


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a><span data-ttu-id="5529e-234">Разрешение ярлыка</span><span class="sxs-lookup"><span data-stu-id="5529e-234">Resolving a Shortcut</span></span>

<span data-ttu-id="5529e-235">Приложению может потребоваться доступ к созданному ранее ярлыку и управление им.</span><span class="sxs-lookup"><span data-stu-id="5529e-235">An application may need to access and manipulate a shortcut that was previously created.</span></span> <span data-ttu-id="5529e-236">Эта операция называется разрешением ярлыка.</span><span class="sxs-lookup"><span data-stu-id="5529e-236">This operation is referred to as resolving the shortcut.</span></span>

<span data-ttu-id="5529e-237">Определяемая приложением функция Ресолвеит в следующем примере разрешает ярлык.</span><span class="sxs-lookup"><span data-stu-id="5529e-237">The application-defined ResolveIt function in the following example resolves a shortcut.</span></span> <span data-ttu-id="5529e-238">Его параметры включают в себя маркер окна, указатель на путь ярлыка и адрес буфера, который получает новый путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="5529e-238">Its parameters include a window handle, a pointer to the path of the shortcut, and the address of a buffer that receives the new path to the object.</span></span> <span data-ttu-id="5529e-239">Обработчик окна определяет родительское окно для всех окон сообщений, которые может потребоваться отобразить оболочке.</span><span class="sxs-lookup"><span data-stu-id="5529e-239">The window handle identifies the parent window for any message boxes that the Shell may need to display.</span></span> <span data-ttu-id="5529e-240">Например, оболочка может отображать окно сообщения, если ссылка находится на необщем носителе, в случае возникновения проблем в сети, если пользователю нужно вставить дискету и т. д.</span><span class="sxs-lookup"><span data-stu-id="5529e-240">For example, the Shell can display a message box if the link is on unshared media, if network problems occur, if the user needs to insert a floppy disk, and so on.</span></span>

<span data-ttu-id="5529e-241">Функция Ресолвеит вызывает функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) и предполагает, что функция [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) уже была вызвана.</span><span class="sxs-lookup"><span data-stu-id="5529e-241">The ResolveIt function calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and assumes that the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function has already been called.</span></span> <span data-ttu-id="5529e-242">Обратите внимание, что Ресолвеит должен использовать интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) для хранения сведений о ссылках.</span><span class="sxs-lookup"><span data-stu-id="5529e-242">Note that ResolveIt needs to use the [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface to store the link information.</span></span> <span data-ttu-id="5529e-243">**IPersistFile** реализуется объектом [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .</span><span class="sxs-lookup"><span data-stu-id="5529e-243">**IPersistFile** is implemented by the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) object.</span></span> <span data-ttu-id="5529e-244">Сведения о связи должны быть загружены до получения сведений о пути, которые показаны Далее в примере.</span><span class="sxs-lookup"><span data-stu-id="5529e-244">The link information must be loaded before the path information is retrieved, which is shown later in the example.</span></span> <span data-ttu-id="5529e-245">Сбой загрузки сведений о ссылках приводит к сбою вызовов функций членов [**ишелллинк::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) Ишелллинк и [**:: undescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) .</span><span class="sxs-lookup"><span data-stu-id="5529e-245">Failing to load the link information causes the calls to the [**IShellLink::GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) and [**IShellLink::GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) member functions to fail.</span></span>


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a><span data-ttu-id="5529e-246">Создание ярлыка для нефайлового объекта</span><span class="sxs-lookup"><span data-stu-id="5529e-246">Creating a Shortcut to a Nonfile Object</span></span>

<span data-ttu-id="5529e-247">Создание ярлыка для нефайлового объекта, например принтера, похоже на создание ярлыка для файла, за исключением того, что вместо указания пути к файлу необходимо задать для списка идентификаторов принтер.</span><span class="sxs-lookup"><span data-stu-id="5529e-247">Creating a shortcut to a nonfile object, such as a printer, is similar to creating a shortcut to a file except that rather than setting the path to the file, you must set the identifier list to the printer.</span></span> <span data-ttu-id="5529e-248">Чтобы задать список идентификаторов, вызовите метод [**ишелллинк:: сетидлист**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) , указав адрес списка идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="5529e-248">To set the identifier list, call the [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) method, specifying the address of an identifier list.</span></span>

<span data-ttu-id="5529e-249">Каждый объект в пространстве имен оболочки имеет идентификатор элемента.</span><span class="sxs-lookup"><span data-stu-id="5529e-249">Each object within the Shell's namespace has an item identifier.</span></span> <span data-ttu-id="5529e-250">Оболочка часто объединяет идентификаторы элементов в списки, заканчивающиеся нулем, состоящие из любого числа идентификаторов элементов.</span><span class="sxs-lookup"><span data-stu-id="5529e-250">The Shell often concatenates item identifiers into null-terminated lists consisting of any number of item identifiers.</span></span> <span data-ttu-id="5529e-251">Дополнительные сведения об идентификаторах элементов см. в разделе [идентификаторы элементов и списки идентификаторов](#item-identifiers-and-identifier-lists).</span><span class="sxs-lookup"><span data-stu-id="5529e-251">For more information about item identifiers, see [Item Identifiers and Identifier Lists](#item-identifiers-and-identifier-lists).</span></span>

<span data-ttu-id="5529e-252">В общем случае, если необходимо задать ярлык для элемента, у которого нет имени файла, например принтера, у вас уже есть указатель на интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-252">In general, if you need to set a shortcut to an item that does not have a file name, such as a printer, you will already have a pointer to the object's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="5529e-253">**Ишеллфолдер** используется для создания расширений пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5529e-253">**IShellFolder** is used to create namespace extensions.</span></span>

<span data-ttu-id="5529e-254">После получения идентификатора класса для [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)можно вызвать функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы получить адрес интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5529e-254">Once you have the class identifier for [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), you can call the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve the address of the interface.</span></span> <span data-ttu-id="5529e-255">Затем можно вызвать интерфейс для перечисления объектов в папке и получить адрес идентификатора элемента для искомого объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-255">Then you can call the interface to enumerate the objects in the folder and retrieve the address of the item identifier for the object that you are searching for.</span></span> <span data-ttu-id="5529e-256">Наконец, можно использовать адрес в вызове функции-члена [**ишелллинк:: сетидлист**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) , чтобы создать ярлык для объекта.</span><span class="sxs-lookup"><span data-stu-id="5529e-256">Finally, you can use the address in a call to the [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) member function to create a shortcut to the object.</span></span>

 

 
