---
title: Локализация строк сообщений
description: Каждая строка сообщения, указанная в манифесте, должна ссылаться на строку в разделе локализации манифеста.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7812aed8bf376994a2cbecfa5997737d9740ec1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070305"
---
# <a name="localizing-message-strings"></a>Локализация строк сообщений

Каждая строка сообщения, указанная в манифесте, должна ссылаться на строку в разделе **локализации** манифеста. Раздел локализации содержит раздел таблицы строк для каждого поддерживаемого языкового стандарта.

В следующем примере показано, как определить таблицу строк. Необходимо указать атрибуты **ID** и **value** строки. Значение атрибута **ID** используется для ссылки на строку в манифесте. Атрибут **value** содержит локализованную строку.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider" 
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}" 
                symbol="PROVIDER_GUID" 
                resourceFileName="<path to the exe or dll that contains the metadata resources>" 
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.ProviderName)">

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="ProviderName" value="Sample Provider"/>
                <string id="PathNotFound" value="The path %1 was not found."/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```


Вместо добавления локализованных строк в манифест необходимо создать файл многоязычного пользовательского интерфейса (MUI) для каждого поддерживаемого языка. Используйте текстовый файл сообщения для указания локализованных строк.

В следующей процедуре описывается создание файла MUI для английского и французского языков.

**Создание файла MUI для английского и французского языков**

1.  Создайте текстовый файл сообщения, в котором создаются строки сообщений на французском языке. Дополнительные сведения о создании текстового файла сообщения см. в разделе [текстовые файлы сообщений](/windows/desktop/EventLog/message-text-files). Идентификаторы сообщений, указываемые в текстовом файле сообщения, должны совпадать с идентификаторами ресурсов, созданными компилятором сообщений для тех же строк в манифесте. Сведения об определении идентификаторов ресурсов, используемых для строк в манифесте, см. в файле. h, созданном компилятором сообщений при компиляции манифеста.
    ```Text
    LanguageNames=(French=0x40C:MSG0040C)

    ; // The following are message definitions.

    MessageId=0x00000065
    SymbolicName=MSG_ProviderName
    Language=French
    <FRENCH STRING GOES HERE>
    .


    MessageId=0x00000066
    SymbolicName=MSG_PathNotFound
    Language=French
    <FRENCH STRING GOES HERE>
    .
    
    ```


2.  Выполните следующие команды, чтобы создать БИБЛИОТЕКУ ресурсов, содержащую локализованные строки. Файл messages.mc — это текстовый файл сообщения, созданный на шаге 1.
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  В папке, содержащей поставщик, создайте вложенную папку для каждого поддерживаемого языкового стандарта. Имя вложенной папки должно быть именем языка для этого языкового стандарта. Например, для 0x0409 используйте в качестве имени папки en-US.
4.  Создайте ркконфиг-файл, который сообщает средству Muirct.exe, что необходимо разделить ресурсы строки сообщения из исполняемого файла и библиотек DLL ресурсов. Ниже приведен пример файла ркконфиг.
    ```XML
    <localization>
          <resources>
                <win32Resources fileType="Application">
                      <neutralResources>
                      </neutralResources>
                      <localizedResources>
                            <resourceType typeNameId="#11"/>
                      </localizedResources>
                </win32Resources>
          </resources>
    </localization>
    ```
  

5.  Выполните следующие Muirct.exe команды, чтобы разделить строки на английском языке из исполняемого файла поставщика.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  Выполните следующие Muirct.exe команды, чтобы разделить строки на французском из библиотеки ресурсов. После создания файла MUI удалите файл, не зависящий от языка (fr-FR \\messages.dll).
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  Переименуйте provider.exe. LN в provider.exe.