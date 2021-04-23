---
title: Сложный тип Типелисттипе
description: Определяет типы, используемые в манифесте.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- Журнал событий сложных типов Типелисттипе
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691899"
---
# <a name="typelisttype-complex-type"></a><span data-ttu-id="c0a39-104">Сложный тип Типелисттипе</span><span class="sxs-lookup"><span data-stu-id="c0a39-104">TypeListType Complex Type</span></span>

<span data-ttu-id="c0a39-105">Определяет типы, используемые в манифесте.</span><span class="sxs-lookup"><span data-stu-id="c0a39-105">Defines the types that are used in the manifest.</span></span>

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c0a39-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c0a39-106">Child elements</span></span>



| <span data-ttu-id="c0a39-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="c0a39-107">Element</span></span>                                                               | <span data-ttu-id="c0a39-108">Тип</span><span class="sxs-lookup"><span data-stu-id="c0a39-108">Type</span></span>                                                                           | <span data-ttu-id="c0a39-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c0a39-109">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0a39-110">**нетипизированные типы**</span><span class="sxs-lookup"><span data-stu-id="c0a39-110">**inTypes**</span></span>](eventmanifestschema-intypes-typelisttype-element.md)   | [<span data-ttu-id="c0a39-111">**инпуттипелисттипе**</span><span class="sxs-lookup"><span data-stu-id="c0a39-111">**InputTypeListType**</span></span>](eventmanifestschema-inputtypelisttype-complextype.md) | <span data-ttu-id="c0a39-112">Определяет список входных типов данных.</span><span class="sxs-lookup"><span data-stu-id="c0a39-112">Defines a list of input data types.</span></span><br/>                                                              |
| [<span data-ttu-id="c0a39-113">**ксмлтипес**</span><span class="sxs-lookup"><span data-stu-id="c0a39-113">**xmlTypes**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md) | [<span data-ttu-id="c0a39-114">**ксмлтипелисттипе**</span><span class="sxs-lookup"><span data-stu-id="c0a39-114">**XmlTypeListType**</span></span>](eventmanifestschema-xmltypelisttype-complextype.md)     | <span data-ttu-id="c0a39-115">Определяет выходные типы списка, которые служба использует для определения способа визуализации входного типа данных.</span><span class="sxs-lookup"><span data-stu-id="c0a39-115">Defines a list output types that the service uses to determine how to render an input data type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c0a39-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c0a39-116">Requirements</span></span>



| <span data-ttu-id="c0a39-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c0a39-117">Requirement</span></span> | <span data-ttu-id="c0a39-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c0a39-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0a39-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0a39-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a39-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0a39-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0a39-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0a39-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a39-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0a39-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





