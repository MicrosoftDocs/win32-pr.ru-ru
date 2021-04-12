---
title: Сложный тип ProviderType
description: Определяет поставщик и метаданные, используемые для определения его событий. | Сложный тип ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Журнал событий сложного типа ProviderType
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353372"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="99351-105">Сложный тип ProviderType</span><span class="sxs-lookup"><span data-stu-id="99351-105">ProviderType Complex Type</span></span>

<span data-ttu-id="99351-106">Определяет поставщик и метаданные, используемые для определения его событий.</span><span class="sxs-lookup"><span data-stu-id="99351-106">Defines a provider and the metadata that it uses to define its events.</span></span>

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
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
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="99351-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="99351-107">Child elements</span></span>



| <span data-ttu-id="99351-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="99351-108">Element</span></span>                                                                       | <span data-ttu-id="99351-109">Тип</span><span class="sxs-lookup"><span data-stu-id="99351-109">Type</span></span>                                                                         | <span data-ttu-id="99351-110">Описание</span><span class="sxs-lookup"><span data-stu-id="99351-110">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99351-111">**канала**</span><span class="sxs-lookup"><span data-stu-id="99351-111">**channels**</span></span>](eventmanifestschema-channels-providertype-element.md)         | [<span data-ttu-id="99351-112">**чаннеллисттипе**</span><span class="sxs-lookup"><span data-stu-id="99351-112">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md)   | <span data-ttu-id="99351-113">Определяет список каналов, к которым поставщики могут регистрировать события.</span><span class="sxs-lookup"><span data-stu-id="99351-113">Defines a list of channels to which providers can log events.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="99351-114">**событиях**</span><span class="sxs-lookup"><span data-stu-id="99351-114">**events**</span></span>](eventmanifestschema-events-providertype-element.md)             | [<span data-ttu-id="99351-115">**дефинитионтипе**</span><span class="sxs-lookup"><span data-stu-id="99351-115">**DefinitionType**</span></span>](eventmanifestschema-definitiontype-complextype.md)     | <span data-ttu-id="99351-116">Определяет список определений событий событий, которые поставщик может заносить в журнал.</span><span class="sxs-lookup"><span data-stu-id="99351-116">Defines a list of event definitions of the events that the provider can log.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="99351-117">**фильтрующ**</span><span class="sxs-lookup"><span data-stu-id="99351-117">**filters**</span></span>                                                                   | [<span data-ttu-id="99351-118">**филтерлисттипе**</span><span class="sxs-lookup"><span data-stu-id="99351-118">**FilterListType**</span></span>](eventmanifestschema-filterlisttype-complextype.md)     | <span data-ttu-id="99351-119">Определяет список фильтров, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="99351-119">Defines a list of filters that your provider supports.</span></span> <span data-ttu-id="99351-120">Можно использовать фильтры, как и ключевые слова, чтобы определить, нужно ли создавать событие.</span><span class="sxs-lookup"><span data-stu-id="99351-120">You can use the filters, as you would level and keywords, to determine if you want to write an event.</span></span> <br/> <span data-ttu-id="99351-121">**Windows Server 2008 и Windows Vista:** Не поддерживается до Windows 7.</span><span class="sxs-lookup"><span data-stu-id="99351-121">**Windows Server 2008 and Windows Vista:** Not supported until Windows 7.</span></span><br/> |
| [<span data-ttu-id="99351-122">**словами**</span><span class="sxs-lookup"><span data-stu-id="99351-122">**keywords**</span></span>](eventmanifestschema-keywords-providertype-element.md)         | [<span data-ttu-id="99351-123">**кэйвордлисттипе**</span><span class="sxs-lookup"><span data-stu-id="99351-123">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md)   | <span data-ttu-id="99351-124">Определяет список ключевых слов, которые классифицируют события.</span><span class="sxs-lookup"><span data-stu-id="99351-124">Defines a list of keywords that categorize events.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="99351-125">**Выравнивание**</span><span class="sxs-lookup"><span data-stu-id="99351-125">**levels**</span></span>](eventmanifestschema-levels-providertype-element.md)             | [<span data-ttu-id="99351-126">**левеллисттипе**</span><span class="sxs-lookup"><span data-stu-id="99351-126">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)       | <span data-ttu-id="99351-127">Определяет список уровней, указывающих серьезность события.</span><span class="sxs-lookup"><span data-stu-id="99351-127">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="99351-128">**указания**</span><span class="sxs-lookup"><span data-stu-id="99351-128">**maps**</span></span>](eventmanifestschema-maps-providertype-element.md)                 | [<span data-ttu-id="99351-129">**MapType**</span><span class="sxs-lookup"><span data-stu-id="99351-129">**MapType**</span></span>](eventmanifestschema-maptype-complextype.md)                   | <span data-ttu-id="99351-130">Определяет список пар "имя-значение", на которые можно ссылаться в разделе шаблона манифеста.</span><span class="sxs-lookup"><span data-stu-id="99351-130">Defines a list of name/value pairs that you can reference in the template section of the manifest.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="99351-131">**намедкуериес**</span><span class="sxs-lookup"><span data-stu-id="99351-131">**namedQueries**</span></span>](eventmanifestschema-namedqueries-providertype-element.md) | [<span data-ttu-id="99351-132">**намедкуеритипе**</span><span class="sxs-lookup"><span data-stu-id="99351-132">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)     | <span data-ttu-id="99351-133">Не используется.</span><span class="sxs-lookup"><span data-stu-id="99351-133">Not used.</span></span> <span data-ttu-id="99351-134">Определяет список именованных запросов, которые запрашивают строку сообщения о событии для значения и выполняют указанное действие, если оно найдено.</span><span class="sxs-lookup"><span data-stu-id="99351-134">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="99351-135">**коды операций**</span><span class="sxs-lookup"><span data-stu-id="99351-135">**opcodes**</span></span>](eventmanifestschema-opcodes-providertype-element.md)           | [<span data-ttu-id="99351-136">**опкоделисттипе**</span><span class="sxs-lookup"><span data-stu-id="99351-136">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)     | <span data-ttu-id="99351-137">Определяет список кодов операций, которые можно использовать для группирования событий в задаче.</span><span class="sxs-lookup"><span data-stu-id="99351-137">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="99351-138">**операции**</span><span class="sxs-lookup"><span data-stu-id="99351-138">**tasks**</span></span>](eventmanifestschema-tasks-providertype-element.md)               | [<span data-ttu-id="99351-139">**тасклисттипе**</span><span class="sxs-lookup"><span data-stu-id="99351-139">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)         | <span data-ttu-id="99351-140">Определяет список задач, которые поставщик может использовать для группирования событий.</span><span class="sxs-lookup"><span data-stu-id="99351-140">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="99351-141">Как правило, задачи используются для группирования событий для компонента или компонента поставщика.</span><span class="sxs-lookup"><span data-stu-id="99351-141">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/>                                                                                              |
| [<span data-ttu-id="99351-142">**шаблоны**</span><span class="sxs-lookup"><span data-stu-id="99351-142">**templates**</span></span>](eventmanifestschema-templates-providertype-element.md)       | [<span data-ttu-id="99351-143">**темплателисттипе**</span><span class="sxs-lookup"><span data-stu-id="99351-143">**TemplateListType**</span></span>](eventmanifestschema-templatelisttype-complextype.md) | <span data-ttu-id="99351-144">Определяет список шаблонов, указывающих данные, включаемые в события.</span><span class="sxs-lookup"><span data-stu-id="99351-144">Defines a list of templates that specify the data to include with the events.</span></span><br/>                                                                                                                                                                      |



## <a name="attributes"></a><span data-ttu-id="99351-145">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="99351-145">Attributes</span></span>



| <span data-ttu-id="99351-146">Имя</span><span class="sxs-lookup"><span data-stu-id="99351-146">Name</span></span>                                | <span data-ttu-id="99351-147">Тип</span><span class="sxs-lookup"><span data-stu-id="99351-147">Type</span></span>                                                              | <span data-ttu-id="99351-148">Описание</span><span class="sxs-lookup"><span data-stu-id="99351-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99351-149">guid</span><span class="sxs-lookup"><span data-stu-id="99351-149">guid</span></span>                                | [<span data-ttu-id="99351-150">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="99351-150">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="99351-151">Идентификатор GUID, который однозначно идентифицирует поставщик.</span><span class="sxs-lookup"><span data-stu-id="99351-151">A GUID that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="99351-152">helpLink</span><span class="sxs-lookup"><span data-stu-id="99351-152">helpLink</span></span>                            | <span data-ttu-id="99351-153">anyURI</span><span class="sxs-lookup"><span data-stu-id="99351-153">anyURI</span></span>                                                            | <span data-ttu-id="99351-154">Ссылка на URL-адрес или MS Help на содержимое, содержащее сведения о событиях, которые вызывает поставщик.</span><span class="sxs-lookup"><span data-stu-id="99351-154">The URL or MS help link to content that provides information about the events that the provider raises.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="99351-155">message</span><span class="sxs-lookup"><span data-stu-id="99351-155">message</span></span>                             | [<span data-ttu-id="99351-156">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="99351-156">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="99351-157">Локализованное отображаемое имя для поставщика.</span><span class="sxs-lookup"><span data-stu-id="99351-157">The localized display name for the provider.</span></span> <span data-ttu-id="99351-158">Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.</span><span class="sxs-lookup"><span data-stu-id="99351-158">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="99351-159">мессажефиленаме</span><span class="sxs-lookup"><span data-stu-id="99351-159">messageFileName</span></span>                     | [<span data-ttu-id="99351-160">**Равно**</span><span class="sxs-lookup"><span data-stu-id="99351-160">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="99351-161">Полный путь к файлу, содержащему ресурсы локализованного сообщения поставщика.</span><span class="sxs-lookup"><span data-stu-id="99351-161">The full path to the file that contains the provider's localized message resources.</span></span> <span data-ttu-id="99351-162">Файл может быть исполняемым файлом или DLL-файлом.</span><span class="sxs-lookup"><span data-stu-id="99351-162">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="99351-163">name</span><span class="sxs-lookup"><span data-stu-id="99351-163">name</span></span>                                | <span data-ttu-id="99351-164">anyURI</span><span class="sxs-lookup"><span data-stu-id="99351-164">anyURI</span></span>                                                            | <span data-ttu-id="99351-165">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="99351-165">The name of the provider.</span></span> <span data-ttu-id="99351-166">Имя должно иметь форму,  -  - *компонент* продукта компании.</span><span class="sxs-lookup"><span data-stu-id="99351-166">The name should be of the form, *Company*-*Product*-*Component*.</span></span><br/> <span data-ttu-id="99351-167">Имя не может быть длиннее 255 символов и не может содержать символы: ">", "<", "&", "" "," "," \| \\ ",": "," ","? "," \* "или символы с кодами меньше 31.</span><span class="sxs-lookup"><span data-stu-id="99351-167">The name cannot be longer than 255 characters, and cannot contain the characters: '>', '<', '&', '"', '\|', '\\', ':', '', '?', '\*', or characters with codes less than 31.</span></span> <span data-ttu-id="99351-168">Кроме того, имя должно соответствовать общим ограничениям на имена файлов и разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="99351-168">In addition, the name must follow the general constraints on file and registry key names.</span></span> <span data-ttu-id="99351-169">Эти ограничения можно найти по [имени файла](/windows/desktop/FileIO/naming-a-file)и [ограничению размера элементов реестра](/windows/desktop/SysInfo/registry-element-size-limits).</span><span class="sxs-lookup"><span data-stu-id="99351-169">These constraints can be found at [Naming a File](/windows/desktop/FileIO/naming-a-file), and [Registry Element Size Limits](/windows/desktop/SysInfo/registry-element-size-limits).</span></span><br/> |
| <span data-ttu-id="99351-170">параметерфиленаме</span><span class="sxs-lookup"><span data-stu-id="99351-170">parameterFileName</span></span>                   | [<span data-ttu-id="99351-171">**Равно**</span><span class="sxs-lookup"><span data-stu-id="99351-171">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="99351-172">Полный путь к файлу, содержащему строковые ресурсы параметра поставщика.</span><span class="sxs-lookup"><span data-stu-id="99351-172">The full path to the file that contain the provider's parameter string resources.</span></span> <span data-ttu-id="99351-173">Файл может быть исполняемым файлом или DLL-файлом.</span><span class="sxs-lookup"><span data-stu-id="99351-173">The file can be an executable file or DLL file.</span></span> <span data-ttu-id="99351-174">Можно указать более одного файла параметров, разделяя их точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="99351-174">You can specify more than one parameter file separated by a semicolon.</span></span> <span data-ttu-id="99351-175">Файл ищется, если строка сообщения события содержит строку параметра.</span><span class="sxs-lookup"><span data-stu-id="99351-175">The file is searched when an event's message string contains a parameter string.</span></span> <span data-ttu-id="99351-176">Параметры позволяют предоставлять локализуемые строки вставки.</span><span class="sxs-lookup"><span data-stu-id="99351-176">Parameters let you provide localizable insert strings.</span></span> <span data-ttu-id="99351-177">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="99351-177">See Remarks for more information.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="99351-178">ресаурцефиленаме</span><span class="sxs-lookup"><span data-stu-id="99351-178">resourceFileName</span></span>                    | [<span data-ttu-id="99351-179">**Равно**</span><span class="sxs-lookup"><span data-stu-id="99351-179">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="99351-180">Полный путь к файлу, содержащему ресурсы метаданных поставщика.</span><span class="sxs-lookup"><span data-stu-id="99351-180">The full path to the file that contains the provider's metadata resources.</span></span> <span data-ttu-id="99351-181">Файл может быть исполняемым файлом или DLL-файлом.</span><span class="sxs-lookup"><span data-stu-id="99351-181">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="99351-182">source</span><span class="sxs-lookup"><span data-stu-id="99351-182">source</span></span>                              |                                                                   | <span data-ttu-id="99351-183">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="99351-183">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="99351-184">символ</span><span class="sxs-lookup"><span data-stu-id="99351-184">symbol</span></span>                              | [<span data-ttu-id="99351-185">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="99351-185">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="99351-186">Символ, используемый для ссылки на идентификатор GUID поставщика в приложении.</span><span class="sxs-lookup"><span data-stu-id="99351-186">The symbol to use to reference the provider's GUID in your application.</span></span> <span data-ttu-id="99351-187">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для идентификатора GUID поставщика в файле заголовка, создаваемом компилятором.</span><span class="sxs-lookup"><span data-stu-id="99351-187">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the provider's GUID in the header file that the compiler generates.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="99351-188">варнонаппликатионкомпатибилитеррор</span><span class="sxs-lookup"><span data-stu-id="99351-188">warnOnApplicationCompatibilityError</span></span> | <span data-ttu-id="99351-189">**xs:boolean**</span><span class="sxs-lookup"><span data-stu-id="99351-189">**xs:boolean**</span></span>                                                    | <span data-ttu-id="99351-190">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="99351-190">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="99351-191">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99351-191">Remarks</span></span>

<span data-ttu-id="99351-192">Просмотр событий Windows (Eventvwr.exe) будет использовать локализованную строку сообщения, если она доступна; в противном случае используется строка из атрибута Name.</span><span class="sxs-lookup"><span data-stu-id="99351-192">The Windows Event Viewer (Eventvwr.exe) will use the localized message string if available; otherwise, it uses the string from the name attribute.</span></span>

<span data-ttu-id="99351-193">Пути для Ресаурцефиленаме, Мессажефиленаме и Параметерфиленаме могут содержать переменные среды.</span><span class="sxs-lookup"><span data-stu-id="99351-193">The paths for resourceFileName, messageFileName, and parameterFileName can contain environment variables.</span></span> <span data-ttu-id="99351-194">Если вы определили новую переменную среды для использования в пути, необходимо перезагрузить компьютер, чтобы служба журнала событий могла выбрать новую переменную. в противном случае служба не сможет найти ресурсы поставщика.</span><span class="sxs-lookup"><span data-stu-id="99351-194">If you define a new environment variable to use in the path, you must restart the computer so that the event log service can pick up the new variable; otherwise, the service will not be able to find your provider's resources.</span></span>

<span data-ttu-id="99351-195">Строка сообщения события может содержать строки вставки и строки параметров.</span><span class="sxs-lookup"><span data-stu-id="99351-195">An event's message string can contain insertion strings and parameter strings.</span></span> <span data-ttu-id="99351-196">Строка вставки имеет форму%*n*, где *n* — это Отсчитываемый от единицы индекс, определяющий элемент данных из шаблона данных события, который необходимо вставить в сообщение.</span><span class="sxs-lookup"><span data-stu-id="99351-196">An insertion string is of the form %*n*, where *n* is a one-based index that identifies a data item from the event's data template that you want to insert into the message.</span></span> <span data-ttu-id="99351-197">Строка параметра (см. атрибут **параметерфиленаме** ) имеет вид%%*n*, где n — это идентификатор сообщения в таблице сообщений.</span><span class="sxs-lookup"><span data-stu-id="99351-197">A parameter string (see the **parameterFileName** attribute) is of the form %%*n*, where n is the identifier of a message in the message table.</span></span> <span data-ttu-id="99351-198">Если строка сообщения события содержит "%1% %11 = %2% %12", а значения элементов данных для %1 и %2 — 8 и 2, соответственно, а строки параметров для% %11 и %12 были "кварты" и "галлоны" соответственно, отформатированная строка будет иметь значение "8 кварт = 2 галлоны".</span><span class="sxs-lookup"><span data-stu-id="99351-198">If the event's message string contained "%1 %%11 = %2 %%12" and the data item values for %1 and %2 were 8 and 2, respectively, and the parameter strings for %%11 and %%12 were "quarts" and "gallons", respectively, the formatted string would be "8 quarts = 2 gallons".</span></span>

## <a name="requirements"></a><span data-ttu-id="99351-199">Требования</span><span class="sxs-lookup"><span data-stu-id="99351-199">Requirements</span></span>



| <span data-ttu-id="99351-200">Требование</span><span class="sxs-lookup"><span data-stu-id="99351-200">Requirement</span></span> | <span data-ttu-id="99351-201">Значение</span><span class="sxs-lookup"><span data-stu-id="99351-201">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99351-202">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99351-202">Minimum supported client</span></span><br/> | <span data-ttu-id="99351-203">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99351-203">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99351-204">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99351-204">Minimum supported server</span></span><br/> | <span data-ttu-id="99351-205">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99351-205">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

