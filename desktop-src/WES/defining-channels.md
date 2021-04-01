---
title: Определение каналов
description: События могут записываться в каналы журнала событий, файлы журнала трассировки событий или и то, и другое. Канал — это, по сути, приемник, собирающий события.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3c73697aa11e7b63ace0ece33be23ca7a1b883
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104133595"
---
# <a name="defining-channels"></a><span data-ttu-id="04859-104">Определение каналов</span><span class="sxs-lookup"><span data-stu-id="04859-104">Defining Channels</span></span>

<span data-ttu-id="04859-105">События могут записываться в каналы журнала событий, файлы журнала трассировки событий или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="04859-105">Events can be written to event log channels, event tracing log files, or both.</span></span> <span data-ttu-id="04859-106">Канал — это, по сути, приемник, собирающий события.</span><span class="sxs-lookup"><span data-stu-id="04859-106">A channel is basically a sink that collects events.</span></span> <span data-ttu-id="04859-107">Если целевая аудитория для событий использует потребителей событий, например Просмотр событий Windows, необходимо определить новые каналы для получения событий или импортировать существующий канал, определенный другим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="04859-107">If the target audience for your events uses event consumers such as the Windows Event Viewer, you must define new channels to collect your events or import an existing channel that another provider defined.</span></span>

<span data-ttu-id="04859-108">Чтобы определить собственные каналы, используйте элемент **Channel** .</span><span class="sxs-lookup"><span data-stu-id="04859-108">To define your own channels, use the **channel** element.</span></span> <span data-ttu-id="04859-109">Чтобы определить импортированный канал, используйте элемент **импортчаннел** .</span><span class="sxs-lookup"><span data-stu-id="04859-109">To define an imported channel, use the **importChannel** element.</span></span> <span data-ttu-id="04859-110">Можно указать до восьми каналов в любом сочетании импортированных каналов или каналов.</span><span class="sxs-lookup"><span data-stu-id="04859-110">You can specify up to eight channels in any combination of imported channels or channels that you define.</span></span>

<span data-ttu-id="04859-111">Канал должен иметь один из четырех типов: Admin, эксплуатация, аналитика и отладка.</span><span class="sxs-lookup"><span data-stu-id="04859-111">The channel must be of one of four types: Admin, Operational, Analytic, and Debug.</span></span> <span data-ttu-id="04859-112">Каждый тип канала имеет предполагаемую аудиторию, которая определяет тип событий, записываемых в канал.</span><span class="sxs-lookup"><span data-stu-id="04859-112">Each channel type has an intended audience, which determines the type of events that you write to the channel.</span></span> <span data-ttu-id="04859-113">Описание каждого типа см. в описании сложного типа [**чаннелтипе**](eventmanifestschema-channeltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="04859-113">For a description of each type, see the [**ChannelType**](eventmanifestschema-channeltype-complextype.md) complex type.</span></span>

<span data-ttu-id="04859-114">Чтобы указать канал, на который записывается событие, задайте для атрибута **канала** определения события то же значение, что и для атрибута **Чид** в определении канала.</span><span class="sxs-lookup"><span data-stu-id="04859-114">To specify the channel to which an event is written, set the event definition's **channel** attribute to the same value as the channel definition's **chid** attribute.</span></span> <span data-ttu-id="04859-115">События могут записываться только в один канал за раз, но также могут собираться до 7 других сеансов ETW одновременно.</span><span class="sxs-lookup"><span data-stu-id="04859-115">Events can only be written to one channel at a time, but can also be collected by up to 7 other ETW sessions at the same time.</span></span>

<span data-ttu-id="04859-116">В следующем примере показано, как импортировать канал.</span><span class="sxs-lookup"><span data-stu-id="04859-116">The following example shows how to import a channel.</span></span> <span data-ttu-id="04859-117">Необходимо задать атрибуты **Чид** и **Name** .</span><span class="sxs-lookup"><span data-stu-id="04859-117">You must set the **chid** and **name** attributes.</span></span> <span data-ttu-id="04859-118">Атрибут **Чид** однозначно определяет канал — каждый идентификатор канала в списке каналов должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="04859-118">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="04859-119">Задайте для атрибута **Name** то же имя, которое поставщик использовал при определении канала.</span><span class="sxs-lookup"><span data-stu-id="04859-119">Set the **name** attribute to the same name that the provider used when it defined the channel.</span></span>


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

<span data-ttu-id="04859-120">Хотя Winmeta.xml определяет устаревшие каналы, которые можно импортировать, их не следует использовать, если только не поддерживают устаревших потребителей, использующих события из устаревших каналов (например, приложения или системы).</span><span class="sxs-lookup"><span data-stu-id="04859-120">Although Winmeta.xml defines legacy channels that you can import, you should not use them unless you are supporting legacy consumers that consume events out of the legacy channels (for example, Application or System).</span></span> <span data-ttu-id="04859-121">Файл Winmeta.xml включен в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="04859-121">The Winmeta.xml file is included in the Windows SDK.</span></span>

<span data-ttu-id="04859-122">В следующем примере показано, как определить канал.</span><span class="sxs-lookup"><span data-stu-id="04859-122">The following example shows how to define a channel.</span></span> <span data-ttu-id="04859-123">Необходимо задать атрибуты **Чид**, **Name** и **Type** .</span><span class="sxs-lookup"><span data-stu-id="04859-123">You must set the **chid**, **name**, and **type** attributes.</span></span> <span data-ttu-id="04859-124">Атрибут **Чид** однозначно определяет канал — каждый идентификатор канала в списке каналов должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="04859-124">The **chid** attribute uniquely identifies the channel—each channel identifier in your list of channels must be unique.</span></span> <span data-ttu-id="04859-125">Задайте для атрибута **Чид** значение, которое является уникальным для каналов, перечисленных поставщиком. на идентификатор канала указывает ссылка в одном или нескольких определениях событий.</span><span class="sxs-lookup"><span data-stu-id="04859-125">Set the **chid** attribute to a value that is unique for the channels that your provider lists; the channel identifier is referenced in one or more of your event definitions.</span></span> <span data-ttu-id="04859-126">Соглашение об именовании канала заключается в использовании имени поставщика и типа канала в форме, *providerName* / *чаннелтипе*.</span><span class="sxs-lookup"><span data-stu-id="04859-126">The convention for naming the channel is to use the provider name and channel type in the form, *providername*/*channeltype*.</span></span>

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
