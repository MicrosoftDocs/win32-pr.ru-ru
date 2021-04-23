---
description: Прежде чем можно будет использовать объект пространства имен, необходимо получить способ его распознавания.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Получение идентификатора папки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2e62454bf27f2c203f59aecb325cefe6537d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997734"
---
# <a name="getting-a-folders-id"></a><span data-ttu-id="b23b2-103">Получение идентификатора папки</span><span class="sxs-lookup"><span data-stu-id="b23b2-103">Getting a Folder's ID</span></span>

<span data-ttu-id="b23b2-104">Прежде чем можно будет использовать объект пространства имен, необходимо получить способ его распознавания.</span><span class="sxs-lookup"><span data-stu-id="b23b2-104">Before you can make use of a namespace object, you need a way to identify it.</span></span> <span data-ttu-id="b23b2-105">Это означает получение либо указателя на список идентификаторов элементов (ПИДЛ), либо, в случае с объектами файловой системы, его путь.</span><span class="sxs-lookup"><span data-stu-id="b23b2-105">This means obtaining either its pointer to an item identifier list (PIDL) or, in the case of file system objects, its path.</span></span> <span data-ttu-id="b23b2-106">В этом разделе обсуждаются два простых способа получения идентификаторов объектов.</span><span class="sxs-lookup"><span data-stu-id="b23b2-106">This section discusses two of the simpler ways to obtain object IDs.</span></span>

<span data-ttu-id="b23b2-107">Для более эффективного подхода, который будет работать с любой папкой, используйте интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="b23b2-107">For a more powerful approach that will work with any folder, use the [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="b23b2-108">Дополнительные сведения см. [в разделе Получение сведений о содержимом папки](folder-info.md) .</span><span class="sxs-lookup"><span data-stu-id="b23b2-108">See [Getting Information About the Contents of a Folder](folder-info.md) for more details.</span></span>

-   [<span data-ttu-id="b23b2-109">Диалоговое окно OpenFiles</span><span class="sxs-lookup"><span data-stu-id="b23b2-109">The OpenFiles Dialog Box</span></span>](#the-openfiles-dialog-box)
-   [<span data-ttu-id="b23b2-110">Диалоговое окно "Шбровсефорфолдер"</span><span class="sxs-lookup"><span data-stu-id="b23b2-110">The SHBrowseForFolder Dialog Box</span></span>](#the-shbrowseforfolder-dialog-box)
-   [<span data-ttu-id="b23b2-111">Специальные папки и Ксидлс</span><span class="sxs-lookup"><span data-stu-id="b23b2-111">Special Folders and CSIDLs</span></span>](#special-folders-and-csidls)
-   [<span data-ttu-id="b23b2-112">Простой пример использования Ксидлс и Шбровсефорфолдер</span><span class="sxs-lookup"><span data-stu-id="b23b2-112">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a><span data-ttu-id="b23b2-113">Диалоговое окно OpenFiles</span><span class="sxs-lookup"><span data-stu-id="b23b2-113">The OpenFiles Dialog Box</span></span>

<span data-ttu-id="b23b2-114">Чтобы разрешить пользователю переходить по пространству имен и выбрать папку, приложение может использовать интерфейс [**ифиледиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) .</span><span class="sxs-lookup"><span data-stu-id="b23b2-114">To enable the user to navigate the namespace and select a folder, your application can use the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface.</span></span> <span data-ttu-id="b23b2-115">Вызов этого интерфейса с помощью флага **\_ пиккфолдерс Фос** открывает диалоговое окно Общие [файлы](../dlgbox/open-and-save-as-dialog-boxes.md) в режиме "Выбор папок".</span><span class="sxs-lookup"><span data-stu-id="b23b2-115">Calling this interface with the **FOS\_PICKFOLDERS** flag launches the [Open Files](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box in "pick folders" mode.</span></span>

<span data-ttu-id="b23b2-116">Для Windows Vista и более поздних версий это рекомендуемый способ выбора папок.</span><span class="sxs-lookup"><span data-stu-id="b23b2-116">For Windows Vista and later, this is the recommended way to pick folders.</span></span>

## <a name="the-shbrowseforfolder-dialog-box"></a><span data-ttu-id="b23b2-117">Диалоговое окно "Шбровсефорфолдер"</span><span class="sxs-lookup"><span data-stu-id="b23b2-117">The SHBrowseForFolder Dialog Box</span></span>

<span data-ttu-id="b23b2-118">Чтобы разрешить пользователю переходить по пространству имен и выбрать папку, приложение может просто вызвать [**шбровсефорфолдер**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="b23b2-118">To enable the user to navigate the namespace and select a folder, your application can simply invoke [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="b23b2-119">При вызове этой функции открывается диалоговое окно с пользовательским интерфейсом, который похож на общие диалоговые окна [Open или SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) .</span><span class="sxs-lookup"><span data-stu-id="b23b2-119">Calling this function launches a dialog box with a UI that works somewhat like the [Open or SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog boxes.</span></span>

<span data-ttu-id="b23b2-120">Когда пользователь выбирает папку, [**шбровсефорфолдер**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) ВОЗВРАЩАЕТ полный Пидл папки и ее отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="b23b2-120">When the user selects a folder, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) returns the folder's fully qualified PIDL and its display name.</span></span> <span data-ttu-id="b23b2-121">Если папка находится в файловой системе, приложение может преобразовать ПИДЛ в путь, вызвав [**шжетпасфромидлист**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span><span class="sxs-lookup"><span data-stu-id="b23b2-121">If the folder is in the file system, the application can convert the PIDL to a path by calling [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span></span> <span data-ttu-id="b23b2-122">Приложение также может ограничить диапазон папок, которые пользователь может выбрать из, указав корневую папку.</span><span class="sxs-lookup"><span data-stu-id="b23b2-122">The application can also restrict the range of folders that the user can select from by specifying a root folder.</span></span> <span data-ttu-id="b23b2-123">Отобразятся только те папки, которые находятся ниже корневого каталога в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b23b2-123">Only folders that are below that root in the namespace will appear.</span></span> <span data-ttu-id="b23b2-124">На следующем рисунке показано диалоговое окно **шбровсефорфолдер** , в котором корневая папка имеет значение Program Files.</span><span class="sxs-lookup"><span data-stu-id="b23b2-124">The following illustration shows the **SHBrowseForFolder** dialog box, with the root folder set to Program Files.</span></span>

![снимок экрана — диалоговое окно "Выбор папки"](images/shell1.png)

<span data-ttu-id="b23b2-126">Ниже приведен простой пример использования [**шбровсефорфолдер**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) .</span><span class="sxs-lookup"><span data-stu-id="b23b2-126">A simple example of how to use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) is provided later.</span></span>

## <a name="special-folders-and-csidls"></a><span data-ttu-id="b23b2-127">Специальные папки и Ксидлс</span><span class="sxs-lookup"><span data-stu-id="b23b2-127">Special Folders and CSIDLs</span></span>

<span data-ttu-id="b23b2-128">Некоторые часто используемые папки обозначены системой как *Специальные* .</span><span class="sxs-lookup"><span data-stu-id="b23b2-128">A number of commonly used folders are designated as *special* by the system.</span></span> <span data-ttu-id="b23b2-129">Эти папки имеют четко определенную цель, и большинство из них есть на всех системах.</span><span class="sxs-lookup"><span data-stu-id="b23b2-129">These folders have a well-defined purpose, and most of them are present on all systems.</span></span> <span data-ttu-id="b23b2-130">Даже если они отсутствуют изначально, их имена и расположения по-прежнему определяются, поэтому их можно добавить позже.</span><span class="sxs-lookup"><span data-stu-id="b23b2-130">Even if they are not present initially, their names and locations are still defined, so they can be added later.</span></span> <span data-ttu-id="b23b2-131">Коллекция специальных папок включает все стандартные виртуальные папки системы, такие как принтеры, мои документы и сетевое окружение.</span><span class="sxs-lookup"><span data-stu-id="b23b2-131">The collection of special folders includes all of the system's standard virtual folders, such as Printers, My Documents, and Network Neighborhood.</span></span> <span data-ttu-id="b23b2-132">Он также включает ряд стандартных папок файловой системы, таких как Program Files и System.</span><span class="sxs-lookup"><span data-stu-id="b23b2-132">It also includes a number of standard file system folders, such as Program Files and System.</span></span>

<span data-ttu-id="b23b2-133">Несмотря на то что папки являются стандартными компонентами всех систем, их имена и расположения в пространстве имен могут различаться.</span><span class="sxs-lookup"><span data-stu-id="b23b2-133">Even though the folders are a standard component of all systems, their names and locations in the namespace can vary.</span></span> <span data-ttu-id="b23b2-134">Например, системный каталог — C: \\ WinNT \\ system32 в некоторых системах и C: \\ Windows \\ system32 на других компьютерах.</span><span class="sxs-lookup"><span data-stu-id="b23b2-134">For example, the System directory is C:\\Winnt\\System32 on some systems and C:\\Windows\\System32 on others.</span></span> <span data-ttu-id="b23b2-135">В прошлом переменные среды предоставили способ определения имени и расположения специальной папки в любой конкретной системе.</span><span class="sxs-lookup"><span data-stu-id="b23b2-135">In the past, environment variables provided a way to determine the name and location of a special folder on any particular system.</span></span> <span data-ttu-id="b23b2-136">Теперь оболочка предоставляет более надежный и гибкий способ обнаружения специальных папок, [**ксидлс**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="b23b2-136">The Shell now provides a more robust and flexible way to identify special folders, [**CSIDLs**](csidl.md).</span></span> <span data-ttu-id="b23b2-137">Обычно их следует использовать вместо переменных среды.</span><span class="sxs-lookup"><span data-stu-id="b23b2-137">You should generally use them instead of environment variables.</span></span>

<span data-ttu-id="b23b2-138">Ксидлс обеспечивают единообразный способ идентификации и обнаружения специальных папок, независимо от их имени или расположения в определенной системе.</span><span class="sxs-lookup"><span data-stu-id="b23b2-138">CSIDLs provide a uniform way of identifying and locating special folders, regardless of their name or location on a particular system.</span></span> <span data-ttu-id="b23b2-139">В отличие от переменных среды, Ксидлс можно использовать с виртуальными папками, а также с папками файловой системы.</span><span class="sxs-lookup"><span data-stu-id="b23b2-139">Unlike environment variables, CSIDLs can be used with virtual folders as well as file system folders.</span></span> <span data-ttu-id="b23b2-140">Каждой особой папке назначается уникальный код CSID.</span><span class="sxs-lookup"><span data-stu-id="b23b2-140">Each special folder has a unique CSIDL assigned to it.</span></span> <span data-ttu-id="b23b2-141">Например, папка "Program Files" имеет код CSID **\_ программных \_ файлов CSid**, а виртуальная папка сетевого окружения имеет CSid-код CSID **\_ сети**.</span><span class="sxs-lookup"><span data-stu-id="b23b2-141">For example, the Program Files file system folder has a CSIDL of **CSIDL\_PROGRAM\_FILES**, and the Network Neighborhood virtual folder has a CSIDL of **CSIDL\_NETWORK**.</span></span>

<span data-ttu-id="b23b2-142">CSID используется в сочетании с одной из нескольких функций оболочки для получения ПИДЛ специальной папки или пути к особой папке файловой системы.</span><span class="sxs-lookup"><span data-stu-id="b23b2-142">A CSIDL is used in conjunction with one of several Shell functions to retrieve a special folder's PIDL, or a special file system folder's path.</span></span> <span data-ttu-id="b23b2-143">Если папка не существует в системе, приложение может принудительно создать его, объединив его маркер CSID с параметром **CSid \_ \_ CREATE**.</span><span class="sxs-lookup"><span data-stu-id="b23b2-143">If the folder does not exist on a system, your application can force it to be created by combining its CSIDL with **CSIDL\_FLAG\_CREATE**.</span></span> <span data-ttu-id="b23b2-144">Код CSID можно передать следующим функциям:</span><span class="sxs-lookup"><span data-stu-id="b23b2-144">The CSIDL can be passed to the following functions:</span></span>

-   <span data-ttu-id="b23b2-145">[**Шжетфолдерлокатион**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), который извлекает Пидл специальной папки.</span><span class="sxs-lookup"><span data-stu-id="b23b2-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), which retrieves the PIDL of a special folder.</span></span>
-   <span data-ttu-id="b23b2-146">[**Шжетфолдерпас**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), который извлекает путь к специальной папке файловой системы.</span><span class="sxs-lookup"><span data-stu-id="b23b2-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), which retrieves the path of a file system special folder.</span></span>

<span data-ttu-id="b23b2-147">Обратите внимание, что эти две функции появились в оболочке версии 5,0 и заменяют функции [**шжетспеЦиалфолдерлокатион**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) и [**шжетспеЦиалфолдерпас**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) .</span><span class="sxs-lookup"><span data-stu-id="b23b2-147">Note that these two functions were introduced with version 5.0 of the Shell and supersede the [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) and [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) functions.</span></span>

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a><span data-ttu-id="b23b2-148">Простой пример использования Ксидлс и Шбровсефорфолдер</span><span class="sxs-lookup"><span data-stu-id="b23b2-148">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>

<span data-ttu-id="b23b2-149">В следующем примере функции Пидлбровсе показано, как использовать Ксидлс для получения ПИДЛ папки и использовать [**шбровсефорфолдер**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) для выбора пользователем папки.</span><span class="sxs-lookup"><span data-stu-id="b23b2-149">The following sample function, PidlBrowse, illustrates how to use CSIDLs to retrieve a folder's PIDL, and use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) to have the user select a folder.</span></span> <span data-ttu-id="b23b2-150">Он возвращает ПИДЛ и отображаемое имя выбранной папки.</span><span class="sxs-lookup"><span data-stu-id="b23b2-150">It returns the PIDL and display name of the selected folder.</span></span>


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



<span data-ttu-id="b23b2-151">Вызывающее приложение передает в обработчик окна, который необходим для [**шбровсефорфолдер**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="b23b2-151">The calling application passes in a window handle, which is needed by [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="b23b2-152">Параметр *нксидл* — это необязательный CSid, который используется для указания корневой папки.</span><span class="sxs-lookup"><span data-stu-id="b23b2-152">The *nCSIDL* parameter is an optional CSIDL that is used to specify a root folder.</span></span> <span data-ttu-id="b23b2-153">Будут отображены только папки, расположенные под корневой папкой в иерархии.</span><span class="sxs-lookup"><span data-stu-id="b23b2-153">Only folders below the root folder in the hierarchy will be displayed.</span></span> <span data-ttu-id="b23b2-154">Иллюстрация, показанная ранее, была создана путем вызова этой функции с *нксидл* , для которой заданы **\_ программные \_ файлы CSid**.</span><span class="sxs-lookup"><span data-stu-id="b23b2-154">The illustration shown earlier was generated by calling this function with *nCSIDL* set to **CSIDL\_PROGRAM\_FILES**.</span></span> <span data-ttu-id="b23b2-155">Вызывающее приложение также передает строковый буфер *pszDisplayName* для хранения отображаемого имени выбранной папки, когда пидлбровсе возвращает.</span><span class="sxs-lookup"><span data-stu-id="b23b2-155">The calling application also passes in a string buffer, *pszDisplayName*, to hold the display name of the selected folder when PidlBrowse returns.</span></span> <span data-ttu-id="b23b2-156">Вызывающее приложение отвечает за освобождение IDList, возвращенного **шбровсефорфолдер** с помощью [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="b23b2-156">It is the responsibility of the calling application to free the IDList returned by **SHBrowseForFolder** using [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

 

 
