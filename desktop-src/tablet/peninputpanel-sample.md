---
description: Этот пример построен на примере формы Auto Claims путем интеграции объекта Пенинпутпанел. Пример находится в \# каталоге C пипанел в папке автозаявок.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Пример Пенинпутпанел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d60f33ff3f61e1a2930841e5fd3d3ce3f9fc5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693568"
---
# <a name="peninputpanel-sample"></a><span data-ttu-id="28dad-104">Пример Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="28dad-104">PenInputPanel Sample</span></span>

<span data-ttu-id="28dad-105">Этот пример построен на примере формы Auto Claims путем интеграции объекта [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="28dad-105">This sample builds on the Auto Claims Form sample by integrating the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="28dad-106">Пример находится в \# каталоге C пипанел в папке автозаявок.</span><span class="sxs-lookup"><span data-stu-id="28dad-106">The sample is in the C\# PIPanel directory in the AutoClaims folder.</span></span>

> [!Note]  
> <span data-ttu-id="28dad-107">Для работы с этим примером требуется, чтобы система оснащена устройством пера.</span><span class="sxs-lookup"><span data-stu-id="28dad-107">This sample requires that your system is equipped with a pen device.</span></span> <span data-ttu-id="28dad-108">Если вы используете только мышь (или другое устройство, не поддерживающее интерфейс HID), [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) не отображается.</span><span class="sxs-lookup"><span data-stu-id="28dad-108">If you are using just a mouse (or other non-human interface device (HID) pointing device) the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) does not appear.</span></span>

 

<span data-ttu-id="28dad-109">Дополнительные сведения о образце Auto Claims см. в разделе [образец формы Auto Claims](auto-claims-form-sample.md).</span><span class="sxs-lookup"><span data-stu-id="28dad-109">For more information about the Auto Claims Form sample, see [Auto Claims Form Sample](auto-claims-form-sample.md).</span></span> <span data-ttu-id="28dad-110">Дополнительные сведения об объекте [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) см. в разделе [Программирование панели ввода с помощью класса пенинпутпанел](programming-the-input-panel-using-the-peninputpanel-class.md).</span><span class="sxs-lookup"><span data-stu-id="28dad-110">For more information about the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, see [Programming the Input Panel Using the PenInputPanel Class](programming-the-input-panel-using-the-peninputpanel-class.md).</span></span>

<span data-ttu-id="28dad-111">В примере форма "автоматические утверждения" содержит пять полей, в которые пользователю предлагается ввести сведения, относящиеся к утверждению: номер политики, название страхования, год, Марка и модель автомобиля.</span><span class="sxs-lookup"><span data-stu-id="28dad-111">In the sample, the Auto Claims Form contains five fields into which the user is asked to put information relevant to the claim: policy number, insured name, the year, make, and model of the car.</span></span> <span data-ttu-id="28dad-112">Объект [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) прикрепляется к каждому полю ввода, чтобы предоставить простые средства для ввода значений с помощью пера.</span><span class="sxs-lookup"><span data-stu-id="28dad-112">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is attached to each input field to provide an easy means for entering values with a pen.</span></span>

<span data-ttu-id="28dad-113">Существует два способа присоединения объекта [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) к полям ввода в форме.</span><span class="sxs-lookup"><span data-stu-id="28dad-113">There are two techniques for attaching a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to the input fields on your form.</span></span> <span data-ttu-id="28dad-114">Первым методом является назначение отдельного экземпляра объекта каждому входному полю во время разработки.</span><span class="sxs-lookup"><span data-stu-id="28dad-114">The first technique is to assign a separate instance of the object to each input field at design time.</span></span> <span data-ttu-id="28dad-115">Второй — создание единственного экземпляра объекта, а затем присоединение этого экземпляра объекта во время выполнения к полю при получении фокуса.</span><span class="sxs-lookup"><span data-stu-id="28dad-115">The second is to create a single instance of the object and then attach that object instance at run time to a field when it receives focus.</span></span> <span data-ttu-id="28dad-116">В этом образце демонстрируются обе методики.</span><span class="sxs-lookup"><span data-stu-id="28dad-116">This sample demonstrates both techniques.</span></span>

<span data-ttu-id="28dad-117">Существуют компромиссы при принятии решения о том, какой метод использовать.</span><span class="sxs-lookup"><span data-stu-id="28dad-117">There are tradeoffs involved in deciding which technique to use.</span></span> <span data-ttu-id="28dad-118">Создание уникального экземпляра объекта для каждого поля формы требует немного больше памяти при загрузке формы.</span><span class="sxs-lookup"><span data-stu-id="28dad-118">Creating a unique instance of the object for each form field requires slightly more memory when the form is loaded.</span></span> <span data-ttu-id="28dad-119">Однако он сохраняет необходимость в обработке событий фокуса для полей, чтобы назначить один экземпляр текущему полю во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="28dad-119">However, it saves having to handle focus events for the fields to assign a single instance to the current field at run time.</span></span>

<span data-ttu-id="28dad-120">Так как объект [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) поддерживается только на планшетном ПК, этот пример создает объекты пенинпутпанел в блоке обработки исключений.</span><span class="sxs-lookup"><span data-stu-id="28dad-120">Because the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is supported only on a Tablet PC, the sample creates the PenInputPanel objects within an exception-handling block.</span></span>

## <a name="one-object-per-field"></a><span data-ttu-id="28dad-121">Один объект на поле</span><span class="sxs-lookup"><span data-stu-id="28dad-121">One Object per Field</span></span>

<span data-ttu-id="28dad-122">В примере демонстрируется первый метод (один объект [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) для каждого поля) путем назначения полей ввода для номера политики ( `inkEdPolicyNumber` ) и имени страхования ( `inkEdName` ) уникального экземпляра объекта пенинпутпанел.</span><span class="sxs-lookup"><span data-stu-id="28dad-122">The sample demonstrates the first technique (one [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object per field) by assigning the input fields for policy number (`inkEdPolicyNumber`) and insured name (`inkEdName`) a unique instance of the PenInputPanel object.</span></span> <span data-ttu-id="28dad-123">Перегруженный конструктор для объекта Пенинпутпанел может принимать имя элемента управления вводом в качестве аргумента, тем самым связывая элементы управления.</span><span class="sxs-lookup"><span data-stu-id="28dad-123">An overloaded constructor for the PenInputPanel object can take the name of the input control as an argument, thus associating the controls.</span></span> <span data-ttu-id="28dad-124">Следующие строки из обработчика событий [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) формы показывают это:</span><span class="sxs-lookup"><span data-stu-id="28dad-124">The following lines from the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler shows this:</span></span>


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a><span data-ttu-id="28dad-125">Один объект на форму</span><span class="sxs-lookup"><span data-stu-id="28dad-125">One Object per Form</span></span>

<span data-ttu-id="28dad-126">Второй метод также показан в примере: единственный экземпляр объекта [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) , который `pipShared` является общим для полей "Year", "make" и "input Model".</span><span class="sxs-lookup"><span data-stu-id="28dad-126">The second technique is also shown in the sample: a single instance of a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, `pipShared`, is shared between the Year, Make, and Model input fields.</span></span> <span data-ttu-id="28dad-127">Общий объект создается с помощью конструктора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28dad-127">The shared object is created by using the default constructor.</span></span>


```C++
pipShared = new PenInputPanel();
```



<span data-ttu-id="28dad-128">При использовании этого метода форма должна содержать только один экземпляр объекта [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="28dad-128">Using this technique requires that your form have only a single instance of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="28dad-129">Это экономит память, но необходимо добавить код, обрабатывающий событие при получении фокусом поля ввода.</span><span class="sxs-lookup"><span data-stu-id="28dad-129">This saves memory, but you must add code to handle the event when an input field receives focus.</span></span> <span data-ttu-id="28dad-130">Если элемент управления, использующий общий экземпляр объекта Пенинпутпанел, получает фокус, установите для свойства [аттачедедитконтрол](/previous-versions/aa514050(v=msdn.10)) объекта пенинпутпанел значение этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="28dad-130">When a control that uses a shared instance of a PenInputPanel object gets focus, set the PenInputPanel object's [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) property to that control.</span></span> <span data-ttu-id="28dad-131">В следующем коде показан обработчик событий для событий «год», «Марка» и «поле модели» `Enter` .</span><span class="sxs-lookup"><span data-stu-id="28dad-131">The following code shows an event handler for the Year, Make, and Model fields' `Enter` events.</span></span>


```C++
private void inkEdYear_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Year field
    pipShared.AttachedEditControl = inkEdYear;

    // set the NUMBER factoid to bias recognition for numbers
    pipShared.Factoid = "NUMBER";

    // Enable correction UI on the inkEdYear field
    pipShared.EnableTsf(true);
}

private void inkEdMake_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Make field
    pipShared.AttachedEditControl = inkEdMake;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdMake field
    pipShared.EnableTsf(true);
}
private void inkEdModel_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Model field
    pipShared.AttachedEditControl = inkEdModel;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdModel field
    pipShared.EnableTsf(true);
}
```



<span data-ttu-id="28dad-132">Не забудьте задать свойства, которые должны быть установлены при изменении фокуса на новый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="28dad-132">Be sure to set any properties that need to be set when focus changes to a new control.</span></span> <span data-ttu-id="28dad-133">В предыдущих обработчиках событий, например, свойство [фактоид](/previous-versions/ms571978(v=vs.100)) задано соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="28dad-133">In the previous event handlers, for example, the [Factoid](/previous-versions/ms571978(v=vs.100)) property is set as appropriate.</span></span>

## <a name="usability-considerations"></a><span data-ttu-id="28dad-134">Рекомендации по удобству использования</span><span class="sxs-lookup"><span data-stu-id="28dad-134">Usability Considerations</span></span>

<span data-ttu-id="28dad-135">При использовании объекта [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) в приложении учитывайте следующие рекомендации по удобству использования.</span><span class="sxs-lookup"><span data-stu-id="28dad-135">Keep the following usability considerations in mind when using the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object in your application.</span></span>

### <a name="positioning-the-peninputpanel"></a><span data-ttu-id="28dad-136">Размещение Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="28dad-136">Positioning the PenInputPanel</span></span>

<span data-ttu-id="28dad-137">Поскольку поля располагаются вертикально на форме в этом примере, Пользовательский интерфейс [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) для каждого элемента управления вводом размещается справа от элемента управления вводом, чтобы упростить его использование.</span><span class="sxs-lookup"><span data-stu-id="28dad-137">Because the fields are laid out vertically on the form in this sample, the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) user interface for each input control is positioned slightly to the right of the input control to make it easier to use.</span></span> <span data-ttu-id="28dad-138">Это предотвращает появление Пенинпутпанел в следующем поле ввода, что упрощает выборку для следующего поля ввода.</span><span class="sxs-lookup"><span data-stu-id="28dad-138">This prevents the PenInputPanel from covering up the next edit box, making it easier to target the next edit box.</span></span>


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a><span data-ttu-id="28dad-139">Выбор панели ввода для показа</span><span class="sxs-lookup"><span data-stu-id="28dad-139">Selecting Input Panel to Display</span></span>

<span data-ttu-id="28dad-140">Поскольку номера политик часто являются сочетаниями чисел, букв и других символов, они могут быть подвержены ошибкам распознавания.</span><span class="sxs-lookup"><span data-stu-id="28dad-140">Because policy numbers are often combinations of numbers, letters, and other characters, they can be prone to recognition errors.</span></span> <span data-ttu-id="28dad-141">Таким образом, в примере для панели по умолчанию, отображаемой объектом [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) , задается клавиатура при присоединении к полю номера политики.</span><span class="sxs-lookup"><span data-stu-id="28dad-141">Therefore, the sample sets the default panel displayed by the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to be the keyboard when it is attached to the policy number field.</span></span>


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



<span data-ttu-id="28dad-142">Поведение объекта [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) по умолчанию — использовать панель, выбранную последним пользователем.</span><span class="sxs-lookup"><span data-stu-id="28dad-142">The default behavior of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is to use the panel the user selected last.</span></span>

### <a name="text-services-framework-correction-user-interface"></a><span data-ttu-id="28dad-143">Пользовательский интерфейс исправления платформы текстовых служб</span><span class="sxs-lookup"><span data-stu-id="28dad-143">Text Services Framework Correction User Interface</span></span>

<span data-ttu-id="28dad-144">В этом примере все поля ввода являются элементами управления [InkEdit](/previous-versions/ms552265(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="28dad-144">In this sample all of the input fields are [InkEdit](/previous-versions/ms552265(v=vs.100)) controls.</span></span> <span data-ttu-id="28dad-145">Это важно, поскольку элемент управления InkEdit имеет встроенную поддержку [платформы текстовых служб](../tsf/text-services-framework.md) (TSF) и поэтому может поддерживать пользовательский интерфейс исправления на месте для ввода данных, полученных от объекта [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="28dad-145">This is significant because the InkEdit control has built-in support for the [Text Services Framework](../tsf/text-services-framework.md) (TSF) and is thus capable of supporting the in-place correction user interface for input received from the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span>

<span data-ttu-id="28dad-146">Значение по умолчанию для [енаблетсф](/previous-versions/ms569656(v=vs.100)) — **true**.</span><span class="sxs-lookup"><span data-stu-id="28dad-146">The default value for [EnableTsf](/previous-versions/ms569656(v=vs.100)) is **TRUE**.</span></span> <span data-ttu-id="28dad-147">Это приводит к тому, что объект [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) пытается запустить платформу текстовых служб (TSF) на присоединенном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="28dad-147">This causes the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to attempt to start the Text Services Framework (TSF) on the attached control.</span></span> <span data-ttu-id="28dad-148">В случае успеха пользовательский интерфейс исправления отображается в элементе управления и обеспечивает доступ к альтернативам распознавания.</span><span class="sxs-lookup"><span data-stu-id="28dad-148">If successful, the correction user interface shows in the control, and it allows access to recognition alternates.</span></span> <span data-ttu-id="28dad-149">Вызов этого метода с параметром **false** пытается завершить работу TSF на присоединенном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="28dad-149">Calling this method with a **FALSE** parameter attempts to shut down TSF on the attached control.</span></span>

<span data-ttu-id="28dad-150">Элемент управления [InkEdit](/previous-versions/ms552265(v=vs.100)) уже предоставляет пользовательский интерфейс исправления, но в примере [енаблетсф](/previous-versions/ms569656(v=vs.100)) используется, чтобы разрешить [ПЕНИНПУТПАНЕЛ](/previous-versions/aa514041(v=msdn.10)) использовать контекст распознавания вставки TSF вместо функции [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) для отправки результатов распознавания рукописного текста в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="28dad-150">The [InkEdit](/previous-versions/ms552265(v=vs.100)) control already provides a correction user interface, but in the sample [EnableTsf](/previous-versions/ms569656(v=vs.100)) is used to enable the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) to use the TSF insertion recognizer context rather than the [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) function to send the handwriting recognition results into the control.</span></span> <span data-ttu-id="28dad-151">В результате текст можно вставить, даже если поле больше не находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="28dad-151">The result is that text can be inserted even if the field no longer has focus.</span></span>


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a><span data-ttu-id="28dad-152">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="28dad-152">Closing the Form</span></span>

<span data-ttu-id="28dad-153">В коде, созданном конструктором форм Windows Forms, элементы управления [InkEdit](/previous-versions/ms552265(v=vs.100)) и [InkPicture](/previous-versions/aa514604(v=msdn.10)) добавляются в список компонентов формы при инициализации формы.</span><span class="sxs-lookup"><span data-stu-id="28dad-153">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms552265(v=vs.100)) and [InkPicture](/previous-versions/aa514604(v=msdn.10)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="28dad-154">При закрытии формы элементы управления InkEdit и InkPicture удаляются, а также другие компоненты формы методом [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) формы.</span><span class="sxs-lookup"><span data-stu-id="28dad-154">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span> <span data-ttu-id="28dad-155">Метод Dispose формы также удаляет объекты [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) , созданные для формы.</span><span class="sxs-lookup"><span data-stu-id="28dad-155">The form's Dispose method also disposes the [Ink](/previous-versions/aa515768(v=msdn.10)) objects that are created for the form.</span></span>

 

 
