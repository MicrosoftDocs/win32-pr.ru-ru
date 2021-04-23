---
title: Определение ключевых слов, используемых для классификации типов событий
description: Поставщики используют ключевые слова для классификации различных типов событий.
ms.assetid: 1cbad719-bc59-4255-8a15-9e45f363d199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48992c5cbafec5f945fa2f133924ccf0e2e7e96
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "103890327"
---
# <a name="defining-keywords-used-to-classify-types-of-events"></a><span data-ttu-id="114b1-103">Определение ключевых слов, используемых для классификации типов событий</span><span class="sxs-lookup"><span data-stu-id="114b1-103">Defining Keywords Used to Classify Types of Events</span></span>

<span data-ttu-id="114b1-104">Поставщики используют ключевые слова для классификации различных типов событий.</span><span class="sxs-lookup"><span data-stu-id="114b1-104">Providers use keywords to classify different types of events.</span></span> <span data-ttu-id="114b1-105">Например, можно создать ключевое слово для всех событий Read, а затем применить ключевое слово Read к любому событию, которое выполняет операцию чтения, например чтение из файла или реестра.</span><span class="sxs-lookup"><span data-stu-id="114b1-105">For example, you can create a keyword for all read events and then apply the read keyword to any event that performs a read operation such as reading from a file or registry.</span></span> <span data-ttu-id="114b1-106">Затем потребители могут использовать значения битового слова для фильтрации по разным классификациям событий.</span><span class="sxs-lookup"><span data-stu-id="114b1-106">Consumers could then use the keyword bit values to filter for different classification of events.</span></span> <span data-ttu-id="114b1-107">Например, потребитель может запросить все события чтения или все события чтения из задачи X (если также группировать события по задаче).</span><span class="sxs-lookup"><span data-stu-id="114b1-107">For example, the consumer could request all read events or all read events from task X (if you also group events by task).</span></span> <span data-ttu-id="114b1-108">Чтобы определить ключевое слово, используйте элемент **keyword** .</span><span class="sxs-lookup"><span data-stu-id="114b1-108">To define a keyword, use the **keyword** element.</span></span>

<span data-ttu-id="114b1-109">Сеанс трассировки ETW может использовать ключевые слова (так же, как и уровень) для ограничения событий, записываемых службой ETW в свой файл журнала трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="114b1-109">An ETW tracing session can use the keywords (in the same way that it uses level) to limit the events that the ETW service writes to its event tracing log file.</span></span> <span data-ttu-id="114b1-110">Сеанс трассировки может включить поставщик, используя два набора битовых масок ключевых слов: битовая маска "любая", в которой событие записывается, если любое из битов ключевых слов события соответствует любому из битов, заданных в этой маске, и битовой маске "все", где для этих событий, соответствующих варианту "Any", событие записывается, только если в битовой маске ключевого слова события есть все биты в маске "все".</span><span class="sxs-lookup"><span data-stu-id="114b1-110">A tracing session can enable the provider using two sets of keyword bitmasks: an "Any" bitmask where the event is written if any of the event's keyword bits match any of the bits set in this mask, and an "All" bitmask where for those events that matched the "Any" case, the event is written only if all of the bits in the "All" mask exist in the event's keyword bitmask.</span></span>

<span data-ttu-id="114b1-111">Например, если поставщик определяет событие, указывающее ключевое слово Read (бит 0) и ключевое слово локального доступа (бит 1), а второе событие, задающее ключевое слово Read (бит 0) и ключевое слово для удаленного доступа (бит 2), можно присвоить битовой маске ANY значение 1, чтобы получать все события чтения, или задать для битовой маски ANY значение 1, а для битовой маски «все» — значения 3, чтобы получать только локальные операции чтения.</span><span class="sxs-lookup"><span data-stu-id="114b1-111">For example, if the provider defines an event that specifies a read keyword (bit 0) and a local access keyword (bit 1), and a second event that specifies a read keyword (bit 0) and a remote access keyword (bit 2), you could set the "Any" bitmask to 1 to receive all read events, or you could set the "Any" bitmask to 1 and "All" bitmask to 3 to receive only local reads.</span></span>

<span data-ttu-id="114b1-112">Необходимо указать атрибуты **имени** и **маски** ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="114b1-112">You must specify the keyword's **name** and **mask** attributes.</span></span> <span data-ttu-id="114b1-113">Маска должна задавать только один бит, между битом 0 и битом 47.</span><span class="sxs-lookup"><span data-stu-id="114b1-113">The mask must set only one bit, between bit 0 and bit 47.</span></span> <span data-ttu-id="114b1-114">Биты с 48 по 64 зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="114b1-114">Bits 48 through 64 are reserved.</span></span>

<span data-ttu-id="114b1-115">Атрибуты **symbol** и **Message** являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="114b1-115">The **symbol** and **message** attributes are optional.</span></span>

<span data-ttu-id="114b1-116">В следующем примере показано, как определить ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="114b1-116">The following example shows how to define a keyword.</span></span>

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

                <keywords>
                    <keyword name="Read" mask="0x1" symbol="READ_KEYWORD"/>
                    <keyword name="Write" mask="0x2" symbol="WRITE_KEYWORD"/>
                    <keyword name="Local" mask="0x4" symbol="LOCAL_KEYWORD"/>
                    <keyword name="Remote" mask="0x8" symbol="REMOTE_KEYWORD"/>
                </keywords>

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
