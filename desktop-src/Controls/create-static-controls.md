---
title: Создание статических элементов управления
description: В примере в этом разделе показано, как создать анимированный статический элемент управления.
ms.assetid: D2DA38CB-360C-49EC-90BC-9AFA88C4B751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217135a6590fcee60286d21f00233916c4eba967
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "104487377"
---
# <a name="how-to-create-static-controls"></a><span data-ttu-id="dea92-103">Создание статических элементов управления</span><span class="sxs-lookup"><span data-stu-id="dea92-103">How to Create Static Controls</span></span>

<span data-ttu-id="dea92-104">В примере в этом разделе показано, как создать анимированный статический элемент управления.</span><span class="sxs-lookup"><span data-stu-id="dea92-104">The example in this section demonstrates how to create an animated static control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="dea92-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="dea92-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="dea92-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="dea92-106">Technologies</span></span>

-   [<span data-ttu-id="dea92-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="dea92-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="dea92-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="dea92-108">Prerequisites</span></span>

-   <span data-ttu-id="dea92-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="dea92-109">C/C++</span></span>
-   <span data-ttu-id="dea92-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="dea92-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="dea92-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="dea92-111">Instructions</span></span>

### <a name="create-a-static-control"></a><span data-ttu-id="dea92-112">Создание статического элемента управления</span><span class="sxs-lookup"><span data-stu-id="dea92-112">Create a Static Control</span></span>

<span data-ttu-id="dea92-113">В следующем примере кода используется таймер и STM- [**сообщение \_ сетикон**](stm-seticon.md) для анимации статического элемента управления "значок" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="dea92-113">The following code example uses a timer and the [**STM\_SETICON**](stm-seticon.md) message to animate a static icon control in a dialog box.</span></span>


```C++
#define MAXICONS 3 
#define HALF_SECOND 500

INT_PTR CALLBACK StaticDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam) 
{ 
    static HICON aIcons[MAXICONS]; 
    static UINT i = 0; 
    static UINT idTimer = 1; 

    switch (message) 
    { 
        case WM_INITDIALOG: 

            // Load the icon resources. g_hInst is the global instance handle.
            aIcons[i]   = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON1)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON2)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON3)); 
            
            // Reset the array index.
            i = 0;
 
            // Set a timer. 
            SetTimer(hDlg, idTimer, HALF_SECOND, (TIMERPROC) NULL); 
            return TRUE; 

        case WM_TIMER: 

            // Use STM_SETICON to associate a new icon with the static icon
            // control whenever a WM_TIMER message is received. 
            SendDlgItemMessage(hDlg, IDC_STATIC_ICON, STM_SETICON, 
                (WPARAM) aIcons[i], 0);                    

            // Reset the array index, if necessary.
            if (++i == MAXICONS)
                i = 0;

            return 0; 

        case WM_COMMAND: 
            if (wParam == IDOK 
                || wParam == IDCANCEL) 
            { 
                EndDialog(hDlg, TRUE); 
            } 
            return TRUE; 
 
        case WM_DESTROY: 
            KillTimer(hDlg, idTimer); 

            // Note that it is not necessary to call DestroyIcon here. LoadIcon
            // obtains a shared icon, which is valid as long as the module from 
            // which it was loaded is in memory. 
 
            return 0; 
    } 
    return FALSE; 

    UNREFERENCED_PARAMETER(lParam); 
} 
```



## <a name="remarks"></a><span data-ttu-id="dea92-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dea92-114">Remarks</span></span>

<span data-ttu-id="dea92-115">Идентификатор элемента управления "статический значок" ( \_ статический \_ значок ИДИ) определен в файле глобального заголовка, а значки загружаются из ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="dea92-115">The identifier of the static icon control (IDI\_STATIC\_ICON) is defined in a global header file, and the icons are loaded from the application resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dea92-116">См. также</span><span class="sxs-lookup"><span data-stu-id="dea92-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea92-117">Использование статических элементов управления</span><span class="sxs-lookup"><span data-stu-id="dea92-117">Using Static Controls</span></span>](using-static-controls.md)
</dt> <dt>

<span data-ttu-id="dea92-118">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="dea92-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




