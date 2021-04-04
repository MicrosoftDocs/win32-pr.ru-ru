---
title: String (Стрингтаблетипе), элемент
description: Определяет локализованную строку.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- Журнал событий элемента строки
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988842"
---
# <a name="string-stringtabletype-element"></a><span data-ttu-id="d0e24-104">String (Стрингтаблетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="d0e24-104">string (StringTableType) Element</span></span>

<span data-ttu-id="d0e24-105">Определяет локализованную строку.</span><span class="sxs-lookup"><span data-stu-id="d0e24-105">Defines a localized string.</span></span>

``` syntax
<xs:element name="string">
    <xs:complexType>
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
```

<span data-ttu-id="d0e24-106">Элемент **строки** определяется сложным типом [**стрингтаблетипе**](eventmanifestschema-stringtabletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d0e24-106">The **string** element is defined by the [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="d0e24-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d0e24-107">Attributes</span></span>



| <span data-ttu-id="d0e24-108">Имя</span><span class="sxs-lookup"><span data-stu-id="d0e24-108">Name</span></span>       | <span data-ttu-id="d0e24-109">Тип</span><span class="sxs-lookup"><span data-stu-id="d0e24-109">Type</span></span>   | <span data-ttu-id="d0e24-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d0e24-110">Description</span></span>                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e24-111">идентификатор</span><span class="sxs-lookup"><span data-stu-id="d0e24-111">id</span></span>         | <span data-ttu-id="d0e24-112">строка</span><span class="sxs-lookup"><span data-stu-id="d0e24-112">string</span></span> | <span data-ttu-id="d0e24-113">Идентификатор, однозначно определяющий строку в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="d0e24-113">An identifier that uniquely identifies the string within the string table.</span></span><br/> |
| <span data-ttu-id="d0e24-114">стрингтипе</span><span class="sxs-lookup"><span data-stu-id="d0e24-114">stringType</span></span> | <span data-ttu-id="d0e24-115">строка</span><span class="sxs-lookup"><span data-stu-id="d0e24-115">string</span></span> | <span data-ttu-id="d0e24-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d0e24-116">Not used.</span></span><br/>                                                                  |
| <span data-ttu-id="d0e24-117">value</span><span class="sxs-lookup"><span data-stu-id="d0e24-117">value</span></span>      | <span data-ttu-id="d0e24-118">строка</span><span class="sxs-lookup"><span data-stu-id="d0e24-118">string</span></span> | <span data-ttu-id="d0e24-119">Локализованная строка.</span><span class="sxs-lookup"><span data-stu-id="d0e24-119">The localized string.</span></span><br/>                                                      |



## <a name="requirements"></a><span data-ttu-id="d0e24-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d0e24-120">Requirements</span></span>



| <span data-ttu-id="d0e24-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d0e24-121">Requirement</span></span> | <span data-ttu-id="d0e24-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d0e24-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0e24-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0e24-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e24-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0e24-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d0e24-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0e24-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e24-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0e24-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0e24-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0e24-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0e24-128">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="d0e24-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="d0e24-129">**stringTable (Локализатионтипе)**</span><span class="sxs-lookup"><span data-stu-id="d0e24-129">**stringTable (LocalizationType)**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





