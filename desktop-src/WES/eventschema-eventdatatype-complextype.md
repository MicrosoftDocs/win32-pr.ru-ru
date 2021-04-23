---
title: Сложный тип Евентдататипе
description: Определяет элементы данных событий и структуры, содержащие данные события.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- Журнал событий сложных типов Евентдататипе
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801432"
---
# <a name="eventdatatype-complex-type"></a><span data-ttu-id="b052e-104">Сложный тип Евентдататипе</span><span class="sxs-lookup"><span data-stu-id="b052e-104">EventDataType Complex Type</span></span>

<span data-ttu-id="b052e-105">Определяет элементы данных событий и структуры, содержащие данные события.</span><span class="sxs-lookup"><span data-stu-id="b052e-105">Defines the event data items and structures that contains the event data.</span></span>

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b052e-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b052e-106">Child elements</span></span>



| <span data-ttu-id="b052e-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="b052e-107">Element</span></span>                                                              | <span data-ttu-id="b052e-108">Тип</span><span class="sxs-lookup"><span data-stu-id="b052e-108">Type</span></span>                                                               | <span data-ttu-id="b052e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b052e-109">Description</span></span>                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b052e-110">**Двоичный**</span><span class="sxs-lookup"><span data-stu-id="b052e-110">**Binary**</span></span>](eventschema-binary-eventdatatype-element.md)           | <span data-ttu-id="b052e-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="b052e-111">hexBinary</span></span>                                                          | <span data-ttu-id="b052e-112">Двоичный BLOB-объект данных для событий, записываемых с помощью [ведения журнала событий](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="b052e-112">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span><br/> |
| [<span data-ttu-id="b052e-113">**комплексдата**</span><span class="sxs-lookup"><span data-stu-id="b052e-113">**ComplexData**</span></span>](eventschema-complexdata-eventdatatype-element.md) | [<span data-ttu-id="b052e-114">**комплексдататипе**</span><span class="sxs-lookup"><span data-stu-id="b052e-114">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md) | <span data-ttu-id="b052e-115">Структура, определенная в шаблоне для события.</span><span class="sxs-lookup"><span data-stu-id="b052e-115">A structure that is defined in the template for the event.</span></span><br/>                                |
| [<span data-ttu-id="b052e-116">**Data**</span><span class="sxs-lookup"><span data-stu-id="b052e-116">**Data**</span></span>](eventschema-data-eventdatatype-element.md)               | [<span data-ttu-id="b052e-117">**DataType**</span><span class="sxs-lookup"><span data-stu-id="b052e-117">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)          | <span data-ttu-id="b052e-118">Элемент данных верхнего уровня, определенный в шаблоне для события.</span><span class="sxs-lookup"><span data-stu-id="b052e-118">A top-level data item that is defined in the template for the event.</span></span><br/>                      |



## <a name="attributes"></a><span data-ttu-id="b052e-119">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b052e-119">Attributes</span></span>



| <span data-ttu-id="b052e-120">Имя</span><span class="sxs-lookup"><span data-stu-id="b052e-120">Name</span></span> | <span data-ttu-id="b052e-121">Тип</span><span class="sxs-lookup"><span data-stu-id="b052e-121">Type</span></span>   | <span data-ttu-id="b052e-122">Описание</span><span class="sxs-lookup"><span data-stu-id="b052e-122">Description</span></span>                                                       |
|------|--------|-------------------------------------------------------------------|
| <span data-ttu-id="b052e-123">Название</span><span class="sxs-lookup"><span data-stu-id="b052e-123">Name</span></span> | <span data-ttu-id="b052e-124">строка</span><span class="sxs-lookup"><span data-stu-id="b052e-124">string</span></span> | <span data-ttu-id="b052e-125">Имя шаблона, содержащего элементы данных.</span><span class="sxs-lookup"><span data-stu-id="b052e-125">The name of the template that contains the data items.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b052e-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b052e-126">Remarks</span></span>

<span data-ttu-id="b052e-127">Функция [**евтрендер**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) отображает массивы и структуры как двоичные BLOB-объекты.</span><span class="sxs-lookup"><span data-stu-id="b052e-127">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders arrays and structures as binary blobs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b052e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="b052e-128">Requirements</span></span>



| <span data-ttu-id="b052e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="b052e-129">Requirement</span></span> | <span data-ttu-id="b052e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="b052e-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b052e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b052e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b052e-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b052e-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b052e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b052e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b052e-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b052e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

