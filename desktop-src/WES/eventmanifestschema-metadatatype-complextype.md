---
title: Сложный тип Метадататипе
description: Определяет типы метаданных, которые можно определить в разделе метаданных манифеста.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- Журнал событий сложных типов Метадататипе
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071981"
---
# <a name="metadatatype-complex-type"></a><span data-ttu-id="fa545-104">Сложный тип Метадататипе</span><span class="sxs-lookup"><span data-stu-id="fa545-104">MetadataType Complex Type</span></span>

<span data-ttu-id="fa545-105">Определяет типы метаданных, которые можно определить в разделе метаданных манифеста.</span><span class="sxs-lookup"><span data-stu-id="fa545-105">Defines the metadata types that you can define in the metadata section of the manifest.</span></span>

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="fa545-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fa545-106">Child elements</span></span>



| <span data-ttu-id="fa545-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="fa545-107">Element</span></span>                                                                       | <span data-ttu-id="fa545-108">Тип</span><span class="sxs-lookup"><span data-stu-id="fa545-108">Type</span></span>                                                                       | <span data-ttu-id="fa545-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fa545-109">Description</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa545-110">**канала**</span><span class="sxs-lookup"><span data-stu-id="fa545-110">**channels**</span></span>](eventmanifestschema-channels-metadatatype-element.md)         | [<span data-ttu-id="fa545-111">**чаннеллисттипе**</span><span class="sxs-lookup"><span data-stu-id="fa545-111">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md) | <span data-ttu-id="fa545-112">Определяет список каналов, к которым поставщики могут регистрировать события.</span><span class="sxs-lookup"><span data-stu-id="fa545-112">Defines a list of channels to which providers can log events.</span></span> <span data-ttu-id="fa545-113">Затем поставщик может импортировать один или несколько каналов в своем манифесте.</span><span class="sxs-lookup"><span data-stu-id="fa545-113">A provider can then import one or more of the channels in their manifest.</span></span><br/>               |
| [<span data-ttu-id="fa545-114">**словами**</span><span class="sxs-lookup"><span data-stu-id="fa545-114">**keywords**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)         | [<span data-ttu-id="fa545-115">**кэйвордлисттипе**</span><span class="sxs-lookup"><span data-stu-id="fa545-115">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md) | <span data-ttu-id="fa545-116">Определяет список ключевых слов, которые определяют категорию событий, записываемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="fa545-116">Defines a list of keywords that determine the category of events that the provider writes.</span></span><br/>                                                            |
| [<span data-ttu-id="fa545-117">**Выравнивание**</span><span class="sxs-lookup"><span data-stu-id="fa545-117">**levels**</span></span>](eventmanifestschema-levels-metadatatype-element.md)             | [<span data-ttu-id="fa545-118">**левеллисттипе**</span><span class="sxs-lookup"><span data-stu-id="fa545-118">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)     | <span data-ttu-id="fa545-119">Определяет список уровней, указывающих серьезность события.</span><span class="sxs-lookup"><span data-stu-id="fa545-119">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                       |
| <span data-ttu-id="fa545-120">**message**</span><span class="sxs-lookup"><span data-stu-id="fa545-120">**message**</span></span>                                                                   |                                                                            | <span data-ttu-id="fa545-121">Определяет строку сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa545-121">Defines a message string.</span></span><br/>                                                                                                                             |
| <span data-ttu-id="fa545-122">**мессажетабле**</span><span class="sxs-lookup"><span data-stu-id="fa545-122">**messageTable**</span></span>                                                              |                                                                            | <span data-ttu-id="fa545-123">Определяет список строк сообщений.</span><span class="sxs-lookup"><span data-stu-id="fa545-123">Defines a list of message strings.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="fa545-124">**намедкуериес**</span><span class="sxs-lookup"><span data-stu-id="fa545-124">**namedQueries**</span></span>](eventmanifestschema-namedqueries-metadatatype-element.md) | [<span data-ttu-id="fa545-125">**намедкуеритипе**</span><span class="sxs-lookup"><span data-stu-id="fa545-125">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)   | <span data-ttu-id="fa545-126">Определяет список именованных запросов, использующих регулярные выражения для выполнения операций поиска и замены в строке сообщения события.</span><span class="sxs-lookup"><span data-stu-id="fa545-126">Defines a list of named queries that use regular expressions to perform find and replace actions on an event's message string.</span></span><br/>                        |
| [<span data-ttu-id="fa545-127">**коды операций**</span><span class="sxs-lookup"><span data-stu-id="fa545-127">**opcodes**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)           | [<span data-ttu-id="fa545-128">**опкоделисттипе**</span><span class="sxs-lookup"><span data-stu-id="fa545-128">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)   | <span data-ttu-id="fa545-129">Определяет список кодов операций, которые можно использовать для группирования событий в задаче.</span><span class="sxs-lookup"><span data-stu-id="fa545-129">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                             |
| <span data-ttu-id="fa545-130">**операции**</span><span class="sxs-lookup"><span data-stu-id="fa545-130">**tasks**</span></span>                                                                     | [<span data-ttu-id="fa545-131">**тасклисттипе**</span><span class="sxs-lookup"><span data-stu-id="fa545-131">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)       | <span data-ttu-id="fa545-132">Определяет список задач, которые поставщик может использовать для группирования событий.</span><span class="sxs-lookup"><span data-stu-id="fa545-132">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="fa545-133">Как правило, задачи используются для группирования событий для компонента или компонента поставщика.</span><span class="sxs-lookup"><span data-stu-id="fa545-133">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/> |
| [<span data-ttu-id="fa545-134">**типов**</span><span class="sxs-lookup"><span data-stu-id="fa545-134">**types**</span></span>](eventmanifestschema-types-metadatatype-element.md)               | [<span data-ttu-id="fa545-135">**типелисттипе**</span><span class="sxs-lookup"><span data-stu-id="fa545-135">**TypeListType**</span></span>](eventmanifestschema-typelisttype-complextype.md)       | <span data-ttu-id="fa545-136">Определяет список типов XML.</span><span class="sxs-lookup"><span data-stu-id="fa545-136">Defines a list of XML types.</span></span><br/>                                                                                                                          |



## <a name="attributes"></a><span data-ttu-id="fa545-137">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fa545-137">Attributes</span></span>



| <span data-ttu-id="fa545-138">Имя</span><span class="sxs-lookup"><span data-stu-id="fa545-138">Name</span></span>    | <span data-ttu-id="fa545-139">Тип</span><span class="sxs-lookup"><span data-stu-id="fa545-139">Type</span></span>                                                              | <span data-ttu-id="fa545-140">Описание</span><span class="sxs-lookup"><span data-stu-id="fa545-140">Description</span></span>                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa545-141">message</span><span class="sxs-lookup"><span data-stu-id="fa545-141">message</span></span> | [<span data-ttu-id="fa545-142">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="fa545-142">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="fa545-143">Ссылка на локализованную строку в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="fa545-143">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="fa545-144">mid</span><span class="sxs-lookup"><span data-stu-id="fa545-144">mid</span></span>     | <span data-ttu-id="fa545-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa545-145">xs:string</span></span>                                                         | <span data-ttu-id="fa545-146">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fa545-146">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="fa545-147">name</span><span class="sxs-lookup"><span data-stu-id="fa545-147">name</span></span>    | <span data-ttu-id="fa545-148">anyURI</span><span class="sxs-lookup"><span data-stu-id="fa545-148">anyURI</span></span>                                                            | <span data-ttu-id="fa545-149">URI мета файла.</span><span class="sxs-lookup"><span data-stu-id="fa545-149">The URI of the meta file.</span></span> <br/>                                                              |
| <span data-ttu-id="fa545-150">символ</span><span class="sxs-lookup"><span data-stu-id="fa545-150">symbol</span></span>  | [<span data-ttu-id="fa545-151">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="fa545-151">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="fa545-152">Символьное имя, создаваемое компилятором сообщений для этой строки сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa545-152">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="fa545-153">значение</span><span class="sxs-lookup"><span data-stu-id="fa545-153">value</span></span>   | [<span data-ttu-id="fa545-154">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="fa545-154">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="fa545-155">Число, используемое в качестве идентификатора сообщения для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa545-155">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="remarks"></a><span data-ttu-id="fa545-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa545-156">Remarks</span></span>

<span data-ttu-id="fa545-157">Несмотря на то, что можно создать манифест, содержащий раздел метаданных, служба не будет использовать ее. единственными метаданными, распознаваемыми службой, являются метаданные, найденные в файле Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="fa545-157">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa545-158">Требования</span><span class="sxs-lookup"><span data-stu-id="fa545-158">Requirements</span></span>



| <span data-ttu-id="fa545-159">Требование</span><span class="sxs-lookup"><span data-stu-id="fa545-159">Requirement</span></span> | <span data-ttu-id="fa545-160">Значение</span><span class="sxs-lookup"><span data-stu-id="fa545-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa545-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa545-161">Minimum supported client</span></span><br/> | <span data-ttu-id="fa545-162">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa545-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa545-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa545-163">Minimum supported server</span></span><br/> | <span data-ttu-id="fa545-164">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa545-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





