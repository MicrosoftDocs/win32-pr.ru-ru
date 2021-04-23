---
title: Сложный тип Рендерингинфотипе
description: Определяет отрисованные сообщения для события.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Журнал событий сложных типов Рендерингинфотипе
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492684"
---
# <a name="renderinginfotype-complex-type"></a><span data-ttu-id="b33af-104">Сложный тип Рендерингинфотипе</span><span class="sxs-lookup"><span data-stu-id="b33af-104">RenderingInfoType Complex Type</span></span>

<span data-ttu-id="b33af-105">Определяет отрисованные сообщения для события.</span><span class="sxs-lookup"><span data-stu-id="b33af-105">Defines the rendered messages for the event.</span></span>

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b33af-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b33af-106">Child elements</span></span>



| <span data-ttu-id="b33af-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="b33af-107">Element</span></span>                                                             | <span data-ttu-id="b33af-108">Тип</span><span class="sxs-lookup"><span data-stu-id="b33af-108">Type</span></span>   | <span data-ttu-id="b33af-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b33af-109">Description</span></span>                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="b33af-110">**Канал**</span><span class="sxs-lookup"><span data-stu-id="b33af-110">**Channel**</span></span>](eventschema-task-renderingtype-element.md)           | <span data-ttu-id="b33af-111">строка</span><span class="sxs-lookup"><span data-stu-id="b33af-111">string</span></span> | <span data-ttu-id="b33af-112">Строка отображаемого сообщения канала, указанного в событии.</span><span class="sxs-lookup"><span data-stu-id="b33af-112">The rendered message string of the channel specified in the event.</span></span><br/> |
| [<span data-ttu-id="b33af-113">**Ключевое слово**</span><span class="sxs-lookup"><span data-stu-id="b33af-113">**Keyword**</span></span>](eventschema-keyword-keywords-element.md)             | <span data-ttu-id="b33af-114">строка</span><span class="sxs-lookup"><span data-stu-id="b33af-114">string</span></span> | <span data-ttu-id="b33af-115">Строка отображаемого сообщения ключевого слова, указанного в событии.</span><span class="sxs-lookup"><span data-stu-id="b33af-115">The rendered message string of a keyword specified in the event.</span></span><br/>   |
| [<span data-ttu-id="b33af-116">**Keywords**</span><span class="sxs-lookup"><span data-stu-id="b33af-116">**Keywords**</span></span>](eventschema-keywords-renderingtype-element.md)      |        | <span data-ttu-id="b33af-117">Список отображаемых ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="b33af-117">A list of rendered keywords.</span></span><br/>                                       |
| [<span data-ttu-id="b33af-118">**Уровню**</span><span class="sxs-lookup"><span data-stu-id="b33af-118">**Level**</span></span>](eventschema-level-renderingtype-element.md)            | <span data-ttu-id="b33af-119">строка</span><span class="sxs-lookup"><span data-stu-id="b33af-119">string</span></span> | <span data-ttu-id="b33af-120">Строка отображаемого сообщения уровня, указанного в событии.</span><span class="sxs-lookup"><span data-stu-id="b33af-120">The rendered message string of the level specified in the event.</span></span><br/>   |
| [<span data-ttu-id="b33af-121">**Сообщение**</span><span class="sxs-lookup"><span data-stu-id="b33af-121">**Message**</span></span>](eventschema-message-renderingtype-element.md)        | <span data-ttu-id="b33af-122">строка</span><span class="sxs-lookup"><span data-stu-id="b33af-122">string</span></span> | <span data-ttu-id="b33af-123">Строка отображаемого сообщения события.</span><span class="sxs-lookup"><span data-stu-id="b33af-123">The rendered message string of the event.</span></span><br/>                          |
| [<span data-ttu-id="b33af-124">**Код операции**</span><span class="sxs-lookup"><span data-stu-id="b33af-124">**Opcode**</span></span>](eventschema-opcode-renderingtype-element.md)          | <span data-ttu-id="b33af-125">строка</span><span class="sxs-lookup"><span data-stu-id="b33af-125">string</span></span> | <span data-ttu-id="b33af-126">Строка отображаемого сообщения кода операции, указанного в событии.</span><span class="sxs-lookup"><span data-stu-id="b33af-126">The rendered message string of the opcode specified in the event.</span></span><br/>  |
| [<span data-ttu-id="b33af-127">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="b33af-127">**Provider**</span></span>](eventschema-publisher-renderinginfotype-element.md) | <span data-ttu-id="b33af-128">строка</span><span class="sxs-lookup"><span data-stu-id="b33af-128">string</span></span> | <span data-ttu-id="b33af-129">Строка отображаемого сообщения для поставщика.</span><span class="sxs-lookup"><span data-stu-id="b33af-129">The rendered message string for the provider.</span></span><br/>                      |
| [<span data-ttu-id="b33af-130">**Задача**</span><span class="sxs-lookup"><span data-stu-id="b33af-130">**Task**</span></span>](eventschema-task-renderingtype-element.md)              | <span data-ttu-id="b33af-131">строка</span><span class="sxs-lookup"><span data-stu-id="b33af-131">string</span></span> | <span data-ttu-id="b33af-132">Строка отображаемого сообщения задачи, указанной в событии.</span><span class="sxs-lookup"><span data-stu-id="b33af-132">The rendered message string of the task specified in the event.</span></span><br/>    |



## <a name="attributes"></a><span data-ttu-id="b33af-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b33af-133">Attributes</span></span>



| <span data-ttu-id="b33af-134">Имя</span><span class="sxs-lookup"><span data-stu-id="b33af-134">Name</span></span>    | <span data-ttu-id="b33af-135">Тип</span><span class="sxs-lookup"><span data-stu-id="b33af-135">Type</span></span>     | <span data-ttu-id="b33af-136">Описание</span><span class="sxs-lookup"><span data-stu-id="b33af-136">Description</span></span>                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b33af-137">culture</span><span class="sxs-lookup"><span data-stu-id="b33af-137">Culture</span></span> | <span data-ttu-id="b33af-138">Язык</span><span class="sxs-lookup"><span data-stu-id="b33af-138">language</span></span> | <span data-ttu-id="b33af-139">Имя языка (например, EN-US), определяющее языковой стандарт, используемый для отображения строк сообщений.</span><span class="sxs-lookup"><span data-stu-id="b33af-139">The language name (for example, en-US) that identifies the locale used to render the message strings.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b33af-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b33af-140">Remarks</span></span>

<span data-ttu-id="b33af-141">Этот раздел будет содержать только события, собранные с помощью службы [сборщика событий Windows](/windows/desktop/WEC/windows-event-collector) .</span><span class="sxs-lookup"><span data-stu-id="b33af-141">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span>

## <a name="requirements"></a><span data-ttu-id="b33af-142">Требования</span><span class="sxs-lookup"><span data-stu-id="b33af-142">Requirements</span></span>



| <span data-ttu-id="b33af-143">Требование</span><span class="sxs-lookup"><span data-stu-id="b33af-143">Requirement</span></span> | <span data-ttu-id="b33af-144">Значение</span><span class="sxs-lookup"><span data-stu-id="b33af-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b33af-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b33af-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b33af-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b33af-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b33af-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b33af-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b33af-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b33af-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

