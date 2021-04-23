---
title: Сложный тип Актионстипе
description: Определяет дочерние элементы и атрибут для элемента Actions.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- планировщик задач сложного типа Актионстипе
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2cf95803f6e4a02d4ec00d7aa767aa4e8a8a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415880"
---
# <a name="actionstype-complex-type"></a><span data-ttu-id="15a5e-104">Сложный тип Актионстипе</span><span class="sxs-lookup"><span data-stu-id="15a5e-104">actionsType Complex Type</span></span>

<span data-ttu-id="15a5e-105">Определяет дочерние элементы и атрибут для элемента [**Actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="15a5e-105">Defines the child elements and attribute for the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="15a5e-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="15a5e-106">Attributes</span></span>



| <span data-ttu-id="15a5e-107">Имя</span><span class="sxs-lookup"><span data-stu-id="15a5e-107">Name</span></span>    | <span data-ttu-id="15a5e-108">Тип</span><span class="sxs-lookup"><span data-stu-id="15a5e-108">Type</span></span>  | <span data-ttu-id="15a5e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="15a5e-109">Description</span></span>                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15a5e-110">Контекст</span><span class="sxs-lookup"><span data-stu-id="15a5e-110">Context</span></span> | <span data-ttu-id="15a5e-111">IDREF</span><span class="sxs-lookup"><span data-stu-id="15a5e-111">IDREF</span></span> | <span data-ttu-id="15a5e-112">Идентификатор субъекта используемого, который является контекстом безопасности для действий задачи.</span><span class="sxs-lookup"><span data-stu-id="15a5e-112">Principal identifier of the used who is the security context for the actions of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="15a5e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="15a5e-113">Requirements</span></span>



| <span data-ttu-id="15a5e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="15a5e-114">Requirement</span></span> | <span data-ttu-id="15a5e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="15a5e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15a5e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15a5e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15a5e-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15a5e-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="15a5e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15a5e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15a5e-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15a5e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15a5e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15a5e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a5e-121">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="15a5e-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="15a5e-122">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="15a5e-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





