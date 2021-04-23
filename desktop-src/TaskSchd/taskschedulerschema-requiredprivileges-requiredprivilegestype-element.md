---
title: Рекуиредпривилежес (Рекуиредпривилежестипе), элемент
description: Указывает привилегии, необходимые для задачи.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- планировщик задач элемента Рекуиредпривилежес
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137682"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a><span data-ttu-id="650a9-104">Рекуиредпривилежес (Рекуиредпривилежестипе), элемент</span><span class="sxs-lookup"><span data-stu-id="650a9-104">RequiredPrivileges (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="650a9-105">Указывает привилегии, необходимые для задачи.</span><span class="sxs-lookup"><span data-stu-id="650a9-105">Specifies the privileges that are required by the task.</span></span>

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

<span data-ttu-id="650a9-106">Элемент **рекуиредпривилежес** определяется сложным типом [**рекуиредпривилежестипе**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="650a9-106">The **RequiredPrivileges** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="650a9-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="650a9-107">Parent element</span></span>



| <span data-ttu-id="650a9-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="650a9-108">Element</span></span>                                                                                  | <span data-ttu-id="650a9-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="650a9-109">Derived from</span></span>                                                           | <span data-ttu-id="650a9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="650a9-110">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="650a9-111">**Субъект (ПринЦипалтипе)**</span><span class="sxs-lookup"><span data-stu-id="650a9-111">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="650a9-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="650a9-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="650a9-113">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="650a9-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="650a9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="650a9-114">Remarks</span></span>

<span data-ttu-id="650a9-115">Для разработки на C++ эта информация доступна через свойство [**IPrincipal2:: рекуиредпривилеже**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="650a9-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="650a9-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="650a9-116">Examples</span></span>

<span data-ttu-id="650a9-117">Следующий XML-код определяет, используя идентификатор группы и необходимые привилегии.</span><span class="sxs-lookup"><span data-stu-id="650a9-117">The following XML defines using a group identifier and the required privileges.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="650a9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="650a9-118">Requirements</span></span>



| <span data-ttu-id="650a9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="650a9-119">Requirement</span></span> | <span data-ttu-id="650a9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="650a9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="650a9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="650a9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="650a9-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="650a9-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="650a9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="650a9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="650a9-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="650a9-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="650a9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="650a9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650a9-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="650a9-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





