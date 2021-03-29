---
title: Создание элемента управления "Выбор даты и времени"
description: В этом разделе показано, как динамически создать элемент управления "Выбор даты и времени" (DTP).
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1253a2972b8d858a7440b3e472d5b3aa347b8175
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104261013"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a><span data-ttu-id="9cf61-103">Создание элемента управления "Выбор даты и времени"</span><span class="sxs-lookup"><span data-stu-id="9cf61-103">How to Create a Date and Time Picker Control</span></span>

<span data-ttu-id="9cf61-104">В этом разделе показано, как динамически создать элемент управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="9cf61-104">This topic demonstrates how to dynamically create a date and time picker (DTP) control.</span></span> <span data-ttu-id="9cf61-105">В сопутствующем примере кода C++ создается элемент управления DTP в немодальном диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="9cf61-105">The accompanying C++ code example creates a DTP control in a modeless dialog box.</span></span> <span data-ttu-id="9cf61-106">В нем используется [**стиль \_ Шовноне служб DTS**](date-and-time-picker-control-styles.md) , позволяющий пользователю имитировать деактивацию даты в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="9cf61-106">It uses the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style to enable the user to simulate deactivation of the date within the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9cf61-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="9cf61-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9cf61-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="9cf61-108">Technologies</span></span>

-   [<span data-ttu-id="9cf61-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="9cf61-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9cf61-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="9cf61-110">Prerequisites</span></span>

-   <span data-ttu-id="9cf61-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="9cf61-111">C/C++</span></span>
-   <span data-ttu-id="9cf61-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="9cf61-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9cf61-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="9cf61-113">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="9cf61-114">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="9cf61-114">Step 1:</span></span>

<span data-ttu-id="9cf61-115">Зарегистрируйте класс окна, вызвав функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) и указав бит для \_ классов ICC Date \_ в сопутствующей структуре [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="9cf61-115">Register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the ICC\_DATE\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a><span data-ttu-id="9cf61-116">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="9cf61-116">Step 2:</span></span>

<span data-ttu-id="9cf61-117">Чтобы создать элемент управления DTP, используйте функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="9cf61-117">To create the DTP control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="9cf61-118">Укажите [**\_ класс датетимепикк**](common-control-window-classes.md) в качестве класса окна и передайте этот маркер родительскому диалоговому окну.</span><span class="sxs-lookup"><span data-stu-id="9cf61-118">Specify [**DATETIMEPICK\_CLASS**](common-control-window-classes.md) as the window class, and pass the handle to the parent dialog box.</span></span>

<span data-ttu-id="9cf61-119">В следующем примере кода C++ для создания немодального диалогового окна используется функция [**креатедиалог**](/windows/desktop/api/winuser/nf-winuser-createdialoga) .</span><span class="sxs-lookup"><span data-stu-id="9cf61-119">The following C++ code example uses the [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) function to create a modeless dialog box.</span></span> <span data-ttu-id="9cf61-120">Затем он вызывает **CreateWindowEx** для создания элемента управления DTP.</span><span class="sxs-lookup"><span data-stu-id="9cf61-120">It then calls **CreateWindowEx** to create the DTP control.</span></span>


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a><span data-ttu-id="9cf61-121">Полный пример</span><span class="sxs-lookup"><span data-stu-id="9cf61-121">Complete example</span></span>


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
}

```



## <a name="related-topics"></a><span data-ttu-id="9cf61-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9cf61-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cf61-123">Использование элементов управления "Выбор даты и времени"</span><span class="sxs-lookup"><span data-stu-id="9cf61-123">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="9cf61-124">Справочник по элементу выбора даты и времени</span><span class="sxs-lookup"><span data-stu-id="9cf61-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="9cf61-125">Выбор даты и времени</span><span class="sxs-lookup"><span data-stu-id="9cf61-125">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 