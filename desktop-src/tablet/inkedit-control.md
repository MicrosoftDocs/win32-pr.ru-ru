---
description: Элемент управления InkEdit обеспечивает простой способ захвата, распознавания и показа рукописных данных.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: Элемент управления InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910756"
---
# <a name="inkedit-control"></a><span data-ttu-id="c8577-103">Элемент управления InkEdit</span><span class="sxs-lookup"><span data-stu-id="c8577-103">InkEdit Control</span></span>

<span data-ttu-id="c8577-104">Элемент управления [InkEdit](inkedit-control-reference.md) обеспечивает простой способ захвата, распознавания и показа рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="c8577-104">The [InkEdit](inkedit-control-reference.md) control provides an easy way to capture, recognize, and display ink.</span></span>

<span data-ttu-id="c8577-105">Эта реализация элемента управления [InkEdit](inkedit-control-reference.md) основана на элементе управления [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="c8577-105">This implementation of the [InkEdit](inkedit-control-reference.md) control is based on the [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) control.</span></span> <span data-ttu-id="c8577-106">Управляемая (платформа .NET Framework) реализация [InkEdit](/previous-versions/ms835842(v=msdn.10)) основана на элементе управления [**RichTextBox**](/previous-versions/windows/) .</span><span class="sxs-lookup"><span data-stu-id="c8577-106">The managed (.NET Framework) implementation of [InkEdit](/previous-versions/ms835842(v=msdn.10)) is based on the [**RichTextBox**](/previous-versions/windows/) control.</span></span>

<span data-ttu-id="c8577-107">Основной целью элемента управления [InkEdit](inkedit-control-reference.md) является получение рукописного ввода, его распознавание и отображение в текстовой форме.</span><span class="sxs-lookup"><span data-stu-id="c8577-107">The primary purpose of the [InkEdit](inkedit-control-reference.md) control is to collect ink, recognize it, and display it in text form.</span></span> <span data-ttu-id="c8577-108">Кроме того, он поддерживает отображение рукописного ввода в виде внедренного объекта с возможностями форматирования текста, такими как полужирный и подчеркнутый.</span><span class="sxs-lookup"><span data-stu-id="c8577-108">Additionally, it supports displaying ink as an embedded object with text formatting capabilities, such as bold and underline.</span></span>

## <a name="gestures-and-correction"></a><span data-ttu-id="c8577-109">Жесты и исправление</span><span class="sxs-lookup"><span data-stu-id="c8577-109">Gestures and Correction</span></span>

<span data-ttu-id="c8577-110">[InkEdit](inkedit-control-reference.md) поддерживает следующие жесты.</span><span class="sxs-lookup"><span data-stu-id="c8577-110">[InkEdit](inkedit-control-reference.md) supports the following gestures.</span></span>



| <span data-ttu-id="c8577-111">жесты</span><span class="sxs-lookup"><span data-stu-id="c8577-111">Gesture</span></span>                                                                    | <span data-ttu-id="c8577-112">Имя жеста</span><span class="sxs-lookup"><span data-stu-id="c8577-112">Gesture Name</span></span>              | <span data-ttu-id="c8577-113">Действие</span><span class="sxs-lookup"><span data-stu-id="c8577-113">Action</span></span>               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![жест вниз слева](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | <span data-ttu-id="c8577-115">Вниз, слева</span><span class="sxs-lookup"><span data-stu-id="c8577-115">Down-left</span></span><br/>      | <span data-ttu-id="c8577-116">ВВОД</span><span class="sxs-lookup"><span data-stu-id="c8577-116">Enter</span></span><br/>     |
| ![жест нажатия левой клавиши Long](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | <span data-ttu-id="c8577-118">Вниз-слева-длинное</span><span class="sxs-lookup"><span data-stu-id="c8577-118">Down-left-long</span></span><br/> | <span data-ttu-id="c8577-119">ВВОД</span><span class="sxs-lookup"><span data-stu-id="c8577-119">Enter</span></span><br/>     |
| ![жест справа направо](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | <span data-ttu-id="c8577-121">Вверх и вправо</span><span class="sxs-lookup"><span data-stu-id="c8577-121">Up-right</span></span><br/>       | <span data-ttu-id="c8577-122">Вкладка</span><span class="sxs-lookup"><span data-stu-id="c8577-122">Tab</span></span><br/>       |
| ![жест, подходящий для длительного времени.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | <span data-ttu-id="c8577-124">До правого времени</span><span class="sxs-lookup"><span data-stu-id="c8577-124">Up-right-long</span></span><br/>  | <span data-ttu-id="c8577-125">Вкладка</span><span class="sxs-lookup"><span data-stu-id="c8577-125">Tab</span></span><br/>       |
| ![правый жест](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | <span data-ttu-id="c8577-127">Правый</span><span class="sxs-lookup"><span data-stu-id="c8577-127">Right</span></span><br/>          | <span data-ttu-id="c8577-128">Пробел</span><span class="sxs-lookup"><span data-stu-id="c8577-128">Space</span></span><br/>     |
| ![левый жест](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | <span data-ttu-id="c8577-130">Левый</span><span class="sxs-lookup"><span data-stu-id="c8577-130">Left</span></span><br/>           | <span data-ttu-id="c8577-131">Отмена</span><span class="sxs-lookup"><span data-stu-id="c8577-131">Backspace</span></span><br/> |



 

<span data-ttu-id="c8577-132">События жестов, которые можно обменять, содержат жесты, штрихи и сведения о курсоре, которые можно использовать для отправки текста в [InkEdit](inkedit-control-reference.md) или размещения данных в буфере обмена.</span><span class="sxs-lookup"><span data-stu-id="c8577-132">Gesture events that you can handle contain gesture, stroke, and cursor information you can use to send text to [InkEdit](inkedit-control-reference.md) or place data on the clipboard.</span></span>

<span data-ttu-id="c8577-133">[InkEdit](inkedit-control-reference.md) также предоставляет пользовательский интерфейс исправления, позволяющий пользователям просматривать и выбирать из альтернатив, использовать экранную клавиатуру и распознаватели символов/букв/блоков.</span><span class="sxs-lookup"><span data-stu-id="c8577-133">[InkEdit](inkedit-control-reference.md) also provides a correction user interface that enables users to view and select from alternates, use the on-screen keyboard, and character/letter/block recognizers.</span></span>

## <a name="other-details"></a><span data-ttu-id="c8577-134">Другие сведения</span><span class="sxs-lookup"><span data-stu-id="c8577-134">Other Details</span></span>

<span data-ttu-id="c8577-135">Объект [InkEdit](inkedit-control-reference.md) хорошо работает в виде сценария для одной строки, а также для многострочного текстового ввода и редактирования.</span><span class="sxs-lookup"><span data-stu-id="c8577-135">[InkEdit](inkedit-control-reference.md) is designed to work well in a form scenario for single line as well as multiline text entry and editing.</span></span> <span data-ttu-id="c8577-136">Основным предполагаемым использованием для InkEdit является получение текстового ввода от пользователя в виде рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="c8577-136">The primary intended use for InkEdit is to get text input from a user in the form of handwriting.</span></span> <span data-ttu-id="c8577-137">По умолчанию вводимые рукописные данные распознаются, а текст вставляется в свое место.</span><span class="sxs-lookup"><span data-stu-id="c8577-137">By default, ink input is recognized and text is inserted in its place.</span></span> <span data-ttu-id="c8577-138">Пользовательский интерфейс по умолчанию для InkEdit напоминает элемент управления [**RichTextBox**](/previous-versions/windows/) , за исключением случаев, когда пользователь выполняет размещение рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c8577-138">The default user interface for InkEdit resembles that of the [**RichTextBox**](/previous-versions/windows/) control, except when the user is laying down ink.</span></span> <span data-ttu-id="c8577-139">Можно отобразить исходные рукописные данные, а не текст. Однако рукописный ввод масштабируется до текущего размера входного шрифта элемента управления InkEdit и отображается вместе с другим текстом.</span><span class="sxs-lookup"><span data-stu-id="c8577-139">You can display original ink rather than text; however, the ink is scaled to the current input font size of the InkEdit control and is displayed inline with other text.</span></span>

> [!Note]  
> <span data-ttu-id="c8577-140">По соображениям безопасности необходимо использовать стандартные процедуры для открытия или закрытия файла, потокового ввода-вывода и установки свойства [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) или [**текста**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) .</span><span class="sxs-lookup"><span data-stu-id="c8577-140">For security reasons, you must use standard procedures to open or close a file, stream the input/output, and set the [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) or [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) property.</span></span>

 

<span data-ttu-id="c8577-141">Элемент управления [InkEdit](inkedit-control-reference.md) настроен на распознавание рукописного текста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c8577-141">The [InkEdit](inkedit-control-reference.md) control is set to recognize ink as text by default.</span></span> <span data-ttu-id="c8577-142">Чтобы разрешить пользователям добавлять рукописные данные в виде рукописных данных, установите для свойства [**инкинсертмоде**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) значение **инсертасинк**.</span><span class="sxs-lookup"><span data-stu-id="c8577-142">To enable users to add ink as ink, set the [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) property to **InsertAsInk**.</span></span>

<span data-ttu-id="c8577-143">Подробные справочные сведения об элементе управления [InkEdit](inkedit-control-reference.md) см. в разделе InkEdit.</span><span class="sxs-lookup"><span data-stu-id="c8577-143">For detailed reference information about the [InkEdit](inkedit-control-reference.md) control, see InkEdit.</span></span>

> [!Note]  
> <span data-ttu-id="c8577-144">Если вы используете элемент управления " [InkEdit](inkedit-control-reference.md) " Win32 и размещаете его внутри поля группы, убедитесь, что поле имеет прозрачный стиль. в противном случае InkEdit не сможет собираются рукописные данные.</span><span class="sxs-lookup"><span data-stu-id="c8577-144">If you use the Win32 [InkEdit](inkedit-control-reference.md) control and place it inside a group box, make sure the box has a transparent style; otherwise, InkEdit is not able to collect ink.</span></span>

 

> [!Note]  
> <span data-ttu-id="c8577-145">Чтобы обеспечить правильное отображение рукописного ввода, вызовите метод [**элемента**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) управления [InkEdit](inkedit-control-reference.md) при получении события [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) или [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="c8577-145">To ensure ink is displayed properly, call the [InkEdit](inkedit-control-reference.md) control [**Refresh**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) method when it receives an [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) or [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) event.</span></span>

 

<span data-ttu-id="c8577-146">В следующих разделах подробно описано использование элемента управления [InkEdit](inkedit-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="c8577-146">The following sections detail the use of the [InkEdit](inkedit-control-reference.md) control:</span></span>

-   [<span data-ttu-id="c8577-147">Создание экземпляра InkEdit</span><span class="sxs-lookup"><span data-stu-id="c8577-147">Instantiating InkEdit</span></span>](instantiating-inkedit.md)
-   [<span data-ttu-id="c8577-148">Сравнение слов и распознавания символов</span><span class="sxs-lookup"><span data-stu-id="c8577-148">Word vs. Character Recognition</span></span>](word-vs--character-recognition.md)
-   [<span data-ttu-id="c8577-149">Отображение рукописного ввода в виде рукописного текста</span><span class="sxs-lookup"><span data-stu-id="c8577-149">Displaying Ink as Ink</span></span>](displaying-ink-as-ink.md)
-   [<span data-ttu-id="c8577-150">Использование InkEdit в более ранних версиях Windows</span><span class="sxs-lookup"><span data-stu-id="c8577-150">Using InkEdit on Earlier Versions of Windows</span></span>](using-inkedit-on-earlier-versions-of-windows.md)
-   [<span data-ttu-id="c8577-151">Использование словаря приложения с InkEdit</span><span class="sxs-lookup"><span data-stu-id="c8577-151">Using an Application Dictionary with InkEdit</span></span>](using-an-application-dictionary-with-inkedit.md)

 

