---
title: Создание подсказки для элемента управления
description: Следующий пример функции создает подсказку и связывает ее с элементом управления, чей идентификатор ресурса передается.
ms.assetid: FDA3B2A0-1256-4DAC-86CF-8F123894E760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f341c1be1e749c4e0d6f18caf97a3f897cf429e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067551"
---
# <a name="how-to-create-a-tooltip-for-a-control"></a><span data-ttu-id="d4ec9-103">Создание подсказки для элемента управления</span><span class="sxs-lookup"><span data-stu-id="d4ec9-103">How to Create a Tooltip for a Control</span></span>

<span data-ttu-id="d4ec9-104">Следующий пример функции создает подсказку и связывает ее с элементом управления, чей идентификатор ресурса передается.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-104">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d4ec9-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="d4ec9-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d4ec9-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="d4ec9-106">Technologies</span></span>

-   [<span data-ttu-id="d4ec9-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="d4ec9-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d4ec9-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="d4ec9-108">Prerequisites</span></span>

-   <span data-ttu-id="d4ec9-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="d4ec9-109">C/C++</span></span>
-   <span data-ttu-id="d4ec9-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="d4ec9-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d4ec9-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="d4ec9-111">Instructions</span></span>

### <a name="create-a-tooltip-for-a-control"></a><span data-ttu-id="d4ec9-112">Создание подсказки для элемента управления</span><span class="sxs-lookup"><span data-stu-id="d4ec9-112">Create a Tooltip for a Control</span></span>

<span data-ttu-id="d4ec9-113">Следующий пример функции создает подсказку и связывает ее с элементом управления, чей идентификатор ресурса передается.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-113">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span>


```C++
// Description:
//   Creates a tooltip for an item in a dialog box. 
// Parameters:
//   idTool - identifier of an dialog box item.
//   nDlg - window handle of the dialog box.
//   pszText - string to use as the tooltip text.
// Returns:
//   The handle to the tooltip.
//
HWND CreateToolTip(int toolID, HWND hDlg, PTSTR pszText)
{
    if (!toolID || !hDlg || !pszText)
    {
        return FALSE;
    }
    // Get the window of the tool.
    HWND hwndTool = GetDlgItem(hDlg, toolID);
    
    // Create the tooltip. g_hInst is the global instance handle.
    HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                              WS_POPUP |TTS_ALWAYSTIP | TTS_BALLOON,
                              CW_USEDEFAULT, CW_USEDEFAULT,
                              CW_USEDEFAULT, CW_USEDEFAULT,
                              hDlg, NULL, 
                              g_hInst, NULL);
    
   if (!hwndTool || !hwndTip)
   {
       return (HWND)NULL;
   }                              
                              
    // Associate the tooltip with the tool.
    TOOLINFO toolInfo = { 0 };
    toolInfo.cbSize = sizeof(toolInfo);
    toolInfo.hwnd = hDlg;
    toolInfo.uFlags = TTF_IDISHWND | TTF_SUBCLASS;
    toolInfo.uId = (UINT_PTR)hwndTool;
    toolInfo.lpszText = pszText;
    SendMessage(hwndTip, TTM_ADDTOOL, 0, (LPARAM)&toolInfo);

    return hwndTip;
}
```



## <a name="related-topics"></a><span data-ttu-id="d4ec9-114">См. также</span><span class="sxs-lookup"><span data-stu-id="d4ec9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4ec9-115">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="d4ec9-115">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




