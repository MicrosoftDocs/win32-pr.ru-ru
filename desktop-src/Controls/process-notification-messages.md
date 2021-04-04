---
title: Обработка сообщений с уведомлениями
description: Страница свойств отправляет сообщения WM \_ Notify для получения сведений со страниц и для уведомления страниц действий пользователя.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789355"
---
# <a name="how-to-process-notification-messages"></a><span data-ttu-id="0dd51-103">Обработка сообщений с уведомлениями</span><span class="sxs-lookup"><span data-stu-id="0dd51-103">How to Process Notification Messages</span></span>

<span data-ttu-id="0dd51-104">Страница свойств отправляет сообщения [**WM \_ Notify**](wm-notify.md) для получения сведений со страниц и для уведомления страниц действий пользователя.</span><span class="sxs-lookup"><span data-stu-id="0dd51-104">A property sheet sends [**WM\_NOTIFY**](wm-notify.md) messages to retrieve information from the pages and to notify the pages of user actions.</span></span>

<span data-ttu-id="0dd51-105">Параметр *lParam* сообщения является адресом структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , которая содержит маркер диалогового окна страницы свойств, обработчика для диалогового окна страница и код уведомления.</span><span class="sxs-lookup"><span data-stu-id="0dd51-105">The *lParam* parameter of the message is the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, which contains the handle to the property sheet dialog box, the handle to the page dialog box, and a notification code.</span></span> <span data-ttu-id="0dd51-106">Страница должна отвечать на некоторые сообщения уведомления, присвоив параметру DWL \_ мсгресулт страницы значение **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="0dd51-106">The page must respond to some notification messages by setting the DWL\_MSGRESULT value of the page to either **TRUE** or **FALSE**.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0dd51-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="0dd51-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0dd51-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="0dd51-108">Technologies</span></span>

-   [<span data-ttu-id="0dd51-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="0dd51-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0dd51-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="0dd51-110">Prerequisites</span></span>

-   <span data-ttu-id="0dd51-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="0dd51-111">C/C++</span></span>
-   <span data-ttu-id="0dd51-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="0dd51-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0dd51-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="0dd51-113">Instructions</span></span>

### <a name="process-notification-messages"></a><span data-ttu-id="0dd51-114">Обработка сообщений уведомления</span><span class="sxs-lookup"><span data-stu-id="0dd51-114">Process Notification Messages</span></span>

<span data-ttu-id="0dd51-115">Следующий пример является фрагментом кода из процедуры диалогового окна для страницы.</span><span class="sxs-lookup"><span data-stu-id="0dd51-115">The following example is a code fragment from the dialog box procedure for a page.</span></span> <span data-ttu-id="0dd51-116">В нем показано, как обработать код уведомления [ \_ справки PSN](psn-help.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd51-116">It shows how to process the [PSN\_HELP](psn-help.md) notification code.</span></span>


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a><span data-ttu-id="0dd51-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0dd51-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dd51-118">Использование страниц свойств</span><span class="sxs-lookup"><span data-stu-id="0dd51-118">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

<span data-ttu-id="0dd51-119">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="0dd51-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




