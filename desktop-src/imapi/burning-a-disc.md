---
title: Запись образа диска
description: Основное (запись диска) с помощью IMAPI состоит из следующих этапов создания образа файловой системы, содержащего каталоги и файлы для записи на диск. Настройте устройство записи дисков для взаимодействия с оптическим устройством. Создайте модуль записи данных и запишите образ на диск.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337193"
---
# <a name="burning-a-disc-image"></a>Запись образа диска

Основной процесс (запись диска) с помощью IMAPI состоит из следующих шагов:

1.  Создайте образ файловой системы, содержащий каталоги и файлы для записи на диск.
2.  [Настройте устройство записи дисков](#set-up-a-disc-recorder) для взаимодействия с оптическим устройством.
3.  [Создайте модуль записи данных](#create-a-data-writer-and-write-the-burn-image) и запишите образ на диск.

Пример, в котором записывается образ диска, см. в разделе [пример на языке VBScript](#vbscript-example).

## <a name="construct-a-burn-image"></a>Создание образа записи

Образ записи — это поток данных, готовый для записи на оптические носители. Образ записи для форматов ISO9660, Жолиет и UDF состоит из файловой системы отдельных файлов и каталогов. Объект **кфилесистемимаже** — это объект файловой системы, содержащий файлы и каталоги для размещения на оптическом носителе. Интерфейс [**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) предоставляет доступ к объекту и параметрам файловой системы.

После создания объекта файловой системы вызовите методы [**ифилесистемимаже:: креатефилеитем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) и [**Ифилесистемимаже:: креатедиректоритем**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) для создания объектов File и Directory соответственно. Объекты File и Directory можно использовать для предоставления конкретных сведений о файле и каталоге. Методы обработчика событий, доступные для [**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) , могут определять текущий файл, добавляемый в образ файловой системы, число уже скопированных секторов и общее число секторов, которые будут скопированы.

При необходимости загрузочный образ можно подключить к файловой системе с помощью свойства [**ифилесистемимаже::p UT \_ бутимажеоптионс**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) . Пример см. в разделе [Добавление загрузочного образа](adding-a-boot-image.md).

Наконец, вызовите [**ифилесистемимаже:: креатересултимаже**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) , чтобы создать поток данных и предоставить доступ через [**ифилесистемимажересулт**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult). Затем новый поток данных может быть предоставлен непосредственно методу [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) или сохранен в файл для последующего использования.

## <a name="set-up-a-disc-recorder"></a>Настройка средства записи дисков

Объект **MsftDiscMaster2** предоставляет перечисление оптических устройств в системе. Интерфейс [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) предоставляет доступ к результирующему перечислению устройств. Прохождение перечислений для нахождения соответствующего устройства записи. Объект **MsftDiscMaster2** также предоставляет уведомления о событиях при добавлении или удалении оптических устройств с компьютера.

После нахождения оптического устройства записи и получения его идентификатора создайте объект **MsftDiscRecorder2** и инициализируйте средство записи с помощью идентификатора устройства. Интерфейс [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) предоставляет доступ к объекту средства записи, а также к некоторым основным сведениям об устройстве, таким как идентификатор поставщика, идентификатор продукта, версия продукта и методы для извлечения носителя и закрытия области.

## <a name="create-a-data-writer-and-write-the-burn-image"></a>Создание модуля записи данных и запись образа записи

Объект **MsftDiscFormat2Data** предоставляет метод записи, свойства функции записи и свойства, относящиеся к носителю. Интерфейс [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) предоставляет доступ к объекту **MsftDiscFormat2Data** .

Устройство записи дисков связывается с модулем записи формата с помощью свойства [**IDiscFormat2Data::p UT \_ Record**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) . После привязки средства записи к модулю записи формата можно выполнять запросы к носителю и обновлять свойства, связанные с записью, перед записью полученного образа на диск с помощью метода [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .

Другие интерфейсы записи формата, предоставляемые IMAPI, работают аналогично. к дополнительным интерфейсам записи формата относятся:

-   [**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) удаляет перезаписываемый оптический носитель.
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) записывает необработанный образ на оптический носитель.
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) записывает звуковые дорожки на оптические носители.

> [!Note]  
> Переход в состояние электропитания может происходить во время операции записи (т. е. выход пользователя из системы или приостановки работы систем), что приводит к прерыванию процесса записи и возможной потери данных. Рекомендации по программированию см. [в статье предотвращение выхода из системы или приостановка выполнения во время записи](preventing-logoff-or-suspend-during-a-burn.md).

 

## <a name="vbscript-example"></a>Пример на языке VBScript

В этом примере сценария показано, как использовать объекты IMAPI для записи оптического носителя. в частности, следует записать каталог на чистый диск. Код не содержит проверки на ошибки и предполагает следующее:

-   В системе установлено совместимое устройство чтения.
-   Дисковое устройство является вторым диском в системе.
-   В устройство вставляется совместимый диск.
-   Диск пуст.
-   Файлы для записи на диск находятся в папке "g: \\ бурндир".

В этот сценарий можно добавить дополнительные функции, такие как проверка ошибок, совместимость устройств и носителей, уведомление о событиях и вычисление свободного места на диске.


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование IMAPI](using-imapi.md)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[**ифилесистемимаже**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 