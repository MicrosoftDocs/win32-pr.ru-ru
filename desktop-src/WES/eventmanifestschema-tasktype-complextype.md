---
title: Сложный тип TaskType
description: Определяет компонент или подкомпонент приложения. | Сложный тип TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- Журнал событий сложных типов TaskType
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694067"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="19c55-105">Сложный тип TaskType</span><span class="sxs-lookup"><span data-stu-id="19c55-105">TaskType Complex Type</span></span>

<span data-ttu-id="19c55-106">Определяет компонент или подкомпонент приложения.</span><span class="sxs-lookup"><span data-stu-id="19c55-106">Defines a component or subcomponent of an application.</span></span>

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="19c55-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="19c55-107">Child elements</span></span>



| <span data-ttu-id="19c55-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="19c55-108">Element</span></span>                                                         | <span data-ttu-id="19c55-109">Тип</span><span class="sxs-lookup"><span data-stu-id="19c55-109">Type</span></span>                                                                     | <span data-ttu-id="19c55-110">Описание</span><span class="sxs-lookup"><span data-stu-id="19c55-110">Description</span></span>                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19c55-111">**коды операций**</span><span class="sxs-lookup"><span data-stu-id="19c55-111">**opcodes**</span></span>](eventmanifestschema-opcodes-tasktype-element.md) | [<span data-ttu-id="19c55-112">**опкоделисттипе**</span><span class="sxs-lookup"><span data-stu-id="19c55-112">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md) | <span data-ttu-id="19c55-113">Определяет список кодов операций, относящихся к задачам.</span><span class="sxs-lookup"><span data-stu-id="19c55-113">Defines a list of task-specific opcodes.</span></span> <span data-ttu-id="19c55-114">Нельзя использовать значения кодов операций, определенные в Winmeta.xml, для кодов операций, относящихся к задачам.</span><span class="sxs-lookup"><span data-stu-id="19c55-114">You cannot use the opcode values defined in Winmeta.xml for task-specific opcodes.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="19c55-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="19c55-115">Attributes</span></span>



| <span data-ttu-id="19c55-116">Имя</span><span class="sxs-lookup"><span data-stu-id="19c55-116">Name</span></span>      | <span data-ttu-id="19c55-117">Тип</span><span class="sxs-lookup"><span data-stu-id="19c55-117">Type</span></span>                                                              | <span data-ttu-id="19c55-118">Описание</span><span class="sxs-lookup"><span data-stu-id="19c55-118">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19c55-119">евентгуид</span><span class="sxs-lookup"><span data-stu-id="19c55-119">eventGUID</span></span> | [<span data-ttu-id="19c55-120">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="19c55-120">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="19c55-121">Глобальный уникальный идентификатор в формате реестра, определяющий задачу.</span><span class="sxs-lookup"><span data-stu-id="19c55-121">A globally unique identifier, in Registry format, that identifies the task.</span></span> <span data-ttu-id="19c55-122">Этот атрибут является обязательным, если для создания класса MOF для поддержки прежних версий используется аргумент компилятора сообщений-MOF.</span><span class="sxs-lookup"><span data-stu-id="19c55-122">This attribute is required if you use the -mof message compiler argument to generate a MOF class for downlevel support.</span></span><br/>                                                                                                   |
| <span data-ttu-id="19c55-123">message</span><span class="sxs-lookup"><span data-stu-id="19c55-123">message</span></span>   | [<span data-ttu-id="19c55-124">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="19c55-124">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="19c55-125">Локализованное отображаемое имя для задачи.</span><span class="sxs-lookup"><span data-stu-id="19c55-125">The localized display name for the task.</span></span> <span data-ttu-id="19c55-126">Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.</span><span class="sxs-lookup"><span data-stu-id="19c55-126">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                   |
| <span data-ttu-id="19c55-127">name</span><span class="sxs-lookup"><span data-stu-id="19c55-127">name</span></span>      | <span data-ttu-id="19c55-128">**QName**</span><span class="sxs-lookup"><span data-stu-id="19c55-128">**QName**</span></span>                                                         | <span data-ttu-id="19c55-129">Имя данной задачи.</span><span class="sxs-lookup"><span data-stu-id="19c55-129">The name of the task.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="19c55-130">символ</span><span class="sxs-lookup"><span data-stu-id="19c55-130">symbol</span></span>    | [<span data-ttu-id="19c55-131">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="19c55-131">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="19c55-132">Символ, используемый для ссылки на задачу в приложении.</span><span class="sxs-lookup"><span data-stu-id="19c55-132">The symbol to use to reference the task in your application.</span></span> <span data-ttu-id="19c55-133">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для задачи в файле заголовка, создаваемом компилятором.</span><span class="sxs-lookup"><span data-stu-id="19c55-133">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the task in the header file that the compiler generates.</span></span> <span data-ttu-id="19c55-134">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="19c55-134">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="19c55-135">значение</span><span class="sxs-lookup"><span data-stu-id="19c55-135">value</span></span>     | [<span data-ttu-id="19c55-136">**UInt16Type**</span><span class="sxs-lookup"><span data-stu-id="19c55-136">**UInt16Type**</span></span>](eventmanifestschema-hexint16type-simpletype.md) | <span data-ttu-id="19c55-137">Числовое значение, однозначно идентифицирующее эту задачу в списке задач, определяемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="19c55-137">A numeric value that uniquely identifies this task within the list of tasks that the provider defines.</span></span> <span data-ttu-id="19c55-138">Значение должно находиться в диапазоне от 1 до 239.</span><span class="sxs-lookup"><span data-stu-id="19c55-138">The value must be in the range from 1 through 239.</span></span><br/>                                                                                                                                             |



## <a name="examples"></a><span data-ttu-id="19c55-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="19c55-139">Examples</span></span>

<span data-ttu-id="19c55-140">В следующем примере показано, как указать задачу.</span><span class="sxs-lookup"><span data-stu-id="19c55-140">The following example shows how to specify a task.</span></span>


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a><span data-ttu-id="19c55-141">Требования</span><span class="sxs-lookup"><span data-stu-id="19c55-141">Requirements</span></span>



| <span data-ttu-id="19c55-142">Требование</span><span class="sxs-lookup"><span data-stu-id="19c55-142">Requirement</span></span> | <span data-ttu-id="19c55-143">Значение</span><span class="sxs-lookup"><span data-stu-id="19c55-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19c55-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19c55-144">Minimum supported client</span></span><br/> | <span data-ttu-id="19c55-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19c55-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="19c55-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19c55-146">Minimum supported server</span></span><br/> | <span data-ttu-id="19c55-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19c55-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





