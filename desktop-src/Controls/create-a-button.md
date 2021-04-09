---
title: Создание кнопки
description: Для динамического создания кнопок используется функция CreateWindow или CreateWindowEx. В этом разделе показано, как использовать функцию CreateWindow для создания кнопки отправки по умолчанию.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070884"
---
# <a name="how-to-create-a-button"></a><span data-ttu-id="e5a0b-104">Создание кнопки</span><span class="sxs-lookup"><span data-stu-id="e5a0b-104">How to Create a Button</span></span>

<span data-ttu-id="e5a0b-105">Для динамического создания кнопок используется функция [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="e5a0b-105">To create buttons dynamically, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="e5a0b-106">В этом разделе показано, как использовать функцию **CreateWindow** для создания кнопки отправки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5a0b-106">This topic demonstrates how to use the **CreateWindow** function to create a default push button.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e5a0b-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="e5a0b-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e5a0b-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="e5a0b-108">Technologies</span></span>

-   [<span data-ttu-id="e5a0b-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="e5a0b-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e5a0b-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e5a0b-110">Prerequisites</span></span>

-   <span data-ttu-id="e5a0b-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="e5a0b-111">C/C++</span></span>
-   <span data-ttu-id="e5a0b-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="e5a0b-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e5a0b-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="e5a0b-113">Instructions</span></span>


<span data-ttu-id="e5a0b-114">Используйте функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) для создания элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="e5a0b-114">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a button control.</span></span>

<span data-ttu-id="e5a0b-115">В следующем примере C++ параметр *m \_ HWND* является дескриптором родительского окна.</span><span class="sxs-lookup"><span data-stu-id="e5a0b-115">In the following C++ example, the *m\_hwnd* parameter is the handle to the parent window.</span></span> <span data-ttu-id="e5a0b-116">Стиль " [**BS \_ дефпушбуттон**](button-styles.md) " указывает, что должна быть создана кнопка принудительной установки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5a0b-116">The [**BS\_DEFPUSHBUTTON**](button-styles.md) style specifies that a default push button should be created.</span></span> <span data-ttu-id="e5a0b-117">Обратите внимание, что значения размера и расположения должны быть заданы, так как при использовании **\_ Уседефаулт во Вт** . для кнопки устанавливаются нулевые значения.</span><span class="sxs-lookup"><span data-stu-id="e5a0b-117">Note that the size and position values must be specified because using **CW\_USEDEFAULT** for a button sets the values to zero.</span></span>


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a><span data-ttu-id="e5a0b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e5a0b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a0b-119">О кнопках</span><span class="sxs-lookup"><span data-stu-id="e5a0b-119">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="e5a0b-120">Справочник по элементу управления Button</span><span class="sxs-lookup"><span data-stu-id="e5a0b-120">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e5a0b-121">Использование кнопок</span><span class="sxs-lookup"><span data-stu-id="e5a0b-121">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="e5a0b-122">Кнопка</span><span class="sxs-lookup"><span data-stu-id="e5a0b-122">Button</span></span>](buttons.md)
</dt> </dl>

 

 