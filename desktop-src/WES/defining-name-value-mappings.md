---
title: Определение сопоставлений имен и значений
description: Поставщик может определить список пар "имя-значение", которые потребители используют для отображения целочисленных значений в строках.
ms.assetid: d16b2410-a0de-42da-8f2a-98341c90ed87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62020adeb46bac96cada70cf5830e17213d69868
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104412733"
---
# <a name="defining-namevalue-mappings"></a><span data-ttu-id="cbd60-103">Определение сопоставлений имен и значений</span><span class="sxs-lookup"><span data-stu-id="cbd60-103">Defining Name/Value Mappings</span></span>

<span data-ttu-id="cbd60-104">Поставщик может определить список пар "имя-значение", которые потребители используют для отображения целочисленных значений в строках.</span><span class="sxs-lookup"><span data-stu-id="cbd60-104">A provider can define a list of name/value pairs that consumers use to map integer values to strings.</span></span> <span data-ttu-id="cbd60-105">Пары "имя-значение" могут сопоставлять целочисленные значения со строками или битовыми значениями битовых значений строкам. Каждое значение соответствует строковому значению.</span><span class="sxs-lookup"><span data-stu-id="cbd60-105">The name/value pairs can map integer values to strings or bit values bit values to strings; each value corresponds to a string value.</span></span> <span data-ttu-id="cbd60-106">Используйте сопоставления для целочисленных элементов данных, содержащих значения перечисления.</span><span class="sxs-lookup"><span data-stu-id="cbd60-106">Use mappings on integer data items that contain enumeration values.</span></span>

<span data-ttu-id="cbd60-107">Потребители могут использовать карту значений для получения строки, связанной со значением, и отображения ее вместо целочисленного или битового значения.</span><span class="sxs-lookup"><span data-stu-id="cbd60-107">Consumers can use the value map to retrieve the string associated with a value and display it instead of displaying the integer or bit value.</span></span> <span data-ttu-id="cbd60-108">Чтобы определить карту целочисленного значения, используйте элементы **valueMap** и **Map** .</span><span class="sxs-lookup"><span data-stu-id="cbd60-108">To define an integer value map, use the **valueMap** and **map** elements.</span></span> <span data-ttu-id="cbd60-109">Чтобы определить карту битового значения, используйте элементы **Bitmap** и **Map** .</span><span class="sxs-lookup"><span data-stu-id="cbd60-109">To define a bit value map, use the **bitmap** and **map** elements.</span></span>

<span data-ttu-id="cbd60-110">В следующем примере показано, как определить карту значений и точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="cbd60-110">The following example shows how to define a value map and a bitmap.</span></span> <span data-ttu-id="cbd60-111">Необходимо указать атрибут **имени** Map.</span><span class="sxs-lookup"><span data-stu-id="cbd60-111">You must specify the map's **name** attribute.</span></span> <span data-ttu-id="cbd60-112">Для каждой пары "имя-значение" необходимо указать атрибут **value** и **Message** .</span><span class="sxs-lookup"><span data-stu-id="cbd60-112">For each name/value pair, you must specify the **value** and **message** attribute.</span></span>


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

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
