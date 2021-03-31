---
title: Группа actionGroup
description: Определяет группу действий, которые может выполнять задача.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- планировщик задач группы actionGroup
- actionGroup планировщик задач
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801775"
---
# <a name="actiongroup-group"></a><span data-ttu-id="905b4-105">Группа actionGroup</span><span class="sxs-lookup"><span data-stu-id="905b4-105">actionGroup Group</span></span>

<span data-ttu-id="905b4-106">Определяет группу действий, которые может выполнять задача.</span><span class="sxs-lookup"><span data-stu-id="905b4-106">Defines the group of actions that a task can perform.</span></span>

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="905b4-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="905b4-107">Child elements</span></span>



| <span data-ttu-id="905b4-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="905b4-108">Element</span></span>                                                                    | <span data-ttu-id="905b4-109">Тип</span><span class="sxs-lookup"><span data-stu-id="905b4-109">Type</span></span>                                                                       | <span data-ttu-id="905b4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="905b4-110">Description</span></span>                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="905b4-111">**комхандлер**</span><span class="sxs-lookup"><span data-stu-id="905b4-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="905b4-112">**комхандлертипе**</span><span class="sxs-lookup"><span data-stu-id="905b4-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="905b4-113">Представляет действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="905b4-113">Represents an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="905b4-114">**Exec**</span><span class="sxs-lookup"><span data-stu-id="905b4-114">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="905b4-115">**ексектипе**</span><span class="sxs-lookup"><span data-stu-id="905b4-115">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="905b4-116">Представляет действие, выполняющее операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="905b4-116">Represents an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="905b4-117">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="905b4-117">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="905b4-118">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="905b4-118">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="905b4-119">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="905b4-119">Represents an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="905b4-120">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="905b4-120">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="905b4-121">**шовмессажетипе**</span><span class="sxs-lookup"><span data-stu-id="905b4-121">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="905b4-122">Представляет действие, показывающее окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="905b4-122">Represents an action that shows a message box.</span></span><br/>               |



## <a name="remarks"></a><span data-ttu-id="905b4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="905b4-123">Remarks</span></span>

<span data-ttu-id="905b4-124">При чтении или записи XML элементы, определенные этой группой, являются дочерними элементами элемента [**Actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="905b4-124">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="905b4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="905b4-125">Requirements</span></span>



| <span data-ttu-id="905b4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="905b4-126">Requirement</span></span> | <span data-ttu-id="905b4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="905b4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="905b4-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="905b4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="905b4-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="905b4-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="905b4-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="905b4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="905b4-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="905b4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="905b4-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="905b4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="905b4-133">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="905b4-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





