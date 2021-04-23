---
title: Сложный тип Дебугдататипе
description: Определяет данные, которые могут регистрироваться для событий препроцессора трассировки программного обеспечения Windows (WPP).
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- Журнал событий сложных типов Дебугдататипе
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071049"
---
# <a name="debugdatatype-complex-type"></a><span data-ttu-id="70c83-104">Сложный тип Дебугдататипе</span><span class="sxs-lookup"><span data-stu-id="70c83-104">DebugDataType Complex Type</span></span>

<span data-ttu-id="70c83-105">Определяет данные, которые могут регистрироваться для событий препроцессора трассировки программного обеспечения Windows (WPP).</span><span class="sxs-lookup"><span data-stu-id="70c83-105">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span>

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
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

## <a name="child-elements"></a><span data-ttu-id="70c83-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="70c83-106">Child elements</span></span>



| <span data-ttu-id="70c83-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="70c83-107">Element</span></span>                                                                    | <span data-ttu-id="70c83-108">Тип</span><span class="sxs-lookup"><span data-stu-id="70c83-108">Type</span></span>        | <span data-ttu-id="70c83-109">Описание</span><span class="sxs-lookup"><span data-stu-id="70c83-109">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70c83-110">**Компонент**</span><span class="sxs-lookup"><span data-stu-id="70c83-110">**Component**</span></span>](eventschema-component-debugdatatype-element.md)           | <span data-ttu-id="70c83-111">строка</span><span class="sxs-lookup"><span data-stu-id="70c83-111">string</span></span>      | <span data-ttu-id="70c83-112">Имя компонента, который записал в журнал сообщение трассировки.</span><span class="sxs-lookup"><span data-stu-id="70c83-112">The name of the component that logged the trace message.</span></span><br/>                                                |
| [<span data-ttu-id="70c83-113">**филелине**</span><span class="sxs-lookup"><span data-stu-id="70c83-113">**FileLine**</span></span>](eventschema-fileline-debugdatatype-element.md)             | <span data-ttu-id="70c83-114">строка</span><span class="sxs-lookup"><span data-stu-id="70c83-114">string</span></span>      | <span data-ttu-id="70c83-115">Имя исходного файла и строка в исходном файле, которая записала в журнал сообщение трассировки.</span><span class="sxs-lookup"><span data-stu-id="70c83-115">The name of the source file and the line within the source file that logged the trace message.</span></span><br/>          |
| [<span data-ttu-id="70c83-116">**флагснаме**</span><span class="sxs-lookup"><span data-stu-id="70c83-116">**FlagsName**</span></span>](eventschema-flagname-debugdatatype-element.md)            | <span data-ttu-id="70c83-117">строка</span><span class="sxs-lookup"><span data-stu-id="70c83-117">string</span></span>      | <span data-ttu-id="70c83-118">Значение флага, передаваемое поставщику при его включении.</span><span class="sxs-lookup"><span data-stu-id="70c83-118">The flag value passed to the provider when it was enabled.</span></span><br/>                                              |
| [<span data-ttu-id="70c83-119">**Функций**</span><span class="sxs-lookup"><span data-stu-id="70c83-119">**Function**</span></span>](eventschema-function-debugdatatype-element.md)             | <span data-ttu-id="70c83-120">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70c83-120">unsignedInt</span></span> | <span data-ttu-id="70c83-121">Имя функции, которая зарегистрировала сообщение трассировки.</span><span class="sxs-lookup"><span data-stu-id="70c83-121">The name of the function that logged the trace message.</span></span><br/>                                                 |
| [<span data-ttu-id="70c83-122">**LevelName**</span><span class="sxs-lookup"><span data-stu-id="70c83-122">**LevelName**</span></span>](eventschema-levelname-debugdatatype-element.md)           | <span data-ttu-id="70c83-123">строка</span><span class="sxs-lookup"><span data-stu-id="70c83-123">string</span></span>      | <span data-ttu-id="70c83-124">Значение уровня, передаваемое поставщику при его включении.</span><span class="sxs-lookup"><span data-stu-id="70c83-124">The level value passed to the provider when it was enabled.</span></span><br/>                                             |
| [<span data-ttu-id="70c83-125">**Сообщение**</span><span class="sxs-lookup"><span data-stu-id="70c83-125">**Message**</span></span>](eventschema-message-debugdatatype-element.md)               | <span data-ttu-id="70c83-126">строка</span><span class="sxs-lookup"><span data-stu-id="70c83-126">string</span></span>      | <span data-ttu-id="70c83-127">Строка сообщения.</span><span class="sxs-lookup"><span data-stu-id="70c83-127">The message string.</span></span> <span data-ttu-id="70c83-128">XML-код содержит этот элемент, если в событии WPP указано поле Форматтедстринг.</span><span class="sxs-lookup"><span data-stu-id="70c83-128">The XML contains this element if the WPP event specified the FormattedString field.</span></span><br/> |
| [<span data-ttu-id="70c83-129">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="70c83-129">**SequenceNumber**</span></span>](eventschema-sequencenumber-debugdatatype-element.md) | <span data-ttu-id="70c83-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70c83-130">unsignedInt</span></span> | <span data-ttu-id="70c83-131">Локальный или глобальный порядковый номер сообщения трассировки.</span><span class="sxs-lookup"><span data-stu-id="70c83-131">The local or global sequence number of the trace message.</span></span><br/>                                               |
| [<span data-ttu-id="70c83-132">**Вспомогательный компонент**</span><span class="sxs-lookup"><span data-stu-id="70c83-132">**SubComponent**</span></span>](eventschema-subcomponent-debugdatatype-element.md)     | <span data-ttu-id="70c83-133">строка</span><span class="sxs-lookup"><span data-stu-id="70c83-133">string</span></span>      | <span data-ttu-id="70c83-134">Имя подкомпонента, который записал в журнал сообщение трассировки.</span><span class="sxs-lookup"><span data-stu-id="70c83-134">The name of the subcomponent that logged the trace message.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="70c83-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70c83-135">Remarks</span></span>

<span data-ttu-id="70c83-136">Элементы включаются, только если поставщик установил \_ \_ для переменной среды префикс формата% Trace%, чтобы включить их.</span><span class="sxs-lookup"><span data-stu-id="70c83-136">The elements are included only if the provider set the %TRACE\_FORMAT\_PREFIX% environment variable to include them.</span></span> <span data-ttu-id="70c83-137">Дополнительные сведения об этих элементах см. в разделе префикс сообщения трассировки.</span><span class="sxs-lookup"><span data-stu-id="70c83-137">For details on these elements, see Trace Message Prefix.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c83-138">Требования</span><span class="sxs-lookup"><span data-stu-id="70c83-138">Requirements</span></span>



| <span data-ttu-id="70c83-139">Требование</span><span class="sxs-lookup"><span data-stu-id="70c83-139">Requirement</span></span> | <span data-ttu-id="70c83-140">Значение</span><span class="sxs-lookup"><span data-stu-id="70c83-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="70c83-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70c83-141">Minimum supported client</span></span><br/> | <span data-ttu-id="70c83-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70c83-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="70c83-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70c83-143">Minimum supported server</span></span><br/> | <span data-ttu-id="70c83-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70c83-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





