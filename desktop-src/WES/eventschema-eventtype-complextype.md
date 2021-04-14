---
title: Сложный тип EventType
description: Определяет корневой узел схемы событий.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- Журнал событий сложного типа EventType
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414881"
---
# <a name="eventtype-complex-type"></a><span data-ttu-id="2cbea-104">Сложный тип EventType</span><span class="sxs-lookup"><span data-stu-id="2cbea-104">EventType Complex Type</span></span>

<span data-ttu-id="2cbea-105">Определяет корневой узел схемы событий.</span><span class="sxs-lookup"><span data-stu-id="2cbea-105">Defines the root node of the Event schema.</span></span>

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2cbea-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2cbea-106">Child elements</span></span>



| <span data-ttu-id="2cbea-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="2cbea-107">Element</span></span>                                                                          | <span data-ttu-id="2cbea-108">Тип</span><span class="sxs-lookup"><span data-stu-id="2cbea-108">Type</span></span>                                                                               | <span data-ttu-id="2cbea-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2cbea-109">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cbea-110">**бинаревентдата**</span><span class="sxs-lookup"><span data-stu-id="2cbea-110">**BinaryEventData**</span></span>](eventschema-binaryeventdata-eventtype-element.md)         | <span data-ttu-id="2cbea-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="2cbea-111">hexBinary</span></span>                                                                          | <span data-ttu-id="2cbea-112">Содержит данные события как двоичный BLOB-объект.</span><span class="sxs-lookup"><span data-stu-id="2cbea-112">Contains the event data as a binary blob.</span></span> <span data-ttu-id="2cbea-113">Данные события подготавливаются к просмотру как двоичный BLOB-объект, если функция отрисовки не может найти метаданные, используемые для декодирования события.</span><span class="sxs-lookup"><span data-stu-id="2cbea-113">The event data is rendered as a binary blob if the rendering function cannot find the metadata used to decode the event.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="2cbea-114">**дебугдата**</span><span class="sxs-lookup"><span data-stu-id="2cbea-114">**DebugData**</span></span>](eventschema-debugdata-eventtype-element.md)                     | [<span data-ttu-id="2cbea-115">**дебугдататипе**</span><span class="sxs-lookup"><span data-stu-id="2cbea-115">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="2cbea-116">Содержит данные, которые могут быть зарегистрированы для событий препроцессора трассировки программного обеспечения Windows (WPP).</span><span class="sxs-lookup"><span data-stu-id="2cbea-116">Contains the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="2cbea-117">**EventData**</span><span class="sxs-lookup"><span data-stu-id="2cbea-117">**EventData**</span></span>](eventschema-eventdata-eventtype-element.md)                     | [<span data-ttu-id="2cbea-118">**евентдататипе**</span><span class="sxs-lookup"><span data-stu-id="2cbea-118">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="2cbea-119">Содержит данные о событии.</span><span class="sxs-lookup"><span data-stu-id="2cbea-119">Contains the event data.</span></span> <span data-ttu-id="2cbea-120">Порядок элементов данных в шаблоне определяет макет данных события.</span><span class="sxs-lookup"><span data-stu-id="2cbea-120">The order of the data items in the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="2cbea-121">**процессинжеррордата**</span><span class="sxs-lookup"><span data-stu-id="2cbea-121">**ProcessingErrorData**</span></span>](eventschema-processingerrordata-eventtype-element.md) | [<span data-ttu-id="2cbea-122">**процессинжеррордататипе**</span><span class="sxs-lookup"><span data-stu-id="2cbea-122">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="2cbea-123">Содержит подробные сведения об ошибке, возникшей при попытке подготовки к просмотру события.</span><span class="sxs-lookup"><span data-stu-id="2cbea-123">Contains details of the error that occurred while trying to render the event.</span></span> <span data-ttu-id="2cbea-124">Это может произойти, если данные события не соответствуют определению данных события в манифесте.</span><span class="sxs-lookup"><span data-stu-id="2cbea-124">This can occur if the event data does not match the event data definition in the manifest.</span></span> <span data-ttu-id="2cbea-125">Данные события включаются в двоичный BLOB-объект.</span><span class="sxs-lookup"><span data-stu-id="2cbea-125">The event data is included as a binary blob.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="2cbea-126">**рендерингинфо**</span><span class="sxs-lookup"><span data-stu-id="2cbea-126">**RenderingInfo**</span></span>](eventschema-renderinginfo-eventtype-element.md)             | [<span data-ttu-id="2cbea-127">**рендерингинфотипе**</span><span class="sxs-lookup"><span data-stu-id="2cbea-127">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="2cbea-128">Содержит строки отображаемых сообщений для события (включая строку сообщения события и строки сообщения для любого свойства события, например уровень, задача и код операции).</span><span class="sxs-lookup"><span data-stu-id="2cbea-128">Contains the rendered message strings for the event (includes the event's message string and the message strings for any of the event's properties such as level, task, and opcode).</span></span> <span data-ttu-id="2cbea-129">Этот раздел будет содержать только события, собранные с помощью службы [сборщика событий Windows](/windows/desktop/WEC/windows-event-collector) .</span><span class="sxs-lookup"><span data-stu-id="2cbea-129">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span><br/> |
| [<span data-ttu-id="2cbea-130">**Система**</span><span class="sxs-lookup"><span data-stu-id="2cbea-130">**System**</span></span>](eventschema-system-eventtype-element.md)                           | [<span data-ttu-id="2cbea-131">**системпропертиестипе**</span><span class="sxs-lookup"><span data-stu-id="2cbea-131">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="2cbea-132">Содержит сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.</span><span class="sxs-lookup"><span data-stu-id="2cbea-132">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="2cbea-133">**UserData**</span><span class="sxs-lookup"><span data-stu-id="2cbea-133">**UserData**</span></span>](eventschema-userdata-eventtype-element.md)                       | [<span data-ttu-id="2cbea-134">**усердататипе**</span><span class="sxs-lookup"><span data-stu-id="2cbea-134">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="2cbea-135">Содержит данные о событии.</span><span class="sxs-lookup"><span data-stu-id="2cbea-135">Contains the event data.</span></span> <span data-ttu-id="2cbea-136">Раздел данных пользователя шаблона определяет макет данных события.</span><span class="sxs-lookup"><span data-stu-id="2cbea-136">The user data section of the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="2cbea-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cbea-137">Remarks</span></span>

<span data-ttu-id="2cbea-138">Как правило, этот раздел будет содержать раздел **EVENTDATA** или **UserData** .</span><span class="sxs-lookup"><span data-stu-id="2cbea-138">Typically, this section will contain with the **EventData** or **UserData** section.</span></span> <span data-ttu-id="2cbea-139">Раздел **EVENTDATA** используется, если шаблон не содержит раздел **UserData** .</span><span class="sxs-lookup"><span data-stu-id="2cbea-139">The **EventData** section is used if the template does not contain a **UserData** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cbea-140">Требования</span><span class="sxs-lookup"><span data-stu-id="2cbea-140">Requirements</span></span>



| <span data-ttu-id="2cbea-141">Требование</span><span class="sxs-lookup"><span data-stu-id="2cbea-141">Requirement</span></span> | <span data-ttu-id="2cbea-142">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbea-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2cbea-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cbea-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2cbea-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2cbea-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2cbea-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cbea-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2cbea-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2cbea-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

