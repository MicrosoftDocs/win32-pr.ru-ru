---
title: Определение уровней серьезности
description: Уровни используются для группирования событий и обычно указывают на серьезность или уровень детализации события.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3c3c5e663e476f98bef5c9be3f20cae5e0e88a74a7996f6f515d1d92599eb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863684"
---
# <a name="defining-severity-levels"></a>Определение уровней серьезности

Уровни используются для группирования событий и обычно указывают на серьезность или уровень детализации события. Чтобы определить уровень, используйте элемент **Level** . Файл Winmeta.xml определяет следующие часто используемые уровни серьезности:

-   win:Critical
-   win:Error
-   win:Warning
-   win:Informational
-   win:Verbose

Потребители используют уровни для запроса событий, содержащих определенное значение уровня. Сеанс трассировки ETW также может использовать уровни для ограничения событий, записываемых в файл журнала трассировки событий. события со значением уровня, равным или меньшим указанного значения уровня, записываются в файл журнала. Например, если сеанс указал значение уровня для Win: Warning, файл журнала будет содержать предупреждения, ошибки и критические события.

В следующем примере показано, как определить уровень. Необходимо указать атрибуты **имени** и **значения** уровня. Значение атрибута **value** должно находиться в диапазоне от 16 до 255. Атрибуты **symbol** и **Message** являются необязательными.


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
