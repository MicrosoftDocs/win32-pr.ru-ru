---
title: Сложный тип Сессионстатечанжетригжертипе
description: Определяет элементы, используемые для создания триггера задачи для подключения консоли или отключения, удаленного подключения или отключения, а также для блокировки или разблокировки рабочей станцией.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- планировщик задач сложного типа Сессионстатечанжетригжертипе
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341300"
---
# <a name="sessionstatechangetriggertype-complex-type"></a><span data-ttu-id="9f031-104">Сложный тип Сессионстатечанжетригжертипе</span><span class="sxs-lookup"><span data-stu-id="9f031-104">sessionStateChangeTriggerType Complex Type</span></span>

<span data-ttu-id="9f031-105">Определяет элементы, используемые для создания триггера задачи для подключения консоли или отключения, удаленного подключения или отключения, а также для блокировки или разблокировки рабочей станцией.</span><span class="sxs-lookup"><span data-stu-id="9f031-105">Defines the elements used to create a task trigger for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9f031-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9f031-106">Child elements</span></span>



| <span data-ttu-id="9f031-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="9f031-107">Element</span></span>                                                                                      | <span data-ttu-id="9f031-108">Тип</span><span class="sxs-lookup"><span data-stu-id="9f031-108">Type</span></span>                                                                                    | <span data-ttu-id="9f031-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9f031-109">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f031-110">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="9f031-110">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="9f031-111">длительность</span><span class="sxs-lookup"><span data-stu-id="9f031-111">duration</span></span>                                                                                | <span data-ttu-id="9f031-112">Задает значение, указывающее длину задержки перед запуском задачи при обнаружении изменения состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="9f031-112">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="9f031-113">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="9f031-113">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="9f031-114">**сессионстатечанжетипе**</span><span class="sxs-lookup"><span data-stu-id="9f031-114">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="9f031-115">Указывает тип изменения сеанса сервера терминалов, запускающего запуск задачи.</span><span class="sxs-lookup"><span data-stu-id="9f031-115">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="9f031-116">**UserId**</span><span class="sxs-lookup"><span data-stu-id="9f031-116">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="9f031-117">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="9f031-117">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="9f031-118">Указывает пользователя для сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="9f031-118">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="9f031-119">При обнаружении изменения состояния сеанса для этого пользователя запускается задача.</span><span class="sxs-lookup"><span data-stu-id="9f031-119">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="9f031-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9f031-120">Requirements</span></span>



| <span data-ttu-id="9f031-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9f031-121">Requirement</span></span> | <span data-ttu-id="9f031-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9f031-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f031-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f031-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9f031-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f031-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9f031-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f031-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9f031-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f031-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





