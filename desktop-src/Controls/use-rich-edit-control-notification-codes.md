---
title: Использование расширенных кодов уведомлений элемента управления редактированием
description: Родительское окно элемента управления Rich Edit может обрабатывать коды уведомлений для отслеживания событий, влияющих на элемент управления. Элементы управления Rich Edit поддерживают все коды уведомлений, используемые с элементами управления "поле ввода", а также несколько дополнительных.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103987295"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a><span data-ttu-id="cf8f7-104">Использование расширенных кодов уведомлений элемента управления редактированием</span><span class="sxs-lookup"><span data-stu-id="cf8f7-104">How to Use Rich Edit Control Notification Codes</span></span>

<span data-ttu-id="cf8f7-105">Родительское окно элемента управления Rich Edit может обрабатывать коды уведомлений для отслеживания событий, влияющих на элемент управления.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-105">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="cf8f7-106">Элементы управления Rich Edit поддерживают все коды уведомлений, используемые с элементами управления "поле ввода", а также несколько дополнительных.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-106">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cf8f7-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="cf8f7-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cf8f7-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="cf8f7-108">Technologies</span></span>

-   [<span data-ttu-id="cf8f7-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="cf8f7-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cf8f7-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="cf8f7-110">Prerequisites</span></span>

-   <span data-ttu-id="cf8f7-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="cf8f7-111">C/C++</span></span>
-   <span data-ttu-id="cf8f7-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="cf8f7-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cf8f7-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="cf8f7-113">Instructions</span></span>

### <a name="use-a-rich-edit-control-notification-code"></a><span data-ttu-id="cf8f7-114">Использование расширенного кода уведомления элемента управления редактированием</span><span class="sxs-lookup"><span data-stu-id="cf8f7-114">Use a Rich Edit Control Notification Code</span></span>

<span data-ttu-id="cf8f7-115">Вы можете определить, какие коды уведомлений элемент управления расширенного редактирования отправляет свое родительское окно, установив его маску событий.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-115">You can determine which notification codes a rich edit control sends its parent window by setting its event mask.</span></span> <span data-ttu-id="cf8f7-116">Чтобы задать маску событий для элемента управления расширенного редактирования, используйте сообщение [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8f7-116">To set the event mask for a rich edit control, use the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="cf8f7-117">Вы можете получить текущую маску событий для элемента управления Rich Edit с помощью сообщения [**EM \_ GETEVENTMASK**](em-geteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8f7-117">You can retrieve the current event mask for a rich edit control by using the [**EM\_GETEVENTMASK**](em-geteventmask.md) message.</span></span> <span data-ttu-id="cf8f7-118">Список флагов маски событий см. в разделе [Флаги Маски событий элемента управления Rich Edit](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cf8f7-118">For a list of event mask flags, see [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).</span></span>

<span data-ttu-id="cf8f7-119">Родительское окно элемента управления Rich Edit может фильтровать все входные данные клавиатуры и мыши в элементе управления путем обработки кода уведомления [en \_ мсгфилтер](en-msgfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8f7-119">A rich edit control's parent window can filter all keyboard and mouse input to the control by processing the [EN\_MSGFILTER](en-msgfilter.md) notification code.</span></span> <span data-ttu-id="cf8f7-120">Родительское окно может препятствовать обработке сообщения клавиатуры или мыши или изменению сообщения путем изменения указанной структуры [**мсгфилтер**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) .</span><span class="sxs-lookup"><span data-stu-id="cf8f7-120">The parent window can prevent the keyboard or mouse message from being processed or can change the message by modifying the specified [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure.</span></span>

<span data-ttu-id="cf8f7-121">Приложение может обработать код уведомления [, \_ защищенный коротким](en-protected.md) кодом, чтобы определить, когда пользователь пытается изменить защищенный текст.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-121">An application can process the [EN\_PROTECTED](en-protected.md) notification code to detect when the user attempts to modify protected text.</span></span> <span data-ttu-id="cf8f7-122">Чтобы пометить диапазон текста как защищенный, можно задать защищенный символ.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-122">To mark a range of text as protected, you can set the protected character effect.</span></span>

<span data-ttu-id="cf8f7-123">Вы можете разрешить пользователю удалять файлы в элементе управления Rich Edit, обрабатывая код уведомления [en \_ дропфилес](en-dropfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8f7-123">You can enable the user to drop files in a rich edit control by processing the [EN\_DROPFILES](en-dropfiles.md) notification code.</span></span> <span data-ttu-id="cf8f7-124">Указанная структура [**ендропфилес**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) содержит сведения о удаляемых файлах.</span><span class="sxs-lookup"><span data-stu-id="cf8f7-124">The specified [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure contains information about the files that are being dropped.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf8f7-125">См. также</span><span class="sxs-lookup"><span data-stu-id="cf8f7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf8f7-126">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="cf8f7-126">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="cf8f7-127">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="cf8f7-127">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




