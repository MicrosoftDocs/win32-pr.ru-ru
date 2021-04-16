---
description: В этом примере демонстрируется сериализация и десериализация рукописного ввода в различных форматах.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Пример сериализации рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e898f91db17efcb7579c067e7db5c422da8213a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540410"
---
# <a name="ink-serialization-sample"></a><span data-ttu-id="c7029-103">Пример сериализации рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="c7029-103">Ink Serialization Sample</span></span>

<span data-ttu-id="c7029-104">В этом примере демонстрируется сериализация и десериализация рукописного ввода в различных форматах.</span><span class="sxs-lookup"><span data-stu-id="c7029-104">This sample demonstrates how to serialize and de-serialize ink in various formats.</span></span> <span data-ttu-id="c7029-105">Приложение представляет форму с полями для вывода имени, фамилии и сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="c7029-105">The application represents a form with fields for inputting first name, last name, and signature.</span></span> <span data-ttu-id="c7029-106">Пользователь может сохранить эти данные как чистый сериализованный формат (ISF), язык XML (XML), используя кодировку Base64 ISF или HTML, которая ссылается на рукописный ввод в виде изображения в формате GIF с кодировкой base64.</span><span class="sxs-lookup"><span data-stu-id="c7029-106">The user may save this data as pure ink serialized format (ISF), Extensible Markup Language (XML) using base64 encoded ISF, or HTML, which references ink in a base64 encoded fortified Graphics Interchange Format (GIF) image.</span></span> <span data-ttu-id="c7029-107">Приложение также позволяет пользователю открывать файлы, сохраненные в формате XML и ISF.</span><span class="sxs-lookup"><span data-stu-id="c7029-107">The application also enables the user to open files that were saved as XML and ISF formats.</span></span> <span data-ttu-id="c7029-108">Формат ISF использует расширенные свойства для хранения имени и фамилии, а форматы XML и HTML хранят эти сведения в пользовательских атрибутах.</span><span class="sxs-lookup"><span data-stu-id="c7029-108">The ISF format uses extended properties to store the first name and last name, whereas the XML and HTML formats store this information in custom attributes.</span></span>

<span data-ttu-id="c7029-109">Этот пример не поддерживает загрузку из формата HTML, так как HTML не подходит для хранения структурированных данных.</span><span class="sxs-lookup"><span data-stu-id="c7029-109">This sample does not support loading from the HTML format, because HTML is not suitable for storing structured data.</span></span> <span data-ttu-id="c7029-110">Поскольку данные разделяются по имени, подписи и т. д., требуется формат, сохраняющий это разделение, например XML или другой формат базы данных.</span><span class="sxs-lookup"><span data-stu-id="c7029-110">Because the data is separated into name, signature, and so on, a format that preserves this separation, such as XML or another kind of database format, is required.</span></span>

<span data-ttu-id="c7029-111">HTML очень полезен в среде, в которой важно форматирование, например в документе обработки текста.</span><span class="sxs-lookup"><span data-stu-id="c7029-111">HTML is very useful in an environment in which formatting is important, such as in a word processing document.</span></span> <span data-ttu-id="c7029-112">HTML-код, сохраненный в этом образце, использует специальная GIF.</span><span class="sxs-lookup"><span data-stu-id="c7029-112">The HTML that is saved by this sample uses fortified GIFs.</span></span> <span data-ttu-id="c7029-113">Эти GIF в них внедрены ISF, что сохраняет полную точность рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c7029-113">These GIFs have ISF embedded within them, which preserves the full fidelity of the ink.</span></span> <span data-ttu-id="c7029-114">Приложение для обработки текстов может сохранить документ, содержащий несколько типов данных, таких как изображения, таблицы, форматированный текст, и рукописный ввод, сохраненный в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="c7029-114">A word processing application can save a document containing multiple types of data, such as images, tables, formatted text, and ink persisted in an HTML format.</span></span> <span data-ttu-id="c7029-115">Этот HTML-код будет отображаться в браузерах, не распознающих рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="c7029-115">This HTML would render in browsers that do not recognize ink.</span></span> <span data-ttu-id="c7029-116">Однако при загрузке в приложение, поддерживающее рукописный ввод, вся достоверность исходного рукописного ввода доступна и может быть визуализирована, изменена или использована для распознавания.</span><span class="sxs-lookup"><span data-stu-id="c7029-116">However, when loaded into an application that is ink-enabled, the full fidelity of the original ink is available and can be rendered, edited, or used for recognition.</span></span>

<span data-ttu-id="c7029-117">В этом примере используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="c7029-117">The following features are used in this sample:</span></span>

-   <span data-ttu-id="c7029-118">Метод [Load](/previous-versions/ms569609(v=vs.100)) объекта [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c7029-118">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method</span></span>
-   <span data-ttu-id="c7029-119">Метод [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) объекта [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c7029-119">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method</span></span>
-   <span data-ttu-id="c7029-120">Свойство [расширенных свойств](/previous-versions/ms582214(v=vs.100)) объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c7029-120">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property</span></span>

## <a name="collecting-ink"></a><span data-ttu-id="c7029-121">Сбор рукописных данных</span><span class="sxs-lookup"><span data-stu-id="c7029-121">Collecting Ink</span></span>

<span data-ttu-id="c7029-122">Во-первых, обратитесь к API Tablet PC, который устанавливается вместе с пакетом SDK для Windows Vista и Windows XP Tablet PC Edition (пакет средств разработки программного обеспечения).</span><span class="sxs-lookup"><span data-stu-id="c7029-122">First, reference the Tablet PC API, which are installed with the Windows Vista and Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="c7029-123">Конструктор создает и включает объект [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` для формы.</span><span class="sxs-lookup"><span data-stu-id="c7029-123">The constructor creates and enables an [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic`, for the form.</span></span>


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a><span data-ttu-id="c7029-124">Сохранение файла</span><span class="sxs-lookup"><span data-stu-id="c7029-124">Saving a File</span></span>

<span data-ttu-id="c7029-125">`SaveAsMenu_Click`Метод обрабатывает диалоговое окно Сохранить как, создает файловый поток, в котором сохраняются данные рукописного ввода, и вызывает метод Save, соответствующий выбору пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7029-125">The `SaveAsMenu_Click` method handles the Save As dialog box, creates a file stream in which to save the ink data, and calls the save method that corresponds to the user's choice.</span></span>

## <a name="saving-to-an-isf-file"></a><span data-ttu-id="c7029-126">Сохранение в файл ISF</span><span class="sxs-lookup"><span data-stu-id="c7029-126">Saving to an ISF File</span></span>

<span data-ttu-id="c7029-127">В `SaveISF` методе значения первого и последнего имени добавляются в свойство [расширенных свойств](/previous-versions/ms582214(v=vs.100)) свойства [Ink](/previous-versions/ms836505(v=msdn.10)) объекта [InkCollector](/previous-versions/ms836493(v=msdn.10)) до того, как рукописный ввод сериализуется и записывается в файл.</span><span class="sxs-lookup"><span data-stu-id="c7029-127">In the `SaveISF` method, the first and last name values are added to the [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property of the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [Ink](/previous-versions/ms836505(v=msdn.10)) property, before the ink is serialized and written to the file.</span></span> <span data-ttu-id="c7029-128">После сериализации рукописного ввода значения первого и последнего имени удаляются из свойства расширенных свойств объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="c7029-128">After the ink has been serialized, the first and last name values are removed from the [Ink](/previous-versions/aa515768(v=msdn.10)) object's ExtendedProperties property.</span></span>


```C++
byte[] isf;

// This is the ink object which is serialized
ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Store the name fields in the ink object
// These fields roundtrip through the ISF format
// Ignore empty fields since strictly empty strings 
//       cannot be stored in ExtendedProperties.
if (FirstNameBox.Text.Length > 0)
{
    inkProperties.Add(FirstName, FirstNameBox.Text);
}
if (LastNameBox.Text.Length > 0)
{
    inkProperties.Add(LastName, LastNameBox.Text);
}

// Perform the serialization
isf = ic.Ink.Save(PersistenceFormat.InkSerializedFormat);

// If the first and last names were added as extended
// properties to the ink, remove them - these properties
// are only used for the save and there is no need to
// keep them around on the ink object.
if (inkProperties.DoesPropertyExist(FirstName))
{
    inkProperties.Remove(FirstName);
}
if (inkProperties.DoesPropertyExist(LastName))
{
    inkProperties.Remove(LastName);
}

// Write the ISF to the stream
s.Write(isf,0,isf.Length);
```



## <a name="saving-to-an-xml-file"></a><span data-ttu-id="c7029-129">Сохранение в XML-файл</span><span class="sxs-lookup"><span data-stu-id="c7029-129">Saving to an XML File</span></span>

<span data-ttu-id="c7029-130">В `SaveXML` методе объект [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) используется для создания XML-документа и записи в него.</span><span class="sxs-lookup"><span data-stu-id="c7029-130">In the `SaveXML` method, an [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) object is used to create and write to an XML document.</span></span> <span data-ttu-id="c7029-131">Используя метод [сохранения](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) , рукописный ввод сначала преобразуется в массив байтов в сериализованном формате в кодировке Base64, а затем массив байтов преобразуется в строку, записываемую в XML-файл.</span><span class="sxs-lookup"><span data-stu-id="c7029-131">Using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, the ink is first converted to a base64 encoded Ink Serialized Format byte array, and then the byte array is converted to a string to be written out to the XML file.</span></span> <span data-ttu-id="c7029-132">Текстовые данные из формы также записываются в XML-файл.</span><span class="sxs-lookup"><span data-stu-id="c7029-132">The text data from the form is also written out to the XML file.</span></span>


```C++
// Get the base64 encoded ISF
base64ISF_bytes = ic.Ink.Save(PersistenceFormat.Base64InkSerializedFormat);

// Convert it to a String
base64ISF_string = utf8.GetString(base64ISF_bytes);

// Write the ISF containing node to the XML
xwriter.WriteElementString("Ink", base64ISF_string);

// Write the text data from the form
// Note that the names are stored as XML fields, rather
// than custom properties, so that these properties can 
// be most easily accessible if the XML is saved in a database.
xwriter.WriteElementString("FirstName",FirstNameBox.Text);
xwriter.WriteElementString("LastName",LastNameBox.Text);
```



## <a name="saving-to-an-html-file"></a><span data-ttu-id="c7029-133">Сохранение в HTML-файл</span><span class="sxs-lookup"><span data-stu-id="c7029-133">Saving to an HTML File</span></span>

<span data-ttu-id="c7029-134">Метод Савехтмл использует ограничивающий прямоугольник коллекции [штрихов](/previous-versions/ms827799(v=msdn.10)) для проверки наличия подписи.</span><span class="sxs-lookup"><span data-stu-id="c7029-134">The SaveHTML method uses the bounding box of the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection to test for the presence of a signature.</span></span> <span data-ttu-id="c7029-135">Если сигнатура существует, она преобразуется в формат GIF специальная с помощью метода [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) объекта Ink и записывается в файл.</span><span class="sxs-lookup"><span data-stu-id="c7029-135">If the signature exists, it is converted to the fortified GIF format using the ink object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, and written to a file.</span></span> <span data-ttu-id="c7029-136">Затем в HTML-файле указывается ссылка на GIF-файл.</span><span class="sxs-lookup"><span data-stu-id="c7029-136">The GIF is then referenced in the HTML file.</span></span>


```C++
if (ic.Ink.Strokes.GetBoundingBox().IsEmpty)
{
   MessageBox.Show("Unable to save empty ink in HTML persistence format.");
}
else
{
    FileStream gifFile;
    byte[] fortifiedGif = null;
    ...

    // Create a directory to store the fortified GIF which also contains ISF
    // and open the file for writing
    Directory.CreateDirectory(nameBase + "_files");
    using (FileStream gifFile = File.OpenWrite(nameBase + "_files\\signature.gif"))
    {

        // Generate the fortified GIF represenation of the ink
        fortifiedGif = ic.Ink.Save(PersistenceFormat.Gif);

        // Write and close the gif file
        gifFile.Write(fortifiedGif, 0, fortifiedGif.Length);
    }
```



## <a name="loading-a-file"></a><span data-ttu-id="c7029-137">Загрузка файла</span><span class="sxs-lookup"><span data-stu-id="c7029-137">Loading a File</span></span>

<span data-ttu-id="c7029-138">`OpenMenu_Click`Метод обрабатывает диалоговое окно Открыть, открывает файл и вызывает метод загрузки, соответствующий выбору пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7029-138">The `OpenMenu_Click` method handles the Open dialog box, opens the file, and calls the loading method that corresponds to the user's choice.</span></span>

## <a name="loading-an-isf-file"></a><span data-ttu-id="c7029-139">Загрузка файла ISF</span><span class="sxs-lookup"><span data-stu-id="c7029-139">Loading an ISF File</span></span>

<span data-ttu-id="c7029-140">`LoadISF`Метод считывает ранее созданный файл и преобразует массив байтов в рукописный ввод с помощью метода [Load](/previous-versions/ms569609(v=vs.100)) объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="c7029-140">The `LoadISF` method reads the previously created file and converts the Byte array to ink with the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="c7029-141">Сборщик рукописных данных временно отключен для назначения ему объекта рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c7029-141">The ink collector is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="c7029-142">`LoadISF`Затем метод проверяет свойство [расширенных свойств](/previous-versions/ms582214(v=vs.100)) объекта рукописного ввода для первой и последней строк имени.</span><span class="sxs-lookup"><span data-stu-id="c7029-142">The `LoadISF` method then checks the Ink object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property for the first and last name strings.</span></span>


```C++
Ink loadedInk = new Ink();
byte[] isfBytes = new byte[s.Length];

// read in the ISF
s.Read(isfBytes, 0, (int) s.Length);

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
loadedInk.Load(isfBytes);

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Get the raw data out of this stroke's extended
// properties list, using the previously defined 
// Guid as a key to the extended property.
// Since the save method stored the first and last
// name information as extended properties, this
// information can be remove now that the load is complete.
if (inkProperties.DoesPropertyExist(FirstName))
{
    FirstNameBox.Text = (String) inkProperties[FirstName].Data;
    inkProperties.Remove(FirstName);
}
else
{
    FirstNameBox.Text = String.Empty;
}

if (inkProperties.DoesPropertyExist(LastName))
{
    LastNameBox.Text = (String) inkProperties[LastName].Data;
    inkProperties.Remove(LastName);
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="loading-an-xml-file"></a><span data-ttu-id="c7029-143">Загрузка XML-файла</span><span class="sxs-lookup"><span data-stu-id="c7029-143">Loading an XML File</span></span>

<span data-ttu-id="c7029-144">`LoadXML`Метод загружает ранее созданный XML-файл, получает данные из узла рукописного ввода и преобразует данные в этом узле в рукописный код с помощью метода [Load](/previous-versions/ms569609(v=vs.100)) объекта [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="c7029-144">The `LoadXML` method loads a previously created XML file, retrieves data from the Ink node, and converts the data in the node to ink using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="c7029-145">Объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) временно отключен для назначения ему объекта рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c7029-145">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="c7029-146">Поле подписи становится недействительным, а сведения о первом и последнем имени извлекаются из XML-документа.</span><span class="sxs-lookup"><span data-stu-id="c7029-146">The signature box is invalidated, and the first and last name information is retrieved from the XML document.</span></span>


```C++
// This object encodes our byte data to a UTF8 string
UTF8Encoding utf8 = new UTF8Encoding();

XmlDocument xd = new XmlDocument();
XmlNodeList nodes;
Ink loadedInk = new Ink();

// Load the XML data into a DOM
xd.Load(s);

// Get the data in the ink node
nodes = xd.GetElementsByTagName("Ink");

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
if (0 != nodes.Count)
    loadedInk.Load(utf8.GetBytes(nodes[0].InnerXml));

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

// Get the data in the FirstName node
nodes = xd.GetElementsByTagName("FirstName");
if (0 != nodes.Count)
{
    FirstNameBox.Text = nodes[0].InnerXml;
}
else
{
    FirstNameBox.Text = String.Empty;
}

// Get the data in the LastName node
nodes = xd.GetElementsByTagName("LastName");
if (0 != nodes.Count)
{
    LastNameBox.Text = nodes[0].InnerXml;
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="closing-the-form"></a><span data-ttu-id="c7029-147">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="c7029-147">Closing the Form</span></span>

<span data-ttu-id="c7029-148">Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="c7029-148">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object.</span></span>

 

 
