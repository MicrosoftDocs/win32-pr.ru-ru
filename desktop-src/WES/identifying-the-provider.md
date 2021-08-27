---
title: Определение поставщика
description: Манифест может обозначать одного или нескольких поставщиков. Для обнаружения поставщика используйте элемент provider.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ae37b20ea37d7e67d97846d9e9338e36d52f94
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812669"
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
