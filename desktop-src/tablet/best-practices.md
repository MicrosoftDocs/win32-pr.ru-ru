---
description: Общие сведения о рекомендациях при использовании объекта панели ввода пера.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Рекомендации (планшетный ПК)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272844"
---
# <a name="best-practices-tablet-pc"></a><span data-ttu-id="5ff37-103">Рекомендации (планшетный ПК)</span><span class="sxs-lookup"><span data-stu-id="5ff37-103">Best Practices (Tablet PC)</span></span>

<span data-ttu-id="5ff37-104">При использовании объекта [**пенинпутпанел**](peninputpanel-class.md) необходимо учитывать несколько рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="5ff37-104">There are a few guidelines to keep in mind when using the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

-   [<span data-ttu-id="5ff37-105">Предпочитать элемент управления InkEdit</span><span class="sxs-lookup"><span data-stu-id="5ff37-105">Prefer InkEdit Control</span></span>](#prefer-inkedit-control)
-   [<span data-ttu-id="5ff37-106">Отключение режима рукописного ввода для элементов управления InkEdit</span><span class="sxs-lookup"><span data-stu-id="5ff37-106">Disable Ink Mode on InkEdit Controls</span></span>](#disable-ink-mode-on-inkedit-controls)
-   [<span data-ttu-id="5ff37-107">Использование безоконных элементов управления</span><span class="sxs-lookup"><span data-stu-id="5ff37-107">Using Windowless Controls</span></span>](#using-windowless-controls)
-   [<span data-ttu-id="5ff37-108">См. также</span><span class="sxs-lookup"><span data-stu-id="5ff37-108">Related topics</span></span>](#related-topics)

## <a name="prefer-inkedit-control"></a><span data-ttu-id="5ff37-109">Предпочитать элемент управления InkEdit</span><span class="sxs-lookup"><span data-stu-id="5ff37-109">Prefer InkEdit Control</span></span>

<span data-ttu-id="5ff37-110">[InkEdit](inkedit-control-reference.md) — предпочтительный элемент управления для присоединения объекта [**пенинпутпанел**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5ff37-110">[InkEdit](inkedit-control-reference.md) is the preferred control to which to attach the [**PenInputPanel**](peninputpanel-class.md) object.</span></span> <span data-ttu-id="5ff37-111">Элемент управления InkEdit обеспечивает поддержку [платформы текстовых служб (TSF)](text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="5ff37-111">The InkEdit control provides support for the [Text Services Framework (TSF)](text-services-framework.md).</span></span>

## <a name="disable-ink-mode-on-inkedit-controls"></a><span data-ttu-id="5ff37-112">Отключение режима рукописного ввода для элементов управления InkEdit</span><span class="sxs-lookup"><span data-stu-id="5ff37-112">Disable Ink Mode on InkEdit Controls</span></span>

<span data-ttu-id="5ff37-113">При присоединении к элементу управления [InkEdit](inkedit-control-reference.md) присвойте свойству [**Инкмоде**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) элемента управления InkEdit значение [**инкмоде**](/windows/desktop/api/inked/ne-inked-inkmode) .</span><span class="sxs-lookup"><span data-stu-id="5ff37-113">When attached to an [InkEdit](inkedit-control-reference.md) control, set the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property of the InkEdit control to the [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) value.</span></span> <span data-ttu-id="5ff37-114">Если для свойства **инкмоде** не задано значение **инкмоде** , то элемент управления InkEdit интерпретирует первое касание как росчерк, передает его распознавателю и вставляет текст в элемент управления InkEdit.</span><span class="sxs-lookup"><span data-stu-id="5ff37-114">If the **InkMode** property is not set to the **InkMode** value, the InkEdit control interprets the first tap as a stroke, passes it to the recognizer, and inserts the text in the InkEdit control.</span></span> <span data-ttu-id="5ff37-115">Так как у вас уже есть объект [**пенинпутпанел**](peninputpanel-class.md) , присоединенный к приему рукописного ввода, нет необходимости включать элемент управления InkEdit для рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="5ff37-115">Since you already have a [**PenInputPanel**](peninputpanel-class.md) object attached to accept ink input, there is no need to have the InkEdit control also enabled for ink input.</span></span>

## <a name="using-windowless-controls"></a><span data-ttu-id="5ff37-116">Использование безоконных элементов управления</span><span class="sxs-lookup"><span data-stu-id="5ff37-116">Using Windowless Controls</span></span>

<span data-ttu-id="5ff37-117">Когда объект [**пенинпутпанел**](peninputpanel-class.md) присоединяется к родительскому окну, содержащему более одного безоконного элемента управления, объект **пенинпутпанел** не знает, как отвести курсор в фокусе между дочерними окнами.</span><span class="sxs-lookup"><span data-stu-id="5ff37-117">When a [**PenInputPanel**](peninputpanel-class.md) object is attached to a parent window that contains more than one windowless control, the **PenInputPanel** object does not know how to track the caret as focus moves among windowless children.</span></span> <span data-ttu-id="5ff37-118">Рукописный ввод может отправляться неправильному дочернему элементу, когда фокус перемещается из одного безоконного элемента управления в другой в ожидании ввода.</span><span class="sxs-lookup"><span data-stu-id="5ff37-118">Handwriting input can be sent to the wrong child when focus moves from one windowless control to another while input is pending.</span></span>

<span data-ttu-id="5ff37-119">Чтобы использовать объект [**пенинпутпанел**](peninputpanel-class.md) в безоконной среде, можно использовать следующий метод:</span><span class="sxs-lookup"><span data-stu-id="5ff37-119">To use the [**PenInputPanel**](peninputpanel-class.md) object in a windowless environment, the following technique can be used:</span></span>

1.  <span data-ttu-id="5ff37-120">Создайте экземпляр элемента управления [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) и поместите его в безоконный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="5ff37-120">Instantiate a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control and position it over the windowless control.</span></span>
2.  <span data-ttu-id="5ff37-121">Присоедините объект [**пенинпутпанел**](peninputpanel-class.md) к новому элементу управления "текстовое поле".</span><span class="sxs-lookup"><span data-stu-id="5ff37-121">Attach the [**PenInputPanel**](peninputpanel-class.md) object to the new text box control.</span></span>
3.  <span data-ttu-id="5ff37-122">Пусть элемент управления "текстовое поле" соберет распознанный текст из объекта [**пенинпутпанел**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5ff37-122">Let the text box control collect the recognized text from the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
4.  <span data-ttu-id="5ff37-123">При изменении фокуса с элемента управления "текстовое поле" вызовите метод [**коммитпендингинпут**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) объекта [**пенинпутпанел**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5ff37-123">When focus changes away from the text box control, call the [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) method of the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
5.  <span data-ttu-id="5ff37-124">Скопируйте распознанный текст из элемента управления "текстовое поле" в неоконное дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="5ff37-124">Copy the recognized text from the text box control to the windowless child.</span></span>
6.  <span data-ttu-id="5ff37-125">Отсоедините объект [**пенинпутпанел**](peninputpanel-class.md) , задав свойству [аттачедедитконтрол](/previous-versions/ms582239(v=vs.100)) (только управляемый код) или свойства [**аттачедедитвиндов**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) значение null.</span><span class="sxs-lookup"><span data-stu-id="5ff37-125">Detach the [**PenInputPanel**](peninputpanel-class.md) object by setting its [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (managed code only) property or [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) property to null.</span></span>
7.  <span data-ttu-id="5ff37-126">Уничтожить элемент управления "текстовое поле".</span><span class="sxs-lookup"><span data-stu-id="5ff37-126">Destroy the text box control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ff37-127">См. также</span><span class="sxs-lookup"><span data-stu-id="5ff37-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ff37-128">**Класс Пенинпутпанел**</span><span class="sxs-lookup"><span data-stu-id="5ff37-128">**PenInputPanel Class**</span></span>](peninputpanel-class.md)
</dt> <dt>

<span data-ttu-id="5ff37-129">[Microsoft. Ink. Пенинпутпанел](/previous-versions/ms583923(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="5ff37-129">[Microsoft.Ink.PenInputPanel](/previous-versions/ms583923(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="5ff37-130">инфраструктуры текстовых служб (TSF)</span><span class="sxs-lookup"><span data-stu-id="5ff37-130">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
