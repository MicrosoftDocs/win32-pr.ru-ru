---
title: Сложный тип Локализатионтипе
description: Определяет группу локализованных ресурсов, на которые ссылается манифест. | Сложный тип Локализатионтипе
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- Журнал событий сложных типов Локализатионтипе
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693964"
---
# <a name="localizationtype-complex-type"></a><span data-ttu-id="2d5a7-105">Сложный тип Локализатионтипе</span><span class="sxs-lookup"><span data-stu-id="2d5a7-105">LocalizationType Complex Type</span></span>

<span data-ttu-id="2d5a7-106">Определяет группу локализованных ресурсов, на которые ссылается манифест.</span><span class="sxs-lookup"><span data-stu-id="2d5a7-106">Defines a group of localized resources that you reference in your manifest.</span></span>

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2d5a7-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2d5a7-107">Child elements</span></span>



| <span data-ttu-id="2d5a7-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="2d5a7-108">Element</span></span>                                                                         | <span data-ttu-id="2d5a7-109">Тип</span><span class="sxs-lookup"><span data-stu-id="2d5a7-109">Type</span></span>                                                                       | <span data-ttu-id="2d5a7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="2d5a7-110">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d5a7-111">**источников**</span><span class="sxs-lookup"><span data-stu-id="2d5a7-111">**resources**</span></span>](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | <span data-ttu-id="2d5a7-112">Определяет группу строковых таблиц, содержащих локализованные строки, на которые ссылается манифест.</span><span class="sxs-lookup"><span data-stu-id="2d5a7-112">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span><br/> |
| [<span data-ttu-id="2d5a7-113">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="2d5a7-113">**stringTable**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md) | [<span data-ttu-id="2d5a7-114">**стрингтаблетипе**</span><span class="sxs-lookup"><span data-stu-id="2d5a7-114">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="2d5a7-115">Определяет список локализованных строк, на которые можно ссылаться в манифесте.</span><span class="sxs-lookup"><span data-stu-id="2d5a7-115">Defines a list of localized strings that you can reference in your manifest.</span></span><br/>                             |



## <a name="attributes"></a><span data-ttu-id="2d5a7-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2d5a7-116">Attributes</span></span>



| <span data-ttu-id="2d5a7-117">Имя</span><span class="sxs-lookup"><span data-stu-id="2d5a7-117">Name</span></span>            | <span data-ttu-id="2d5a7-118">Тип</span><span class="sxs-lookup"><span data-stu-id="2d5a7-118">Type</span></span>   | <span data-ttu-id="2d5a7-119">Описание</span><span class="sxs-lookup"><span data-stu-id="2d5a7-119">Description</span></span>                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5a7-120">язык и региональные параметры</span><span class="sxs-lookup"><span data-stu-id="2d5a7-120">culture</span></span>         | <span data-ttu-id="2d5a7-121">строка</span><span class="sxs-lookup"><span data-stu-id="2d5a7-121">string</span></span> | <span data-ttu-id="2d5a7-122">Имя языка, определяющее язык и региональные параметры локализованных строк в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="2d5a7-122">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="2d5a7-123">Например, "en-US" для английского языка (США).</span><span class="sxs-lookup"><span data-stu-id="2d5a7-123">For example, "en-US" for English (United States).</span></span><br/> |
| <span data-ttu-id="2d5a7-124">фаллбакккултуре</span><span class="sxs-lookup"><span data-stu-id="2d5a7-124">fallbackCulture</span></span> | <span data-ttu-id="2d5a7-125">строка</span><span class="sxs-lookup"><span data-stu-id="2d5a7-125">string</span></span> | <span data-ttu-id="2d5a7-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2d5a7-126">Not used.</span></span><br/>                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="2d5a7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2d5a7-127">Requirements</span></span>



| <span data-ttu-id="2d5a7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2d5a7-128">Requirement</span></span> | <span data-ttu-id="2d5a7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2d5a7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d5a7-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d5a7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2d5a7-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d5a7-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d5a7-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d5a7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2d5a7-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d5a7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





