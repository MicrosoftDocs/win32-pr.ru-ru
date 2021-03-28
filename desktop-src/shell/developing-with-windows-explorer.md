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
# <a name="developing-with-windows-explorer"></a>Разработка с помощью проводника Windows

Проводник Windows — это мощное приложение для обзора ресурсов и управления ими. Проводник Windows можно использовать как единое целое с помощью Explorer.exe или интерфейса [**иексплорербровсер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . Проводник (Explorer.exe) может быть порожден как отдельный процесс с помощью [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) или аналогичной функции.

> [!Note]  
> Параметры командной строки для Explorer.exe описаны на сайте поддержки Microsoft Windows в статье [параметры Command-Line проводника Windows](https://support.microsoft.com/kb/152457).

 

Открытые окна проводника можно обнаружить и программировать с помощью [**ишеллвиндовс**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ шеллвиндовс), а новые экземпляры проводника можно создать с помощью [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ шеллбровсервиндов).

В следующем образце кода показано, как можно использовать модель автоматизации проводника Windows для создания и обнаружения работающих окон проводника.


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



Клиентскую область проводника Windows можно разместить с помощью интерфейса [иексплорербровсер](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . Клиент проводника Windows и элементы управления деревом пространств имен являются стандартными компонентами Windows Vista и более поздних версий. Разработчики могут повторно использовать интерфейсы как сборки компонентов. Одним из распространенных способов использования этих элементов управления является создание настраиваемых обозревателей, подходящих для проблемного домена.

Элементы управления в проводнике подразделяются на следующие функциональные категории:

-   [Элементы управления навигацией](#navigation-controls)
-   [Командные элементы управления](#command-controls)
-   [Свойства и элементы управления предварительным просмотром](#property-and-preview-controls)
-   [Фильтрация и просмотр элементов управления](#filtering-and-view-controls)
-   [Элемент управления ListView](#listview-control)

## <a name="navigation-controls"></a>Элементы управления навигацией

Элементы управления навигацией помогают пользователям определить контекст и перемещаться по связанному пространству логического домена, называемому пажеспаце. Например, пажеспаце для проводника Windows является пространством имен оболочки. Пажеспацес состоят из нуля или более страниц.

В следующей таблице перечислены и описаны элементы управления навигацией, доступные в проводнике Windows в операционных системах Windows Vista и более поздних версий.



| Элемент управления навигацией               | Описание                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Адресная строка (элемент управления навигатором) | Отображает адрес текущей страницы в пажеспаце. Кнопки навигации можно щелкнуть для перехода к любому предку в пажеспаце. Пользователи также могут вводить URL-адреса и пути для навигации. |
| Дерево папок                      | Предоставляет новую версию элемента управления "дерево", оптимизированную для больших пажеспацес.                                                                                                                  |
| Командировки                           | Позволяет относительную навигацию с помощью кнопок веб-стиля, таких как « **назад** » и « **вперед**».                                                                                                    |
| Заголовок                            | Отображает имя и контекст текущего обозревателя.                                                                                                                                            |
| пажеспаце                        | Отображает текущую ветвь пажеспаце. Страницы могут упорядочиваться по различным критериям. Пользователи могут щелкнуть страницу для перехода к ней.                                                        |



 

## <a name="command-controls"></a>Командные элементы управления

Элементы управления командами объявляют функции и функциональные возможности проводника Windows пользователям. Эти элементы управления выполняют общие действия или действия, относящиеся к одному выбранному элементу или элементам.



| Управление командами | Описание                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Панель инструментов         | Отображает кнопки для часто используемых команд (Новая версия панели инструментов команды). Параметры настройки включают в себя кнопки с раскрывающимся списком, кнопки разделения, необязательный описательный текст и область переполнения. |
| Имиджевая            | Отображается как отдельный необязательный настраиваемый элемент управления в центре панели инструментов. Он представляет основную команду для текущего контекста.                                                             |
| Строка меню        | Представляет команды через меню.                                                                                                                                                                   |
| Контекстное меню    | Перечисляет контекстно-ориентированное подмножество доступных команд, которые отображаются в результате щелчка правой кнопкой мыши элемента.                                                                               |



 

## <a name="property-and-preview-controls"></a>Свойства и элементы управления предварительным просмотром

Элементы управления "свойство" и "предварительный просмотр" используются для предварительного просмотра элементов, а для просмотра и изменения свойств элементов.



| Control    | Описание                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Preview (Предварительный просмотр)    | Отображает предварительный просмотр выбранного элемента, например эскиза или активного значка.                                                                                                                                                                       |
| Свойства | Отображает свойства выбранного элемента. При выборе нескольких элементов отображается сводка свойств выбранной группы элементов. Для выбора со значением NULL отображается сводка свойств текущей страницы (содержимое ListView). |



 

## <a name="filtering-and-view-controls"></a>Фильтрация и просмотр элементов управления

Элементы управления фильтрацией и представления используются для управления набором элементов в ListView и для изменения представления элементов в ListView.



| Control   | Описание                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filter    | Фильтрует или упорядочивает элементы в ListView на основе свойств, перечисленных в виде столбцов. При щелчке по столбцу выполняется сортировка по этому свойству. |
| вордвхил | Динамически и постепенно фильтрует отображаемые элементы в ListView на основе входной текстовой строки.                      |
| Представление      | Позволяет пользователю изменять режим просмотра элемента управления ListView. Для определения размера значка можно использовать ползунок.                |



 

## <a name="listview-control"></a>Элемент управления ListView

Элемент управления ListView используется для просмотра набора элементов в одном из четырех режимов представления: «сведения», «плитки», «значки» или «Панорама». Элемент управления ListView также позволяет пользователю выбрать и активировать один или несколько элементов.

> [!Caution]  
> Хотя некоторые из этих элементов управления имеют имена и (или) функции, аналогичные элементам управления "Стандартный Windows Presentation Foundation (WPF)", которые находятся в пространстве имен System. Windows. Controls, они являются отдельными классами.

 

Эти отдельные элементы управления работают вместе в основном через события, созданные пользователем или самими элементами управления. В следующей таблице показаны три основные категории событий.



| Категория событий | Например, .                                                       |
|----------------|---------------------------------------------------------------|
| Навигация     | Переход с одной страницы на другую.                               |
| Выбор      | Изменение текущего выделения в ListView.               |
| Просмотр изменений    | Изменение порядка представления или режима просмотра в ListView. |



 

 

 
