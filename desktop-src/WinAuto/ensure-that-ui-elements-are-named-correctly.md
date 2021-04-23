---
title: Проверка правильности имен элементов пользовательского интерфейса
description: В этом разделе описывается правильный способ указания имен элементов пользовательского интерфейса в приложениях Microsoft Win32, чтобы Microsoft Active Accessibility мог точно предоставлять имена клиентским приложениям через метод IAccessible \ 32; Имя свойства.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987570"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a><span data-ttu-id="d85e9-103">Проверка правильности имен элементов пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d85e9-103">Ensuring that UI Elements are Correctly Named</span></span>

<span data-ttu-id="d85e9-104">В этом разделе описывается правильный способ указания имен элементов пользовательского интерфейса в приложениях Microsoft Win32, чтобы Microsoft Active Accessibility мог точно предоставлять имена клиентским приложениям через [свойство имя](name-property.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-104">This topic describes the correct way to specify the names of the UI elements in your Microsoft Win32 applications so that Microsoft Active Accessibility can accurately expose the names to client applications through the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name property](name-property.md).</span></span>

<span data-ttu-id="d85e9-105">Сведения в этом разделе относятся только к Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="d85e9-105">The information in this section applies to Microsoft Active Accessibility only.</span></span> <span data-ttu-id="d85e9-106">Он не применяется к приложениям, использующим автоматизацию пользовательского интерфейса Майкрософт или основанным на языках разметки, таких как HTML, Dynamic HTML (DHTML) или XML.</span><span class="sxs-lookup"><span data-stu-id="d85e9-106">It does not apply to applications that use Microsoft UI Automation or those based on markup languages such as HTML, Dynamic HTML (DHTML), or XML.</span></span>

-   [<span data-ttu-id="d85e9-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="d85e9-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="d85e9-108">Как неправильное именование вызывает проблемы</span><span class="sxs-lookup"><span data-stu-id="d85e9-108">How Incorrect Naming Causes Problems</span></span>](#how-incorrect-naming-causes-problems)
-   [<span data-ttu-id="d85e9-109">Как MSAA получает свойство Name</span><span class="sxs-lookup"><span data-stu-id="d85e9-109">How MSAA Gets the Name Property</span></span>](#how-msaa-gets-the-name-property)
-   [<span data-ttu-id="d85e9-110">Поиск и устранение проблем именования</span><span class="sxs-lookup"><span data-stu-id="d85e9-110">How to Find and Correct Naming Problems</span></span>](#how-to-find-and-correct-naming-problems)
-   [<span data-ttu-id="d85e9-111">Как правильно присвоить имя TrackBar</span><span class="sxs-lookup"><span data-stu-id="d85e9-111">How to Correctly Name a Trackbar</span></span>](#how-to-correctly-name-a-trackbar)
-   [<span data-ttu-id="d85e9-112">Использование невидимых меток для именования элементов управления</span><span class="sxs-lookup"><span data-stu-id="d85e9-112">How to Use Invisible Labels to Name Controls</span></span>](#how-to-use-invisible-labels-to-name-controls)
-   [<span data-ttu-id="d85e9-113">Как использовать прямую заметку для указания свойства Name</span><span class="sxs-lookup"><span data-stu-id="d85e9-113">How to Use Direct Annotation to Specify the Name Property</span></span>](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [<span data-ttu-id="d85e9-114">Действия по аннотированию свойства Name</span><span class="sxs-lookup"><span data-stu-id="d85e9-114">Steps for Annotating the Name Property</span></span>](#steps-for-annotating-the-name-property)
    -   [<span data-ttu-id="d85e9-115">Пример аннотирования свойства Name</span><span class="sxs-lookup"><span data-stu-id="d85e9-115">Example of Annotating the Name Property</span></span>](#example-of-annotating-the-name-property)
-   [<span data-ttu-id="d85e9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d85e9-116">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d85e9-117">Обзор</span><span class="sxs-lookup"><span data-stu-id="d85e9-117">Overview</span></span>

<span data-ttu-id="d85e9-118">В Microsoft Active Accessibility каждый элемент пользовательского интерфейса в приложении представлен объектом, предоставляющим интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-118">In Microsoft Active Accessibility, each UI element in an application is represented by an object that exposes the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="d85e9-119">Клиентские приложения используют свойства и методы интерфейса **IAccessible** для взаимодействия с элементом пользовательского интерфейса и получения сведений о нем.</span><span class="sxs-lookup"><span data-stu-id="d85e9-119">Client applications use the properties and methods of the **IAccessible** interface to interact with the UI element and to retrieve information about it.</span></span> <span data-ttu-id="d85e9-120">Одним из наиболее важных свойств, предоставляемых интерфейсом **IAccessible** , является [свойство Name](name-property.md).</span><span class="sxs-lookup"><span data-stu-id="d85e9-120">One of the most important properties exposed by the **IAccessible** interface is the [Name property](name-property.md).</span></span> <span data-ttu-id="d85e9-121">Клиентские приложения используют свойство Name для поиска, определения или объявления элемента пользовательского интерфейса пользователю.</span><span class="sxs-lookup"><span data-stu-id="d85e9-121">Client applications rely on the Name property to find, identify, or announce a UI element to the user.</span></span> <span data-ttu-id="d85e9-122">Если Microsoft Active Accessibility не может правильно предоставить свойство Name определенного элемента пользовательского интерфейса, клиентские приложения не смогут представить этот элемент пользовательского интерфейса пользователю, а элемент пользовательского интерфейса будет недоступен для пользователей с ограниченными возможностями.</span><span class="sxs-lookup"><span data-stu-id="d85e9-122">If Microsoft Active Accessibility cannot properly expose the Name property of a particular UI element, client applications will be unable to present that UI element to the user, and the UI element will be inaccessible to users with disabilities.</span></span>

## <a name="how-incorrect-naming-causes-problems"></a><span data-ttu-id="d85e9-123">Как неправильное именование вызывает проблемы</span><span class="sxs-lookup"><span data-stu-id="d85e9-123">How Incorrect Naming Causes Problems</span></span>

<span data-ttu-id="d85e9-124">Чтобы продемонстрировать проблемы, вызванные неверным именованием элементов пользовательского интерфейса, рассмотрите форму ввода имени, показанную на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d85e9-124">To illustrate the problems caused by incorrect naming of UI elements, consider the name entry form shown in the following illustration.</span></span>

![Иллюстрация простой формы для ввода имени и фамилии](images/incorrect-form.png)

<span data-ttu-id="d85e9-126">Хотя элементы пользовательского интерфейса в форме выглядят нормально, программная реализация неверна.</span><span class="sxs-lookup"><span data-stu-id="d85e9-126">Although the UI elements in the form look okay, the programmatic implementation is incorrect.</span></span> <span data-ttu-id="d85e9-127">Для клиента Microsoft Active Accessibility, такого как средство чтения с экрана, [свойство Name](name-property.md) элемента управления "поле ввода" имеет значение "Last Name:", а свойство Name нижнего элемента управления "поле ввода" — пустая строка ("").</span><span class="sxs-lookup"><span data-stu-id="d85e9-127">To a Microsoft Active Accessibility client such as a screen reader, the [Name property](name-property.md) of the top edit control is "Last Name:", and the Name property of the bottom edit control is an empty string ("").</span></span> <span data-ttu-id="d85e9-128">Средство чтения с экрана получит верхний элемент управления "поле ввода" как "Фамилия", хотя пользователь должен ввести имя.</span><span class="sxs-lookup"><span data-stu-id="d85e9-128">The screen reader will read the top edit control as "Last Name", although the user is expected to type in the first name.</span></span> <span data-ttu-id="d85e9-129">Средство чтения с экрана будет считывать второй элемент управления "поле ввода" как "без имени", поэтому пользователь не сможет понять, что вводить во второй элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="d85e9-129">The screen reader will read the second edit control as "no name", so the user will have no idea what to type into the second edit control.</span></span> <span data-ttu-id="d85e9-130">Средство чтения с экрана не может помочь пользователю ввести данные в эту простую форму.</span><span class="sxs-lookup"><span data-stu-id="d85e9-130">The screen reader is unable to assist the user in entering data into this simple form.</span></span>

<span data-ttu-id="d85e9-131">Еще одна проблема с формой заключается в том, что никакие сочетания клавиш не назначены ни одному из элементов управления редактирования.</span><span class="sxs-lookup"><span data-stu-id="d85e9-131">Another problem with the form is that no shortcut keys are assigned to either of the edit controls.</span></span> <span data-ttu-id="d85e9-132">Пользователь вынужден переходить на любую вкладку элементов управления или использовать мышь.</span><span class="sxs-lookup"><span data-stu-id="d85e9-132">The user is forced to either tab to the controls or use the mouse.</span></span>

<span data-ttu-id="d85e9-133">В следующих разделах объясняется источник этих проблем и приводятся рекомендации по их исправлению.</span><span class="sxs-lookup"><span data-stu-id="d85e9-133">The following sections explain the source of these problems and provide guidelines for correcting them.</span></span>

## <a name="how-msaa-gets-the-name-property"></a><span data-ttu-id="d85e9-134">Как MSAA получает свойство Name</span><span class="sxs-lookup"><span data-stu-id="d85e9-134">How MSAA Gets the Name Property</span></span>

<span data-ttu-id="d85e9-135">Microsoft Active Accessibility получает строку [свойства Name](name-property.md) из различных расположений в зависимости от типа элемента пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d85e9-135">Microsoft Active Accessibility gets the [Name property](name-property.md) string from different locations depending on the type of the UI element.</span></span> <span data-ttu-id="d85e9-136">Для большинства элементов пользовательского интерфейса, имеющих связанный текст окна, Microsoft Active Accessibility использует текст окна в качестве строки свойства Name.</span><span class="sxs-lookup"><span data-stu-id="d85e9-136">For most UI elements that have associated window text, Microsoft Active Accessibility uses the window text as the Name property string.</span></span> <span data-ttu-id="d85e9-137">Примерами такого типа элемента пользовательского интерфейса являются элементы управления, такие как кнопки, элементы меню и подсказки.</span><span class="sxs-lookup"><span data-stu-id="d85e9-137">Examples of this type of UI element include controls such as buttons, menu items, and tooltips.</span></span>

<span data-ttu-id="d85e9-138">Для следующих элементов управления Microsoft Active Accessibility игнорирует текст окна и вместо этого ищет статическую текстовую метку (или метку поля группы) непосредственно перед элементом управления в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="d85e9-138">For the following controls, Microsoft Active Accessibility ignores the window text and instead looks for a static text label (or group box label) immediately preceding the control in the tab order.</span></span>

-   <span data-ttu-id="d85e9-139">Поля со списком</span><span class="sxs-lookup"><span data-stu-id="d85e9-139">Combo Boxes</span></span>
-   <span data-ttu-id="d85e9-140">Выбор даты и времени</span><span class="sxs-lookup"><span data-stu-id="d85e9-140">Date and Time Pickers</span></span>
-   <span data-ttu-id="d85e9-141">Элементы управления редактированием и форматированным редактированием</span><span class="sxs-lookup"><span data-stu-id="d85e9-141">Edit and Rich Edit controls</span></span>
-   <span data-ttu-id="d85e9-142">Элементы управления IP-адресами</span><span class="sxs-lookup"><span data-stu-id="d85e9-142">IP Address controls</span></span>
-   <span data-ttu-id="d85e9-143">Списки</span><span class="sxs-lookup"><span data-stu-id="d85e9-143">List Boxes</span></span>
-   <span data-ttu-id="d85e9-144">Представления списка</span><span class="sxs-lookup"><span data-stu-id="d85e9-144">List Views</span></span>
-   <span data-ttu-id="d85e9-145">Индикаторы выполнения</span><span class="sxs-lookup"><span data-stu-id="d85e9-145">Progress Bars</span></span>
-   <span data-ttu-id="d85e9-146">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="d85e9-146">Scrollbars</span></span>
-   <span data-ttu-id="d85e9-147">Статические элементы управления, имеющие \_ значок SS или \_ стиль битовой карты SS</span><span class="sxs-lookup"><span data-stu-id="d85e9-147">Static controls that have the SS\_ICON or SS\_BITMAP style</span></span>
-   <span data-ttu-id="d85e9-148">Линейки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="d85e9-148">Trackbars</span></span>
-   <span data-ttu-id="d85e9-149">Представления в виде дерева</span><span class="sxs-lookup"><span data-stu-id="d85e9-149">Tree Views</span></span>

<span data-ttu-id="d85e9-150">Если предыдущие элементы управления не сопровождаются статическими текстовыми метками или неправильно реализованы метки, Microsoft Active Accessibility не может предоставить для клиентских приложений правильное [свойство Name](name-property.md) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-150">If the preceding controls are not accompanied by static text labels, or if the labels are not implemented correctly, Microsoft Active Accessibility cannot provide the correct [Name property](name-property.md) to client applications.</span></span>

<span data-ttu-id="d85e9-151">Большинство предыдущих элементов управления фактически имеют связанный текст окна.</span><span class="sxs-lookup"><span data-stu-id="d85e9-151">Most of the preceding controls actually do have associated window text.</span></span> <span data-ttu-id="d85e9-152">Редактор ресурсов автоматически создает текст окна, состоящий из универсальной строки, такой как "Edit1" или "listbox3".</span><span class="sxs-lookup"><span data-stu-id="d85e9-152">The resource editor automatically generates the window text, which consists of a generic string such as "edit1" or "listbox3".</span></span> <span data-ttu-id="d85e9-153">Несмотря на то, что разработчики могут заменить созданный текст окна более осмысленным текстом, большинство из них никогда не делают этого.</span><span class="sxs-lookup"><span data-stu-id="d85e9-153">Although developers can replace the generated window text with more meaningful text, most never do.</span></span> <span data-ttu-id="d85e9-154">Поскольку созданный текст окна не имеет смысла для пользователя, Microsoft Active Accessibility пропускает его и использует вместо этого сопроводительную статическую текстовую метку.</span><span class="sxs-lookup"><span data-stu-id="d85e9-154">Because the generated window text has no meaning to the user, Microsoft Active Accessibility ignores it and uses the accompanying static text label instead.</span></span>

## <a name="how-to-find-and-correct-naming-problems"></a><span data-ttu-id="d85e9-155">Поиск и устранение проблем именования</span><span class="sxs-lookup"><span data-stu-id="d85e9-155">How to Find and Correct Naming Problems</span></span>

<span data-ttu-id="d85e9-156">В форме ввода имени, показанной в описании того, как неправильное именование вызывает проблемы, причина проблем заключается в том, что порядок табуляции элементов управления неверен.</span><span class="sxs-lookup"><span data-stu-id="d85e9-156">In the name entry form shown in How Incorrect Naming Causes Problems, the cause of the problems is that the tab order of the controls is incorrect.</span></span> <span data-ttu-id="d85e9-157">Анализ пользовательского интерфейса с помощью средства тестирования, такого как [Проверка](inspect-objects.md) , привело бы к проблемам с иерархией объектов.</span><span class="sxs-lookup"><span data-stu-id="d85e9-157">Examining the UI with a testing tool such as [Inspect](inspect-objects.md) would reveal the problems with the object hierarchy.</span></span> <span data-ttu-id="d85e9-158">На следующем снимке экрана показана неработающая иерархия объектов в форме ввода имени в том виде, в котором она отображается при проверке.</span><span class="sxs-lookup"><span data-stu-id="d85e9-158">The following screen shot shows the broken object hierarchy of the name entry form as it appears in Inspect.</span></span>

![снимок экрана средства проверки, показывающего неправильную иерархию объектов в форме ввода имени](images/incorrect-object-hierarchy.png)

<span data-ttu-id="d85e9-160">На предыдущем снимке экрана Обратите внимание, что иерархия объектов не соответствует структуре элементов управления, отображаемым в пользовательском интерфейсе формы ввода имени.</span><span class="sxs-lookup"><span data-stu-id="d85e9-160">In the previous screen shot, notice that the object hierarchy does not match the structure of the controls as they appear in the user interface of the name entry form.</span></span> <span data-ttu-id="d85e9-161">Также обратите внимание на то, что [Проверка](inspect-objects.md) назначила неверное имя элементу "следующий к последнему" (это элемент управления для ввода имени, который должен иметь имя "First Name:").</span><span class="sxs-lookup"><span data-stu-id="d85e9-161">Also notice that [Inspect](inspect-objects.md) has assigned the incorrect name to the next-to-last item (it is the edit control for entering the first name and should be a named "First Name:".</span></span> <span data-ttu-id="d85e9-162">Наконец, обратите внимание, что проверка не смогла найти имя последнего элемента (это элемент управления для ввода фамилии и должен иметь имя «Last Name:»).</span><span class="sxs-lookup"><span data-stu-id="d85e9-162">Finally, notice that Inspect could not find a name for the last item (it is the edit control for entering the last name and should have a name of "Last Name:".</span></span>

<span data-ttu-id="d85e9-163">В следующем примере показано содержимое файла ресурсов для формы ввода имени.</span><span class="sxs-lookup"><span data-stu-id="d85e9-163">The following example shows the contents of the resource file for the name entry form.</span></span> <span data-ttu-id="d85e9-164">Обратите внимание, что порядок табуляции не согласуется с логической структурой элементов управления, отображаемых в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d85e9-164">Notice that the tab order is not consistent with the logical structure of the controls as they appear in the user interface.</span></span> <span data-ttu-id="d85e9-165">Также обратите внимание, что для двух элементов управления для редактирования не заданы сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="d85e9-165">Also notice that no shortcut keys are specified for the two edit controls.</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

<span data-ttu-id="d85e9-166">Чтобы устранить проблемы с формой ввода имени, необходимо изменить файл ресурса (RC), чтобы указать сочетания клавиш, и элементы управления должны размещаться в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="d85e9-166">To correct the problems with the name entry form, the resource (.rc) file should be edited to specify keyboard shortcuts, and the controls should be placed in the following order:</span></span>

1.  <span data-ttu-id="d85e9-167">Статическая текстовая метка "&First Name:".</span><span class="sxs-lookup"><span data-stu-id="d85e9-167">The "&First Name:" static text label.</span></span>
2.  <span data-ttu-id="d85e9-168">Элемент управления редактированием для ввода имени (IDC \_ EDIT1).</span><span class="sxs-lookup"><span data-stu-id="d85e9-168">The edit control for entering the first name (IDC\_EDIT1).</span></span>
3.  <span data-ttu-id="d85e9-169">Статическая текстовая метка "&Last Name:".</span><span class="sxs-lookup"><span data-stu-id="d85e9-169">The "&Last Name:" static text label.</span></span>
4.  <span data-ttu-id="d85e9-170">Элемент управления редактированием для ввода фамилии (IDC \_ EDIT2).</span><span class="sxs-lookup"><span data-stu-id="d85e9-170">The edit control for entering the last name (IDC\_EDIT2).</span></span>
5.  <span data-ttu-id="d85e9-171">Кнопка "ОК" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d85e9-171">The "OK" default push button.</span></span>

<span data-ttu-id="d85e9-172">В следующем примере показан исправленный файл ресурсов для формы ввода имени:</span><span class="sxs-lookup"><span data-stu-id="d85e9-172">The following example shows the corrected resource file for the name entry form:</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

<span data-ttu-id="d85e9-173">Чтобы внести исправления в файл ресурсов, можно либо изменить файл напрямую, либо воспользоваться инструментом «порядок табуляции» в Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d85e9-173">To make corrections to a resource file, you can either edit the file directly, or you can use the Tab Order tool in Microsoft Visual Studio.</span></span> <span data-ttu-id="d85e9-174">Доступ к средству "порядок табуляции" в Visual Studio можно получить, нажав клавиши CTRL + D или выбрав **последовательность табуляции** в меню **Формат** .</span><span class="sxs-lookup"><span data-stu-id="d85e9-174">You can access the Tab Order tool in Visual Studio either by pressing CTRL+D, or by selecting **Tab Order** from the **Format** menu.</span></span>

<span data-ttu-id="d85e9-175">После исправления и перестроения приложения пользовательский интерфейс формы ввода имен будет выглядеть так же, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="d85e9-175">After correcting and rebuilding the application, the UI of the names entry form will look the same as it did before.</span></span> <span data-ttu-id="d85e9-176">Однако Microsoft Active Accessibility теперь будет предоставлять правильные свойства имени для клиентских приложений и будет правильно устанавливать фокус при нажатии клавиш ALT + F или ALT + L.</span><span class="sxs-lookup"><span data-stu-id="d85e9-176">However, Microsoft Active Accessibility will now provide the correct Name properties to client applications, and will set the focus correctly when the user presses the ALT+F or ALT+L keyboard shortcuts.</span></span> <span data-ttu-id="d85e9-177">Кроме того, при [проверке](inspect-objects.md) отобразится правильная иерархия объектов, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="d85e9-177">Also, [Inspect](inspect-objects.md) will show the correct object hierarchy, as the following screen shot shows.</span></span>

![снимок экрана с доступным инструментом обозревателя, отображающий правильную иерархию объектов в форме ввода имени](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a><span data-ttu-id="d85e9-179">Как правильно присвоить имя TrackBar</span><span class="sxs-lookup"><span data-stu-id="d85e9-179">How to Correctly Name a Trackbar</span></span>

<span data-ttu-id="d85e9-180">При определении значения TrackBar (или ползунка) убедитесь, что Главная статическая текстовая метка для TrackBar отображается перед TrackBar и что статические текстовые метки для минимального и максимального диапазонов отображаются после значения TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d85e9-180">When defining a trackbar (or slider), ensure that the main static text label for the trackbar appears before the trackbar, and that the static text labels for the minimum and maximum ranges appear after the trackbar.</span></span> <span data-ttu-id="d85e9-181">Помните, что в Microsoft Active Accessibility используется статическая текстовая метка, которая непосредственно предшествует элементу управления в качестве [свойства Name](name-property.md) для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d85e9-181">Remember that Microsoft Active Accessibility uses the static text label that immediately precedes a control as the [Name property](name-property.md) for the control.</span></span> <span data-ttu-id="d85e9-182">Размещение основной статической метки непосредственно перед TrackBar и другими метками после нее гарантирует, что Microsoft Active Accessibility предоставляет клиенту правильное свойство Name.</span><span class="sxs-lookup"><span data-stu-id="d85e9-182">Placing the main static text label immediately before the trackbar, and the other labels after it, ensures that Microsoft Active Accessibility provides the correct Name property to a client.</span></span>

<span data-ttu-id="d85e9-183">На следующем рисунке показана типичная линейка с главной статической текстовой меткой "Speed", а также статические текстовые метки для минимального ("min") и максимального ("Max") диапазона.</span><span class="sxs-lookup"><span data-stu-id="d85e9-183">The following illustration shows a typical trackbar with a main static text label called "Speed", and static text labels for the minimum ("min") and maximum ("max") ranges.</span></span>

![Иллюстрация элемента управления TrackBar, имеющего главную метку и метки для минимального и максимального диапазонов](images/speed-trackbar.png)

<span data-ttu-id="d85e9-185">В следующем примере показан правильный способ определения TrackBar и его статических текстовых меток в файле ресурсов:</span><span class="sxs-lookup"><span data-stu-id="d85e9-185">The following example shows the correct way to define a trackbar and its static text labels in the resource file:</span></span>

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a><span data-ttu-id="d85e9-186">Использование невидимых меток для именования элементов управления</span><span class="sxs-lookup"><span data-stu-id="d85e9-186">How to Use Invisible Labels to Name Controls</span></span>

<span data-ttu-id="d85e9-187">Не всегда возможно или нежелательно иметь видимую метку для каждого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d85e9-187">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="d85e9-188">Например, иногда Добавление меток может привести к нежелательным изменениям в внешнем виде пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d85e9-188">For example, sometimes adding labels can cause undesirable changes in the appearance of the UI.</span></span> <span data-ttu-id="d85e9-189">В этом случае можно использовать невидимые метки.</span><span class="sxs-lookup"><span data-stu-id="d85e9-189">In this case, you can use invisible labels.</span></span> <span data-ttu-id="d85e9-190">Microsoft Active Accessibility будет по-прежнему выбирать текст, связанный с невидимой меткой, но метка не будет отображаться в визуальном пользовательском интерфейсе или мешать ему.</span><span class="sxs-lookup"><span data-stu-id="d85e9-190">Microsoft Active Accessibility will still pick up the text associated with an invisible label, but the label will not appear in, or interfere with, the visual UI.</span></span>

<span data-ttu-id="d85e9-191">Как и в случае с видимыми метками, невидимая метка должна находиться непосредственно перед элементом управления в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="d85e9-191">As with visible labels, an invisible label must immediately precede the control in the tab order.</span></span> <span data-ttu-id="d85e9-192">Чтобы сделать метку невидимой в файле ресурсов (. RC), добавьте `NOT WS_VISIBLE` или `|~WS_VISIBLE` в часть Style элемента управления "статический текст".</span><span class="sxs-lookup"><span data-stu-id="d85e9-192">To make a label invisible in a resource file (.rc), add `NOT WS_VISIBLE` or `|~WS_VISIBLE` to the style part of the static text control.</span></span> <span data-ttu-id="d85e9-193">Если вы используете редактор ресурсов в Visual Studio, можно задать для свойства Visible значение false.</span><span class="sxs-lookup"><span data-stu-id="d85e9-193">If you are using the Resource Editor in Visual Studio, you can set the Visible property to False.</span></span>

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a><span data-ttu-id="d85e9-194">Как использовать прямую заметку для указания свойства Name</span><span class="sxs-lookup"><span data-stu-id="d85e9-194">How to Use Direct Annotation to Specify the Name Property</span></span>

<span data-ttu-id="d85e9-195">Прокси-серверы по умолчанию, включаемые в компонент среды выполнения Microsoft Active Accessibility, Oleacc.dll, автоматически предоставляют объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для всех стандартных элементов управления Windows.</span><span class="sxs-lookup"><span data-stu-id="d85e9-195">The default proxies included in the Microsoft Active Accessibility runtime component, Oleacc.dll, automatically provide an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for all of the standard Windows controls.</span></span> <span data-ttu-id="d85e9-196">При настройке стандартного элемента управления Windows прокси-серверы по умолчанию лучше всего обеспечивают точное предоставление всех свойств **IAccessible** для настраиваемого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d85e9-196">If you customize a standard Windows control, the default proxies do their best to accurately provide all of the **IAccessible** properties for your customized control.</span></span> <span data-ttu-id="d85e9-197">Необходимо тщательно протестировать пользовательский элемент управления, чтобы гарантировать, что прокси-серверы по умолчанию предоставляют точные и полные значения свойств.</span><span class="sxs-lookup"><span data-stu-id="d85e9-197">You should thoroughly test a customized control to ensure that the default proxies are providing accurate and complete property values.</span></span> <span data-ttu-id="d85e9-198">Если при тестировании раскрываются неточные или неполные значения свойств, можно использовать методику динамической аннотации под названием "непосредственная Аннотация" для предоставления правильных значений свойств и добавления недостающих.</span><span class="sxs-lookup"><span data-stu-id="d85e9-198">If testing reveals inaccurate or incomplete property values, you may be able to use the Dynamic Annotation technique called direct annotation to provide correct property values and add those that are missing.</span></span>

<span data-ttu-id="d85e9-199">Обратите внимание, что динамическая Аннотация не только для элементов управления, поддерживаемых учетными записями-посредниками Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="d85e9-199">Note that Dynamic Annotation is not just for controls supported by the Microsoft Active Accessibility proxies.</span></span> <span data-ttu-id="d85e9-200">Его также можно использовать для изменения или предоставления свойств для любого элемента управления, предоставляющего собственную реализацию [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-200">You can also use it to modify or provide properties for any control that provides its own [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation.</span></span>

<span data-ttu-id="d85e9-201">В этом разделе основное внимание уделяется использованию прямой аннотации для предоставления правильного значения [свойства Name](name-property.md) объекта [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d85e9-201">This section focuses on using direct annotation to provide a correct value for the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="d85e9-202">Кроме того, можно использовать прямую заметку для предоставления и других значений свойств.</span><span class="sxs-lookup"><span data-stu-id="d85e9-202">You can use direct annotation to provide other properties values as well.</span></span> <span data-ttu-id="d85e9-203">Кроме того, доступны другие методики динамической аннотации для прямых заметок, а функции и возможности API динамической аннотации выходят далеко за рамки, описанной в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d85e9-203">Also, other Dynamic Annotation techniques beside direct annotation are available, and the features and capabilities of the Dynamic Annotation API extend far beyond what is described in this section.</span></span> <span data-ttu-id="d85e9-204">Дополнительные сведения о динамической аннотации см. в разделе [Динамическая Аннотация API](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="d85e9-204">For more information about Dynamic Annotation, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

### <a name="steps-for-annotating-the-name-property"></a><span data-ttu-id="d85e9-205">Действия по аннотированию свойства Name</span><span class="sxs-lookup"><span data-stu-id="d85e9-205">Steps for Annotating the Name Property</span></span>

<span data-ttu-id="d85e9-206">Использование непосредственной аннотации для изменения [свойства Name](name-property.md) элемента управления включает следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="d85e9-206">Using direct annotation to change the [Name Property](name-property.md) of a control involves the following steps.</span></span>

1.  <span data-ttu-id="d85e9-207">Включить следующие файлы заголовков:</span><span class="sxs-lookup"><span data-stu-id="d85e9-207">Include the following header files:</span></span>
    -   <span data-ttu-id="d85e9-208">Инитгуид. h</span><span class="sxs-lookup"><span data-stu-id="d85e9-208">Initguid.h</span></span>
    -   <span data-ttu-id="d85e9-209">Олеакк. h</span><span class="sxs-lookup"><span data-stu-id="d85e9-209">Oleacc.h</span></span>

    > [!Note]  
    > <span data-ttu-id="d85e9-210">Чтобы определить идентификаторы GUID, необходимо включить Инитгуид. h перед Олеакк. h в том же файле.</span><span class="sxs-lookup"><span data-stu-id="d85e9-210">To define GUIDs, you must include Initguid.h before Oleacc.h in the same file.</span></span>

     

2.  <span data-ttu-id="d85e9-211">Инициализируйте библиотеку модели COM, вызывая функцию [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) , как правило, в процессе инициализации приложения.</span><span class="sxs-lookup"><span data-stu-id="d85e9-211">Initialize the Component Object Model (COM) library by calling the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function, typically during the application initialization process.</span></span>
3.  <span data-ttu-id="d85e9-212">Вскоре после создания целевого элемента управления (обычно во время сообщения [WM \_ инитдиалог](../dlgbox/wm-initdialog.md) ) создайте экземпляр диспетчера заметок и получите указатель на его [**иаккпропсервицес**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) указатель.</span><span class="sxs-lookup"><span data-stu-id="d85e9-212">Soon after the target control is created (typically during the [WM\_INITDIALOG](../dlgbox/wm-initdialog.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
4.  <span data-ttu-id="d85e9-213">Заметка [свойства Name](name-property.md) целевого элемента управления с помощью метода [**Иаккпропсервицес:: сесвндпропстр**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-213">Annotate the [Name Property](name-property.md) of the target control by using the [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) method.</span></span>

5.  <span data-ttu-id="d85e9-214">Отпустите указатель [**иаккпропсервицес**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-214">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
6.  <span data-ttu-id="d85e9-215">Перед уничтожением целевого элемента управления (обычно при обработке сообщения [WM \_ destroy](../winmsg/wm-destroy.md) ) создайте экземпляр диспетчера заметок и получите указатель на его интерфейс [**иаккпропсервицес**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-215">Before the target control is destroyed (typically when handling the [WM\_DESTROY](../winmsg/wm-destroy.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) interface.</span></span>
7.  <span data-ttu-id="d85e9-216">Используйте метод [**иаккпропсервицес:: клеархвндпропс**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) , чтобы очистить заметки [свойства Name](name-property.md) из целевого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d85e9-216">Use the [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) method to clear the [Name property](name-property.md) annotations from the target control.</span></span>
8.  <span data-ttu-id="d85e9-217">Отпустите указатель [**иаккпропсервицес**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-217">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
9.  <span data-ttu-id="d85e9-218">Перед завершением работы приложения (как правило, при обработке сообщения [WM \_ destroy](../winmsg/wm-destroy.md) ) ОСВОБОДИТе библиотеку COM, вызвав функцию [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-218">Before your application exits (typically while processing the [WM\_DESTROY](../winmsg/wm-destroy.md) message), release the COM library by calling the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>

<span data-ttu-id="d85e9-219">Функция [**иаккпропсервицес:: сесвндпропстр**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) принимает пять параметров.</span><span class="sxs-lookup"><span data-stu-id="d85e9-219">The [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) function takes five parameters.</span></span> <span data-ttu-id="d85e9-220">Первые три —*HWND*, *идобжект* и *идчилд*— объединяются для обнаружения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d85e9-220">The first three—*hwnd*, *idObject*, and *idChild*—combine to identify the control.</span></span> <span data-ttu-id="d85e9-221">Четвертый параметр, *идпроп*, указывает идентификатор изменяемого свойства.</span><span class="sxs-lookup"><span data-stu-id="d85e9-221">The fourth parameter, *idProp*, specifies the identifier of the property to be changed.</span></span> <span data-ttu-id="d85e9-222">Чтобы изменить [свойство Name](name-property.md), задайте для *идпроп* значение **PropID \_ ACC \_ Name**.</span><span class="sxs-lookup"><span data-stu-id="d85e9-222">To change the [Name property](name-property.md), set *idProp* to **PROPID\_ACC\_NAME**.</span></span> <span data-ttu-id="d85e9-223">(Список других свойств, которые можно задать через прямую заметку, см. в разделе [использование прямой заметки](using-direct-annotation.md).) Последним параметром **сесвндпропстр**, *str* является новая строка, используемая в качестве свойства Name.</span><span class="sxs-lookup"><span data-stu-id="d85e9-223">(For a list of other properties that you can set through direct annotation, see [Using Direct Annotation](using-direct-annotation.md).) The last parameter of **SetHwndPropStr**, *str*, is the new string to use as the Name property.</span></span>

### <a name="example-of-annotating-the-name-property"></a><span data-ttu-id="d85e9-224">Пример аннотирования свойства Name</span><span class="sxs-lookup"><span data-stu-id="d85e9-224">Example of Annotating the Name Property</span></span>

<span data-ttu-id="d85e9-225">В следующем примере кода показано, как использовать прямую заметку для изменения [свойства Name](name-property.md) объекта [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d85e9-225">The following example code shows how to use direct annotation to change the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="d85e9-226">Для простоты в примере используется жестко заданная строка ("New Control Name") для задания свойства Name.</span><span class="sxs-lookup"><span data-stu-id="d85e9-226">To keep things simple, the example uses a hard-coded string ("New Control Name") to set the Name property.</span></span> <span data-ttu-id="d85e9-227">Жестко запрограммированные строки не следует использовать в окончательной версии приложения, так как они не могут быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="d85e9-227">Hard-coded strings should not be used in the final version of your application because they cannot be localized.</span></span> <span data-ttu-id="d85e9-228">Вместо этого всегда загружайте строки из файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d85e9-228">Instead, always load strings from your resource file.</span></span> <span data-ttu-id="d85e9-229">Кроме того, в примере не показаны вызовы функций [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="d85e9-229">Also, the example does not show the calls to the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) functions.</span></span>


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d85e9-230">См. также</span><span class="sxs-lookup"><span data-stu-id="d85e9-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d85e9-231">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d85e9-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d85e9-232">Динамический API аннотации</span><span class="sxs-lookup"><span data-stu-id="d85e9-232">Dynamic Annotation API</span></span>](dynamic-annotation-api.md)
</dt> <dt>

[<span data-ttu-id="d85e9-233">Предоставление свойства Name</span><span class="sxs-lookup"><span data-stu-id="d85e9-233">Providing the Name Property</span></span>](providing-the-name-property.md)
</dt> <dt>

[<span data-ttu-id="d85e9-234">Средства тестирования</span><span class="sxs-lookup"><span data-stu-id="d85e9-234">Testing Tools</span></span>](testing-tools.md)
</dt> </dl>

 

 