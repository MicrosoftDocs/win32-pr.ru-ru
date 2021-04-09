---
title: Определение фильтров
description: Поставщик может определять фильтры, которые сеанс использует для фильтрации событий на основе данных событий.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dd2a21b9c4e01ebc4a32a160b24022c79197b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134442"
---
# <a name="defining-filters"></a>Определение фильтров

Поставщик может определять фильтры, которые сеанс использует для фильтрации событий на основе данных событий. При использовании уровня и ключевых слов ETW определяет, записывается ли событие в журнал. Однако при использовании фильтров поставщик использует критерии фильтрации данных, которые передаются сеансом управления (см. функцию [*енаблекаллбакк*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) ), чтобы определить, записывает ли событие в этот сеанс. Фильтры применяются только в том случае, если сеанс трассировки ETW включает ваш поставщик.

Обычно поставщики просто пишут события, а сеанс определяет типы событий, которые требуется использовать на уровне и ключевые слова. Если поставщик определил фильтр данных для типа события, он может использовать его для фильтрации событий для этого типа событий на основе данных события (семантика фильтра определяется поставщиком). Например, если поставщик создает события обработки, можно определить фильтр данных, который фильтрует события процесса на основе идентификатора процесса. Затем сеанс может передать идентификатор процесса в качестве фильтра данных поставщику и получить только события обработки для этого идентификатора процесса.

В следующем примере показано, как использовать элемент **Filter** для определения фильтра. Необходимо указать атрибуты **имени** и **значения** фильтра; другие атрибуты являются необязательными. Атрибут **tid** является обязательным, если фильтр требует, чтобы сеанс продавал данные фильтра.


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

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
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
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```