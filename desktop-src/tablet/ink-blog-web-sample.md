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
# <a name="ink-blog-web-sample"></a>Пример веб-примера рукописного блога

Пример приложения рукописного ввода блога демонстрирует создание управляемого класса [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) с возможностью рукописного ввода и размещением этого элемента управления в Microsoft Internet Explorer. В этом примере также демонстрируется один из способов отправки рукописных данных по сети с помощью протокола HTTP и сохранения рукописного ввода на сервере.

> [!Note]  
> Для запуска этого примера необходимо установить Microsoft службы IIS (IIS) с ASP.NET. Убедитесь, что компьютер соответствует требованиям, необходимым для запуска приложений ASP.NET на компьютере.

 

> [!Note]  
> Если запустить этот пример на компьютере, отличном от планшетном, с установленным пакетом средств разработки Microsoft Windows XP Tablet PC Edition 1,7, функция распознавания текста для заголовков рукописного ввода не будет работать. Это происходит из-за того, что на компьютере, который не является планшетом с установленным пакетом SDK для Tablet PC 1,7, отсутствуют Распознаватели. Остальная часть приложения выполняется согласно описанию.

 

## <a name="overview"></a>Обзор

Пример рукописного ввода блога создает блог с поддержкой рукописного ввода. Инкблогвеб — это приложение ASP.NET. Рукописный ввод выполняется с помощью пользовательского элемента управления, на который ссылается страница ASP.NET.

Пользовательский элемент управления определяет, установлены ли на клиентском компьютере компоненты платформы Tablet PC. В этом случае пользовательский элемент управления предоставляет пользователю две области с поддержкой рукописного ввода на веб-странице: одну для ввода заголовка для записи блога и одну для текста записи. Если компоненты платформы Tablet PC не установлены, пользователю выдается стандартный элемент управления "текстовое поле" для заголовка и текста записи.

Когда пользователь завершает создание записи, он нажимает кнопку, добавляет блог, а сообщение отправляется на веб-сервер для хранения. На сервере приложение сохраняет текст заголовка и дату публикации, а также ссылку на файл формата GIF. GIF-файл, также сохраненный на сервере, содержит рукописные данные из текста в файле специальная GIF. Дополнительные сведения о формате GIF специальная см. в разделе [Сохранение рукописного ввода в HTML](storing-ink-in-html.md).

В решении Инкблог есть два проекта: проект **инкблогконтролс** и проект **инкблогвеб** .

## <a name="inkblogcontrols-project"></a>Проект Инкблогконтролс

Проект **инкблогконтролс** — это проект [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) , который содержит код для пользовательского элемента управления, обеспечивающего рукописный ввод на веб-странице. Код для этого элемента управления, элемент управления Инкареа, находится в файле Инкареа. cs.

`InkArea`Класс наследует от класса [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) . Конструктор для `InkArea` элемента управления вызывает вспомогательный метод, `CreateInkCollectionSurface` .


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



`CreateInkCollectionSurface`Метод определяет, доступны ли компоненты рукописного ввода Tablet PC на клиенте, пытаясь создать экземпляр класса [InkCollector](/previous-versions/ms583683(v=vs.100)) . Если вызов `CreateInkCollectionSurface` метода завершается с ошибкой, метод возвращает объект [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) в качестве элемента управления.


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



Если происходит сбой конструктора из-за того, что файлы платформы рукописного ввода не найдены, то этот `InputArea` элемент управления создается как элемент управления [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) , а не элемент управления [InkCollector](/previous-versions/ms583683(v=vs.100)) . Затем конструктор изменяет размер элемента управления до размера родительского пользовательского элемента управления и добавляет его в коллекцию Controls родителя.

Класс элементов управления Инкареа реализует три интересных общедоступных свойства: Инкдата, TextData и enable.

Свойство Инкдата доступно только для чтения и предоставляет доступ к сериализованным данным рукописного ввода, если клиент поддерживает рукописный ввод. Если клиент не поддерживает рукописный ввод, свойство Инкдата получает пустую строку. Свойство Инкдата вызывает вспомогательный метод, Сериализеинкдата, чтобы определить, поддерживает ли клиент рукописный ввод.


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



В `SerializeInkData` методе приведение к объекту [InkCollector](/previous-versions/ms583683(v=vs.100)) необходимо при получении объекта [рукописного ввода](/previous-versions/ms583670(v=vs.100)) , поскольку `inputArea` объявляется как [элемент управления](/dotnet/api/system.windows.forms.control?view=netcore-3.1). Если объект рукописного ввода содержит штрихи, то данные рукописного ввода сохраняются в `inkDataBytes` массив байтов как GIF (указывается с помощью значения перечисления [персистенцеформат](/previous-versions/ms552503(v=vs.100)) ). Затем метод преобразует массив байтов в строку в кодировке Base64 и возвращает эту строку.

Предполагая, что клиент может выполнять распознавание, `TextData` свойство возвращает объект [рекогнитионресулт](/previous-versions/ms552537(v=vs.100)) из передачи рукописных данных в распознаватель рукописного ввода. Если клиент не поддерживает рукописный ввод, возвращается содержимое текстового поля, как показано в следующем коде.


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



`TextData`Свойство вызывает вспомогательный метод, `RecognizeInkData` показанный в следующем коде, для выполнения распознавания. Если в системе имеются обработчики распознавания, `RecognizeInkData` метод возвращает строку, содержащую свойство [Топстринг](/previous-versions/ms572009(v=vs.100)) объекта [рекогнитионресулт](/previous-versions/ms552537(v=vs.100)) . В противном случае возвращает пустую строку.


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



`InkEnabled`Свойство является логическим значением только для чтения, указывающим, поддерживается ли рукописный ввод на клиентском компьютере.

Другим важным открытым членом `InkArea` класса Control является `DisposeResources` метод. Этот метод внутренне вызывает `Dispose` метод, чтобы гарантировать очистку всех ресурсов, используемых пользовательским элементом управления. Любое приложение, использующее `InkArea` элемент управления, должно вызывать `DisposeResources` метод после завершения использования элемента управления.

## <a name="inkblogweb-project"></a>Проект Инкблогвеб

Проект Инкблогвеб — это проект развертывания веб-установки, который ссылается на `InkArea` элемент управления для предоставления функциональных возможностей ведения блога. Дополнительные сведения о проектах развертывания веб-установки см. [в разделе Развертывание проекта веб-установки](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Существует два файла. aspx, реализующих пример ведения блогов: Default. aspx и Аддблог. aspx. Default. aspx является страницей по умолчанию для приложения Инкблогвеб. Файл кода программной части для этой страницы — Default. aspx. cs. На этой странице содержится ссылка на страницу, содержащую новую форму записи блога, и отображаются все существующие записи блога. Этот процесс описан далее, после следующего изучения новой страницы формы записи блога Аддблог. aspx.

Аддблог. aspx и его файл кода программной части, Аддблог. aspx. cs, содержат логику и код пользовательского интерфейса для создания новых записей в блоге. Аддблокс. aspx ссылается на два экземпляра класса элемента управления Инкареа, созданный в проекте Инкблогконтролс с помощью элемента объекта HTML, как показано в следующем примере. Один экземпляр имеет `id` атрибут инкблогтитле, а другой имеет атрибут ID инкблогбоди.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

Сборка InkBlogControls.dll должна находиться в том же каталоге, что и ASPX-страница, ссылающаяся на нее. Проект развертывания веб-установки гарантирует, что это так, как свидетельствует присутствие элемента "Основные выходные данные из Инкблогконтролс" в проекте развертывания.

Элемент управления "заголовок" имеет размер 48 пикселей в высоком углу, чтобы упростить ввод одной строки рукописного ввода для заголовка. Элемент управления "текст" имеет размер 296 пикселей в большую часть, чтобы освободить место для больших записей в блоге, имеющих несколько строк или, возможно, чертежей.

Элементы управления Инкареа связаны с функцией скрипта на стороне клиента, Аддблог, посредством стандартного обработчика событий OnClick элемента кнопки HTML.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

На странице также есть HTML-форма, содержащая три скрытых элемента ввода: Блогтитлетекст, Блогбодитекст и Блогбодинкдата. Эта форма используется для передачи данных записи блога обратно на сервер. Аддблог. aspx — это обработчик обратной передачи, определенный для формы.

Функция Аддблог, написанная в Microsoft JScript, <entity type="reg"/> извлекает данные из блога из элементов управления инкареа и отправляет результаты на сервер.


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



Когда данные поступают на сервер, код в Аддблог. aspx. CS проверяет \_ обработчик событий загрузки страницы, чтобы определить, содержит ли свойство формы объекта HttpRequest какие-либо данные. В этом случае он создает имя файла на основе текущего системного времени, помещает данные формы в три строковые переменные и записывает данные в HTML-файл и GIF-файл, содержащий рукописные данные, если они есть, как показано в следующем коде.


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



Дополнительные сведения о вспомогательных методах см. в образце исходного кода.

## <a name="running-the-sample"></a>Запуск примера

Пакет SDK для планшетных ПК 1,7 по умолчанию устанавливает веб-образец рукописного блога. Чтобы запустить пример, в Internet Explorer перейдите по адресу https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Если вы используете Windows Server 2003, замените имя компьютера на "localhost".

> [!Note]  
> Скомпилированные веб-образцы не устанавливаются с помощью параметра установки по умолчанию для пакета SDK. Необходимо выполнить выборочную установку и выбрать подпараметр "предварительно скомпилированные веб-примеры", чтобы установить их.

 

Можно также запустить пример, открыв и создав проект в Microsoft Visual Studio <entity type="reg"/> .NET, а затем развернув его на отдельном компьютере, на котором запущены службы IIS.

## <a name="troubleshooting-the-sample"></a>Диагностика образца

Три области, которые могут вызвать трудности при запуске или размещении примера, — это разрешения и распознавание.

### <a name="permissions"></a>Разрешения

Для примера требуются разрешения на запись в виртуальной корневой папке для учетной записи, которая пытается создать новую запись в блоге. По умолчанию скомпилированная версия примера в пакете SDK для Tablet PC 1,7 имеет правильные разрешения, установленные в соответствии с этим требованием.

Если вы создаете и развертываете пример с помощью предоставленного проекта развертывания веб-приложения, необходимо предоставить группе% MACHINENAME% \\ пользователей доступ на запись к папке файловой системы, на которую указывает виртуальный корневой каталог инкблогвеб (например, C: \\ InetPub \\ wwwroot \\ инкблогвеб). Группа пользователей включает анонимную учетную запись, используемую службами IIS, тем самым позволяя приложению ASP.NET записывать новые записи в файловую систему. Альтернативой является удаление анонимного доступа к виртуальному корню и принудительная проверка подлинности.

### <a name="recognition"></a>Распознавание

Распознаватели рукописного ввода должны быть установлены для распознавания рукописного ввода в заголовке блога. Если вы обращаетесь к приложению Инкблог с компьютера с операционной системой, отличной от Windows XP Tablet PC Edition, но с установленным пакетом SDK 1,7 для Tablet PC, вы можете писать рукописные данные в элементах управления Инкареа, но они не будут отображаться для записей блога. Однако содержимое рукописного ввода в тексте по-прежнему отображается.

### <a name="machine-configuration"></a>Конфигурация компьютера

Если вы установили ASP.NET и платформа .NET Framework на компьютере, а затем удалите и переустановите службы IIS, карты сценариев будут нарушены, и ASP.NET не будет работать. В этом случае можно восстановить карты сценариев ASP.NET с помощью средства регистрации ASP.NET IIS (ASPNET \_regiis.exe-i).

## <a name="related-topics"></a>См. также

<dl> <dt>

[InkCollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Рукописный ввод в Интернете](ink-on-the-web.md)
</dt> <dt>

[Форматы данных рукописного ввода](ink-data-formats.md)
</dt> <dt>

[Класс System. Windows. Forms. UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
