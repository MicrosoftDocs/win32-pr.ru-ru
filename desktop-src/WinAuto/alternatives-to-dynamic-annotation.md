---
title: Альтернативы динамической аннотации
description: Альтернативы динамической аннотации
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134118"
---
# <a name="alternatives-to-dynamic-annotation"></a><span data-ttu-id="aa0ef-103">Альтернативы динамической аннотации</span><span class="sxs-lookup"><span data-stu-id="aa0ef-103">Alternatives to Dynamic Annotation</span></span>

<span data-ttu-id="aa0ef-104">Существуют и другие способы предоставления настраиваемой поддержки [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элементов пользовательского интерфейса, и в некоторых случаях они являются правильным решением.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-104">There are other ways to provide customized [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support for UI elements, and in some cases, they are the correct solution.</span></span> <span data-ttu-id="aa0ef-105">До динамической аннотации эти альтернативные методы были единственными вариантами, доступными для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-105">Prior to Dynamic Annotation, these alternative techniques were the only options available to developers.</span></span> <span data-ttu-id="aa0ef-106">Они включают реализацию всех интерфейсов **IAccessible** и программных методов.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-106">They include implementing all of the **IAccessible** interface and programmatic techniques.</span></span>

## <a name="implementing-all-of-the-iaccessible-interface"></a><span data-ttu-id="aa0ef-107">Реализация всех интерфейсов IAccessible</span><span class="sxs-lookup"><span data-stu-id="aa0ef-107">Implementing All of the IAccessible Interface</span></span>

<span data-ttu-id="aa0ef-108">Одним из альтернативных способов является реализация всего интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="aa0ef-108">One alternative technique is to implement all of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="aa0ef-109">Этот подход часто требуется для пользовательских элементов управления или совершенно различных элементов пользовательского интерфейса. Однако затраты на разработку и тестирование настолько важны, что их следует избегать, если не действительно требуется.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-109">This approach is often necessary for custom controls or radically different UI elements; however, the development and test costs are significant enough that it should be avoided unless truly necessary.</span></span> <span data-ttu-id="aa0ef-110">Если целью является изменение одного свойства, затраты трудно выровнять.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-110">If the goal is to modify a single property, the cost is difficult to justify.</span></span>

## <a name="programmatic-techniques"></a><span data-ttu-id="aa0ef-111">Программные методы</span><span class="sxs-lookup"><span data-stu-id="aa0ef-111">Programmatic Techniques</span></span>

<span data-ttu-id="aa0ef-112">Другой вариант — использовать подклассы и методы упаковки для изменения информации, предоставляемой для конкретного свойства.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-112">Another option is to use subclassing and wrapping techniques to modify the information being exposed for a specific property.</span></span> <span data-ttu-id="aa0ef-113">Это методика, которую должна заменить динамическая Аннотация.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-113">This is the technique that Dynamic Annotation is intended to replace.</span></span> <span data-ttu-id="aa0ef-114">Чтобы переопределить одно свойство с помощью подкласса и упаковки, разработчик должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="aa0ef-114">To override a single property by using subclassing and wrapping, the developer must perform the following steps:</span></span>

1.  <span data-ttu-id="aa0ef-115">Подкласс HWND объекта [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="aa0ef-115">Subclass the HWND of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>
2.  <span data-ttu-id="aa0ef-116">Перехватите сообщение [**WM \_ GetObject**](wm-getobject.md) для правильного значения ипарам/OBJID.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-116">Intercept the [**WM\_GETOBJECT**](wm-getobject.md) message for the correct IParam/OBJID value.</span></span>
3.  <span data-ttu-id="aa0ef-117">Перешлите сообщение [**WM \_ GetObject**](wm-getobject.md) в базовый класс с помощью функции [*каллвндпрок*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aa0ef-117">Forward the [**WM\_GETOBJECT**](wm-getobject.md) message to the base class using the [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) function.</span></span> <span data-ttu-id="aa0ef-118">Если возвращается ноль, вызовите [**креатестдакцессиблеобжект**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); в противном случае вызовите [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) для возвращаемого значения, чтобы получить указатель на собственный интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-118">If zero is returned, call [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); otherwise, call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) on the returned value to obtain the control's native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
4.  <span data-ttu-id="aa0ef-119">Создайте класс-оболочку, который реализует [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и заключает в оболочку указатель интерфейса **IAccessible** , возвращенный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-119">Create a wrapper class, which implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and wraps the **IAccessible** interface pointer returned from the previous step.</span></span> <span data-ttu-id="aa0ef-120">Этот класс-оболочка отправляет все методы и свойства в исходный указатель на интерфейс **IAccessible** , за исключением тех, которые должны быть переопределены.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-120">This wrapper class sends all methods and properties to the original **IAccessible** interface pointer, except those that are to be overridden.</span></span> <span data-ttu-id="aa0ef-121">Это включает написание кода переадресации для всех 21 свойств и методов интерфейса **IAccessible** независимо от того, сколько фактически переопределено.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-121">This involves writing forwarding code for all of the **IAccessible** interface's 21 properties and methods, regardless of how many are actually overridden.</span></span>

<span data-ttu-id="aa0ef-122">Кроме того, разработчики должны проверить следующие условия:</span><span class="sxs-lookup"><span data-stu-id="aa0ef-122">Also, developers must verify the following conditions:</span></span>

-   <span data-ttu-id="aa0ef-123">Переопределенный метод или свойство должны работать только с требуемыми дочерними идентификаторами и пересылать все остальные в исходный указатель на интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="aa0ef-123">The overridden method or property must only handle the required child IDs, and forward all others to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
-   <span data-ttu-id="aa0ef-124">Оболочка также должна пересылать интерфейсы [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) и [**иолевиндов**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) только в том случае, если исходный объект поддерживает их.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-124">Wrapping must also forward [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) and [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) interfaces only if the original object supports them.</span></span>
-   <span data-ttu-id="aa0ef-125">Подсчет ссылок должен обрабатываться правильно, особенно если поддерживаются другие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-125">Reference counting must be handled correctly, especially if other interfaces are supported.</span></span>
-   <span data-ttu-id="aa0ef-126">Возвращаемые значения [**IDispatch**](idispatch-interface.md) должны обрабатываться правильно, особенно с методом [**ITypeInfo:: Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) , который должен вызываться с помощью указателя интерфейса на интерфейс оболочки, а не указателя на исходный интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="aa0ef-126">[**IDispatch**](idispatch-interface.md) return values must be handled correctly, especially with the [**ITypeInfo::Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) method, which must be called with an interface pointer to the wrapper interface, not a pointer to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

<span data-ttu-id="aa0ef-127">Эти методы требуют значительного объема работы, даже если необходимо переопределить только одно или два свойства.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-127">These techniques require a considerable amount of work, even if only one or two properties need to be overridden.</span></span> <span data-ttu-id="aa0ef-128">Большая часть результирующего кода связана с подклассом и оболочкой, и только небольшая часть фактически предоставляет переопределенную информацию.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-128">The majority of the resulting code is concerned with subclassing and wrapping, and only a small fraction is actually providing the overridden information.</span></span>

<span data-ttu-id="aa0ef-129">Однако существуют сценарии, в которых требуются эти методы.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-129">However, there are scenarios in which these techniques are needed.</span></span> <span data-ttu-id="aa0ef-130">Например, если вы вносите структурные изменения для создания элемента пользовательского интерфейса заполнителя, следует использовать эти методы, а не динамические заметки.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-130">For example, if you are making structural changes to create a placeholder UI element, then you should use these techniques rather than Dynamic Annotation.</span></span>

## <a name="fixing-names-derived-from-labels"></a><span data-ttu-id="aa0ef-131">Исправление имен, полученных из меток</span><span class="sxs-lookup"><span data-stu-id="aa0ef-131">Fixing Names Derived from Labels</span></span>

<span data-ttu-id="aa0ef-132">Некоторые общие элементы управления Microsoft Win32, такие как элемент управления "поле ввода", почти всегда используются с меткой (запись ЛТЕКСТ в файле ресурсов) или в поле группы (GROUPBOX в файле ресурсов).</span><span class="sxs-lookup"><span data-stu-id="aa0ef-132">Some Microsoft Win32 common controls, such as the edit box control, are nearly always used with a label (an LTEXT entry in the resource file) or a group box (GROUPBOX in the resource file).</span></span> <span data-ttu-id="aa0ef-133">Microsoft Active Accessibility автоматически извлекает свойство Name элемента управления из его метки.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-133">Microsoft Active Accessibility automatically derives the name property of the control from its label.</span></span> <span data-ttu-id="aa0ef-134">Для таких элементов управления текст окна (отображаемый в Microsoft Visual Studio как свойство "имя" или "идентификатор") игнорируется, так как обычно создается автоматически и редко очень описательно. Например, "IDC \_ EDIT1".</span><span class="sxs-lookup"><span data-stu-id="aa0ef-134">For such controls, the window text (shown in Microsoft Visual Studio as the Name or ID property) is ignored, because it is usually autogenerated and seldom very descriptive; for example, "IDC\_EDIT1".</span></span>

<span data-ttu-id="aa0ef-135">Если пользовательский интерфейс приложения не спроектирован должным образом, Microsoft Active Accessibility может не иметь возможности правильно задать имя.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-135">If the user interface of the application is not designed correctly, Microsoft Active Accessibility might not be able to set the name correctly.</span></span> <span data-ttu-id="aa0ef-136">Для связывания с элементом управления поле метки или группы должно располагаться непосредственно перед динамическим элементом управления в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-136">To be associated with a control, the label or group box must be placed immediately before the dynamic control in the tab order.</span></span>

<span data-ttu-id="aa0ef-137">Порядок табуляции можно изменить с помощью средства в Visual Studio (в меню **Формат** , если открыт редактор ресурсов) или путем непосредственного редактирования файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-137">Tab order can be changed by using the tool in Visual Studio (on the **Format** menu when the resource editor is open) or by directly editing the resource file.</span></span>

<span data-ttu-id="aa0ef-138">В следующем примере показано описание файла ресурсов для диалогового окна, содержащего два поля ввода с метками.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-138">The following example shows a resource file's description of a dialog box that contains two labeled edit boxes.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



<span data-ttu-id="aa0ef-139">В этом примере метки и элементы управления не перечисляются в правильном порядке табуляции.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-139">In this example, the labels and controls are not listed in the correct tab order.</span></span> <span data-ttu-id="aa0ef-140">В результате Microsoft Active Accessibility присваивает имя «Last Name» текстовому полю «имя» и не имеет имени в поле «Last-Name».</span><span class="sxs-lookup"><span data-stu-id="aa0ef-140">As a result, Microsoft Active Accessibility assigns the name "Last Name" to the first-name edit box, and no name at all to the last-name edit box.</span></span>

<span data-ttu-id="aa0ef-141">В следующем примере показан правильный список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-141">The following example shows the correct resource listing.</span></span> <span data-ttu-id="aa0ef-142">Обратите внимание также, что в метках назначены сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-142">Note also that shortcut keys have been designated in the labels.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



<span data-ttu-id="aa0ef-143">Если элементы управления имеют дополнительные метки, например для минимальных и максимальных значений на TrackBar, эти метки должны располагаться после элемента управления в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-143">When controls have supplementary labels, such as for minimum and maximum values on a trackbar, these labels should be placed after the control in the tab order.</span></span> <span data-ttu-id="aa0ef-144">Основная метка элемента управления должна располагаться непосредственно перед самим элементом управления.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-144">The main label of the control must appear immediately before the control itself.</span></span>

## <a name="naming-controls-without-labels"></a><span data-ttu-id="aa0ef-145">Именование элементов управления без меток</span><span class="sxs-lookup"><span data-stu-id="aa0ef-145">Naming Controls Without Labels</span></span>

<span data-ttu-id="aa0ef-146">Не всегда возможно или нежелательно иметь видимую метку для каждого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-146">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="aa0ef-147">Однако вы по-прежнему можете предоставить имя для элемента управления, добавив невидимую метку.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-147">However, you can still provide a name for the control by adding an invisible label.</span></span> <span data-ttu-id="aa0ef-148">Как всегда, невидимая метка должна находиться непосредственно перед элементом управления в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-148">As always, the invisible label must immediately precede the control in the tab order.</span></span>

<span data-ttu-id="aa0ef-149">Если вы используете редактор ресурсов в Microsoft Visual Studio .NET, можно задать для свойства Visible значение false.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-149">If you are using the Resource Editor in Microsoft Visual Studio .NET, you can set the Visible property to False.</span></span> <span data-ttu-id="aa0ef-150">Чтобы сделать метку невидимой при редактировании файла ресурсов (. RC), добавьте параметр NOT- \_ Visible или в часть Style элемента управления Label, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-150">To make the label invisible when editing the resource file (.rc), add NOT WS\_VISIBLE or to the style part of the label control, as shown in the following example.</span></span>


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



<span data-ttu-id="aa0ef-151">Обратите внимание, что все назначенные сочетания клавиш работают даже несмотря на то, что метка невидима.</span><span class="sxs-lookup"><span data-stu-id="aa0ef-151">Note that any designated shortcut key works even though the label is invisible.</span></span>

 

 