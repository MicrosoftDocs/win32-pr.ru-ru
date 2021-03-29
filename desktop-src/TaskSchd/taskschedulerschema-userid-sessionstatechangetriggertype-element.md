---
title: UserId (Сессионстатечанжетригжертипе), элемент
description: Содержит пользователя для сеанса сервера терминалов. При обнаружении изменения состояния сеанса для этого пользователя запускается задача.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
keywords:
- Элемент UserId планировщик задач
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534973"
---
# <a name="userid-sessionstatechangetriggertype-element"></a><span data-ttu-id="fac63-105">UserId (Сессионстатечанжетригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="fac63-105">UserId (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="fac63-106">Содержит пользователя для сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="fac63-106">Contains the user for the Terminal Server session.</span></span> <span data-ttu-id="fac63-107">При обнаружении изменения состояния сеанса для этого пользователя запускается задача.</span><span class="sxs-lookup"><span data-stu-id="fac63-107">When a session state change is detected for this user, a task is started.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="fac63-108">Элемент **UserID** определяется сложным типом [**сессионстатечанжетригжертипе**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fac63-108">The **UserId** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fac63-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="fac63-109">Parent element</span></span>



| <span data-ttu-id="fac63-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="fac63-110">Element</span></span>                       | <span data-ttu-id="fac63-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="fac63-111">Derived from</span></span>                                                                                           | <span data-ttu-id="fac63-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fac63-112">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac63-113">**сессионстатечанжетригжер**</span><span class="sxs-lookup"><span data-stu-id="fac63-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="fac63-114">**сессионстатечанжетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="fac63-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="fac63-115">Указывает триггер, который запускает задачу при изменении состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="fac63-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fac63-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fac63-116">Remarks</span></span>

<span data-ttu-id="fac63-117">Сведения о разработке на языке C++ см. в разделе [**свойство UserId объекта исессионстатечанжетригжер**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span><span class="sxs-lookup"><span data-stu-id="fac63-117">For C++ development, see [**UserId Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span></span>

<span data-ttu-id="fac63-118">Сведения о разработке сценариев см. в разделе [**сессионстатечанжетригжер. UserID**](sessionstatechangetrigger-userid.md).</span><span class="sxs-lookup"><span data-stu-id="fac63-118">For script development, see [**SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fac63-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fac63-119">Requirements</span></span>



| <span data-ttu-id="fac63-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fac63-120">Requirement</span></span> | <span data-ttu-id="fac63-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fac63-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fac63-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fac63-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fac63-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fac63-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fac63-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fac63-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fac63-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fac63-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





