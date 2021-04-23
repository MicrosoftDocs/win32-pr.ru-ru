---
title: StateChange (Сессионстатечанжетригжертипе), элемент
description: Содержит тип изменения сеанса сервера терминалов, запускающего запуск задачи.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- планировщик задач элемента StateChange
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137678"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a><span data-ttu-id="68ebd-104">StateChange (Сессионстатечанжетригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="68ebd-104">StateChange (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="68ebd-105">Содержит тип изменения сеанса сервера терминалов, запускающего запуск задачи.</span><span class="sxs-lookup"><span data-stu-id="68ebd-105">Contains the kind of Terminal Server session change that would trigger a task launch.</span></span>

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

<span data-ttu-id="68ebd-106">Элемент **StateChange** определяется сложным типом [**сессионстатечанжетригжертипе**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="68ebd-106">The **StateChange** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="68ebd-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="68ebd-107">Parent element</span></span>



| <span data-ttu-id="68ebd-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="68ebd-108">Element</span></span>                       | <span data-ttu-id="68ebd-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="68ebd-109">Derived from</span></span>                                                                                           | <span data-ttu-id="68ebd-110">Описание</span><span class="sxs-lookup"><span data-stu-id="68ebd-110">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68ebd-111">**сессионстатечанжетригжер**</span><span class="sxs-lookup"><span data-stu-id="68ebd-111">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="68ebd-112">**сессионстатечанжетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="68ebd-112">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="68ebd-113">Указывает триггер, который запускает задачу при изменении состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="68ebd-113">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="68ebd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68ebd-114">Remarks</span></span>

<span data-ttu-id="68ebd-115">Сведения о разработке на языке C++ см. в разделе [**свойство StateChange объекта исессионстатечанжетригжер**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span><span class="sxs-lookup"><span data-stu-id="68ebd-115">For C++ development, see [**StateChange Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span></span>

<span data-ttu-id="68ebd-116">Сведения о разработке сценариев см. в разделе [**сессионстатечанжетригжер. StateChange**](sessionstatechangetrigger-statechange.md).</span><span class="sxs-lookup"><span data-stu-id="68ebd-116">For script development, see [**SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68ebd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="68ebd-117">Requirements</span></span>



| <span data-ttu-id="68ebd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="68ebd-118">Requirement</span></span> | <span data-ttu-id="68ebd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="68ebd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68ebd-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68ebd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68ebd-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68ebd-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68ebd-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68ebd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68ebd-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68ebd-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





