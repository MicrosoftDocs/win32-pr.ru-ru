---
title: Получение и задание сочетания клавиш
description: В этом разделе показано, как извлечь или задать сочетание клавиш для элемента управления горячего ключа.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105654397"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a><span data-ttu-id="674c8-103">Получение и задание сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="674c8-103">How to Retrieve and Set a Hot Key</span></span>

<span data-ttu-id="674c8-104">В этом разделе показано, как извлечь или задать сочетание клавиш для элемента управления горячего ключа.</span><span class="sxs-lookup"><span data-stu-id="674c8-104">This topic demonstrates how to retrieve or set the key combination for a hot key control.</span></span> <span data-ttu-id="674c8-105">Сообщение [**ХКМ \_ сесоткэй**](hkm-sethotkey.md) позволяет приложению установить сочетание клавиш для элемента управления "горячая клавиша".</span><span class="sxs-lookup"><span data-stu-id="674c8-105">The [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message allows an application to set the hot key combination for a hot key control.</span></span> <span data-ttu-id="674c8-106">Приложения используют сообщение [**ХКМ- \_ горячих**](hkm-gethotkey.md) клавиш, чтобы получить виртуальный код ключа и флаги модификатора для сочетания клавиш, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="674c8-106">Applications use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier flags of the hot key that is chosen by the user.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="674c8-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="674c8-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="674c8-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="674c8-108">Technologies</span></span>

-   [<span data-ttu-id="674c8-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="674c8-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="674c8-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="674c8-110">Prerequisites</span></span>

-   <span data-ttu-id="674c8-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="674c8-111">C/C++</span></span>
-   <span data-ttu-id="674c8-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="674c8-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="674c8-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="674c8-113">Instructions</span></span>


<span data-ttu-id="674c8-114">Используйте сообщение [**ХКМ- \_ горячих**](hkm-gethotkey.md) клавиш, чтобы получить ключ виртуального ключа и клавиши-модификаторы, описывающие горячие клавиши, выбранные пользователем.</span><span class="sxs-lookup"><span data-stu-id="674c8-114">Use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier keys that describe a hot key chosen by the user.</span></span> <span data-ttu-id="674c8-115">Используйте сообщение [**ХКМ \_ сесоткэй**](hkm-sethotkey.md) , чтобы задать эти значения для сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="674c8-115">Use the [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message to set those values for a hot key.</span></span>

<span data-ttu-id="674c8-116">В следующем примере кода C++ определяемая приложением функция использует сообщение [**ХКМ- \_ горячих**](hkm-gethotkey.md) клавиш для получения сочетания клавиш из элемента управления горячих клавиш, а затем использует сообщение [**WM \_ сесоткэй**](/windows/desktop/inputdev/wm-sethotkey) для установки глобального горячего ключа.</span><span class="sxs-lookup"><span data-stu-id="674c8-116">In the following C++ code example, the application-defined function uses the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve a key combination from a hot key control and then uses the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message to set a global hot key.</span></span> <span data-ttu-id="674c8-117">Обратите внимание, что нельзя задать глобальную горячую клавишу для окна, имеющего стиль [**\_ дочернего окна WS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="674c8-117">Note that you cannot set a global hot key for a window that has the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) window style.</span></span>



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="674c8-118">См. также</span><span class="sxs-lookup"><span data-stu-id="674c8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="674c8-119">Ссылка на элемент управления ключами</span><span class="sxs-lookup"><span data-stu-id="674c8-119">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="674c8-120">Сведения об элементах управления горячей клавиши</span><span class="sxs-lookup"><span data-stu-id="674c8-120">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="674c8-121">Использование элементов управления горячими ключами</span><span class="sxs-lookup"><span data-stu-id="674c8-121">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 