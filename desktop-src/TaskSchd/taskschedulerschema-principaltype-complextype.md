---
title: Сложный тип ПринЦипалтипе
description: Определяет атрибут, дочерние элементы и сведения о последовательности для элемента Principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- планировщик задач сложного типа ПринЦипалтипе
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492060"
---
# <a name="principaltype-complex-type"></a><span data-ttu-id="e5296-104">Сложный тип ПринЦипалтипе</span><span class="sxs-lookup"><span data-stu-id="e5296-104">principalType Complex Type</span></span>

<span data-ttu-id="e5296-105">Определяет атрибут, дочерние элементы и сведения о последовательности для элемента [**Principal**](taskschedulerschema-principal-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e5296-105">Defines the attribute, child elements, and sequencing information for the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e5296-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e5296-106">Child elements</span></span>



| <span data-ttu-id="e5296-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="e5296-107">Element</span></span>                                                                                             | <span data-ttu-id="e5296-108">Тип</span><span class="sxs-lookup"><span data-stu-id="e5296-108">Type</span></span>                                                                                     | <span data-ttu-id="e5296-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e5296-109">Description</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5296-110">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="e5296-110">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md)                        | <span data-ttu-id="e5296-111">строка</span><span class="sxs-lookup"><span data-stu-id="e5296-111">string</span></span>                                                                                   | <span data-ttu-id="e5296-112">Указывает имя участника, который отображается в планировщик задач пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e5296-112">Specifies the name of the principal that is displayed in the Task Scheduler user interface (UI).</span></span><br/>                 |
| [<span data-ttu-id="e5296-113">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="e5296-113">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)                                | [<span data-ttu-id="e5296-114">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="e5296-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="e5296-115">Указывает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="e5296-115">Specifies the identifier of the user group that is required to run tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="e5296-116">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="e5296-116">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)                            | [<span data-ttu-id="e5296-117">**logonType**</span><span class="sxs-lookup"><span data-stu-id="e5296-117">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md)                            | <span data-ttu-id="e5296-118">Указывает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="e5296-118">Specifies the security logon method that is required to run tasks that are associated with the principal.</span></span><br/>        |
| [<span data-ttu-id="e5296-119">**процесстокенсидтипе**</span><span class="sxs-lookup"><span data-stu-id="e5296-119">**ProcessTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [<span data-ttu-id="e5296-120">**процесстокенсидтипе**</span><span class="sxs-lookup"><span data-stu-id="e5296-120">**processTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-simpletype.md)        | <span data-ttu-id="e5296-121">Указывает типы идентификаторов безопасности процесса (SID), которые могут использоваться задачами.</span><span class="sxs-lookup"><span data-stu-id="e5296-121">Specifies the types of process security identifier (SID) that can be used by tasks.</span></span><br/>                              |
| [<span data-ttu-id="e5296-122">**рекуиредпривилежес**</span><span class="sxs-lookup"><span data-stu-id="e5296-122">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="e5296-123">**рекуиредпривилежестипе**</span><span class="sxs-lookup"><span data-stu-id="e5296-123">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="e5296-124">Указывает необходимые привилегии для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="e5296-124">Specifies the required privileges to run the task.</span></span><br/>                                                               |
| [<span data-ttu-id="e5296-125">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="e5296-125">**RunLevel**</span></span>](taskschedulerschema-runlevel-principaltype-element.md)                              | [<span data-ttu-id="e5296-126">**рунлевелтипе**</span><span class="sxs-lookup"><span data-stu-id="e5296-126">**runLevelType**</span></span>](taskschedulerschema-runleveltype-simpletype.md)                      | <span data-ttu-id="e5296-127">Указывает уровень разрешений, в котором будет выполняться задача.</span><span class="sxs-lookup"><span data-stu-id="e5296-127">Specifies the permission level that the task will be run at.</span></span><br/>                                                     |
| [<span data-ttu-id="e5296-128">**UserId**</span><span class="sxs-lookup"><span data-stu-id="e5296-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)                                  | [<span data-ttu-id="e5296-129">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="e5296-129">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="e5296-130">Указывает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="e5296-130">Specifies the user identifier that is required to run tasks that are associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="e5296-131">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e5296-131">Attributes</span></span>



| <span data-ttu-id="e5296-132">Имя</span><span class="sxs-lookup"><span data-stu-id="e5296-132">Name</span></span> | <span data-ttu-id="e5296-133">Тип</span><span class="sxs-lookup"><span data-stu-id="e5296-133">Type</span></span> | <span data-ttu-id="e5296-134">Описание</span><span class="sxs-lookup"><span data-stu-id="e5296-134">Description</span></span>                                           |
|------|------|-------------------------------------------------------|
| <span data-ttu-id="e5296-135">идентификатор</span><span class="sxs-lookup"><span data-stu-id="e5296-135">id</span></span>   | <span data-ttu-id="e5296-136">ID</span><span class="sxs-lookup"><span data-stu-id="e5296-136">ID</span></span>   | <span data-ttu-id="e5296-137">Указывает идентификатор участника.</span><span class="sxs-lookup"><span data-stu-id="e5296-137">Specifies the identifier of the principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e5296-138">Требования</span><span class="sxs-lookup"><span data-stu-id="e5296-138">Requirements</span></span>



| <span data-ttu-id="e5296-139">Требование</span><span class="sxs-lookup"><span data-stu-id="e5296-139">Requirement</span></span> | <span data-ttu-id="e5296-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e5296-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e5296-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5296-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e5296-142">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e5296-142">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e5296-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5296-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e5296-144">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e5296-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5296-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5296-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5296-146">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="e5296-146">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="e5296-147">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e5296-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





