---
title: Сложный тип Стрингтаблетипе
description: Определяет список локализованных строк, на которые можно ссылаться в манифесте. | Сложный тип Стрингтаблетипе
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Журнал событий сложных типов Стрингтаблетипе
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694017"
---
# <a name="stringtabletype-complex-type"></a><span data-ttu-id="d3de4-105">Сложный тип Стрингтаблетипе</span><span class="sxs-lookup"><span data-stu-id="d3de4-105">StringTableType Complex Type</span></span>

<span data-ttu-id="d3de4-106">Определяет список локализованных строк, на которые можно ссылаться в манифесте.</span><span class="sxs-lookup"><span data-stu-id="d3de4-106">Defines a list of localized strings that you can reference in your manifest.</span></span>

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d3de4-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d3de4-107">Child elements</span></span>



| <span data-ttu-id="d3de4-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d3de4-108">Element</span></span>                                                              | <span data-ttu-id="d3de4-109">Тип</span><span class="sxs-lookup"><span data-stu-id="d3de4-109">Type</span></span> | <span data-ttu-id="d3de4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d3de4-110">Description</span></span>                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [<span data-ttu-id="d3de4-111">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d3de4-111">**string**</span></span>](eventmanifestschema-string-stringtabletype-element.md) |      | <span data-ttu-id="d3de4-112">Определяет локализованную строку.</span><span class="sxs-lookup"><span data-stu-id="d3de4-112">Defines a localized string.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="d3de4-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d3de4-113">Attributes</span></span>



| <span data-ttu-id="d3de4-114">Имя</span><span class="sxs-lookup"><span data-stu-id="d3de4-114">Name</span></span>       | <span data-ttu-id="d3de4-115">Тип</span><span class="sxs-lookup"><span data-stu-id="d3de4-115">Type</span></span>   | <span data-ttu-id="d3de4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d3de4-116">Description</span></span>                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3de4-117">идентификатор</span><span class="sxs-lookup"><span data-stu-id="d3de4-117">id</span></span>         | <span data-ttu-id="d3de4-118">строка</span><span class="sxs-lookup"><span data-stu-id="d3de4-118">string</span></span> | <span data-ttu-id="d3de4-119">Идентификатор, однозначно определяющий строку в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="d3de4-119">An identifier that uniquely identifies the string within the string table.</span></span> <span data-ttu-id="d3de4-120">Например, «Printer. Connection».</span><span class="sxs-lookup"><span data-stu-id="d3de4-120">For example, "Printer.Connection".</span></span><br/> |
| <span data-ttu-id="d3de4-121">стрингтипе</span><span class="sxs-lookup"><span data-stu-id="d3de4-121">stringType</span></span> | <span data-ttu-id="d3de4-122">строка</span><span class="sxs-lookup"><span data-stu-id="d3de4-122">string</span></span> | <span data-ttu-id="d3de4-123">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d3de4-123">Not used.</span></span><br/>                                                                                                     |
| <span data-ttu-id="d3de4-124">value</span><span class="sxs-lookup"><span data-stu-id="d3de4-124">value</span></span>      | <span data-ttu-id="d3de4-125">строка</span><span class="sxs-lookup"><span data-stu-id="d3de4-125">string</span></span> | <span data-ttu-id="d3de4-126">Локализованная строка.</span><span class="sxs-lookup"><span data-stu-id="d3de4-126">The localized string.</span></span><br/>                                                                                         |



## <a name="remarks"></a><span data-ttu-id="d3de4-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3de4-127">Remarks</span></span>

<span data-ttu-id="d3de4-128">Можно ссылаться на строки из любого типа манифеста, содержащего атрибут Message.</span><span class="sxs-lookup"><span data-stu-id="d3de4-128">You can reference the strings from any manifest type that contains the message attribute.</span></span> <span data-ttu-id="d3de4-129">Чтобы сослаться на строку с Стрингтипе строки и идентификатором "Printer. Connection", используйте $ (String. Printer. Connection) в качестве значения атрибута Message.</span><span class="sxs-lookup"><span data-stu-id="d3de4-129">To reference a string with a stringType of "string" and an id of "Printer.Connection", use $(string.Printer.Connection) as the value of the message attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3de4-130">Требования</span><span class="sxs-lookup"><span data-stu-id="d3de4-130">Requirements</span></span>



| <span data-ttu-id="d3de4-131">Требование</span><span class="sxs-lookup"><span data-stu-id="d3de4-131">Requirement</span></span> | <span data-ttu-id="d3de4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d3de4-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3de4-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3de4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d3de4-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3de4-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d3de4-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3de4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d3de4-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3de4-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





