---
description: Пример приложения рукописного ввода блога демонстрирует создание управляемого класса UserControl с возможностью рукописного ввода и размещением этого элемента управления в Microsoft Internet Explorer.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Пример веб-примера рукописного блога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24f132d355a95c9cb8debebe074df3f976e3b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143930"
---
# <a name="ink-blog-web-sample"></a><span data-ttu-id="9776a-103">Пример веб-примера рукописного блога</span><span class="sxs-lookup"><span data-stu-id="9776a-103">Ink Blog Web Sample</span></span>

<span data-ttu-id="9776a-104">Пример приложения рукописного ввода блога демонстрирует создание управляемого класса [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) с возможностью рукописного ввода и размещением этого элемента управления в Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9776a-104">The Ink Blog sample application demonstrates how to create a managed [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class that has inking capability and host that control in Microsoft Internet Explorer.</span></span> <span data-ttu-id="9776a-105">В этом примере также демонстрируется один из способов отправки рукописных данных по сети с помощью протокола HTTP и сохранения рукописного ввода на сервере.</span><span class="sxs-lookup"><span data-stu-id="9776a-105">The sample also demonstrates one technique for sending ink data across a network by using HTTP and for persisting ink on a server.</span></span>

> [!Note]  
> <span data-ttu-id="9776a-106">Для запуска этого примера необходимо установить Microsoft службы IIS (IIS) с ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="9776a-106">You must have Microsoft Internet Information Services (IIS) with ASP.NET installed to run this sample.</span></span> <span data-ttu-id="9776a-107">Убедитесь, что компьютер соответствует требованиям, необходимым для запуска приложений ASP.NET на компьютере.</span><span class="sxs-lookup"><span data-stu-id="9776a-107">Make sure that your computer meets the requirements necessary for ASP.NET applications to run on your computer.</span></span>

 

> [!Note]  
> <span data-ttu-id="9776a-108">Если запустить этот пример на компьютере, отличном от планшетном, с установленным пакетом средств разработки Microsoft Windows XP Tablet PC Edition 1,7, функция распознавания текста для заголовков рукописного ввода не будет работать.</span><span class="sxs-lookup"><span data-stu-id="9776a-108">If you run this sample on a non-Tablet PC computer with the Microsoft Windows XP Tablet PC Edition Development Kit 1.7 installed the text recognition feature for the ink title will not function.</span></span> <span data-ttu-id="9776a-109">Это происходит из-за того, что на компьютере, который не является планшетом с установленным пакетом SDK для Tablet PC 1,7, отсутствуют Распознаватели.</span><span class="sxs-lookup"><span data-stu-id="9776a-109">This occurs because a non-Tablet PC computer with the Tablet PC SDK 1.7 installed lacks recognizers.</span></span> <span data-ttu-id="9776a-110">Остальная часть приложения выполняется согласно описанию.</span><span class="sxs-lookup"><span data-stu-id="9776a-110">The rest of the application performs as described.</span></span>

 

## <a name="overview"></a><span data-ttu-id="9776a-111">Обзор</span><span class="sxs-lookup"><span data-stu-id="9776a-111">Overview</span></span>

<span data-ttu-id="9776a-112">Пример рукописного ввода блога создает блог с поддержкой рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="9776a-112">The Ink Blog sample creates an ink-enabled Weblog.</span></span> <span data-ttu-id="9776a-113">Инкблогвеб — это приложение ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="9776a-113">InkBlogWeb is an ASP.NET application.</span></span> <span data-ttu-id="9776a-114">Рукописный ввод выполняется с помощью пользовательского элемента управления, на который ссылается страница ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="9776a-114">Ink entry is accomplished by means of a user control that is referenced from an ASP.NET page.</span></span>

<span data-ttu-id="9776a-115">Пользовательский элемент управления определяет, установлены ли на клиентском компьютере компоненты платформы Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="9776a-115">The user control detects whether the Tablet PC platform components are installed on the client computer.</span></span> <span data-ttu-id="9776a-116">В этом случае пользовательский элемент управления предоставляет пользователю две области с поддержкой рукописного ввода на веб-странице: одну для ввода заголовка для записи блога и одну для текста записи.</span><span class="sxs-lookup"><span data-stu-id="9776a-116">If so, the user control presents the user with two ink-enabled areas on the Web page: one for inking a title for the blog entry and one for the body of the entry.</span></span> <span data-ttu-id="9776a-117">Если компоненты платформы Tablet PC не установлены, пользователю выдается стандартный элемент управления "текстовое поле" для заголовка и текста записи.</span><span class="sxs-lookup"><span data-stu-id="9776a-117">If the Tablet PC Platform components are not installed, then the user is given a standard text box control for the title and body of the entry.</span></span>

<span data-ttu-id="9776a-118">Когда пользователь завершает создание записи, он нажимает кнопку, добавляет блог, а сообщение отправляется на веб-сервер для хранения.</span><span class="sxs-lookup"><span data-stu-id="9776a-118">When the user finishes creating the entry, she clicks a button, Add Blog, and the post is sent to the Web server for storage.</span></span> <span data-ttu-id="9776a-119">На сервере приложение сохраняет текст заголовка и дату публикации, а также ссылку на файл формата GIF.</span><span class="sxs-lookup"><span data-stu-id="9776a-119">On the server, the application saves the title text and posting date, as well as a reference to a Graphics Interchange Format (GIF) file.</span></span> <span data-ttu-id="9776a-120">GIF-файл, также сохраненный на сервере, содержит рукописные данные из текста в файле специальная GIF.</span><span class="sxs-lookup"><span data-stu-id="9776a-120">The GIF file, also saved to the server, contains the ink data from the body in a fortified GIF file.</span></span> <span data-ttu-id="9776a-121">Дополнительные сведения о формате GIF специальная см. в разделе [Сохранение рукописного ввода в HTML](storing-ink-in-html.md).</span><span class="sxs-lookup"><span data-stu-id="9776a-121">For more information about the fortified GIF format, see [Storing Ink in HTML](storing-ink-in-html.md).</span></span>

<span data-ttu-id="9776a-122">В решении Инкблог есть два проекта: проект **инкблогконтролс** и проект **инкблогвеб** .</span><span class="sxs-lookup"><span data-stu-id="9776a-122">There are two projects in the InkBlog solution: the **InkBlogControls** project and the **InkBlogWeb** project.</span></span>

## <a name="inkblogcontrols-project"></a><span data-ttu-id="9776a-123">Проект Инкблогконтролс</span><span class="sxs-lookup"><span data-stu-id="9776a-123">InkBlogControls Project</span></span>

<span data-ttu-id="9776a-124">Проект **инкблогконтролс** — это проект [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) , который содержит код для пользовательского элемента управления, обеспечивающего рукописный ввод на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="9776a-124">The **InkBlogControls** project is a [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) project that contains the code for the user control that enables inking on the Web page.</span></span> <span data-ttu-id="9776a-125">Код для этого элемента управления, элемент управления Инкареа, находится в файле Инкареа. cs.</span><span class="sxs-lookup"><span data-stu-id="9776a-125">The code for this control, the InkArea control, is in the InkArea.cs file.</span></span>

<span data-ttu-id="9776a-126">`InkArea`Класс наследует от класса [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="9776a-126">The `InkArea` Class inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class.</span></span> <span data-ttu-id="9776a-127">Конструктор для `InkArea` элемента управления вызывает вспомогательный метод, `CreateInkCollectionSurface` .</span><span class="sxs-lookup"><span data-stu-id="9776a-127">The constructor for the `InkArea` control calls a helper method, `CreateInkCollectionSurface`.</span></span>


```C++
public InkArea()
{
    // Standard template code

    try
    {
        inputArea = CreateInkCollectionSurface();
    }
    catch (FileNotFoundException)
    { 
        inputArea = new TextBox();
        ((TextBox)inputArea).Multiline = true;
    }

    inputArea.Size = this.Size;

    // Add the control used for collecting blog input
    this.Controls.Add(inputArea);
}
```



<span data-ttu-id="9776a-128">`CreateInkCollectionSurface`Метод определяет, доступны ли компоненты рукописного ввода Tablet PC на клиенте, пытаясь создать экземпляр класса [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="9776a-128">The `CreateInkCollectionSurface` method determines whether the Tablet PC inking components are available on the client by attempting to create an instance of the [InkCollector](/previous-versions/ms583683(v=vs.100)) class.</span></span> <span data-ttu-id="9776a-129">Если вызов `CreateInkCollectionSurface` метода завершается с ошибкой, метод возвращает объект [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) в качестве элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9776a-129">If the call to the `CreateInkCollectionSurface` method succeeds, the method returns a [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) object as the control.</span></span>


```C++
protected Control CreateInkCollectionSurface()
{
    try
    {
        Panel inkPanel = new Panel();
        inkPanel.BorderStyle = BorderStyle.Fixed3D;
        inkCollector = new InkCollector(inkPanel);
        ((InkCollector)inkCollector).Enabled = true;
        return inkPanel;
    }
    catch
    {
        throw;
    }
}
```



<span data-ttu-id="9776a-130">Если происходит сбой конструктора из-за того, что файлы платформы рукописного ввода не найдены, то этот `InputArea` элемент управления создается как элемент управления [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) , а не элемент управления [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="9776a-130">If the constructor fails because the inking platform files are not found, then the `InputArea` control is instantiated as a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control rather than a [InkCollector](/previous-versions/ms583683(v=vs.100)) control.</span></span> <span data-ttu-id="9776a-131">Затем конструктор изменяет размер элемента управления до размера родительского пользовательского элемента управления и добавляет его в коллекцию Controls родителя.</span><span class="sxs-lookup"><span data-stu-id="9776a-131">The constructor then sizes the control to the size of the parent user control and adds it to the parent's Controls collection.</span></span>

<span data-ttu-id="9776a-132">Класс элементов управления Инкареа реализует три интересных общедоступных свойства: Инкдата, TextData и enable.</span><span class="sxs-lookup"><span data-stu-id="9776a-132">The InkArea control class implements three interesting public properties: InkData, TextData, and WebEnabled.</span></span>

<span data-ttu-id="9776a-133">Свойство Инкдата доступно только для чтения и предоставляет доступ к сериализованным данным рукописного ввода, если клиент поддерживает рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="9776a-133">The InkData property is read-only and provides access to the serialized ink data, if the client supports inking.</span></span> <span data-ttu-id="9776a-134">Если клиент не поддерживает рукописный ввод, свойство Инкдата получает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="9776a-134">If the client does not support inking, the InkData property gets an empty string.</span></span> <span data-ttu-id="9776a-135">Свойство Инкдата вызывает вспомогательный метод, Сериализеинкдата, чтобы определить, поддерживает ли клиент рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="9776a-135">The InkData property calls a helper method, SerializeInkData, to determine if the client supports inking.</span></span>


```C++
protected String SerializeInkData()
{
    Debug.Assert(InkEnabled, null, "Client must be ink-enabled");

    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    // Serialize the ink
    if (ink.Strokes.Count > 0) 
    {
        byte[] inkDataBytes = ink.Save(PersistenceFormat.Gif);
        return Convert.ToBase64String(inkDataBytes);
    }

    // Default to returning the empty string.
    return String.Empty;
}
```



<span data-ttu-id="9776a-136">В `SerializeInkData` методе приведение к объекту [InkCollector](/previous-versions/ms583683(v=vs.100)) необходимо при получении объекта [рукописного ввода](/previous-versions/ms583670(v=vs.100)) , поскольку `inputArea` объявляется как [элемент управления](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="9776a-136">In the `SerializeInkData` method, the cast to [InkCollector](/previous-versions/ms583683(v=vs.100)) is necessary when obtaining the [Ink](/previous-versions/ms583670(v=vs.100)) object, because `inputArea` is declared as a [Control](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="9776a-137">Если объект рукописного ввода содержит штрихи, то данные рукописного ввода сохраняются в `inkDataBytes` массив байтов как GIF (указывается с помощью значения перечисления [персистенцеформат](/previous-versions/ms552503(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="9776a-137">If the Ink object contains any strokes, the ink data is saved into the `inkDataBytes` byte array as a GIF (specified by using the [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) enumeration value).</span></span> <span data-ttu-id="9776a-138">Затем метод преобразует массив байтов в строку в кодировке Base64 и возвращает эту строку.</span><span class="sxs-lookup"><span data-stu-id="9776a-138">The method then converts the byte array to a Base64-encoded string and returns this string.</span></span>

<span data-ttu-id="9776a-139">Предполагая, что клиент может выполнять распознавание, `TextData` свойство возвращает объект [рекогнитионресулт](/previous-versions/ms552537(v=vs.100)) из передачи рукописных данных в распознаватель рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="9776a-139">Assuming that the client can perform recognition, the `TextData` property returns the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object from passing the ink data to a handwriting recognizer.</span></span> <span data-ttu-id="9776a-140">Если клиент не поддерживает рукописный ввод, возвращается содержимое текстового поля, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="9776a-140">If the client is not ink-aware, the text box contents are returned, as shown in the following code.</span></span>


```C++
public string TextData
{
    get
    {
        if (this.WebEnabled) 
        {
            return RecognizeInkData();
        }
        else
        {
            return ((TextBox)inputArea).Text;
        }
    }
}
```



<span data-ttu-id="9776a-141">`TextData`Свойство вызывает вспомогательный метод, `RecognizeInkData` показанный в следующем коде, для выполнения распознавания.</span><span class="sxs-lookup"><span data-stu-id="9776a-141">The `TextData` property calls a helper method, `RecognizeInkData`, shown in the following code, to carry out the recognition.</span></span> <span data-ttu-id="9776a-142">Если в системе имеются обработчики распознавания, `RecognizeInkData` метод возвращает строку, содержащую свойство [Топстринг](/previous-versions/ms572009(v=vs.100)) объекта [рекогнитионресулт](/previous-versions/ms552537(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="9776a-142">When recognition engines are present on the system, the `RecognizeInkData` method returns a string containing the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object's [TopString](/previous-versions/ms572009(v=vs.100)) property.</span></span> <span data-ttu-id="9776a-143">В противном случае возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="9776a-143">Otherwise, it returns an empty string.</span></span>


```C++
protected String RecognizeInkData()
{
    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    if (ink.Strokes.Count > 0) 
    {

        // Attempt to create a recognition context and use it to
        // retrieve the top alternate.
        try 
        {
            RecognizerContext recognizerContext = new RecognizerContext();
            RecognitionStatus recognitionStatus;
            recognizerContext.Strokes = ink.Strokes;
            RecognitionResult recognitionResult = recognizerContext.Recognize(out recognitionStatus);
            if (recognitionStatus == RecognitionStatus.NoError) && ( null != recognitionResult) )
            {
                return recognitionResult.TopString;
            }
        }
        catch (Exception)
        {
            // An exception will occur if the client does not have
            // any handwriting recognizers installed on their system.
            // In this case, we default to returning an empty string. 
        }
    }

    return String.Empty;
}
```



<span data-ttu-id="9776a-144">`InkEnabled`Свойство является логическим значением только для чтения, указывающим, поддерживается ли рукописный ввод на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="9776a-144">The `InkEnabled` property is a read-only Boolean value that indicates whether inking is supported on the client machine.</span></span>

<span data-ttu-id="9776a-145">Другим важным открытым членом `InkArea` класса Control является `DisposeResources` метод.</span><span class="sxs-lookup"><span data-stu-id="9776a-145">Another important public member of the `InkArea` control class is the `DisposeResources` method.</span></span> <span data-ttu-id="9776a-146">Этот метод внутренне вызывает `Dispose` метод, чтобы гарантировать очистку всех ресурсов, используемых пользовательским элементом управления.</span><span class="sxs-lookup"><span data-stu-id="9776a-146">This method internally calls the `Dispose` method to ensure that all resources leveraged by the user control are cleaned up.</span></span> <span data-ttu-id="9776a-147">Любое приложение, использующее `InkArea` элемент управления, должно вызывать `DisposeResources` метод после завершения использования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9776a-147">Any application that uses the `InkArea` control must call the `DisposeResources` method when it is finished using the control.</span></span>

## <a name="inkblogweb-project"></a><span data-ttu-id="9776a-148">Проект Инкблогвеб</span><span class="sxs-lookup"><span data-stu-id="9776a-148">InkBlogWeb Project</span></span>

<span data-ttu-id="9776a-149">Проект Инкблогвеб — это проект развертывания веб-установки, который ссылается на `InkArea` элемент управления для предоставления функциональных возможностей ведения блога.</span><span class="sxs-lookup"><span data-stu-id="9776a-149">The InkBlogWeb project is a Web Setup deployment project that references the `InkArea` control to provide the blogging functionality.</span></span> <span data-ttu-id="9776a-150">Дополнительные сведения о проектах развертывания веб-установки см. [в разделе Развертывание проекта веб-установки](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="9776a-150">For more information about Web Setup deployment projects, see [Deployment of a Web Setup Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span></span>

<span data-ttu-id="9776a-151">Существует два файла. aspx, реализующих пример ведения блогов: Default. aspx и Аддблог. aspx.</span><span class="sxs-lookup"><span data-stu-id="9776a-151">There are two .aspx files that implement the blogging sample: Default.aspx and AddBlog.aspx.</span></span> <span data-ttu-id="9776a-152">Default. aspx является страницей по умолчанию для приложения Инкблогвеб.</span><span class="sxs-lookup"><span data-stu-id="9776a-152">Default.aspx is the default page for the InkBlogWeb application.</span></span> <span data-ttu-id="9776a-153">Файл кода программной части для этой страницы — Default. aspx. cs.</span><span class="sxs-lookup"><span data-stu-id="9776a-153">The code behind file for this page is Default.aspx.cs.</span></span> <span data-ttu-id="9776a-154">На этой странице содержится ссылка на страницу, содержащую новую форму записи блога, и отображаются все существующие записи блога.</span><span class="sxs-lookup"><span data-stu-id="9776a-154">This page provides a link to the page containing the new blog entry form and displays any existing blog entries.</span></span> <span data-ttu-id="9776a-155">Этот процесс описан далее, после следующего изучения новой страницы формы записи блога Аддблог. aspx.</span><span class="sxs-lookup"><span data-stu-id="9776a-155">This process is described later, after the following examination of the new blog entry form page, AddBlog.aspx.</span></span>

<span data-ttu-id="9776a-156">Аддблог. aspx и его файл кода программной части, Аддблог. aspx. cs, содержат логику и код пользовательского интерфейса для создания новых записей в блоге.</span><span class="sxs-lookup"><span data-stu-id="9776a-156">AddBlog.aspx and its code-behind file, AddBlog.aspx.cs, contain the logic and user interface code for creating new blog entries.</span></span> <span data-ttu-id="9776a-157">Аддблокс. aspx ссылается на два экземпляра класса элемента управления Инкареа, созданный в проекте Инкблогконтролс с помощью элемента объекта HTML, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="9776a-157">AddBlox.aspx references two instances of the InkArea control class created in the InkBlogControls project by using the HTML OBJECT element as shown in the following example.</span></span> <span data-ttu-id="9776a-158">Один экземпляр имеет `id` атрибут инкблогтитле, а другой имеет атрибут ID инкблогбоди.</span><span class="sxs-lookup"><span data-stu-id="9776a-158">One instance has an `id` attribute of inkBlogTitle and the other has an id attribute of inkBlogBody.</span></span>

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

<span data-ttu-id="9776a-159">Сборка InkBlogControls.dll должна находиться в том же каталоге, что и ASPX-страница, ссылающаяся на нее.</span><span class="sxs-lookup"><span data-stu-id="9776a-159">The InkBlogControls.dll assembly must be present in the same directory as the .aspx page that is referencing it.</span></span> <span data-ttu-id="9776a-160">Проект развертывания веб-установки гарантирует, что это так, как свидетельствует присутствие элемента "Основные выходные данные из Инкблогконтролс" в проекте развертывания.</span><span class="sxs-lookup"><span data-stu-id="9776a-160">The Web Setup deployment project ensures that this is the case, as evidenced by the presence of the "Primary output from InkBlogControls" item in the Deployment Project.</span></span>

<span data-ttu-id="9776a-161">Элемент управления "заголовок" имеет размер 48 пикселей в высоком углу, чтобы упростить ввод одной строки рукописного ввода для заголовка.</span><span class="sxs-lookup"><span data-stu-id="9776a-161">The title control is only 48 pixels high to facilitate the entry of a single line of ink for the title.</span></span> <span data-ttu-id="9776a-162">Элемент управления "текст" имеет размер 296 пикселей в большую часть, чтобы освободить место для больших записей в блоге, имеющих несколько строк или, возможно, чертежей.</span><span class="sxs-lookup"><span data-stu-id="9776a-162">The body control is 296 pixels high to make room for larger blog entries of multiple lines or perhaps drawings.</span></span>

<span data-ttu-id="9776a-163">Элементы управления Инкареа связаны с функцией скрипта на стороне клиента, Аддблог, посредством стандартного обработчика событий OnClick элемента кнопки HTML.</span><span class="sxs-lookup"><span data-stu-id="9776a-163">The InkArea controls are connected to a client-side script function, AddBlog, by means of a standard HTML BUTTON element's onclick event handler.</span></span>

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

<span data-ttu-id="9776a-164">На странице также есть HTML-форма, содержащая три скрытых элемента ввода: Блогтитлетекст, Блогбодитекст и Блогбодинкдата.</span><span class="sxs-lookup"><span data-stu-id="9776a-164">There is also an HTML form on the page that contains three hidden INPUT elements: BlogTitleText, BlogBodyText, and BlogBodyInkData.</span></span> <span data-ttu-id="9776a-165">Эта форма используется для передачи данных записи блога обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="9776a-165">This form is used to post the blog entry data back to the server.</span></span> <span data-ttu-id="9776a-166">Аддблог. aspx — это обработчик обратной передачи, определенный для формы.</span><span class="sxs-lookup"><span data-stu-id="9776a-166">AddBlog.aspx is the post-back handler defined for the form.</span></span>

<span data-ttu-id="9776a-167">Функция Аддблог, написанная в Microsoft JScript, <entity type="reg"/> извлекает данные из блога из элементов управления инкареа и отправляет результаты на сервер.</span><span class="sxs-lookup"><span data-stu-id="9776a-167">The AddBlog function-written in Microsoft JScript<entity type="reg"/>-extracts the blog data from the InkArea controls and posts the results to the server.</span></span>


```C++
function AddBlog() 
{
    // Extract the blog's title data as ink and text
    form.BlogTitleText.value  = inkBlogTitle.TextData;
    
    // Extract the blog's body data as ink and text
    form.BlogBodyText.value = inkBlogBody.TextData;
    form.BlogBodyInkData.value = inkBlogBody.InkData;   

    form.submit();
}
```



<span data-ttu-id="9776a-168">Когда данные поступают на сервер, код в Аддблог. aspx. CS проверяет \_ обработчик событий загрузки страницы, чтобы определить, содержит ли свойство формы объекта HttpRequest какие-либо данные.</span><span class="sxs-lookup"><span data-stu-id="9776a-168">When the data arrives at the server, the code in AddBlog.aspx.cs checks the Page\_Load event handler to see if the HttpRequest object's Form property contains any data.</span></span> <span data-ttu-id="9776a-169">В этом случае он создает имя файла на основе текущего системного времени, помещает данные формы в три строковые переменные и записывает данные в HTML-файл и GIF-файл, содержащий рукописные данные, если они есть, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="9776a-169">If so, it creates a file name based on the current system time, puts the form data into three string variables and writes the data out to an HTML file and a GIF file containing the ink data, if present, as shown in the following code.</span></span>


```C++
if ( (String.Empty != inkBody) )
{           
    // Use helper method to create a GIF image file from ink data 
    CreateGif(imagePath, fileName, inkBody);
    
    // Create an HTML fragment to reference the image file
    content = "<img src=\"Blogs/Images/" + fileName + ".gif\"></img>";
}                
else 
{
    // If no ink data is available create an HTML fragment that contains
    // the blog's text directly.
    content = "<P>" + textBody + "</P>";
}

// Use helper method to create the blog web page on the server
CreateHtm(blogPath, fileName, blogTitle, content);
```



<span data-ttu-id="9776a-170">Дополнительные сведения о вспомогательных методах см. в образце исходного кода.</span><span class="sxs-lookup"><span data-stu-id="9776a-170">For more details about the helper methods, refer to the sample source code.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="9776a-171">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="9776a-171">Running the Sample</span></span>

<span data-ttu-id="9776a-172">Пакет SDK для планшетных ПК 1,7 по умолчанию устанавливает веб-образец рукописного блога.</span><span class="sxs-lookup"><span data-stu-id="9776a-172">The Tablet PC SDK 1.7 installs the Ink Blog Web sample by default.</span></span> <span data-ttu-id="9776a-173">Чтобы запустить пример, в Internet Explorer перейдите по адресу https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx .</span><span class="sxs-lookup"><span data-stu-id="9776a-173">To run the sample, in Internet Explorer, navigate to https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx.</span></span> <span data-ttu-id="9776a-174">Если вы используете Windows Server 2003, замените имя компьютера на "localhost".</span><span class="sxs-lookup"><span data-stu-id="9776a-174">If you are running Windows Server 2003, substitute your computer name for "localhost".</span></span>

> [!Note]  
> <span data-ttu-id="9776a-175">Скомпилированные веб-образцы не устанавливаются с помощью параметра установки по умолчанию для пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="9776a-175">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="9776a-176">Необходимо выполнить выборочную установку и выбрать подпараметр "предварительно скомпилированные веб-примеры", чтобы установить их.</span><span class="sxs-lookup"><span data-stu-id="9776a-176">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="9776a-177">Можно также запустить пример, открыв и создав проект в Microsoft Visual Studio <entity type="reg"/> .NET, а затем развернув его на отдельном компьютере, на котором запущены службы IIS.</span><span class="sxs-lookup"><span data-stu-id="9776a-177">You can also run the sample by opening and building the project in Microsoft Visual Studio<entity type="reg"/> .NET and then deploying it to a separate computer running IIS.</span></span>

## <a name="troubleshooting-the-sample"></a><span data-ttu-id="9776a-178">Диагностика образца</span><span class="sxs-lookup"><span data-stu-id="9776a-178">Troubleshooting the Sample</span></span>

<span data-ttu-id="9776a-179">Три области, которые могут вызвать трудности при запуске или размещении примера, — это разрешения и распознавание.</span><span class="sxs-lookup"><span data-stu-id="9776a-179">Three areas that may cause difficulty when running or hosting the sample are permissions and recognition.</span></span>

### <a name="permissions"></a><span data-ttu-id="9776a-180">Разрешения</span><span class="sxs-lookup"><span data-stu-id="9776a-180">Permissions</span></span>

<span data-ttu-id="9776a-181">Для примера требуются разрешения на запись в виртуальной корневой папке для учетной записи, которая пытается создать новую запись в блоге.</span><span class="sxs-lookup"><span data-stu-id="9776a-181">The sample requires write permissions within the virtual root folder for the account that is attempting to create a new blog entry.</span></span> <span data-ttu-id="9776a-182">По умолчанию скомпилированная версия примера в пакете SDK для Tablet PC 1,7 имеет правильные разрешения, установленные в соответствии с этим требованием.</span><span class="sxs-lookup"><span data-stu-id="9776a-182">By default, the compiled version of the sample provided in the Tablet PC SDK 1.7 has the correct permissions set to meet this requirement.</span></span>

<span data-ttu-id="9776a-183">Если вы создаете и развертываете пример с помощью предоставленного проекта развертывания веб-приложения, необходимо предоставить группе% MACHINENAME% \\ пользователей доступ на запись к папке файловой системы, на которую указывает виртуальный корневой каталог инкблогвеб (например, C: \\ InetPub \\ wwwroot \\ инкблогвеб).</span><span class="sxs-lookup"><span data-stu-id="9776a-183">If you build and deploy the sample by using the provided Web Setup deployment project, you must give the %MACHINENAME%\\Users group write-access to the file system folder pointed to by the InkBlogWeb virtual root (for example, C:\\InetPub\\WWWRoot\\InkBlogWeb).</span></span> <span data-ttu-id="9776a-184">Группа пользователей включает анонимную учетную запись, используемую службами IIS, тем самым позволяя приложению ASP.NET записывать новые записи в файловую систему.</span><span class="sxs-lookup"><span data-stu-id="9776a-184">The Users group includes the Anonymous account used by IIS, thus allowing the ASP.NET application to write the new blog entries to the file system.</span></span> <span data-ttu-id="9776a-185">Альтернативой является удаление анонимного доступа к виртуальному корню и принудительная проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="9776a-185">An alternative is to remove anonymous access to the virtual root and force authentication.</span></span>

### <a name="recognition"></a><span data-ttu-id="9776a-186">Распознавание</span><span class="sxs-lookup"><span data-stu-id="9776a-186">Recognition</span></span>

<span data-ttu-id="9776a-187">Распознаватели рукописного ввода должны быть установлены для распознавания рукописного ввода в заголовке блога.</span><span class="sxs-lookup"><span data-stu-id="9776a-187">The handwriting recognizers must be installed in order to recognize the ink in the title of the blog.</span></span> <span data-ttu-id="9776a-188">Если вы обращаетесь к приложению Инкблог с компьютера с операционной системой, отличной от Windows XP Tablet PC Edition, но с установленным пакетом SDK 1,7 для Tablet PC, вы можете писать рукописные данные в элементах управления Инкареа, но они не будут отображаться для записей блога.</span><span class="sxs-lookup"><span data-stu-id="9776a-188">If you access the InkBlog application from a computer with an operating system other than Windows XP Tablet PC Edition but with the Tablet PC SDK 1.7 installed, you can write in ink in the InkArea controls, but the recognition engines will not be present and no titles will appear for your blog entries.</span></span> <span data-ttu-id="9776a-189">Однако содержимое рукописного ввода в тексте по-прежнему отображается.</span><span class="sxs-lookup"><span data-stu-id="9776a-189">The ink content in the body still appears, though.</span></span>

### <a name="machine-configuration"></a><span data-ttu-id="9776a-190">Конфигурация компьютера</span><span class="sxs-lookup"><span data-stu-id="9776a-190">Machine Configuration</span></span>

<span data-ttu-id="9776a-191">Если вы установили ASP.NET и платформа .NET Framework на компьютере, а затем удалите и переустановите службы IIS, карты сценариев будут нарушены, и ASP.NET не будет работать.</span><span class="sxs-lookup"><span data-stu-id="9776a-191">If you have installed ASP.NET and the .NET Framework on a computer and you then uninstall and reinstall IIS, the script maps will break and ASP.NET will not work.</span></span> <span data-ttu-id="9776a-192">В этом случае можно восстановить карты сценариев ASP.NET с помощью средства регистрации ASP.NET IIS (ASPNET \_regiis.exe-i).</span><span class="sxs-lookup"><span data-stu-id="9776a-192">If this happens, you can repair the ASP.NET script maps with the ASP.NET IIS Registration tool (Aspnet\_regiis.exe -i).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9776a-193">См. также</span><span class="sxs-lookup"><span data-stu-id="9776a-193">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9776a-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="9776a-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="9776a-195">Рукописный ввод в Интернете</span><span class="sxs-lookup"><span data-stu-id="9776a-195">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> <dt>

[<span data-ttu-id="9776a-196">Форматы данных рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9776a-196">Ink Data Formats</span></span>](ink-data-formats.md)
</dt> <dt>

[<span data-ttu-id="9776a-197">Класс System. Windows. Forms. UserControl</span><span class="sxs-lookup"><span data-stu-id="9776a-197">System.Windows.Forms.UserControl Class</span></span>](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
