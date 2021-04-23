---
title: Определение уровней серьезности
description: Уровни используются для группирования событий и обычно указывают на серьезность или уровень детализации события.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8e2e979e75057a77cca267e540b3ec5469562f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104412732"
---
# <a name="defining-severity-levels"></a><span data-ttu-id="d36d7-103">Определение уровней серьезности</span><span class="sxs-lookup"><span data-stu-id="d36d7-103">Defining Severity Levels</span></span>

<span data-ttu-id="d36d7-104">Уровни используются для группирования событий и обычно указывают на серьезность или уровень детализации события.</span><span class="sxs-lookup"><span data-stu-id="d36d7-104">Levels are used to group events and typically indicate the severity or verbosity of an event.</span></span> <span data-ttu-id="d36d7-105">Чтобы определить уровень, используйте элемент **Level** .</span><span class="sxs-lookup"><span data-stu-id="d36d7-105">To define a level, use the **level** element.</span></span> <span data-ttu-id="d36d7-106">Файл Winmeta.xml определяет следующие часто используемые уровни серьезности:</span><span class="sxs-lookup"><span data-stu-id="d36d7-106">The Winmeta.xml file defines the following commonly used severity levels:</span></span>

-   <span data-ttu-id="d36d7-107">win:Critical</span><span class="sxs-lookup"><span data-stu-id="d36d7-107">win:Critical</span></span>
-   <span data-ttu-id="d36d7-108">win:Error</span><span class="sxs-lookup"><span data-stu-id="d36d7-108">win:Error</span></span>
-   <span data-ttu-id="d36d7-109">win:Warning</span><span class="sxs-lookup"><span data-stu-id="d36d7-109">win:Warning</span></span>
-   <span data-ttu-id="d36d7-110">win:Informational</span><span class="sxs-lookup"><span data-stu-id="d36d7-110">win:Informational</span></span>
-   <span data-ttu-id="d36d7-111">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="d36d7-111">win:Verbose</span></span>

<span data-ttu-id="d36d7-112">Потребители используют уровни для запроса событий, содержащих определенное значение уровня.</span><span class="sxs-lookup"><span data-stu-id="d36d7-112">Consumers use levels to query for events that contain a specific level value.</span></span> <span data-ttu-id="d36d7-113">Сеанс трассировки ETW также может использовать уровни для ограничения событий, записываемых в файл журнала трассировки событий. события со значением уровня, равным или меньшим указанного значения уровня, записываются в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="d36d7-113">An ETW tracing session can also use levels to limit the events that are written to the event tracing log file; events with a level value equal to or less than the specified level value are written to the log file.</span></span> <span data-ttu-id="d36d7-114">Например, если сеанс указал значение уровня для Win: Warning, файл журнала будет содержать предупреждения, ошибки и критические события.</span><span class="sxs-lookup"><span data-stu-id="d36d7-114">For example, if the session specified the level value for win:Warning, the log file would contain warning, error, and critical events.</span></span>

<span data-ttu-id="d36d7-115">В следующем примере показано, как определить уровень.</span><span class="sxs-lookup"><span data-stu-id="d36d7-115">The following example shows how to define a level.</span></span> <span data-ttu-id="d36d7-116">Необходимо указать атрибуты **имени** и **значения** уровня.</span><span class="sxs-lookup"><span data-stu-id="d36d7-116">You must specify the level's **name** and **value** attributes.</span></span> <span data-ttu-id="d36d7-117">Значение атрибута **value** должно находиться в диапазоне от 16 до 255.</span><span class="sxs-lookup"><span data-stu-id="d36d7-117">The value of the **value** attribute must be in the range from 16 through 255.</span></span> <span data-ttu-id="d36d7-118">Атрибуты **symbol** и **Message** являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="d36d7-118">The **symbol** and **message** attributes are optional.</span></span>


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

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>
                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
