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
# <a name="localizing-message-strings"></a><span data-ttu-id="d3866-103">Локализация строк сообщений</span><span class="sxs-lookup"><span data-stu-id="d3866-103">Localizing Message Strings</span></span>

<span data-ttu-id="d3866-104">Каждая строка сообщения, указанная в манифесте, должна ссылаться на строку в разделе **локализации** манифеста.</span><span class="sxs-lookup"><span data-stu-id="d3866-104">Each message string that you specify in the manifest must reference a string in the **localization** section of the manifest.</span></span> <span data-ttu-id="d3866-105">Раздел локализации содержит раздел таблицы строк для каждого поддерживаемого языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="d3866-105">The localization section contains a string table section for each locale that you support.</span></span>

<span data-ttu-id="d3866-106">В следующем примере показано, как определить таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="d3866-106">The following example shows how to define a string table.</span></span> <span data-ttu-id="d3866-107">Необходимо указать атрибуты **ID** и **value** строки.</span><span class="sxs-lookup"><span data-stu-id="d3866-107">You must specify the string's **id** and **value** attributes.</span></span> <span data-ttu-id="d3866-108">Значение атрибута **ID** используется для ссылки на строку в манифесте.</span><span class="sxs-lookup"><span data-stu-id="d3866-108">You use the value of the **id** attribute to reference the string in your manifest.</span></span> <span data-ttu-id="d3866-109">Атрибут **value** содержит локализованную строку.</span><span class="sxs-lookup"><span data-stu-id="d3866-109">The **value** attribute contains the localized string.</span></span>


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


<span data-ttu-id="d3866-110">Вместо добавления локализованных строк в манифест необходимо создать файл многоязычного пользовательского интерфейса (MUI) для каждого поддерживаемого языка.</span><span class="sxs-lookup"><span data-stu-id="d3866-110">Instead of adding localized strings to the manifest, you should create a multilingual user interface (MUI) file for each language that you support.</span></span> <span data-ttu-id="d3866-111">Используйте текстовый файл сообщения для указания локализованных строк.</span><span class="sxs-lookup"><span data-stu-id="d3866-111">Use a message text file to specify your localized strings.</span></span>

<span data-ttu-id="d3866-112">В следующей процедуре описывается создание файла MUI для английского и французского языков.</span><span class="sxs-lookup"><span data-stu-id="d3866-112">The following procedure describes how to create a MUI file for English and French.</span></span>

<span data-ttu-id="d3866-113">**Создание файла MUI для английского и французского языков**</span><span class="sxs-lookup"><span data-stu-id="d3866-113">**To create a MUI file for English and French**</span></span>

1.  <span data-ttu-id="d3866-114">Создайте текстовый файл сообщения, в котором создаются строки сообщений на французском языке.</span><span class="sxs-lookup"><span data-stu-id="d3866-114">Create a message text file that creates the French message strings.</span></span> <span data-ttu-id="d3866-115">Дополнительные сведения о создании текстового файла сообщения см. в разделе [текстовые файлы сообщений](/windows/desktop/EventLog/message-text-files).</span><span class="sxs-lookup"><span data-stu-id="d3866-115">For details on creating a message text file, see [Message Text Files](/windows/desktop/EventLog/message-text-files).</span></span> <span data-ttu-id="d3866-116">Идентификаторы сообщений, указываемые в текстовом файле сообщения, должны совпадать с идентификаторами ресурсов, созданными компилятором сообщений для тех же строк в манифесте.</span><span class="sxs-lookup"><span data-stu-id="d3866-116">The message identifiers that you specify in the message text file must match the resource identifiers that the message compiler generated for the same strings in the manifest.</span></span> <span data-ttu-id="d3866-117">Сведения об определении идентификаторов ресурсов, используемых для строк в манифесте, см. в файле. h, созданном компилятором сообщений при компиляции манифеста.</span><span class="sxs-lookup"><span data-stu-id="d3866-117">To determine the resource identifiers used for the strings in the manifest, see the .h file that the message compiler generated when you compiled the manifest.</span></span>
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


2.  <span data-ttu-id="d3866-118">Выполните следующие команды, чтобы создать БИБЛИОТЕКУ ресурсов, содержащую локализованные строки.</span><span class="sxs-lookup"><span data-stu-id="d3866-118">Run the following commands to create the resource DLL that contains your localized strings.</span></span> <span data-ttu-id="d3866-119">Файл messages.mc — это текстовый файл сообщения, созданный на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="d3866-119">The messages.mc file is the message text file that you created in step 1.</span></span>
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  <span data-ttu-id="d3866-120">В папке, содержащей поставщик, создайте вложенную папку для каждого поддерживаемого языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="d3866-120">In the folder that contains your provider, create a subfolder for each locale that you support.</span></span> <span data-ttu-id="d3866-121">Имя вложенной папки должно быть именем языка для этого языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="d3866-121">The name of the subfolder must be the language name for that locale.</span></span> <span data-ttu-id="d3866-122">Например, для 0x0409 используйте в качестве имени папки en-US.</span><span class="sxs-lookup"><span data-stu-id="d3866-122">For example, for 0x0409, use en-US as the folder name.</span></span>
4.  <span data-ttu-id="d3866-123">Создайте ркконфиг-файл, который сообщает средству Muirct.exe, что необходимо разделить ресурсы строки сообщения из исполняемого файла и библиотек DLL ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d3866-123">Create a .rcconfig file that tells the Muirct.exe tool that you want to split the message string resources from the executable and the resource DLLs.</span></span> <span data-ttu-id="d3866-124">Ниже приведен пример файла ркконфиг.</span><span class="sxs-lookup"><span data-stu-id="d3866-124">The following is an example .rcconfig file.</span></span>
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
  

5.  <span data-ttu-id="d3866-125">Выполните следующие Muirct.exe команды, чтобы разделить строки на английском языке из исполняемого файла поставщика.</span><span class="sxs-lookup"><span data-stu-id="d3866-125">Run the following Muirct.exe commands to split the English strings from the provider executable file.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  <span data-ttu-id="d3866-126">Выполните следующие Muirct.exe команды, чтобы разделить строки на французском из библиотеки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d3866-126">Run the following Muirct.exe commands to split the French strings from the resource DLL.</span></span> <span data-ttu-id="d3866-127">После создания файла MUI удалите файл, не зависящий от языка (fr-FR \\messages.dll).</span><span class="sxs-lookup"><span data-stu-id="d3866-127">Remove the language neutral file (fr-FR\\messages.dll) after the MUI file is created.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  <span data-ttu-id="d3866-128">Переименуйте provider.exe. LN в provider.exe.</span><span class="sxs-lookup"><span data-stu-id="d3866-128">Rename provider.exe.ln to provider.exe.</span></span>