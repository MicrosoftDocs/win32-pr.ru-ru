---
title: Динамическое добавление меток для кнопок панели инструментов
description: Можно назначить текст существующей кнопке с помощью \_ сообщения СЕТБУТТОНИНФО ТБ.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "104487376"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a><span data-ttu-id="b4ff9-103">Динамическое добавление меток для кнопок панели инструментов</span><span class="sxs-lookup"><span data-stu-id="b4ff9-103">How to Dynamically Label Toolbar Buttons</span></span>

<span data-ttu-id="b4ff9-104">Можно назначить текст существующей кнопке с помощью сообщения [**\_ сетбуттонинфо ТБ**](tb-setbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="b4ff9-104">You can assign text to an existing button by using the [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b4ff9-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="b4ff9-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b4ff9-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="b4ff9-106">Technologies</span></span>

-   [<span data-ttu-id="b4ff9-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="b4ff9-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b4ff9-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="b4ff9-108">Prerequisites</span></span>

-   <span data-ttu-id="b4ff9-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="b4ff9-109">C/C++</span></span>
-   <span data-ttu-id="b4ff9-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="b4ff9-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b4ff9-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="b4ff9-111">Instructions</span></span>

### <a name="dynamically-label-a-toolbar-button"></a><span data-ttu-id="b4ff9-112">Динамическое добавление метки для кнопки панели инструментов</span><span class="sxs-lookup"><span data-stu-id="b4ff9-112">Dynamically Label a Toolbar Button</span></span>

<span data-ttu-id="b4ff9-113">В следующем примере показано, как изменить текст третьей кнопки в предыдущих примерах с **Save** на **Сохранить как**.</span><span class="sxs-lookup"><span data-stu-id="b4ff9-113">The following example demonstrates how to change the text of the third button in the previous examples from **Save** to **Save As**.</span></span>


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a><span data-ttu-id="b4ff9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4ff9-114">Remarks</span></span>

<span data-ttu-id="b4ff9-115">Изменение текста кнопки с помощью [**ТБ \_ сетбуттонинфо**](tb-setbuttoninfo.md) не влияет на строку, назначенную этой кнопке в списке внутренних строк.</span><span class="sxs-lookup"><span data-stu-id="b4ff9-115">Changing a button's text by using [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) does not affect the string that is assigned to that button in the internal string list.</span></span>

<span data-ttu-id="b4ff9-116">При добавлении строки кнопки панели инструментов во внутренний текстовый список невозможно получить индекс этой строки путем вызова [ТБН \_ жетбуттонинфо](tbn-getbuttoninfo.md)— вместо этого следует использовать сообщение о [**\_ кнопке ТБ**](tb-getbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="b4ff9-116">If you add a toolbar button string to the internal text list, you cannot retrieve the index of that string by calling [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md)—you must use the [**TB\_GETBUTTON**](tb-getbutton.md) message instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4ff9-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b4ff9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4ff9-118">Использование элементов управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="b4ff9-118">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="b4ff9-119">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="b4ff9-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




