---
description: Проводник Windows — это мощное приложение для обзора ресурсов и управления ими.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Разработка с помощью проводника Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7b68d48f2d1becea23311847a5ce41b3776321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497043"
---
# <a name="developing-with-windows-explorer"></a><span data-ttu-id="e91b1-103">Разработка с помощью проводника Windows</span><span class="sxs-lookup"><span data-stu-id="e91b1-103">Developing with Windows Explorer</span></span>

<span data-ttu-id="e91b1-104">Проводник Windows — это мощное приложение для обзора ресурсов и управления ими.</span><span class="sxs-lookup"><span data-stu-id="e91b1-104">Windows Explorer is a powerful resource-browsing and management application.</span></span> <span data-ttu-id="e91b1-105">Проводник Windows можно использовать как единое целое с помощью Explorer.exe или интерфейса [**иексплорербровсер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="e91b1-105">Windows Explorer can be accessed as an integrated whole through Explorer.exe or the [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="e91b1-106">Проводник (Explorer.exe) может быть порожден как отдельный процесс с помощью [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) или аналогичной функции.</span><span class="sxs-lookup"><span data-stu-id="e91b1-106">Windows Explorer (Explorer.exe) can be spawned as a separate process using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) or a similar function.</span></span>

> [!Note]  
> <span data-ttu-id="e91b1-107">Параметры командной строки для Explorer.exe описаны на сайте поддержки Microsoft Windows в статье [параметры Command-Line проводника Windows](https://support.microsoft.com/kb/152457).</span><span class="sxs-lookup"><span data-stu-id="e91b1-107">Command-line options for Explorer.exe are documented on the Microsoft Windows Support site in the article [Windows Explorer Command-Line Options](https://support.microsoft.com/kb/152457).</span></span>

 

<span data-ttu-id="e91b1-108">Открытые окна проводника можно обнаружить и программировать с помощью [**ишеллвиндовс**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ шеллвиндовс), а новые экземпляры проводника можно создать с помощью [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ шеллбровсервиндов).</span><span class="sxs-lookup"><span data-stu-id="e91b1-108">Open explorer windows can be discovered and programmed by using [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID\_ShellWindows), and new instances of Windows Explorer can be created by using [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID\_ShellBrowserWindow).</span></span>

<span data-ttu-id="e91b1-109">В следующем образце кода показано, как можно использовать модель автоматизации проводника Windows для создания и обнаружения работающих окон проводника.</span><span class="sxs-lookup"><span data-stu-id="e91b1-109">The following code sample demonstrates how the Windows Explorer automation model can be used to create and discover explorer windows that are running.</span></span>


```
#define _WIN32_WINNT 0x0600
#define _WIN32_IE 0x0700
#define _UNICODE

#include <windows.h>
#include <shobjidl.h>
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>
#include <propvarutil.h>
 
#pragma comment(lib, "shlwapi.lib")
#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "shell32.lib")
#pragma comment(lib, "propsys.lib")
 
// Use the Shell Windows object to find all of the explorer and IExplorer 
// windows and close them.
 
void CloseExplorerWindows()
{
    IShellWindows* psw;
    
    if (SUCCEEDED(CoCreateInstance(CLSID_ShellWindows, 
                                   NULL,  
                                   CLSCTX_LOCAL_SERVER, 
                                   IID_PPV_ARGS(&psw))))
    {
        VARIANT v = { VT_I4 };
        if (SUCCEEDED(psw->get_Count(&v.lVal)))
        {
            // Walk backward to make sure that the windows that close
            // do not cause the array to be reordered.
            while (--v.lVal >= 0)
            {
                IDispatch *pdisp;
                
                if (S_OK == psw->Item(v, &pdisp))
                {
                    IWebBrowser2 *pwb;
                    if (SUCCEEDED(pdisp->QueryInterface(IID_PPV_ARGS(&pwb))))
                    {
                        pwb->Quit();
                        pwb->Release();
                    }
                    pdisp->Release();
                }
            }
        }
        psw->Release();
    }
}
 
// Convert an IShellItem or IDataObject into a VARIANT that holds an IDList
// suitable for use with IWebBrowser2::Navigate2.
 
HRESULT InitVariantFromObject(IUnknown *punk, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetIDListFromObject(punk, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}
 
HRESULT ParseItemAsVariant(PCWSTR pszItem, IBindCtx *pbc, VARIANT *pvar)
{
    VariantInit(pvar);
 
    IShellItem *psi;
    HRESULT hr = SHCreateItemFromParsingName(pszItem, NULL, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

HRESULT GetKnownFolderAsVariant(REFKNOWNFOLDERID kfid, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetKnownFolderIDList(kfid, 0, NULL, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}

HRESULT GetShellItemFromCommandLine(REFIID riid, void **ppv)
{
    *ppv = NULL;
    HRESULT hr = E_FAIL;

    int cArgs;
    PWSTR *ppszCmd = CommandLineToArgvW(GetCommandLineW(), &cArgs);
    if (ppszCmd && cArgs > 1)
    {
        WCHAR szSpec[MAX_PATH];
        StringCchCopyW(szSpec, ARRAYSIZE(szSpec), ppszCmd[1]);
        PathUnquoteSpacesW(szSpec);

        hr = szSpec[0] ? S_OK : E_FAIL;   // Protect against empty data
        if (SUCCEEDED(hr))
        {
            hr = SHCreateItemFromParsingName(szSpec, NULL, riid, ppv);
            if (FAILED(hr))
            {
                WCHAR szFolder[MAX_PATH];
                GetCurrentDirectoryW(ARRAYSIZE(szFolder), szFolder);

                hr = PathAppendW(szFolder, szSpec) ? S_OK : E_FAIL;
                if (SUCCEEDED(hr))
                {
                    hr = SHCreateItemFromParsingName(szFolder, NULL, riid, ppv);
                }
            }
        }
    }
    return hr;
}

HRESULT GetShellItemFromCommandLineAsVariant(VARIANT *pvar)
{
    VariantInit(pvar);

    IShellItem *psi;
    HRESULT hr = GetShellItemFromCommandLine(IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

void OpenWindow()
{
    IWebBrowser2 *pwb;
    HRESULT hr = CoCreateInstance(CLSID_ShellBrowserWindow, 
                                  NULL,
                                  CLSCTX_LOCAL_SERVER, 
                                  IID_PPV_ARGS(&pwb));
    if (SUCCEEDED(hr))
    {
        CoAllowSetForegroundWindow(pwb, 0);

        pwb->put_Left(100);
        pwb->put_Top(100);
        pwb->put_Height(600);
        pwb->put_Width(800);
 
        VARIANT varTarget = {0};
        hr = GetShellItemFromCommandLineAsVariant(&varTarget);
        if (FAILED(hr))
        {
            hr = GetKnownFolderAsVariant(FOLDERID_UsersFiles, &varTarget);
        }

        if (SUCCEEDED(hr))
        {
            VARIANT vEmpty = {0};
            hr = pwb->Navigate2(&varTarget, &vEmpty, &vEmpty, &vEmpty, &vEmpty);
            if (SUCCEEDED(hr))
            {
                pwb->put_Visible(VARIANT_TRUE);
            }
            VariantClear(&varTarget);
        }
        pwb->Release();
    }
}

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |  COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CloseExplorerWindows();

        OpenWindow();

        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="e91b1-110">Клиентскую область проводника Windows можно разместить с помощью интерфейса [иексплорербровсер](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="e91b1-110">The Windows Explorer client area can be hosted by using the [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="e91b1-111">Клиент проводника Windows и элементы управления деревом пространств имен являются стандартными компонентами Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e91b1-111">The Windows Explorer client and the namespace tree controls are standard components of Windows Vista and later.</span></span> <span data-ttu-id="e91b1-112">Разработчики могут повторно использовать интерфейсы как сборки компонентов.</span><span class="sxs-lookup"><span data-stu-id="e91b1-112">Developers can reuse the interfaces as building components.</span></span> <span data-ttu-id="e91b1-113">Одним из распространенных способов использования этих элементов управления является создание настраиваемых обозревателей, подходящих для проблемного домена.</span><span class="sxs-lookup"><span data-stu-id="e91b1-113">One common use of these controls is to create customized explorers appropriate to the problem domain.</span></span>

<span data-ttu-id="e91b1-114">Элементы управления в проводнике подразделяются на следующие функциональные категории:</span><span class="sxs-lookup"><span data-stu-id="e91b1-114">The controls in Windows Explorer are classified into the following functional categories:</span></span>

-   [<span data-ttu-id="e91b1-115">Элементы управления навигацией</span><span class="sxs-lookup"><span data-stu-id="e91b1-115">Navigation Controls</span></span>](#navigation-controls)
-   [<span data-ttu-id="e91b1-116">Командные элементы управления</span><span class="sxs-lookup"><span data-stu-id="e91b1-116">Command Controls</span></span>](#command-controls)
-   [<span data-ttu-id="e91b1-117">Свойства и элементы управления предварительным просмотром</span><span class="sxs-lookup"><span data-stu-id="e91b1-117">Property and Preview Controls</span></span>](#property-and-preview-controls)
-   [<span data-ttu-id="e91b1-118">Фильтрация и просмотр элементов управления</span><span class="sxs-lookup"><span data-stu-id="e91b1-118">Filtering and View Controls</span></span>](#filtering-and-view-controls)
-   [<span data-ttu-id="e91b1-119">Элемент управления ListView</span><span class="sxs-lookup"><span data-stu-id="e91b1-119">Listview Control</span></span>](#listview-control)

## <a name="navigation-controls"></a><span data-ttu-id="e91b1-120">Элементы управления навигацией</span><span class="sxs-lookup"><span data-stu-id="e91b1-120">Navigation Controls</span></span>

<span data-ttu-id="e91b1-121">Элементы управления навигацией помогают пользователям определить контекст и перемещаться по связанному пространству логического домена, называемому пажеспаце.</span><span class="sxs-lookup"><span data-stu-id="e91b1-121">Navigation controls assist users in determining context and navigating the associated logical domain space, called the pagespace.</span></span> <span data-ttu-id="e91b1-122">Например, пажеспаце для проводника Windows является пространством имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="e91b1-122">For example, the pagespace for Windows Explorer is the Shell namespace.</span></span> <span data-ttu-id="e91b1-123">Пажеспацес состоят из нуля или более страниц.</span><span class="sxs-lookup"><span data-stu-id="e91b1-123">Pagespaces are composed of zero or more pages.</span></span>

<span data-ttu-id="e91b1-124">В следующей таблице перечислены и описаны элементы управления навигацией, доступные в проводнике Windows в операционных системах Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e91b1-124">The following table lists and describes the navigation controls available in Windows Explorer in the Windows Vista and later operating systems.</span></span>



| <span data-ttu-id="e91b1-125">Элемент управления навигацией</span><span class="sxs-lookup"><span data-stu-id="e91b1-125">Navigation control</span></span>               | <span data-ttu-id="e91b1-126">Описание</span><span class="sxs-lookup"><span data-stu-id="e91b1-126">Description</span></span>                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e91b1-127">Адресная строка (элемент управления навигатором)</span><span class="sxs-lookup"><span data-stu-id="e91b1-127">Address Bar (Breadcrumb control)</span></span> | <span data-ttu-id="e91b1-128">Отображает адрес текущей страницы в пажеспаце.</span><span class="sxs-lookup"><span data-stu-id="e91b1-128">Displays the address of the current page in the pagespace.</span></span> <span data-ttu-id="e91b1-129">Кнопки навигации можно щелкнуть для перехода к любому предку в пажеспаце.</span><span class="sxs-lookup"><span data-stu-id="e91b1-129">Breadcrumb buttons can be clicked to navigate to any ancestor in the pagespace.</span></span> <span data-ttu-id="e91b1-130">Пользователи также могут вводить URL-адреса и пути для навигации.</span><span class="sxs-lookup"><span data-stu-id="e91b1-130">Users can also type URLs and paths to navigate.</span></span> |
| <span data-ttu-id="e91b1-131">Дерево папок</span><span class="sxs-lookup"><span data-stu-id="e91b1-131">Folder Tree</span></span>                      | <span data-ttu-id="e91b1-132">Предоставляет новую версию элемента управления "дерево", оптимизированную для больших пажеспацес.</span><span class="sxs-lookup"><span data-stu-id="e91b1-132">Provides a new version of a tree control, optimized for large pagespaces.</span></span>                                                                                                                  |
| <span data-ttu-id="e91b1-133">Командировки</span><span class="sxs-lookup"><span data-stu-id="e91b1-133">Travel</span></span>                           | <span data-ttu-id="e91b1-134">Позволяет относительную навигацию с помощью кнопок веб-стиля, таких как « **назад** » и « **вперед**».</span><span class="sxs-lookup"><span data-stu-id="e91b1-134">Enables relative navigation through web-style buttons such as **Back** and **Forward**.</span></span>                                                                                                    |
| <span data-ttu-id="e91b1-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e91b1-135">Title</span></span>                            | <span data-ttu-id="e91b1-136">Отображает имя и контекст текущего обозревателя.</span><span class="sxs-lookup"><span data-stu-id="e91b1-136">Displays the current explorer name and context.</span></span>                                                                                                                                            |
| <span data-ttu-id="e91b1-137">пажеспаце</span><span class="sxs-lookup"><span data-stu-id="e91b1-137">Pagespace</span></span>                        | <span data-ttu-id="e91b1-138">Отображает текущую ветвь пажеспаце.</span><span class="sxs-lookup"><span data-stu-id="e91b1-138">Displays the current branch of the pagespace.</span></span> <span data-ttu-id="e91b1-139">Страницы могут упорядочиваться по различным критериям.</span><span class="sxs-lookup"><span data-stu-id="e91b1-139">Pages can be ordered by different criteria.</span></span> <span data-ttu-id="e91b1-140">Пользователи могут щелкнуть страницу для перехода к ней.</span><span class="sxs-lookup"><span data-stu-id="e91b1-140">Users can click a page to navigate to it.</span></span>                                                        |



 

## <a name="command-controls"></a><span data-ttu-id="e91b1-141">Командные элементы управления</span><span class="sxs-lookup"><span data-stu-id="e91b1-141">Command Controls</span></span>

<span data-ttu-id="e91b1-142">Элементы управления командами объявляют функции и функциональные возможности проводника Windows пользователям.</span><span class="sxs-lookup"><span data-stu-id="e91b1-142">Command controls advertise the features and functionality of the Windows Explorer to users.</span></span> <span data-ttu-id="e91b1-143">Эти элементы управления выполняют общие действия или действия, относящиеся к одному выбранному элементу или элементам.</span><span class="sxs-lookup"><span data-stu-id="e91b1-143">These controls perform either general actions or actions specific to one selected item or items.</span></span>



| <span data-ttu-id="e91b1-144">Управление командами</span><span class="sxs-lookup"><span data-stu-id="e91b1-144">Command control</span></span> | <span data-ttu-id="e91b1-145">Описание</span><span class="sxs-lookup"><span data-stu-id="e91b1-145">Description</span></span>                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e91b1-146">Панель инструментов</span><span class="sxs-lookup"><span data-stu-id="e91b1-146">Toolbar</span></span>         | <span data-ttu-id="e91b1-147">Отображает кнопки для часто используемых команд (Новая версия панели инструментов команды).</span><span class="sxs-lookup"><span data-stu-id="e91b1-147">Displays buttons for commonly used commands (a new version of a command toolbar).</span></span> <span data-ttu-id="e91b1-148">Параметры настройки включают в себя кнопки с раскрывающимся списком, кнопки разделения, необязательный описательный текст и область переполнения.</span><span class="sxs-lookup"><span data-stu-id="e91b1-148">Customization options include drop-down buttons, split buttons, optional descriptive text, and an overflow area.</span></span> |
| <span data-ttu-id="e91b1-149">Имиджевая</span><span class="sxs-lookup"><span data-stu-id="e91b1-149">Hero</span></span>            | <span data-ttu-id="e91b1-150">Отображается как отдельный необязательный настраиваемый элемент управления в центре панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="e91b1-150">Appears as a single, optional, custom control in the center of the toolbar.</span></span> <span data-ttu-id="e91b1-151">Он представляет основную команду для текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="e91b1-151">It represents the primary command for the current context.</span></span>                                                             |
| <span data-ttu-id="e91b1-152">Строка меню</span><span class="sxs-lookup"><span data-stu-id="e91b1-152">Menu Bar</span></span>        | <span data-ttu-id="e91b1-153">Представляет команды через меню.</span><span class="sxs-lookup"><span data-stu-id="e91b1-153">Presents commands through menus.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="e91b1-154">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="e91b1-154">Context Menu</span></span>    | <span data-ttu-id="e91b1-155">Перечисляет контекстно-ориентированное подмножество доступных команд, которые отображаются в результате щелчка правой кнопкой мыши элемента.</span><span class="sxs-lookup"><span data-stu-id="e91b1-155">Lists a contextually relevant subset of available commands that are displayed as a result of right-clicking an item.</span></span>                                                                               |



 

## <a name="property-and-preview-controls"></a><span data-ttu-id="e91b1-156">Свойства и элементы управления предварительным просмотром</span><span class="sxs-lookup"><span data-stu-id="e91b1-156">Property and Preview Controls</span></span>

<span data-ttu-id="e91b1-157">Элементы управления "свойство" и "предварительный просмотр" используются для предварительного просмотра элементов, а для просмотра и изменения свойств элементов.</span><span class="sxs-lookup"><span data-stu-id="e91b1-157">Property and preview controls are used to preview items, and to view and edit item properties.</span></span>



| <span data-ttu-id="e91b1-158">Control</span><span class="sxs-lookup"><span data-stu-id="e91b1-158">Control</span></span>    | <span data-ttu-id="e91b1-159">Описание</span><span class="sxs-lookup"><span data-stu-id="e91b1-159">Description</span></span>                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e91b1-160">Preview (Предварительный просмотр)</span><span class="sxs-lookup"><span data-stu-id="e91b1-160">Preview</span></span>    | <span data-ttu-id="e91b1-161">Отображает предварительный просмотр выбранного элемента, например эскиза или активного значка.</span><span class="sxs-lookup"><span data-stu-id="e91b1-161">Displays a preview of the selected item, such as a thumbnail or a Live Icon.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="e91b1-162">Свойства</span><span class="sxs-lookup"><span data-stu-id="e91b1-162">Properties</span></span> | <span data-ttu-id="e91b1-163">Отображает свойства выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="e91b1-163">Displays properties of the selected item.</span></span> <span data-ttu-id="e91b1-164">При выборе нескольких элементов отображается сводка свойств выбранной группы элементов.</span><span class="sxs-lookup"><span data-stu-id="e91b1-164">For multiple selections, it displays a summary of properties for the selected group of items.</span></span> <span data-ttu-id="e91b1-165">Для выбора со значением NULL отображается сводка свойств текущей страницы (содержимое ListView).</span><span class="sxs-lookup"><span data-stu-id="e91b1-165">For a null selection, it displays a summary of properties for the current page (contents of the listview).</span></span> |



 

## <a name="filtering-and-view-controls"></a><span data-ttu-id="e91b1-166">Фильтрация и просмотр элементов управления</span><span class="sxs-lookup"><span data-stu-id="e91b1-166">Filtering and View Controls</span></span>

<span data-ttu-id="e91b1-167">Элементы управления фильтрацией и представления используются для управления набором элементов в ListView и для изменения представления элементов в ListView.</span><span class="sxs-lookup"><span data-stu-id="e91b1-167">Filtering and view controls are used to manipulate the set of items in the listview and to change the presentation of items in the listview.</span></span>



| <span data-ttu-id="e91b1-168">Control</span><span class="sxs-lookup"><span data-stu-id="e91b1-168">Control</span></span>   | <span data-ttu-id="e91b1-169">Описание</span><span class="sxs-lookup"><span data-stu-id="e91b1-169">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e91b1-170">Filter</span><span class="sxs-lookup"><span data-stu-id="e91b1-170">Filter</span></span>    | <span data-ttu-id="e91b1-171">Фильтрует или упорядочивает элементы в ListView на основе свойств, перечисленных в виде столбцов.</span><span class="sxs-lookup"><span data-stu-id="e91b1-171">Filters or arranges items in a listview based on properties listed as columns.</span></span> <span data-ttu-id="e91b1-172">При щелчке по столбцу выполняется сортировка по этому свойству.</span><span class="sxs-lookup"><span data-stu-id="e91b1-172">Clicking on a column sorts by that property.</span></span> |
| <span data-ttu-id="e91b1-173">вордвхил</span><span class="sxs-lookup"><span data-stu-id="e91b1-173">Wordwheel</span></span> | <span data-ttu-id="e91b1-174">Динамически и постепенно фильтрует отображаемые элементы в ListView на основе входной текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="e91b1-174">Dynamically and incrementally filters the displayed items in a listview based on an input text string.</span></span>                      |
| <span data-ttu-id="e91b1-175">Представление</span><span class="sxs-lookup"><span data-stu-id="e91b1-175">View</span></span>      | <span data-ttu-id="e91b1-176">Позволяет пользователю изменять режим просмотра элемента управления ListView.</span><span class="sxs-lookup"><span data-stu-id="e91b1-176">Enables the user to change the view mode of a listview control.</span></span> <span data-ttu-id="e91b1-177">Для определения размера значка можно использовать ползунок.</span><span class="sxs-lookup"><span data-stu-id="e91b1-177">A slider can be used to determine icon size.</span></span>                |



 

## <a name="listview-control"></a><span data-ttu-id="e91b1-178">Элемент управления ListView</span><span class="sxs-lookup"><span data-stu-id="e91b1-178">Listview Control</span></span>

<span data-ttu-id="e91b1-179">Элемент управления ListView используется для просмотра набора элементов в одном из четырех режимов представления: «сведения», «плитки», «значки» или «Панорама».</span><span class="sxs-lookup"><span data-stu-id="e91b1-179">The listview control is used to view a set of items in one of four view modes: details, tiles, icons, or panorama.</span></span> <span data-ttu-id="e91b1-180">Элемент управления ListView также позволяет пользователю выбрать и активировать один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="e91b1-180">The listview control also enables the user to select and activate one or more items.</span></span>

> [!Caution]  
> <span data-ttu-id="e91b1-181">Хотя некоторые из этих элементов управления имеют имена и (или) функции, аналогичные элементам управления "Стандартный Windows Presentation Foundation (WPF)", которые находятся в пространстве имен System. Windows. Controls, они являются отдельными классами.</span><span class="sxs-lookup"><span data-stu-id="e91b1-181">Although some of these controls have names and/or functionality that is similar to standard Windows Presentation Foundation (WPF) controls found in the System.Windows.Controls namespace, they are distinct classes.</span></span>

 

<span data-ttu-id="e91b1-182">Эти отдельные элементы управления работают вместе в основном через события, созданные пользователем или самими элементами управления.</span><span class="sxs-lookup"><span data-stu-id="e91b1-182">These separate controls work together largely through events generated either by user interaction or by the controls themselves.</span></span> <span data-ttu-id="e91b1-183">В следующей таблице показаны три основные категории событий.</span><span class="sxs-lookup"><span data-stu-id="e91b1-183">The following table shows the three primary event categories.</span></span>



| <span data-ttu-id="e91b1-184">Категория событий</span><span class="sxs-lookup"><span data-stu-id="e91b1-184">Event category</span></span> | <span data-ttu-id="e91b1-185">Например, .</span><span class="sxs-lookup"><span data-stu-id="e91b1-185">Example</span></span>                                                       |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="e91b1-186">Навигация</span><span class="sxs-lookup"><span data-stu-id="e91b1-186">Navigation</span></span>     | <span data-ttu-id="e91b1-187">Переход с одной страницы на другую.</span><span class="sxs-lookup"><span data-stu-id="e91b1-187">Going from one page to another.</span></span>                               |
| <span data-ttu-id="e91b1-188">Выбор</span><span class="sxs-lookup"><span data-stu-id="e91b1-188">Selection</span></span>      | <span data-ttu-id="e91b1-189">Изменение текущего выделения в ListView.</span><span class="sxs-lookup"><span data-stu-id="e91b1-189">Changing the current selection in the listview.</span></span>               |
| <span data-ttu-id="e91b1-190">Просмотр изменений</span><span class="sxs-lookup"><span data-stu-id="e91b1-190">View Change</span></span>    | <span data-ttu-id="e91b1-191">Изменение порядка представления или режима просмотра в ListView.</span><span class="sxs-lookup"><span data-stu-id="e91b1-191">Changing the presentation order or view mode in the listview.</span></span> |



 

 

 
