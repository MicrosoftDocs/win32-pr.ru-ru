---
title: Создание ссылки на команду
description: В этом разделе описывается один из способов создания ссылки на команду.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488393"
---
# <a name="how-to-create-a-command-link"></a><span data-ttu-id="38db8-103">Создание ссылки на команду</span><span class="sxs-lookup"><span data-stu-id="38db8-103">How to Create a Command Link</span></span>

<span data-ttu-id="38db8-104">В этом разделе описывается один из способов создания ссылки на команду.</span><span class="sxs-lookup"><span data-stu-id="38db8-104">This topic describes one way to create a command link.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="38db8-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="38db8-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="38db8-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="38db8-106">Technologies</span></span>

-   [<span data-ttu-id="38db8-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="38db8-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="38db8-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="38db8-108">Prerequisites</span></span>

-   <span data-ttu-id="38db8-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="38db8-109">C/C++</span></span>
-   <span data-ttu-id="38db8-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="38db8-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="38db8-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="38db8-111">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-command-link-button"></a><span data-ttu-id="38db8-112">Шаг 1. Создайте экземпляр кнопки «ссылка на команду».</span><span class="sxs-lookup"><span data-stu-id="38db8-112">Step 1: Create an instance of the command link button.</span></span>

<span data-ttu-id="38db8-113">В следующем примере кода C++ константа стиля " [**BS" \_ коммандлинк**](button-styles.md) Указывает кнопку как кнопку Command Link.</span><span class="sxs-lookup"><span data-stu-id="38db8-113">In the following C++ code example, the style constant [**BS\_COMMANDLINK**](button-styles.md) specifies the button as a command link button.</span></span>


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a><span data-ttu-id="38db8-114">Шаг 2. Задание метки и текста описания для ссылки на команду</span><span class="sxs-lookup"><span data-stu-id="38db8-114">Step 2: Set the command link label and explanation text</span></span>

<span data-ttu-id="38db8-115">Используйте функцию [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , чтобы задать метку ссылки на команду и дополнительный текст с помощью сообщения [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) и сообщения [**BCM \_ сетноте**](bcm-setnote.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="38db8-115">Use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to set the command link label and supplementary text via the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message and the [**BCM\_SETNOTE**](bcm-setnote.md) message, respectively.</span></span>


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a><span data-ttu-id="38db8-116">См. также</span><span class="sxs-lookup"><span data-stu-id="38db8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38db8-117">О кнопках</span><span class="sxs-lookup"><span data-stu-id="38db8-117">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="38db8-118">Справочник по элементу управления Button</span><span class="sxs-lookup"><span data-stu-id="38db8-118">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="38db8-119">Использование кнопок</span><span class="sxs-lookup"><span data-stu-id="38db8-119">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="38db8-120">Кнопка</span><span class="sxs-lookup"><span data-stu-id="38db8-120">Button</span></span>](buttons.md)
</dt> </dl>

 

 