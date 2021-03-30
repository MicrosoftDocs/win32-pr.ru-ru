---
title: Execution (Системпропертиестипе), элемент
description: Содержит сведения о процессе и потоке, которые зарегистрировали событие.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- Журнал событий элемента выполнения
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801420"
---
# <a name="execution-systempropertiestype-element"></a><span data-ttu-id="0f4e3-104">Execution (Системпропертиестипе), элемент</span><span class="sxs-lookup"><span data-stu-id="0f4e3-104">Execution (SystemPropertiesType) Element</span></span>

<span data-ttu-id="0f4e3-105">Содержит сведения о процессе и потоке, которые зарегистрировали событие.</span><span class="sxs-lookup"><span data-stu-id="0f4e3-105">Contains information about the process and thread that logged the event.</span></span>

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="0f4e3-106">Элемент **Execution** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0f4e3-106">The **Execution** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="0f4e3-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0f4e3-107">Attributes</span></span>



| <span data-ttu-id="0f4e3-108">Имя</span><span class="sxs-lookup"><span data-stu-id="0f4e3-108">Name</span></span>          | <span data-ttu-id="0f4e3-109">Тип</span><span class="sxs-lookup"><span data-stu-id="0f4e3-109">Type</span></span>         | <span data-ttu-id="0f4e3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0f4e3-110">Description</span></span>                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f4e3-111">кернелтиме</span><span class="sxs-lookup"><span data-stu-id="0f4e3-111">KernelTime</span></span>    | <span data-ttu-id="0f4e3-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f4e3-112">unsignedInt</span></span>  | <span data-ttu-id="0f4e3-113">Затраченное время выполнения инструкций режима ядра в единицах времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="0f4e3-113">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span><br/>                        |
| <span data-ttu-id="0f4e3-114">ProcessID</span><span class="sxs-lookup"><span data-stu-id="0f4e3-114">ProcessID</span></span>     | <span data-ttu-id="0f4e3-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f4e3-115">unsignedInt</span></span>  | <span data-ttu-id="0f4e3-116">Указывает процесс, создавший событие.</span><span class="sxs-lookup"><span data-stu-id="0f4e3-116">Identifies the process that generated the event.</span></span><br/>                                               |
| <span data-ttu-id="0f4e3-117">процессорид</span><span class="sxs-lookup"><span data-stu-id="0f4e3-117">ProcessorID</span></span>   | <span data-ttu-id="0f4e3-118">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="0f4e3-118">unsignedByte</span></span> | <span data-ttu-id="0f4e3-119">Идентификационный номер процессора, который обработал событие.</span><span class="sxs-lookup"><span data-stu-id="0f4e3-119">The identification number for the processor that processed the event.</span></span><br/>                          |
| <span data-ttu-id="0f4e3-120">процессортиме</span><span class="sxs-lookup"><span data-stu-id="0f4e3-120">ProcessorTime</span></span> | <span data-ttu-id="0f4e3-121">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f4e3-121">unsignedInt</span></span>  | <span data-ttu-id="0f4e3-122">Для частных сеансов ETW — затраченное время выполнения инструкций пользовательского режима в тактах ЦП.</span><span class="sxs-lookup"><span data-stu-id="0f4e3-122">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span><br/> |
| <span data-ttu-id="0f4e3-123">SessionID</span><span class="sxs-lookup"><span data-stu-id="0f4e3-123">SessionID</span></span>     | <span data-ttu-id="0f4e3-124">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f4e3-124">unsignedInt</span></span>  | <span data-ttu-id="0f4e3-125">Идентификационный номер сеанса сервера терминалов, в котором произошло событие.</span><span class="sxs-lookup"><span data-stu-id="0f4e3-125">The identification number for the terminal server session in which the event occurred.</span></span><br/>         |
| <span data-ttu-id="0f4e3-126">ThreadID</span><span class="sxs-lookup"><span data-stu-id="0f4e3-126">ThreadID</span></span>      | <span data-ttu-id="0f4e3-127">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f4e3-127">unsignedInt</span></span>  | <span data-ttu-id="0f4e3-128">Указывает поток, создавший событие.</span><span class="sxs-lookup"><span data-stu-id="0f4e3-128">Identifies the thread that generated the event.</span></span><br/>                                                |
| <span data-ttu-id="0f4e3-129">усертиме</span><span class="sxs-lookup"><span data-stu-id="0f4e3-129">UserTime</span></span>      | <span data-ttu-id="0f4e3-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f4e3-130">unsignedInt</span></span>  | <span data-ttu-id="0f4e3-131">Затраченное время выполнения инструкций пользовательского режима в единицах времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="0f4e3-131">Elapsed execution time for user-mode instructions, in CPU time units.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="0f4e3-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0f4e3-132">Requirements</span></span>



| <span data-ttu-id="0f4e3-133">Требование</span><span class="sxs-lookup"><span data-stu-id="0f4e3-133">Requirement</span></span> | <span data-ttu-id="0f4e3-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0f4e3-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f4e3-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f4e3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0f4e3-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f4e3-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0f4e3-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f4e3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0f4e3-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f4e3-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f4e3-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f4e3-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f4e3-140">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="0f4e3-140">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0f4e3-141">**системпропертиестипе**</span><span class="sxs-lookup"><span data-stu-id="0f4e3-141">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

<span data-ttu-id="0f4e3-142">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="0f4e3-142">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0f4e3-143">**Система (EventType)**</span><span class="sxs-lookup"><span data-stu-id="0f4e3-143">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





