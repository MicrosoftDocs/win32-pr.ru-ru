---
title: Создание элементов управления SysLink
description: Вы реализуете гиперссылки элемента управления SysLink через разметку в строке инициализации элемента управления или отправляете \_ сообщение LM сетитем.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794142"
---
# <a name="how-to-create-syslink-controls"></a><span data-ttu-id="69b8e-103">Создание элементов управления SysLink</span><span class="sxs-lookup"><span data-stu-id="69b8e-103">How to Create SysLink Controls</span></span>

<span data-ttu-id="69b8e-104">Вы реализуете гиперссылки элемента управления SysLink через разметку в строке инициализации элемента управления или отправляете сообщение [**LM \_ сетитем**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="69b8e-104">You implement the SysLink control's hyperlinks through markup in the control's initialization string, or by sending it a [**LM\_SETITEM**](lm-setitem.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="69b8e-105">Перед созданием элементов управления SysLink необходимо вызвать функцию [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , указав \_ класс компоновки ICC \_ .</span><span class="sxs-lookup"><span data-stu-id="69b8e-105">Before creating SysLink controls, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_LINK\_CLASS.</span></span>

 

<span data-ttu-id="69b8e-106">Чтобы создать SysLink, вызовите функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указав класс окна [**\_ связи WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="69b8e-106">To create a SysLink, call the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_LINK**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="69b8e-107">Параметр *лпвиндовнаме* , который является общим для этих функций, указывает указатель на строку, завершающуюся нулем, которая содержит помеченный текст для вывода.</span><span class="sxs-lookup"><span data-stu-id="69b8e-107">The *lpWindowName* parameter that is common to these functions specifies a pointer to a zero-terminated string that contains the marked-up text to display.</span></span> <span data-ttu-id="69b8e-108">Стили окон, определенные для элементов управления SysLink, см. в разделе [стили элементов управления Syslink](syslink-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="69b8e-108">For window styles particular to SysLink controls, see [SysLink Control Styles](syslink-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="69b8e-109">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="69b8e-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="69b8e-110">Технологии</span><span class="sxs-lookup"><span data-stu-id="69b8e-110">Technologies</span></span>

-   [<span data-ttu-id="69b8e-111">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="69b8e-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="69b8e-112">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="69b8e-112">Prerequisites</span></span>

-   <span data-ttu-id="69b8e-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="69b8e-113">C/C++</span></span>
-   <span data-ttu-id="69b8e-114">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="69b8e-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="69b8e-115">Инструкции</span><span class="sxs-lookup"><span data-stu-id="69b8e-115">Instructions</span></span>

### <a name="create-a-syslink-control"></a><span data-ttu-id="69b8e-116">Создание элемента управления SysLink</span><span class="sxs-lookup"><span data-stu-id="69b8e-116">Create a SysLink Control</span></span>

<span data-ttu-id="69b8e-117">В следующем примере кода создается элемент управления SysLink, отображающий две гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="69b8e-117">The following example code creates a SysLink control that displays two hyperlinks.</span></span> <span data-ttu-id="69b8e-118">Первая гиперссылка является URL-адресом в Интернете, а вторая — определяемой приложением.</span><span class="sxs-lookup"><span data-stu-id="69b8e-118">The first hyperlink is an Internet URL, and the second is application-defined.</span></span>


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a><span data-ttu-id="69b8e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69b8e-119">Remarks</span></span>

<span data-ttu-id="69b8e-120">Предполагается, что [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) уже вызван.</span><span class="sxs-lookup"><span data-stu-id="69b8e-120">It is assumed that [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) has already been called.</span></span>

<span data-ttu-id="69b8e-121">Указание стиля [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) гарантирует, что пользователь сможет выбрать ссылку с помощью перехода по ссылкам и нажать клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="69b8e-121">Specifying the [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) style ensures that the user will be able to select a link by tabbing to it and pressing the Enter key.</span></span>

<span data-ttu-id="69b8e-122">Версия 6 ComCtl32.dll поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="69b8e-122">Version 6 of ComCtl32.dll supports Unicode only.</span></span> <span data-ttu-id="69b8e-123">Таким образом, нельзя создавать ANSI-версии элементов управления SysLink — только Юникод.</span><span class="sxs-lookup"><span data-stu-id="69b8e-123">Therefore, you cannot create ANSI versions of SysLink controls—only Unicode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69b8e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="69b8e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69b8e-125">Использование элементов управления SysLink</span><span class="sxs-lookup"><span data-stu-id="69b8e-125">Using SysLink Controls</span></span>](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

<span data-ttu-id="69b8e-126">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="69b8e-126">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 