---
title: Инструментатионманифест, элемент
description: Корневой узел манифеста.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- Журнал событий элемента Инструментатионманифест
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273351"
---
# <a name="instrumentationmanifest-element"></a><span data-ttu-id="4a767-104">Инструментатионманифест, элемент</span><span class="sxs-lookup"><span data-stu-id="4a767-104">instrumentationManifest Element</span></span>

<span data-ttu-id="4a767-105">Корневой узел манифеста.</span><span class="sxs-lookup"><span data-stu-id="4a767-105">The root node of the manifest.</span></span>

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="4a767-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4a767-106">Child elements</span></span>



| <span data-ttu-id="4a767-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="4a767-107">Element</span></span>                                                                                        | <span data-ttu-id="4a767-108">Тип</span><span class="sxs-lookup"><span data-stu-id="4a767-108">Type</span></span>                                                                               | <span data-ttu-id="4a767-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4a767-109">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a767-110">**инструментирования**</span><span class="sxs-lookup"><span data-stu-id="4a767-110">**instrumentation**</span></span>](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [<span data-ttu-id="4a767-111">**инструментатионтипе**</span><span class="sxs-lookup"><span data-stu-id="4a767-111">**InstrumentationType**</span></span>](eventmanifestschema-instrumentationtype-complextype.md) | <span data-ttu-id="4a767-112">В этом разделе определяется один или несколько поставщиков событий и событий, которые они регистрируют.</span><span class="sxs-lookup"><span data-stu-id="4a767-112">This section defines one or more event providers and the events that they log.</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="4a767-113">**локализации**</span><span class="sxs-lookup"><span data-stu-id="4a767-113">**localization**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [<span data-ttu-id="4a767-114">**локализатионтипе**</span><span class="sxs-lookup"><span data-stu-id="4a767-114">**LocalizationType**</span></span>](eventmanifestschema-localizationtype-complextype.md)       | <span data-ttu-id="4a767-115">В этом разделе определяются строки локализованных сообщений, используемые потребителями для вывода.</span><span class="sxs-lookup"><span data-stu-id="4a767-115">This section defines the localized message strings that consumers use for display.</span></span> <span data-ttu-id="4a767-116">Например, в этом разделе будет содержаться локализованная строка сообщения для имени поставщика, заданных Вами событий и всех определенных атрибутов событий, таких как каналы, задачи и коды операций.</span><span class="sxs-lookup"><span data-stu-id="4a767-116">For example, this section would contain the localized message string for the name of your provider, the events that you define, and any event attributes that you define, such as channels, tasks, and opcodes.</span></span><br/> |
| [<span data-ttu-id="4a767-117">**метаданных**</span><span class="sxs-lookup"><span data-stu-id="4a767-117">**metadata**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [<span data-ttu-id="4a767-118">**метадататипе**</span><span class="sxs-lookup"><span data-stu-id="4a767-118">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)               | <span data-ttu-id="4a767-119">В этом разделе определяются типы метаданных, которые могут использоваться другими манифестами.</span><span class="sxs-lookup"><span data-stu-id="4a767-119">This section defines metadata types that other manifests can use.</span></span> <span data-ttu-id="4a767-120">Пример см. в файле Winmeta.xml, включенном в \\ папку Include Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4a767-120">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="4a767-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a767-121">Remarks</span></span>

<span data-ttu-id="4a767-122">Элемент **инструментатионманифест** должен содержать следующие пространства имен:</span><span class="sxs-lookup"><span data-stu-id="4a767-122">The **instrumentationManifest** element must contain the following namespaces:</span></span>

<dl> <span data-ttu-id="4a767-123">xmlns = " https://schemas.microsoft.com/win/2004/08/events "</span><span class="sxs-lookup"><span data-stu-id="4a767-123">xmlns="https://schemas.microsoft.com/win/2004/08/events"</span></span>  
<span data-ttu-id="4a767-124">xmlns: Win = " https://manifests.microsoft.com/win/2004/08/windows/events "</span><span class="sxs-lookup"><span data-stu-id="4a767-124">xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"</span></span>  
<span data-ttu-id="4a767-125">xmlns: XS = " https://www.w3.org/2001/XMLSchema "</span><span class="sxs-lookup"><span data-stu-id="4a767-125">xmlns:xs="https://www.w3.org/2001/XMLSchema"</span></span>  
</dl>

<span data-ttu-id="4a767-126">Манифест должен содержать раздел инструментирования и раздел локализации.</span><span class="sxs-lookup"><span data-stu-id="4a767-126">A manifest must contain an instrumentation section and a localization section.</span></span> <span data-ttu-id="4a767-127">Раздел "инструментирование" и раздел метаданных являются взаимоисключающими (нельзя определить оба одновременно в одном манифесте).</span><span class="sxs-lookup"><span data-stu-id="4a767-127">The instrumentation section and metadata section are mutually exclusive (you cannot define both in the same manifest).</span></span> <span data-ttu-id="4a767-128">Несмотря на то, что можно создать манифест, содержащий раздел метаданных, служба не будет использовать ее. единственными метаданными, распознаваемыми службой, являются метаданные, найденные в файле Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="4a767-128">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="examples"></a><span data-ttu-id="4a767-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="4a767-129">Examples</span></span>

<span data-ttu-id="4a767-130">В следующем примере показана скелет полностью определенного манифеста инструментирования.</span><span class="sxs-lookup"><span data-stu-id="4a767-130">The following example shows the skeleton of a fully defined instrumentation manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a><span data-ttu-id="4a767-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4a767-131">Requirements</span></span>



| <span data-ttu-id="4a767-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4a767-132">Requirement</span></span> | <span data-ttu-id="4a767-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4a767-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4a767-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a767-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4a767-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a767-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4a767-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a767-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4a767-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a767-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





