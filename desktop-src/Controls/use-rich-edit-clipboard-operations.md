---
title: Использование многофункциональных операций редактирования буфера обмена
description: Приложение может вставить содержимое буфера обмена в форматируемый элемент управления с помощью наиболее доступного формата буфера обмена или конкретного формата буфера обмена.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987932"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a><span data-ttu-id="3d336-103">Использование многофункциональных операций редактирования буфера обмена</span><span class="sxs-lookup"><span data-stu-id="3d336-103">How to Use Rich Edit Clipboard Operations</span></span>

<span data-ttu-id="3d336-104">Приложение может вставить содержимое буфера обмена в форматируемый элемент управления с помощью наиболее доступного формата буфера обмена или конкретного формата буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="3d336-104">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="3d336-105">Кроме того, можно определить, может ли элемент управления с расширенным редактированием вставлять формат буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="3d336-105">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3d336-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="3d336-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3d336-107">Технологии</span><span class="sxs-lookup"><span data-stu-id="3d336-107">Technologies</span></span>

-   [<span data-ttu-id="3d336-108">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="3d336-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3d336-109">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="3d336-109">Prerequisites</span></span>

-   <span data-ttu-id="3d336-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="3d336-110">C/C++</span></span>
-   <span data-ttu-id="3d336-111">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="3d336-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3d336-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="3d336-112">Instructions</span></span>

### <a name="use-a-rich-edit-clipboard-operation"></a><span data-ttu-id="3d336-113">Использование операции редактирования буфера обмена с богатыми возможностями</span><span class="sxs-lookup"><span data-stu-id="3d336-113">Use a Rich Edit Clipboard Operation</span></span>

<span data-ttu-id="3d336-114">Как и в случае с элементом управления "поле ввода", можно скопировать или вырезать содержимое текущего выделения, используя сообщение [**WM \_ Copy**](/windows/desktop/dataxchg/wm-copy) или [**WM \_ Cut**](/windows/desktop/dataxchg/wm-cut) .</span><span class="sxs-lookup"><span data-stu-id="3d336-114">As with an edit control, you can copy or cut the contents of the current selection by using the [**WM\_COPY**](/windows/desktop/dataxchg/wm-copy) or [**WM\_CUT**](/windows/desktop/dataxchg/wm-cut) message.</span></span> <span data-ttu-id="3d336-115">Аналогичным образом можно вставить содержимое буфера обмена в форматируемый элемент управления, используя сообщение [**\_ вставки WM**](/windows/desktop/dataxchg/wm-paste) .</span><span class="sxs-lookup"><span data-stu-id="3d336-115">Similarly, you can paste the contents of the clipboard into a rich edit control by using the [**WM\_PASTE**](/windows/desktop/dataxchg/wm-paste) message.</span></span> <span data-ttu-id="3d336-116">Элемент управления вставит первый доступный формат, который он распознает, и, вероятно, является наиболее описательным форматом.</span><span class="sxs-lookup"><span data-stu-id="3d336-116">The control pastes the first available format that it recognizes, which presumably is the most descriptive format.</span></span>

<span data-ttu-id="3d336-117">Чтобы вставить конкретный формат буфера обмена, можно использовать сообщение [**EM \_ PASTESPECIAL**](em-pastespecial.md) .</span><span class="sxs-lookup"><span data-stu-id="3d336-117">To paste a specific clipboard format, you can use the [**EM\_PASTESPECIAL**](em-pastespecial.md) message.</span></span> <span data-ttu-id="3d336-118">Это сообщение полезно для приложений с командой **Специальная вставка** , которая позволяет пользователю выбрать формат буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="3d336-118">This message is useful for applications with a **Paste Special** command that enables the user to select the clipboard format.</span></span> <span data-ttu-id="3d336-119">Чтобы определить, распознается ли данный формат элементом управления, можно использовать сообщение [**EM \_ канпасте**](em-canpaste.md) .</span><span class="sxs-lookup"><span data-stu-id="3d336-119">You can use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether a given format is recognized by the control.</span></span>

<span data-ttu-id="3d336-120">Кроме того, можно использовать сообщение [**EM \_ канпасте**](em-canpaste.md) , чтобы определить, распознан ли любой доступный формат буфера обмена элементом управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3d336-120">You can also use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether any available clipboard format is recognized by a rich edit control.</span></span> <span data-ttu-id="3d336-121">Это сообщение полезно при обработке сообщения [**WM \_ инитменупопуп**](/windows/desktop/menurc/wm-initmenupopup) .</span><span class="sxs-lookup"><span data-stu-id="3d336-121">This message is useful when processing the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message.</span></span> <span data-ttu-id="3d336-122">В зависимости от того, может ли элемент управления вставлять любой доступный формат, в приложении может быть включена или серая команда **вставки** .</span><span class="sxs-lookup"><span data-stu-id="3d336-122">An application might enable or gray its **Paste** command depending on whether the control can paste any available format.</span></span>

<span data-ttu-id="3d336-123">Элементы управления Rich Edit регистрируют два формата буфера обмена:</span><span class="sxs-lookup"><span data-stu-id="3d336-123">Rich edit controls register two clipboard formats:</span></span>

-   <span data-ttu-id="3d336-124">Формат форматированного текста</span><span class="sxs-lookup"><span data-stu-id="3d336-124">Rich Text Format</span></span>
-   <span data-ttu-id="3d336-125">Формат форматированного текста без объектов</span><span class="sxs-lookup"><span data-stu-id="3d336-125">Rich Text Format Without Objects</span></span>
-   <span data-ttu-id="3d336-126">Текст и объекты RichEdit</span><span class="sxs-lookup"><span data-stu-id="3d336-126">RichEdit Text and Objects</span></span>

<span data-ttu-id="3d336-127">Приложение может зарегистрировать эти форматы с помощью функции [**регистерклипбоардформат**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) , указав значения параметров "CF \_ RTF", "CF \_ РТФНУБЖС" и "CF ретекстобж" \_ .</span><span class="sxs-lookup"><span data-stu-id="3d336-127">An application can register these formats by using the [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) function, specifying the CF\_RTF, CF\_RTFNOOBJS, and CF\_RETEXTOBJ values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d336-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3d336-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d336-129">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="3d336-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="3d336-130">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="3d336-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 