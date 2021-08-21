---
description: В этом примере демонстрируется сериализация и десериализация рукописного ввода в различных форматах.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Пример сериализации рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e71eed5c91bf4fa1524cc52af163516ced0c7362d0d20b8ecf52ac1a08ccd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032272"
---
# <a name="ink-serialization-sample"></a>Пример сериализации рукописного ввода

В этом примере демонстрируется сериализация и десериализация рукописного ввода в различных форматах. Приложение представляет форму с полями для вывода имени, фамилии и сигнатуры. Пользователь может сохранить эти данные как чистый сериализованный формат (ISF), язык XML (XML), используя кодировку Base64 ISF или HTML, которая ссылается на рукописный ввод в виде изображения в формате GIF с кодировкой base64. Приложение также позволяет пользователю открывать файлы, сохраненные в формате XML и ISF. Формат ISF использует расширенные свойства для хранения имени и фамилии, а форматы XML и HTML хранят эти сведения в пользовательских атрибутах.

Этот пример не поддерживает загрузку из формата HTML, так как HTML не подходит для хранения структурированных данных. Поскольку данные разделяются по имени, подписи и т. д., требуется формат, сохраняющий это разделение, например XML или другой формат базы данных.

HTML очень полезен в среде, в которой важно форматирование, например в документе обработки текста. HTML-код, сохраненный в этом образце, использует специальная GIF. Эти GIF в них внедрены ISF, что сохраняет полную точность рукописного ввода. Приложение для обработки текстов может сохранить документ, содержащий несколько типов данных, таких как изображения, таблицы, форматированный текст, и рукописный ввод, сохраненный в формате HTML. Этот HTML-код будет отображаться в браузерах, не распознающих рукописный ввод. Однако при загрузке в приложение, поддерживающее рукописный ввод, вся достоверность исходного рукописного ввода доступна и может быть визуализирована, изменена или использована для распознавания.

В этом примере используются следующие функции.

-   Метод [Load](/previous-versions/ms569609(v=vs.100)) объекта [Ink](/previous-versions/aa515768(v=msdn.10))
-   Метод [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) объекта [Ink](/previous-versions/aa515768(v=msdn.10))
-   Свойство [расширенных свойств](/previous-versions/ms582214(v=vs.100)) объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10))

## <a name="collecting-ink"></a>Сбор рукописных данных

в первую очередь, сослаться на API-интерфейс tablet pc, который устанавливается вместе с Windows Vista и Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



Конструктор создает и включает объект [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` для формы.


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a>Сохранение файла

`SaveAsMenu_Click`Метод обрабатывает диалоговое окно Сохранить как, создает файловый поток, в котором сохраняются данные рукописного ввода, и вызывает метод Save, соответствующий выбору пользователя.

## <a name="saving-to-an-isf-file"></a>Сохранение в файл ISF

В `SaveISF` методе значения первого и последнего имени добавляются в свойство [расширенных свойств](/previous-versions/ms582214(v=vs.100)) свойства [Ink](/previous-versions/ms836505(v=msdn.10)) объекта [InkCollector](/previous-versions/ms836493(v=msdn.10)) до того, как рукописный ввод сериализуется и записывается в файл. После сериализации рукописного ввода значения первого и последнего имени удаляются из свойства расширенных свойств объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) .


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



## <a name="saving-to-an-xml-file"></a>Сохранение в XML-файл

В `SaveXML` методе объект [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) используется для создания XML-документа и записи в него. Используя метод [сохранения](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) , рукописный ввод сначала преобразуется в массив байтов в сериализованном формате в кодировке Base64, а затем массив байтов преобразуется в строку, записываемую в XML-файл. Текстовые данные из формы также записываются в XML-файл.


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



## <a name="saving-to-an-html-file"></a>Сохранение в HTML-файл

Метод Савехтмл использует ограничивающий прямоугольник коллекции [штрихов](/previous-versions/ms827799(v=msdn.10)) для проверки наличия подписи. Если сигнатура существует, она преобразуется в формат GIF специальная с помощью метода [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) объекта Ink и записывается в файл. Затем в HTML-файле указывается ссылка на GIF-файл.


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



## <a name="loading-a-file"></a>Загрузка файла

`OpenMenu_Click`Метод обрабатывает диалоговое окно Открыть, открывает файл и вызывает метод загрузки, соответствующий выбору пользователя.

## <a name="loading-an-isf-file"></a>Загрузка файла ISF

`LoadISF`Метод считывает ранее созданный файл и преобразует массив байтов в рукописный ввод с помощью метода [Load](/previous-versions/ms569609(v=vs.100)) объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) . Сборщик рукописных данных временно отключен для назначения ему объекта рукописного ввода. `LoadISF`Затем метод проверяет свойство [расширенных свойств](/previous-versions/ms582214(v=vs.100)) объекта рукописного ввода для первой и последней строк имени.


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



## <a name="loading-an-xml-file"></a>Загрузка XML-файла

`LoadXML`Метод загружает ранее созданный XML-файл, получает данные из узла рукописного ввода и преобразует данные в этом узле в рукописный код с помощью метода [Load](/previous-versions/ms569609(v=vs.100)) объекта [Ink](/previous-versions/aa515768(v=msdn.10)) . Объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) временно отключен для назначения ему объекта рукописного ввода. Поле подписи становится недействительным, а сведения о первом и последнем имени извлекаются из XML-документа.


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



## <a name="closing-the-form"></a>Закрытие формы

Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) .

 

 
