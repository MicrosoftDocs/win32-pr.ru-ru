---
title: Как использовать уведомления SysLink
description: Существует два сообщения с уведомлениями, связанные с элементом управления SysLink \ 8212; один для мыши (NM \_ Click (Syslink)), а второй для клавиатуры (NM \_ Return).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "105654275"
---
# <a name="how-to-use-syslink-notifications"></a><span data-ttu-id="46259-103">Как использовать уведомления SysLink</span><span class="sxs-lookup"><span data-stu-id="46259-103">How to Use SysLink Notifications</span></span>

<span data-ttu-id="46259-104">С элементом управления SysLink связаны два сообщения уведомления: один для мыши ([NM \_ Click (Syslink)](nm-click-syslink.md)) и один для клавиатуры ([NM \_ return](nm-return.md)).</span><span class="sxs-lookup"><span data-stu-id="46259-104">There are two notification messages associated with the SysLink control—one for the mouse ([NM\_CLICK (syslink)](nm-click-syslink.md)), and one for the keyboard ([NM\_RETURN](nm-return.md)).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="46259-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="46259-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="46259-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="46259-106">Technologies</span></span>

-   [<span data-ttu-id="46259-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="46259-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="46259-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="46259-108">Prerequisites</span></span>

-   <span data-ttu-id="46259-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="46259-109">C/C++</span></span>
-   <span data-ttu-id="46259-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="46259-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="46259-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="46259-111">Instructions</span></span>

### <a name="use-syslink-notifications"></a><span data-ttu-id="46259-112">Использование уведомлений SysLink</span><span class="sxs-lookup"><span data-stu-id="46259-112">Use SysLink Notifications</span></span>

<span data-ttu-id="46259-113">В следующем примере кода показано, как обрабатывать уведомления SysLink, которые создаются, когда пользователь щелкает одну из двух ссылок в [предыдущем примере](create-syslink-controls.md).</span><span class="sxs-lookup"><span data-stu-id="46259-113">The following example code shows how to process the SysLink notifications that are generated when the user clicks either of the two links in the [previous example](create-syslink-controls.md).</span></span> <span data-ttu-id="46259-114">Когда пользователь щелкает URL-адрес в Интернете, связанная веб-страница открывается в браузере по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46259-114">When the user clicks the Internet URL, the associated webpage opens in the default browser.</span></span> <span data-ttu-id="46259-115">Когда пользователь щелкает гиперссылку, определяемую приложением, отображается окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="46259-115">When the user clicks the application-defined hyperlink, a message box is displayed.</span></span>


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a><span data-ttu-id="46259-116">См. также</span><span class="sxs-lookup"><span data-stu-id="46259-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46259-117">Использование элементов управления SysLink</span><span class="sxs-lookup"><span data-stu-id="46259-117">Using SysLink Controls</span></span>](using-syslink-controls.md)
</dt> <dt>

<span data-ttu-id="46259-118">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="46259-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




