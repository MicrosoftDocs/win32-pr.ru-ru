---
title: Сложный тип Паттернмапвалуетипе
description: Не используется. Определяет регулярные выражения, используемые для поиска соответствующей строки в строке сообщения и ее изменения.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- Журнал событий сложных типов Паттернмапвалуетипе
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800947"
---
# <a name="patternmapvaluetype-complex-type"></a><span data-ttu-id="18d49-105">Сложный тип Паттернмапвалуетипе</span><span class="sxs-lookup"><span data-stu-id="18d49-105">PatternMapValueType Complex Type</span></span>

<span data-ttu-id="18d49-106">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18d49-106">Not used.</span></span> <span data-ttu-id="18d49-107">Определяет регулярные выражения, используемые для поиска соответствующей строки в строке сообщения и ее изменения.</span><span class="sxs-lookup"><span data-stu-id="18d49-107">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span>

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="18d49-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="18d49-108">Attributes</span></span>



| <span data-ttu-id="18d49-109">Имя</span><span class="sxs-lookup"><span data-stu-id="18d49-109">Name</span></span>  | <span data-ttu-id="18d49-110">Тип</span><span class="sxs-lookup"><span data-stu-id="18d49-110">Type</span></span>   | <span data-ttu-id="18d49-111">Описание</span><span class="sxs-lookup"><span data-stu-id="18d49-111">Description</span></span>                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d49-112">name</span><span class="sxs-lookup"><span data-stu-id="18d49-112">name</span></span>  | <span data-ttu-id="18d49-113">строка</span><span class="sxs-lookup"><span data-stu-id="18d49-113">string</span></span> | <span data-ttu-id="18d49-114">Регулярное выражение, используемое для поиска соответствующей строки в строке сообщения.</span><span class="sxs-lookup"><span data-stu-id="18d49-114">The regular expression used to find a matching string in the message string.</span></span><br/>                   |
| <span data-ttu-id="18d49-115">value</span><span class="sxs-lookup"><span data-stu-id="18d49-115">value</span></span> | <span data-ttu-id="18d49-116">строка</span><span class="sxs-lookup"><span data-stu-id="18d49-116">string</span></span> | <span data-ttu-id="18d49-117">Регулярное выражение, используемое для изменения соответствующей строки, найденной в строке сообщения.</span><span class="sxs-lookup"><span data-stu-id="18d49-117">The regular expression used to alter the matching string that was found in the message string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="18d49-118">Требования</span><span class="sxs-lookup"><span data-stu-id="18d49-118">Requirements</span></span>



| <span data-ttu-id="18d49-119">Требование</span><span class="sxs-lookup"><span data-stu-id="18d49-119">Requirement</span></span> | <span data-ttu-id="18d49-120">Значение</span><span class="sxs-lookup"><span data-stu-id="18d49-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="18d49-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18d49-121">Minimum supported client</span></span><br/> | <span data-ttu-id="18d49-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18d49-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="18d49-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18d49-123">Minimum supported server</span></span><br/> | <span data-ttu-id="18d49-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18d49-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





