---
description: Поставщики на основе манифеста используют манифест для публикации схемы для своих событий.
ms.assetid: 37d1a504-ecc7-4df3-bf31-546debb62123
title: Публикация схемы событий для поставщика на основе манифеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c100dd041d5bd454d8ec64d40fcc9a953d8fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991215"
---
# <a name="publishing-your-event-schema-for-a-manifest-based-provider"></a>Публикация схемы событий для поставщика на основе манифеста

Поставщики [на основе манифеста](about-event-tracing.md) используют манифест для публикации схемы для своих событий. Манифест внедряется в двоичный файл поставщика, что означает, что поставщик должен быть доступен на компьютере, чтобы потребитель использовал его события. Подробные сведения о создании манифеста см. в разделе [написание манифеста инструментирования](../wes/writing-an-instrumentation-manifest.md).

Следующий манифест определяет события, которые используются в примерах в разделе [предоставление событий](providing-events.md) и [Использование событий](consuming-events.md) в документе.

``` syntax
<!-- <?xml version="1.0" encoding="UTF-16"?> -->
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>

            <provider name="Microsoft-Windows-ETWProvider" 
                guid="{D8909C24-5BE9-4502-98CA-AB7BDC24899D}" 
                symbol="ProviderGuid" 
                resourceFileName="c:\code\etw\v2provider\debug\v2provider.exe" 
                messageFileName="c:\code\etw\v2provider\debug\v2provider.exe"
                message="$(string.Provider.Name)"
                >

                <keywords>
                    <keyword name="Read" symbol="READ_KEYWORD" mask="0x1" />
                    <keyword name="Write" symbol="WRITE_KEYWORD" mask="0x2" />
                    <keyword name="Local" symbol="LOCAL_KEYWORD" mask="0x4" />
                    <keyword name="Remote" symbol="REMOTE_KEYWORD" mask="0x8" />
                </keywords>

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.Map.Download)"/>
                        <map value="2" message="$(string.Map.Upload)"/>
                        <map value="3" message="$(string.Map.UploadReply)"/>
                    </valueMap>

                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.Map.Sunday)"/>
                        <map value="0x2" message="$(string.Map.Monday)"/>
                        <map value="0x4" message="$(string.Map.Tuesday)"/>
                        <map value="0x8" message="$(string.Map.Wednesday)"/>
                        <map value="0x10" message="$(string.Map.Thursday)"/>
                        <map value="0x20" message="$(string.Map.Friday)"/>
                        <map value="0x40" message="$(string.Map.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>

                   <template tid="TransferTemplate">
                        <data name="Image" inType="win:Pointer"/>
                        <data name="Scores" inType="win:UInt16" count="3"/>
                        <data name="ID" inType="win:GUID"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />

                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Name" inType="win:UnicodeString" />
                            <data name="Value" inType="win:UInt16" />
                        </struct>

                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>

                        <UserData>
                            <EventData xmlns="ProviderNamespace">
                                <Transfer> %10 </Transfer>
                                <Day> %9 </Day>
                                <ValuesCount> %7 </ValuesCount>
                                <Values> %8 </Values>
                                <Path> %6 </Path>
                                <IsLocal> %5 </IsLocal>
                                <Scores> %2 </Scores>
                                <Image> %1 </Image>
                                <Certificate> %4 </Certificate>
                                <ID> %3 </ID>
                            </EventData>
                        </UserData>
                    </template>

                </templates>

                <events>
                    <event value="1" 
                        level="win:Informational" 
                        template="TransferTemplate" 
                        symbol="TransferEvent"
                        message ="$(string.Event.WhenToTransfer)"
                        keywords="Read Local" />
                </events>


            </provider>

        </events>

    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>

                <string id="Provider.Name" value="Microsoft-Windows-ETWProvider"/>

                <string id="Map.Download" value="Download"/>
                <string id="Map.Upload" value="Upload"/>
                <string id="Map.UploadReply" value="Upload-reply"/> 

                <string id="Map.Sunday" value="Sunday"/>
                <string id="Map.Monday" value="Monday"/>
                <string id="Map.Tuesday" value="Tuesday"/>
                <string id="Map.Wednesday" value="Wednesday"/>
                <string id="Map.Thursday" value="Thursday"/>
                <string id="Map.Friday" value="Friday"/>
                <string id="Map.Saturday" value="Saturday"/>

                <string id="Event.WhenToTransfer" value="The %10 transfer will occur %9."/>

            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

 

 
