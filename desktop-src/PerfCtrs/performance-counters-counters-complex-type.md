---
description: Определяет раздел манифеста инструментирования, который определяет поставщик и счетчики, которые они предоставляют.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Сложный тип счетчиков
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998515"
---
# <a name="counters-complex-type"></a><span data-ttu-id="52e0e-103">Сложный тип счетчиков</span><span class="sxs-lookup"><span data-stu-id="52e0e-103">counters Complex Type</span></span>

<span data-ttu-id="52e0e-104">Определяет раздел манифеста инструментирования, который определяет поставщик и счетчики, которые они предоставляют.</span><span class="sxs-lookup"><span data-stu-id="52e0e-104">Defines the section of the instrumentation manifest that identifies the provider and the counters that they provide.</span></span>

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="52e0e-105">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="52e0e-105">Child elements</span></span>



| <span data-ttu-id="52e0e-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="52e0e-106">Element</span></span>      | <span data-ttu-id="52e0e-107">Тип</span><span class="sxs-lookup"><span data-stu-id="52e0e-107">Type</span></span>                                                               | <span data-ttu-id="52e0e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="52e0e-108">Description</span></span>                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="52e0e-109">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="52e0e-109">**provider**</span></span> | [<span data-ttu-id="52e0e-110">**мужчина: поставщик**</span><span class="sxs-lookup"><span data-stu-id="52e0e-110">**man:provider**</span></span>](performance-counters-provider-complex-type.md) | <span data-ttu-id="52e0e-111">Определяет поставщик, предоставляющий счетчики.</span><span class="sxs-lookup"><span data-stu-id="52e0e-111">Identifies a provider that provides counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="52e0e-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="52e0e-112">Attributes</span></span>



| <span data-ttu-id="52e0e-113">Имя</span><span class="sxs-lookup"><span data-stu-id="52e0e-113">Name</span></span>          | <span data-ttu-id="52e0e-114">Тип</span><span class="sxs-lookup"><span data-stu-id="52e0e-114">Type</span></span> | <span data-ttu-id="52e0e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="52e0e-115">Description</span></span>                                                      |
|---------------|------|------------------------------------------------------------------|
| <span data-ttu-id="52e0e-116">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="52e0e-116">schemaVersion</span></span> |      | <span data-ttu-id="52e0e-117">Версия схемы, используемой для записи манифеста.</span><span class="sxs-lookup"><span data-stu-id="52e0e-117">The version of the schema used to write the manifest.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="52e0e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="52e0e-118">Requirements</span></span>



| <span data-ttu-id="52e0e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="52e0e-119">Requirement</span></span> | <span data-ttu-id="52e0e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="52e0e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52e0e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52e0e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52e0e-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52e0e-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="52e0e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52e0e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52e0e-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52e0e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52e0e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52e0e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e0e-126">**инструментирования**</span><span class="sxs-lookup"><span data-stu-id="52e0e-126">**instrumentation**</span></span>](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

