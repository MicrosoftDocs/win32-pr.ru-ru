---
title: Создание многосеансового диска
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: 'Дополнительные сведения: создание многосеансового диска'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95147cbadedc76487ae64797c342eb256df0967bf99efecb9e9cda443b5d3010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758580"
---
# <a name="creating-a-multisession-disc"></a>Создание многосеансового диска

API-интерфейс для работы с [образами](about-imapi.md) (IMAPI) поддерживает добавление и удаление файлов на следующих типах многосеансовых дисков:

-   CD-R/CD-RW
-   Single-Layer DVD + R/DVD-R
-   Двойной слой DVD + R
-   BD-R
-   dvd-rw/dvd + RW (**только Windows 7**)
-   DVD-RAM (**только Windows 7**)
-   BD-RE (**только Windows 7**)

Создание многосеансового диска с помощью IMAPI состоит из следующих шагов. каждый из описанных шагов содержит соответствующую часть полного примера сценария Visual Basic, приведенного в последнем разделе.

## <a name="initializing-the-disc-recorder"></a>Инициализация записи на диск

Перед инициализацией устройства объект **MsftDiscMaster2** предоставляет перечисление оптических устройств в системе. Интерфейс [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) предоставляет доступ к этому перечислению устройств, чтобы упростить расположение соответствующего устройства записи. Объект **MsftDiscMaster2** также предоставляет уведомления о событиях при добавлении или удалении оптических устройств с компьютера.

После обнаружения оптического устройства записи и получения назначенного ему идентификатора создайте новый объект **MsftDiscMaster2** и инициализируйте средство записи, используя конкретный идентификатор устройства.

Интерфейс [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) предоставляет доступ к основным сведениям об устройстве, таким как идентификатор поставщика, идентификатор продукта, версия продукта, а также методы извлечения носителя или закрытия лотка.

> [!Note]  
> Дополнительные константы и измерения, объявленные в следующем примере, используются далее в полном примере сценария, расположенном в последнем разделе этого документа. Эти элементы не являются обязательными для инициализации устройства записи дисков.

 


```VB
' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a>Создание модуля записи данных

Объект **MsftDiscFormat2Data** предоставляет метод записи, его свойства, а также свойства, относящиеся к носителю. Интерфейс [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) предоставляет доступ к этому объекту.

Устройство записи дисков привязывается к модулю записи формата с помощью свойства [**IDiscFormat2Data::p UT \_ Record**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) . После привязки модуля записи к модулю записи формата для записи образа на диск с помощью метода [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) можно выполнить запросы свойств мультимедиа и записи.

> [!Note]  
> Строка имени клиента, указанная в приведенном ниже образце кода, должна быть скорректирована соответствующим образом для конкретного приложения.

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a>Создание объекта файловой системы

Чтобы записать новый сеанс, сначала необходимо создать образ записи. Образ записи для форматов **ISO9660**, **Жолиет** и **UDF** состоит из файловых систем отдельных файлов и каталогов. Объект **мсфтфилесистемимаже** — это объект файловой системы, содержащий файлы и каталоги, которые будут размещены на оптическом носителе. Интерфейс [**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) предоставляет доступ к объекту и параметрам файловой системы.


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a>Импорт файловой системы

Прежде чем продолжать, убедитесь, что диск не пуст, проверив свойство [**IDiscFormat2:: Get \_ медиахеуристикаллибланк**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) .

После создания объекта **мсфтфилесистемимаже** свойство [**ифилесистемимаже::p UT \_ мултисессионинтерфацес**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) должно быть инициализировано до вызова метода [**ифилесистемимаже:: импортфилесистем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) или [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) для импорта файловой системы из последнего записанного сеанса. Эти методы будут автоматически заполнять объект **мсфтфилесистемимаже** сведениями, описывающими ранее записанные файлы и каталоги.

> [!Note]  
> Свойство [**ифилесистемимаже::p UT \_ мултисессионинтерфацес**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) обычно инициализируется с помощью многосеансовых интерфейсов, предоставляемых модулем записи данных через свойство [**IDiscFormat2Data:: Get \_ мултисессионинтерфацес**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) .

 

Попытка установить свойство **ифилесистемимаже::p UT \_ мултисессионинтерфацес** завершится ошибкой, если IMAPI не поддерживает многосеансовую поддержку для вставленного носителя, или не удается добавить носитель по какой-либо другой причине (например, потому, что он закрыт).

Если предыдущий сеанс записи содержал более одного типа файловой системы, метод [**ифилесистемимаже:: импортфилесистем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) будет импортировать данные из наиболее расширенного типа файловой системы. Например, в примере, приведенном в этом разделе, UDF — это импортированная файловая система. Однако использование метода [**ифилесистемимаже:: импортспеЦификфилесистем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) позволяет импортировать определенную файловую систему.

> [!Note]  
> Метод [**ифилесистемимаже:: идентифифилесистемсондиск**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) можно использовать для определения того, какие файловые системы доступны на диске.

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a>Добавление или удаление файлов в файловой системе

После создания объекта файловой системы и импорта файловой системы из предыдущего сеанса вызовите методы [**ифилесистемимаже:: креатефилеитем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) и [**Ифилесистемимаже:: креатедиректоритем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) , чтобы создать новые объекты File и Directory соответственно. Объекты File и Directory содержат конкретные сведения о файлах и каталогах. Кроме того, метод [**ифсидиректоритем:: аддтри**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) объекта каталога, представленного через интерфейс [**ифсидиректоритем**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) , можно использовать для добавления существующих файлов и каталогов с другого устройства хранения (т. е. жесткого диска).

Метод обновления обработчика событий, доступный для [**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) , определяет текущий файл, добавляемый в образ файловой системы, число уже скопированных секторов и общее число секторов для копирования.

Чтобы удалить существующие файлы и каталоги из файловой системы, используйте методы [**ифсидиректоритем:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) и [**Ифсидиректоритем:: ремоветри**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) объектов каталога, представленных через интерфейс [**ифсидиректоритем**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) . Свойство [**ифилесистемимаже:: Get \_ root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) используется для получения указателя на корневой каталог файловой системы и интерфейса **ифсидиректоритем** для прохода по дереву каталогов.

> [!Note]  
> Файлы и каталоги, удаленные с помощью методов [**ифсидиректоритем:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) и [**Ифсидиректоритем:: ремоветри**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) , физически не удаляются с диска, а расширенное программное обеспечение может легко восстановить удаленные данные.

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a>Создание образа файловой системы

Последним шагом является вызов [**ифилесистемимаже:: креатересултимаже**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) для создания потока данных для образа записи и предоставления доступа к нему через интерфейс [**ифилесистемимажересулт**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) . Этот поток данных может быть предоставлен непосредственно методу [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) или сохранен в файл для последующего использования.


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a>Пример сводки

в следующем примере скрипта Visual Basic показано, как использовать объекты IMAPI для создания многосеансовых дисков. В этом примере создается новый сеанс и добавляется каталог на диск. В целях простоты код не выполняет расширенную проверку на наличие ошибок и предполагает следующее:

-   В системе установлено совместимое устройство чтения.
-   Устройство является первым диском в системе.
-   В устройство вставляется совместимый диск.
-   Файлы, добавляемые на диск, находятся в папке "g: \\ бурндир".

Дополнительные функции, такие как обширная проверка ошибок, совместимость с устройствами и носителями, уведомление о событиях и вычисление свободного места на диске, можно добавить в скрипт.


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование IMAPI](using-imapi.md)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
