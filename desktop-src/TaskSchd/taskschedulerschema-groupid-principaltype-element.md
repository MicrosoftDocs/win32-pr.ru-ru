---
title: Элемент GroupId (ПринЦипалтипе)
description: Указывает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Элемент GroupId планировщик задач
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071887"
---
# <a name="groupid-principaltype-element"></a><span data-ttu-id="68163-104">Элемент GroupId (ПринЦипалтипе)</span><span class="sxs-lookup"><span data-stu-id="68163-104">GroupId (principalType) Element</span></span>

<span data-ttu-id="68163-105">Указывает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="68163-105">Specifies the identifier of the user group required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="68163-106">Элемент **groupId** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="68163-106">The **GroupId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="68163-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="68163-107">Parent element</span></span>



| <span data-ttu-id="68163-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="68163-108">Element</span></span>                                                                  | <span data-ttu-id="68163-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="68163-109">Derived from</span></span>                                                           | <span data-ttu-id="68163-110">Описание</span><span class="sxs-lookup"><span data-stu-id="68163-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="68163-111">**Основного**</span><span class="sxs-lookup"><span data-stu-id="68163-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="68163-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="68163-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="68163-113">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="68163-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="68163-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68163-114">Remarks</span></span>

<span data-ttu-id="68163-115">Нельзя одновременно указать идентификатор группы и идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="68163-115">You cannot specify a group identifier and a user identifier at the same time.</span></span> <span data-ttu-id="68163-116">Укажите либо элементы [**UserID**](taskschedulerschema-userid-principaltype-element.md) , либо **groupId** , но не оба.</span><span class="sxs-lookup"><span data-stu-id="68163-116">Specify either the [**UserId**](taskschedulerschema-userid-principaltype-element.md) or **GroupId** elements, but not both.</span></span>

<span data-ttu-id="68163-117">Для разработки скриптов идентификатор группы субъекта указывается с помощью свойства [**Principal. groupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="68163-117">For script development, the group identifier of the principal is specified using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="68163-118">Для разработки на C++ идентификатор группы субъекта указывается с помощью свойства [**IPrincipal:: groupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .</span><span class="sxs-lookup"><span data-stu-id="68163-118">For C++ development, the group identifier of the principal is specified using the [**IPrincipal::GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="68163-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="68163-119">Examples</span></span>

<span data-ttu-id="68163-120">Полный пример XML-кода для задачи, использующей этот элемент, см. в разделе [пример триггера LOGON (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="68163-120">For a complete example of the XML for a task that uses this element, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68163-121">Требования</span><span class="sxs-lookup"><span data-stu-id="68163-121">Requirements</span></span>



| <span data-ttu-id="68163-122">Требование</span><span class="sxs-lookup"><span data-stu-id="68163-122">Requirement</span></span> | <span data-ttu-id="68163-123">Значение</span><span class="sxs-lookup"><span data-stu-id="68163-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68163-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68163-124">Minimum supported client</span></span><br/> | <span data-ttu-id="68163-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68163-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68163-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68163-126">Minimum supported server</span></span><br/> | <span data-ttu-id="68163-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68163-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68163-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68163-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68163-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="68163-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





