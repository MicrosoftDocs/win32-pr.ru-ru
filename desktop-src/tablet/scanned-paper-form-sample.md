---
description: В этом примере на языке C \# бумажная форма была проверена как PNG-файл и задается в качестве фонового изображения во время выполнения для элемента управления InkPicture. В примере используется окно сообщения для вывода результатов распознавания рукописного текста.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Образец печатной формы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712355"
---
# <a name="scanned-paper-form-sample"></a><span data-ttu-id="a80f7-104">Образец печатной формы</span><span class="sxs-lookup"><span data-stu-id="a80f7-104">Scanned Paper Form Sample</span></span>

<span data-ttu-id="a80f7-105">В этом примере на языке C \# бумажная форма была проверена как PNG-файл и задается в качестве фонового изображения во время выполнения для элемента управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a80f7-105">In this C\# sample, a paper form has been scanned as a Portable Network Graphics (PNG) file and specified as the background image at run time for a [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span> <span data-ttu-id="a80f7-106">В примере используется окно сообщения для вывода результатов распознавания рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="a80f7-106">The sample uses a message box to display handwriting recognition results.</span></span>

<span data-ttu-id="a80f7-107">Пример включает файл язык XML (XML) Formdata.xml.</span><span class="sxs-lookup"><span data-stu-id="a80f7-107">The sample includes an Extensible Markup Language (XML) file, Formdata.xml.</span></span> <span data-ttu-id="a80f7-108">XML-файл содержит имя файла PNG.</span><span class="sxs-lookup"><span data-stu-id="a80f7-108">The XML file contains the name of the PNG file.</span></span> <span data-ttu-id="a80f7-109">Он также содержит `FieldInfo` элементы, определяющие прямоугольные области в форме, где пользователь может вводить рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="a80f7-109">It also contains `FieldInfo` elements that define rectangular regions on the form where a user can enter ink.</span></span> <span data-ttu-id="a80f7-110">Сведения в `FieldInfo` элементе показаны в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="a80f7-110">The information in the `FieldInfo` element is shown in the following example:</span></span>


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



<span data-ttu-id="a80f7-111">Левый, верхний, правый и нижний элементы являются определениями координат пикселей для каждого поля.</span><span class="sxs-lookup"><span data-stu-id="a80f7-111">The Left, Top, Right, and Bottom elements are definitions of pixel coordinates for each field.</span></span>

<span data-ttu-id="a80f7-112">В примере инициализируется новый [набор](/dotnet/api/system.data.dataset?view=netcore-3.1) данных с данными, содержащимися в Formdata.xml:</span><span class="sxs-lookup"><span data-stu-id="a80f7-112">The sample initializes a new [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) with the data contained in Formdata.xml:</span></span>


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



<span data-ttu-id="a80f7-113">Изображение формы, указанное в Formdata.xml, загружается как фон элемента управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="a80f7-113">The form image specified in Formdata.xml is loaded as the background of the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



<span data-ttu-id="a80f7-114">Затем включается сбор рукописных данных для элемента управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="a80f7-114">Ink collection is then enabled for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a><span data-ttu-id="a80f7-115">Обработчики событий меню</span><span class="sxs-lookup"><span data-stu-id="a80f7-115">Menu Event Handlers</span></span>

<span data-ttu-id="a80f7-116">Приложение содержит обработчики событий Click для всех меню, отображаемых в верхней части формы.</span><span class="sxs-lookup"><span data-stu-id="a80f7-116">The application includes click event handlers for all of the menus displayed along the top of the form.</span></span>

### <a name="recognize-menu-item"></a><span data-ttu-id="a80f7-117">Распознавать пункт меню</span><span class="sxs-lookup"><span data-stu-id="a80f7-117">Recognize Menu Item</span></span>

<span data-ttu-id="a80f7-118">Обработчик события нажатия кнопки «распознать» отключает сбор рукописных данных для элемента управления и проверяет распознаватель рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="a80f7-118">The Recognize menu click event handler disables ink collection for the control and checks for a handwriting recognizer.</span></span> <span data-ttu-id="a80f7-119">Если распознаватель не установлен, отображается диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a80f7-119">If no recognizer is installed, a dialog box is displayed.</span></span> <span data-ttu-id="a80f7-120">Пользователь должен щелкнуть пункт меню рукописного ввода или пера, чтобы снова включить элемент управления для рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="a80f7-120">A user must then click the Ink or Pen menu option to re-enable the control for ink input.</span></span>

<span data-ttu-id="a80f7-121">Если распознаватель установлен, `Recognize` функция извлекает XML-данные, указывающие координаты пикселей для каждого поля формы.</span><span class="sxs-lookup"><span data-stu-id="a80f7-121">If a recognizer is installed, the `Recognize` function retrieves the XML data that specifies pixel coordinates for each form field.</span></span> <span data-ttu-id="a80f7-122">Координаты преобразуются в координаты пространства рукописного ввода, а прямоугольник определяется для каждого поля формы.</span><span class="sxs-lookup"><span data-stu-id="a80f7-122">The coordinates are converted to ink space coordinates, and a rectangle is defined for each form field.</span></span> <span data-ttu-id="a80f7-123">После определения прямоугольников функция находит штрихи, пересекающие и находящиеся внутри каждого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="a80f7-123">After rectangles are defined, the function finds the strokes that intersect and lie within each rectangle.</span></span> <span data-ttu-id="a80f7-124">Наконец, он выполняет распознавание рукописного ввода и отображает результаты в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="a80f7-124">Finally, it performs recognition on the ink and displays the results in a message box.</span></span>

### <a name="ink-menu-item"></a><span data-ttu-id="a80f7-125">Пункт меню рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="a80f7-125">Ink Menu Item</span></span>

<span data-ttu-id="a80f7-126">Обработчик событий Click в меню рукописного ввода активирует элемент управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a80f7-126">The Ink menu click event handler enables the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span>

### <a name="pen-menu-item"></a><span data-ttu-id="a80f7-127">Пункт меню "перо"</span><span class="sxs-lookup"><span data-stu-id="a80f7-127">Pen Menu Item</span></span>

<span data-ttu-id="a80f7-128">Обработчик событий щелчка мыши в меню пера выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="a80f7-128">The Pen menu click event handler performs the following tasks:</span></span>

-   <span data-ttu-id="a80f7-129">Отключает сбор рукописных данных для элемента управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) (который необходим перед изменением свойства [EditingMode](/previous-versions/ms582189(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="a80f7-129">Disables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control (which is necessary before changing the [EditingMode](/previous-versions/ms582189(v=vs.100)) property).</span></span>
-   <span data-ttu-id="a80f7-130">Задает свойство [EditingMode](/previous-versions/ms582189(v=vs.100)) для получения рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="a80f7-130">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to collect ink.</span></span>
-   <span data-ttu-id="a80f7-131">Повторно включает сбор рукописных данных для элемента управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) и переключает меню пера, выбора и стирания, чтобы указать активный режим.</span><span class="sxs-lookup"><span data-stu-id="a80f7-131">Re-enables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control and toggles the Pen, Select, and Eraser menus to indicate the active mode.</span></span>

### <a name="edit-menu-item"></a><span data-ttu-id="a80f7-132">Изменить пункт меню</span><span class="sxs-lookup"><span data-stu-id="a80f7-132">Edit Menu Item</span></span>

<span data-ttu-id="a80f7-133">Обработчик событий нажатия кнопки «Правка» аналогичен обработчику событий меню «перо».</span><span class="sxs-lookup"><span data-stu-id="a80f7-133">The Edit menu click event handler is similar to the Pen menu event handler.</span></span> <span data-ttu-id="a80f7-134">Она выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="a80f7-134">It performs the following tasks:</span></span>

-   <span data-ttu-id="a80f7-135">Отключает сбор рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="a80f7-135">Disables ink collection.</span></span>
-   <span data-ttu-id="a80f7-136">Устанавливает свойство [EditingMode](/previous-versions/ms582189(v=vs.100)) в значение **SELECT**, которое позволяет пользователю выполнять выделение рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="a80f7-136">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to **Select**, which enables the user to perform ink selection.</span></span>
-   <span data-ttu-id="a80f7-137">Повторно включает сбор рукописных данных и переключает меню пера, правки и стирания, чтобы указать активный режим.</span><span class="sxs-lookup"><span data-stu-id="a80f7-137">Re-enables ink collection and toggles the Pen, Edit, and Eraser menus to indicate the active mode.</span></span>

### <a name="eraser-menu-item"></a><span data-ttu-id="a80f7-138">Пункт меню "Ластик"</span><span class="sxs-lookup"><span data-stu-id="a80f7-138">Eraser Menu Item</span></span>

<span data-ttu-id="a80f7-139">При нажатии кнопки «обработчик событий» в меню резинки задается элемент управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) [EditingMode](/previous-versions/ms582189(v=vs.100)) для **удаления**, что позволяет пользователю стереть рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="a80f7-139">The Eraser menu click event handler sets the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control [EditingMode](/previous-versions/ms582189(v=vs.100)) to **Delete**, which enables a user to erase ink.</span></span> <span data-ttu-id="a80f7-140">Он также переключает пункты меню "перо", "Изменить" и "Ластик".</span><span class="sxs-lookup"><span data-stu-id="a80f7-140">It also toggles the Pen, Edit, and Eraser menu items.</span></span>

### <a name="clear-menu-item"></a><span data-ttu-id="a80f7-141">Очистить пункт меню</span><span class="sxs-lookup"><span data-stu-id="a80f7-141">Clear Menu Item</span></span>

<span data-ttu-id="a80f7-142">Обработчик событий нажатия кнопки Clear меню удаляет текущую коллекцию [штрихов](/previous-versions/ms552701(v=vs.100)) для элемента управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) , тем самым удаляя все рукописные данные в форме.</span><span class="sxs-lookup"><span data-stu-id="a80f7-142">The Clear menu click event handler deletes the current [Strokes](/previous-versions/ms552701(v=vs.100)) collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control, thereby erasing all of the ink on the form.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="a80f7-143">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="a80f7-143">Closing the Form</span></span>

<span data-ttu-id="a80f7-144">В коде, созданном конструктором форм Windows Forms, элемент управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) добавляется в список компонентов формы при инициализации формы.</span><span class="sxs-lookup"><span data-stu-id="a80f7-144">In the Windows Form Designer generated code, the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="a80f7-145">При закрытии формы элемент управления InkPicture удаляется, а также другие компоненты формы с помощью метода [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) формы.</span><span class="sxs-lookup"><span data-stu-id="a80f7-145">When the form closes, the InkPicture control is disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a80f7-146">См. также</span><span class="sxs-lookup"><span data-stu-id="a80f7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a80f7-147">Элемент управления InkEdit</span><span class="sxs-lookup"><span data-stu-id="a80f7-147">InkEdit Control</span></span>](inkedit-control.md)
</dt> <dt>

[<span data-ttu-id="a80f7-148">Элемент управления InkPicture</span><span class="sxs-lookup"><span data-stu-id="a80f7-148">InkPicture Control</span></span>](inkpicture-control.md)
</dt> </dl>

 

 
