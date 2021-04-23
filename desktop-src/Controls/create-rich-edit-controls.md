---
title: Создание элементов управления с богатыми возможностями редактирования
description: Чтобы создать элемент управления Rich Edit, вызовите функцию CreateWindowEx, указав класс окна редактирования Rich.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070672"
---
# <a name="how-to-create-rich-edit-controls"></a><span data-ttu-id="eda9f-103">Создание элементов управления с богатыми возможностями редактирования</span><span class="sxs-lookup"><span data-stu-id="eda9f-103">How to Create Rich Edit Controls</span></span>

<span data-ttu-id="eda9f-104">Чтобы создать элемент управления Rich Edit, вызовите функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , указав класс окна редактирования Rich.</span><span class="sxs-lookup"><span data-stu-id="eda9f-104">To create a rich edit control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the rich edit window class.</span></span> <span data-ttu-id="eda9f-105">Для Microsoft Rich Edit 4,1 (Msftedit.dll) укажите класс МСФТЕДИТ в \_ качестве класса окна.</span><span class="sxs-lookup"><span data-stu-id="eda9f-105">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT\_CLASS as the window class.</span></span> <span data-ttu-id="eda9f-106">Для всех предыдущих версий укажите класс RICHEDIT \_ .</span><span class="sxs-lookup"><span data-stu-id="eda9f-106">For all previous versions, specify RICHEDIT\_CLASS.</span></span> <span data-ttu-id="eda9f-107">Дополнительные сведения см. в разделе [версии расширенного редактирования](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="eda9f-107">For more information, see [Versions of Rich Edit](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="eda9f-108">Широкие возможности управления редактированием поддерживают большинство стилей окон, используемых с элементами управления "поле ввода", а также дополнительными стилями.</span><span class="sxs-lookup"><span data-stu-id="eda9f-108">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="eda9f-109">Если необходимо разрешить несколько строк текста в элементе управления, следует указать [**\_ Многострочный**](edit-control-styles.md) стиль многостраничного окна ES.</span><span class="sxs-lookup"><span data-stu-id="eda9f-109">You should specify the [**ES\_MULTILINE**](edit-control-styles.md) window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="eda9f-110">Дополнительные сведения см. в разделе [стили элементов управления Rich Edit](rich-edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="eda9f-110">For more information, see [Rich Edit Control Styles](rich-edit-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="eda9f-111">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="eda9f-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="eda9f-112">Технологии</span><span class="sxs-lookup"><span data-stu-id="eda9f-112">Technologies</span></span>

-   [<span data-ttu-id="eda9f-113">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="eda9f-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="eda9f-114">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="eda9f-114">Prerequisites</span></span>

-   <span data-ttu-id="eda9f-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="eda9f-115">C/C++</span></span>
-   <span data-ttu-id="eda9f-116">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="eda9f-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="eda9f-117">Инструкции</span><span class="sxs-lookup"><span data-stu-id="eda9f-117">Instructions</span></span>

### <a name="create-a-rich-edit-control"></a><span data-ttu-id="eda9f-118">Создание элемента управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="eda9f-118">Create a Rich Edit Control</span></span>

<span data-ttu-id="eda9f-119">Следующий пример функции создает элемент управления Rich Edit и инициализирует его текстом.</span><span class="sxs-lookup"><span data-stu-id="eda9f-119">The following example function creates a rich edit control and initializes it with some text.</span></span>


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



<span data-ttu-id="eda9f-120">В Microsoft Visual Studio 2005 и более поздних версиях можно добавить элемент управления Rich Edit в шаблон диалогового окна, перетащив элемент управления из панели элементов.</span><span class="sxs-lookup"><span data-stu-id="eda9f-120">In Microsoft Visual Studio 2005 and later, it is possible to add a rich edit control into a dialog template by dragging the control from the toolbox.</span></span> <span data-ttu-id="eda9f-121">Однако при этом в редакторе диалоговых окон не гарантируется, что нужная библиотека будет загружена перед созданием элемента управления.</span><span class="sxs-lookup"><span data-stu-id="eda9f-121">However, doing this in the dialog editor does not ensure that the required library will be loaded before the control is created.</span></span> <span data-ttu-id="eda9f-122">Чтобы загрузить Riched32.dll, Riched20.dll или Msftedit.dll перед созданием диалогового окна, необходимо вызвать функцию [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="eda9f-122">It is necessary to call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Riched32.dll, Riched20.dll, or Msftedit.dll before the dialog is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="eda9f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eda9f-123">Remarks</span></span>

<span data-ttu-id="eda9f-124">Чтобы использовать стили оформления с этими элементами управления, приложение должно включать манифест и вызывать функцию [**иниткоммонконтролс**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) в начале программы.</span><span class="sxs-lookup"><span data-stu-id="eda9f-124">To use visual styles with these controls, an application must include a manifest and must call the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function at the beginning of the program.</span></span> <span data-ttu-id="eda9f-125">Сведения о визуальных стилях см. в разделе [стили визуальных](themes-overview.md)элементов.</span><span class="sxs-lookup"><span data-stu-id="eda9f-125">For information on visual styles, see [Visual Styles](themes-overview.md).</span></span> <span data-ttu-id="eda9f-126">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eda9f-126">For information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eda9f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="eda9f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eda9f-128">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="eda9f-128">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="eda9f-129">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="eda9f-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 