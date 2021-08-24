---
title: Определение каналов
description: События могут записываться в каналы журнала событий, файлы журнала трассировки событий или и то, и другое. Канал — это, по сути, приемник, собирающий события.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c2f932616a131e478c100996fd0b76034b3cccdebf4e3714fd5b9b38ba9678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032484"
---
# <a name="defining-channels"></a>Определение каналов

События могут записываться в каналы журнала событий, файлы журнала трассировки событий или и то, и другое. Канал — это, по сути, приемник, собирающий события. если целевая аудитория для событий использует потребителей событий, например Windows Просмотр событий, необходимо определить новые каналы для получения событий или импортировать существующий канал, определенный другим поставщиком.

Чтобы определить собственные каналы, используйте элемент **Channel** . Чтобы определить импортированный канал, используйте элемент **импортчаннел** . Можно указать до восьми каналов в любом сочетании импортированных каналов или каналов.

Канал должен иметь один из четырех типов: Admin, эксплуатация, аналитика и отладка. Каждый тип канала имеет предполагаемую аудиторию, которая определяет тип событий, записываемых в канал. Описание каждого типа см. в описании сложного типа [**чаннелтипе**](eventmanifestschema-channeltype-complextype.md) .

Чтобы указать канал, на который записывается событие, задайте для атрибута **канала** определения события то же значение, что и для атрибута **Чид** в определении канала. События могут записываться только в один канал за раз, но также могут собираться до 7 других сеансов ETW одновременно.

В следующем примере показано, как импортировать канал. Необходимо задать атрибуты **Чид** и **Name** . Атрибут **Чид** однозначно определяет канал — каждый идентификатор канала в списке каналов должен быть уникальным. Задайте для атрибута **Name** то же имя, которое поставщик использовал при определении канала.


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

                <channels>
                    <channel chid="c1"
                             name="Microsoft-Windows-BaseProvider/Admin"
                             symbol="CHANNEL_BASEPROVIDER_ADMIN"
                             type="Admin"/>
                </channels>

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

Хотя Winmeta.xml определяет устаревшие каналы, которые можно импортировать, их не следует использовать, если только не поддерживают устаревших потребителей, использующих события из устаревших каналов (например, приложения или системы). файл Winmeta.xml включен в Windows SDK.

В следующем примере показано, как определить канал. Необходимо задать атрибуты **Чид**, **Name** и **Type** . Атрибут **Чид** однозначно определяет канал — каждый идентификатор канала в списке каналов должен быть уникальным. Задайте для атрибута **Чид** значение, которое является уникальным для каналов, перечисленных поставщиком. на идентификатор канала указывает ссылка в одном или нескольких определениях событий. Соглашение об именовании канала заключается в использовании имени поставщика и типа канала в форме, *providerName* / *чаннелтипе*.

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

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

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
