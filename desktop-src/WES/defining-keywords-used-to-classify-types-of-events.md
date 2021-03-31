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
# <a name="defining-keywords-used-to-classify-types-of-events"></a>Определение ключевых слов, используемых для классификации типов событий

Поставщики используют ключевые слова для классификации различных типов событий. Например, можно создать ключевое слово для всех событий Read, а затем применить ключевое слово Read к любому событию, которое выполняет операцию чтения, например чтение из файла или реестра. Затем потребители могут использовать значения битового слова для фильтрации по разным классификациям событий. Например, потребитель может запросить все события чтения или все события чтения из задачи X (если также группировать события по задаче). Чтобы определить ключевое слово, используйте элемент **keyword** .

Сеанс трассировки ETW может использовать ключевые слова (так же, как и уровень) для ограничения событий, записываемых службой ETW в свой файл журнала трассировки событий. Сеанс трассировки может включить поставщик, используя два набора битовых масок ключевых слов: битовая маска "любая", в которой событие записывается, если любое из битов ключевых слов события соответствует любому из битов, заданных в этой маске, и битовой маске "все", где для этих событий, соответствующих варианту "Any", событие записывается, только если в битовой маске ключевого слова события есть все биты в маске "все".

Например, если поставщик определяет событие, указывающее ключевое слово Read (бит 0) и ключевое слово локального доступа (бит 1), а второе событие, задающее ключевое слово Read (бит 0) и ключевое слово для удаленного доступа (бит 2), можно присвоить битовой маске ANY значение 1, чтобы получать все события чтения, или задать для битовой маски ANY значение 1, а для битовой маски «все» — значения 3, чтобы получать только локальные операции чтения.

Необходимо указать атрибуты **имени** и **маски** ключевого слова. Маска должна задавать только один бит, между битом 0 и битом 47. Биты с 48 по 64 зарезервированы.

Атрибуты **symbol** и **Message** являются необязательными.

В следующем примере показано, как определить ключевое слово.

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
