---
title: Resources (Локализатионтипе), элемент
description: Определяет группу строковых таблиц, содержащих локализованные строки, на которые ссылается манифест.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- Журнал событий элемента Resources
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691755"
---
# <a name="resources-localizationtype-element"></a><span data-ttu-id="4276e-104">Resources (Локализатионтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="4276e-104">resources (LocalizationType) Element</span></span>

<span data-ttu-id="4276e-105">Определяет группу строковых таблиц, содержащих локализованные строки, на которые ссылается манифест.</span><span class="sxs-lookup"><span data-stu-id="4276e-105">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span>

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4276e-106">Элемент **Resources** определяется сложным типом [**локализатионтипе**](eventmanifestschema-localizationtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4276e-106">The **resources** element is defined by the [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4276e-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4276e-107">Child elements</span></span>



| <span data-ttu-id="4276e-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4276e-108">Element</span></span>                                                                  | <span data-ttu-id="4276e-109">Тип</span><span class="sxs-lookup"><span data-stu-id="4276e-109">Type</span></span>                                                                       | <span data-ttu-id="4276e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4276e-110">Description</span></span>                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="4276e-111">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="4276e-111">**stringTable**</span></span>](eventmanifestschema-stringtable-resources-element.md) | [<span data-ttu-id="4276e-112">**стрингтаблетипе**</span><span class="sxs-lookup"><span data-stu-id="4276e-112">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="4276e-113">Определяет список локализованных строк, на которые можно ссылаться в манифесте.</span><span class="sxs-lookup"><span data-stu-id="4276e-113">Defines a list of localized strings that you can reference in your manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="4276e-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4276e-114">Attributes</span></span>



| <span data-ttu-id="4276e-115">Имя</span><span class="sxs-lookup"><span data-stu-id="4276e-115">Name</span></span>    | <span data-ttu-id="4276e-116">Тип</span><span class="sxs-lookup"><span data-stu-id="4276e-116">Type</span></span>   | <span data-ttu-id="4276e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4276e-117">Description</span></span>                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4276e-118">язык и региональные параметры</span><span class="sxs-lookup"><span data-stu-id="4276e-118">culture</span></span> | <span data-ttu-id="4276e-119">строка</span><span class="sxs-lookup"><span data-stu-id="4276e-119">string</span></span> | <span data-ttu-id="4276e-120">Имя языка, определяющее язык и региональные параметры локализованных строк в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="4276e-120">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="4276e-121">Например, "en-US" для английского языка (США).</span><span class="sxs-lookup"><span data-stu-id="4276e-121">For example, "en-US" for English (United States).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4276e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4276e-122">Requirements</span></span>



| <span data-ttu-id="4276e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4276e-123">Requirement</span></span> | <span data-ttu-id="4276e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4276e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4276e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4276e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4276e-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4276e-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4276e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4276e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4276e-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4276e-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4276e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4276e-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="4276e-130">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="4276e-130">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="4276e-131">**Локализация (Инструментатионманифест)**</span><span class="sxs-lookup"><span data-stu-id="4276e-131">**localization (instrumentationManifest)**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





