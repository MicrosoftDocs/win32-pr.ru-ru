---
title: Определение поставщика
description: Манифест может обозначать одного или нескольких поставщиков. Для обнаружения поставщика используйте элемент provider.
ms.assetid: 3bd40405-2b7a-4709-aef7-8615de8c5b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45941a540f8804beccc408435fc202593ddad601
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104533059"
---
# <a name="identifying-the-provider"></a><span data-ttu-id="ef89b-104">Определение поставщика</span><span class="sxs-lookup"><span data-stu-id="ef89b-104">Identifying the Provider</span></span>

<span data-ttu-id="ef89b-105">Манифест может обозначать одного или нескольких поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ef89b-105">A manifest can identify one or more providers.</span></span> <span data-ttu-id="ef89b-106">Для обнаружения поставщика используйте элемент **provider** .</span><span class="sxs-lookup"><span data-stu-id="ef89b-106">To identify a provider, use the **provider** element.</span></span> <span data-ttu-id="ef89b-107">Необходимо указать атрибуты **Name**, **GUID**, **ресаурцефиленаме**, **мессажефиленаме** и **symbol** .</span><span class="sxs-lookup"><span data-stu-id="ef89b-107">You must specify the **name**, **guid**, **resourceFileName**, **messageFileName**, and **symbol** attributes.</span></span> <span data-ttu-id="ef89b-108">При локализации манифеста также следует указать атрибут **Message** , который потребители используют в качестве отображаемого имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="ef89b-108">If you localize your manifest, you should also specify the **message** attribute, which consumers use as the display the name of the provider.</span></span> <span data-ttu-id="ef89b-109">Если атрибут **Message** не указан, потребители используют значение атрибута **Name** .</span><span class="sxs-lookup"><span data-stu-id="ef89b-109">If you do not specify the **message** attribute, consumers use the value of the **name** attribute.</span></span>

<span data-ttu-id="ef89b-110">В манифесте можно найти до 16 поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ef89b-110">You can identify up to 16 providers in the manifest.</span></span> <span data-ttu-id="ef89b-111">Если требуется определить более 16 поставщиков, необходимо включить раздел **мессажетабле** манифеста, который должен использоваться поставщиками семнадцатого и в для назначения значений ресурсов для определяемых им строк сообщений. Таблица сообщений не должна содержать строки сообщений, для которых определены поставщики от 1 до 16.</span><span class="sxs-lookup"><span data-stu-id="ef89b-111">If you want to identify more than 16 providers, you must include the **messageTable** section of the manifest that the seventeenth and on providers must use to assign resource values for the message strings that they define—the message table must not include any message strings that providers 1 through 16 defined.</span></span>

<span data-ttu-id="ef89b-112">В следующем примере показано, как использовать элемент **provider** для указания поставщика.</span><span class="sxs-lookup"><span data-stu-id="ef89b-112">The following example shows how to use the **provider** element to identify a provider.</span></span>


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
