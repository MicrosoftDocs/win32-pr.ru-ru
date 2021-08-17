---
title: Определение поставщика
description: Манифест может обозначать одного или нескольких поставщиков. Для обнаружения поставщика используйте элемент provider.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbce9b07aa8a2322311397ae9a48b3d72d60b784e5c55b028afc9772b53f63d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470925"
---
# <a name="identifying-the-provider"></a>Определение поставщика

Манифест может обозначать одного или нескольких поставщиков. Для обнаружения поставщика используйте элемент **provider** . Необходимо указать атрибуты **Name**, **GUID**, **ресаурцефиленаме**, **мессажефиленаме** и **symbol** . При локализации манифеста также следует указать атрибут **Message** , который потребители используют в качестве отображаемого имени поставщика. Если атрибут **Message** не указан, потребители используют значение атрибута **Name** .

В манифесте можно найти до 16 поставщиков. Если требуется определить более 16 поставщиков, необходимо включить раздел **мессажетабле** манифеста, который должен использоваться поставщиками семнадцатого и в для назначения значений ресурсов для определяемых им строк сообщений. Таблица сообщений не должна содержать строки сообщений, для которых определены поставщики от 1 до 16.

В следующем примере показано, как использовать элемент **provider** для указания поставщика.


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

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
