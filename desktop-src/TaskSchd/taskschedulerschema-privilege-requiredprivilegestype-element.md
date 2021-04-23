---
title: Элемент Privilege (Рекуиредпривилежестипе)
description: Указывает правую задачу для выполнения различных операций, связанных с системой, таких как завершение работы системы, загрузка драйверов устройств или изменение системного времени.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Элемент Privilege планировщик задач
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492279"
---
# <a name="privilege-requiredprivilegestype-element"></a><span data-ttu-id="bb7cf-104">Элемент Privilege (Рекуиредпривилежестипе)</span><span class="sxs-lookup"><span data-stu-id="bb7cf-104">Privilege (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="bb7cf-105">Указывает правую задачу для выполнения различных операций, связанных с системой, таких как завершение работы системы, загрузка драйверов устройств или изменение системного времени.</span><span class="sxs-lookup"><span data-stu-id="bb7cf-105">Specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

<span data-ttu-id="bb7cf-106">Элемент **Privilege** определяется сложным типом [**рекуиредпривилежестипе**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bb7cf-106">The **Privilege** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bb7cf-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="bb7cf-107">Parent element</span></span>



| <span data-ttu-id="bb7cf-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="bb7cf-108">Element</span></span>                                                                                             | <span data-ttu-id="bb7cf-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="bb7cf-109">Derived from</span></span>                                                                             | <span data-ttu-id="bb7cf-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bb7cf-110">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb7cf-111">**рекуиредпривилежес**</span><span class="sxs-lookup"><span data-stu-id="bb7cf-111">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="bb7cf-112">**рекуиредпривилежестипе**</span><span class="sxs-lookup"><span data-stu-id="bb7cf-112">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="bb7cf-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="bb7cf-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bb7cf-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb7cf-114">Remarks</span></span>

<span data-ttu-id="bb7cf-115">Для разработки на C++ эта информация доступна через свойство [**IPrincipal2:: рекуиредпривилеже**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="bb7cf-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="bb7cf-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="bb7cf-116">Examples</span></span>

<span data-ttu-id="bb7cf-117">Следующий XML-код определяет элемент Settings, который указывает право задачи для выполнения различных операций, связанных с системой, таких как завершение работы системы, загрузка драйверов устройств или изменение системного времени.</span><span class="sxs-lookup"><span data-stu-id="bb7cf-117">The following XML defines a settings element that specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
        
```



## <a name="requirements"></a><span data-ttu-id="bb7cf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bb7cf-118">Requirements</span></span>



| <span data-ttu-id="bb7cf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bb7cf-119">Requirement</span></span> | <span data-ttu-id="bb7cf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bb7cf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bb7cf-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb7cf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb7cf-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bb7cf-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bb7cf-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb7cf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb7cf-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb7cf-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb7cf-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb7cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb7cf-126">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="bb7cf-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





