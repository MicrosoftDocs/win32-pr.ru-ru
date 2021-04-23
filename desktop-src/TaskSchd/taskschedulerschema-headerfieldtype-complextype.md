---
title: Сложный тип Хеадерфиелдтипе
description: Определяет элементы, используемые для создания поля заголовка в сообщении электронной почты.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- планировщик задач сложного типа Хеадерфиелдтипе
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672589"
---
# <a name="headerfieldtype-complex-type"></a><span data-ttu-id="e0a9a-104">Сложный тип Хеадерфиелдтипе</span><span class="sxs-lookup"><span data-stu-id="e0a9a-104">headerFieldType Complex Type</span></span>

<span data-ttu-id="e0a9a-105">Определяет элементы, используемые для создания поля заголовка в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-105">Defines the elements that are used to create a header field in an email message.</span></span>

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e0a9a-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e0a9a-106">Child elements</span></span>



| <span data-ttu-id="e0a9a-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="e0a9a-107">Element</span></span>                                                            | <span data-ttu-id="e0a9a-108">Тип</span><span class="sxs-lookup"><span data-stu-id="e0a9a-108">Type</span></span>                                                                    | <span data-ttu-id="e0a9a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e0a9a-109">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="e0a9a-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e0a9a-110">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="e0a9a-111">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="e0a9a-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="e0a9a-112">Задает имя поля заголовка в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-112">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="e0a9a-113">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e0a9a-113">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="e0a9a-114">**string**</span><span class="sxs-lookup"><span data-stu-id="e0a9a-114">**string**</span></span>                                                              | <span data-ttu-id="e0a9a-115">Задает значение поля заголовка в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-115">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="e0a9a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e0a9a-116">Requirements</span></span>



| <span data-ttu-id="e0a9a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e0a9a-117">Requirement</span></span> | <span data-ttu-id="e0a9a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e0a9a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e0a9a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0a9a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e0a9a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0a9a-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e0a9a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0a9a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e0a9a-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e0a9a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





