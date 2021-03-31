---
title: Сложный тип Темплателисттипе
description: Определяет список шаблонов, указывающих данные, включаемые в события. | Сложный тип Темплателисттипе
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- Журнал событий сложных типов Темплателисттипе
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820725"
---
# <a name="templatelisttype-complex-type"></a><span data-ttu-id="8e016-105">Сложный тип Темплателисттипе</span><span class="sxs-lookup"><span data-stu-id="8e016-105">TemplateListType Complex Type</span></span>

<span data-ttu-id="8e016-106">Определяет список шаблонов, указывающих данные, включаемые в события.</span><span class="sxs-lookup"><span data-stu-id="8e016-106">Defines a list of templates that specify the data to include with the events.</span></span>

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8e016-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8e016-107">Child elements</span></span>



| <span data-ttu-id="8e016-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="8e016-108">Element</span></span>                                                                   | <span data-ttu-id="8e016-109">Тип</span><span class="sxs-lookup"><span data-stu-id="8e016-109">Type</span></span>                                                                         | <span data-ttu-id="8e016-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8e016-110">Description</span></span>                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="8e016-111">**шаблон**</span><span class="sxs-lookup"><span data-stu-id="8e016-111">**template**</span></span>](eventmanifestschema-template-templatelisttype-element.md) | [<span data-ttu-id="8e016-112">**темплатеитемтипе**</span><span class="sxs-lookup"><span data-stu-id="8e016-112">**TemplateItemType**</span></span>](eventmanifestschema-templateitemtype-complextype.md) | <span data-ttu-id="8e016-113">Шаблон, определяющий данные, включаемые в событие.</span><span class="sxs-lookup"><span data-stu-id="8e016-113">A template that defines the data to include with an event.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8e016-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8e016-114">Requirements</span></span>



| <span data-ttu-id="8e016-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8e016-115">Requirement</span></span> | <span data-ttu-id="8e016-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8e016-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8e016-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e016-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e016-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e016-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8e016-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e016-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8e016-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e016-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





