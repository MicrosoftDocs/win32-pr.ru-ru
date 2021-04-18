---
title: Binary (Темплатеитемтипе), элемент
description: Содержит двоичные данные, предоставляемые API журнала событий.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- Журнал событий двоичного элемента
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691908"
---
# <a name="binary-templateitemtype-element"></a><span data-ttu-id="e6829-104">Binary (Темплатеитемтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="e6829-104">binary (TemplateItemType) Element</span></span>

<span data-ttu-id="e6829-105">Содержит двоичные данные, предоставляемые API [журнала событий](/windows/desktop/EventLog/event-logging) .</span><span class="sxs-lookup"><span data-stu-id="e6829-105">Contains the binary data that is supplied by the [Event Log](/windows/desktop/EventLog/event-logging) API.</span></span>

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="e6829-106">Элемент **binary** определяется сложным типом [**темплатеитемтипе**](eventmanifestschema-templateitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e6829-106">The **binary** element is defined by the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="e6829-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e6829-107">Attributes</span></span>



| <span data-ttu-id="e6829-108">Имя</span><span class="sxs-lookup"><span data-stu-id="e6829-108">Name</span></span> | <span data-ttu-id="e6829-109">Тип</span><span class="sxs-lookup"><span data-stu-id="e6829-109">Type</span></span>   | <span data-ttu-id="e6829-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e6829-110">Description</span></span>                                          |
|------|--------|------------------------------------------------------|
| <span data-ttu-id="e6829-111">name</span><span class="sxs-lookup"><span data-stu-id="e6829-111">name</span></span> | <span data-ttu-id="e6829-112">строка</span><span class="sxs-lookup"><span data-stu-id="e6829-112">string</span></span> | <span data-ttu-id="e6829-113">Имя, связанное с двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="e6829-113">The name associated with the binary data.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e6829-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e6829-114">Requirements</span></span>



| <span data-ttu-id="e6829-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e6829-115">Requirement</span></span> | <span data-ttu-id="e6829-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e6829-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6829-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6829-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e6829-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6829-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e6829-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6829-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e6829-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6829-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6829-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6829-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6829-122">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="e6829-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="e6829-123">**шаблон (Темплателисттипе)**</span><span class="sxs-lookup"><span data-stu-id="e6829-123">**template (TemplateListType)**</span></span>](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

