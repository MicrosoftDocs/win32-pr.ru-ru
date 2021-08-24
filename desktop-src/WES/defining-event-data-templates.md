---
title: Определение шаблонов данных событий
description: Поставщики используют шаблоны данных для определения данных событий, которые они включают в событие, и для определения данных фильтра, которые сеанс трассировки ETW может передать поставщику при включении поставщика.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5480ca158916801665943bd33b886bfcd5d73015e8730c1dd108123dadc1995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652614"
---
# <a name="defining-event-data-templates"></a>Определение шаблонов данных событий

Поставщики используют шаблоны данных для определения данных событий, которые они включают в событие, и для определения данных фильтра, которые сеанс трассировки ETW может передать поставщику при включении поставщика. Если событие не содержит данных, связанных с событиями, шаблон не будет определен. Чтобы определить шаблон, используйте элемент **template** . Шаблон включает элемент данных для каждого элемента данных, который поставщик включает в событие. Можно указать целочисленные типы, строки, массивы и структуры. Данные событий необходимо записать в том порядке, в котором элементы данных были определены в шаблоне.

Можно также включить в шаблон XML-фрагмент, который потребители должны использовать для определения способа отображения данных события. Если фрагмент не включен, потребители должны визуализировать данные событий в том порядке, в котором элементы данных были определены в шаблоне.

При определении шаблона необходимо присвоить ему идентификатор шаблона, который используется для ссылки на шаблон в определении события. Каждый элемент данных в шаблоне должен указывать имя и тип входных данных (список входных типов см. в разделе "Примечания" сложного типа [**InputType**](eventmanifestschema-inputtype-complextype.md) ). Если тип входных данных может быть визуализирован в нескольких форматах, следует указать тип выходных данных, который сообщает потребителям о том, как визуализировать элемент данных. Например, тип входных данных UInt32 можно визуализировать как целое число без знака, идентификатор потока, IPv4-адрес и код ошибки Win32. Если тип выходных данных не указан, потребители должны использовать тип вывода по умолчанию входного типа для отрисовки элемента данных.

Чтобы указать массив, включите атрибут **Count** в элемент данных и задайте для него число элементов в массиве. Массив может быть массивом размера переменной или массивом фиксированного размера. Если массив является массивом фиксированного размера, задайте для параметра **Count** значение size массива. Например, если массив целых чисел имеет фиксированный размер 10, установите значение **счетчика** равным 10. При написании массива необходимо записать 40 байт данных.

Если массив является массивом размера переменной, задайте параметру **Count** имя элемента данных, который содержит размер массива. Если массив содержит указатели, адреса указателей записываются в виде данных события, а не данных, на которые указывает точка указателей.

Если элемент данных является двоичным BLOB-объектом, необходимо указать атрибут **length** . Можно также указать атрибут **length** для строк фиксированной длины.

Укажите атрибут **Map** , если элемент данных представляет значение перечисления, и вы хотите, чтобы потребитель печатал строку для значения, а не самого значения.

При включении структур в шаблон следует писать члены структуры по отдельности, а не писать структуру, если вы не гарантируете выравнивание по 8 байтам.

Следует тщательно продумать сведения, включаемые в события, особенно если события записываются в глобальные каналы. Как правило, в события не следует включать частные сведения. Сюда входят пароли в виде открытого текста и персональные данные пользователя. Кроме того, программы, выполняемые пользователем, URL-адреса, посещенные пользователем, и другие сведения, относящиеся к действиям пользователя на компьютере, следует считать частными.

если необходимо записывать в события url-адреса и имена пользователей, не записывает их в Windows каналы (система и приложение), так как эти каналы доступны для чтения всеми пользователями, прошедшим проверку подлинности. Вместо этого запишите их в собственные рабочие или аналитические каналы. Установите разрешения на доступ к этим каналам, чтобы разрешить только администраторам чтение событий. Может потребоваться предоставить соответствующее раскрытие, чтобы уведомить пользователей о том, что личные данные становятся доступными администраторам.

В следующем примере показано, как определить шаблон. Необходимо указать атрибут **tid** шаблона, на который ссылается определение события или определение фильтра.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
