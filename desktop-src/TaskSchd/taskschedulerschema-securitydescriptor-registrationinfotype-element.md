---
title: SecurityDescriptor (Регистратионинфотипе), элемент
description: Указывает дескриптор безопасности задачи.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- планировщик задач элемента SecurityDescriptor
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071296"
---
# <a name="securitydescriptor-registrationinfotype-element"></a><span data-ttu-id="ea15a-104">SecurityDescriptor (Регистратионинфотипе), элемент</span><span class="sxs-lookup"><span data-stu-id="ea15a-104">SecurityDescriptor (registrationInfoType) Element</span></span>

<span data-ttu-id="ea15a-105">Указывает дескриптор безопасности задачи.</span><span class="sxs-lookup"><span data-stu-id="ea15a-105">Specifies the security descriptor of the task.</span></span>

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

<span data-ttu-id="ea15a-106">Элемент **SecurityDescriptor** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ea15a-106">The **SecurityDescriptor** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ea15a-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="ea15a-107">Parent element</span></span>



| <span data-ttu-id="ea15a-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ea15a-108">Element</span></span>                                                                           | <span data-ttu-id="ea15a-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="ea15a-109">Derived from</span></span>                                                                         | <span data-ttu-id="ea15a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ea15a-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea15a-111">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="ea15a-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="ea15a-112">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="ea15a-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="ea15a-113">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="ea15a-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ea15a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea15a-114">Remarks</span></span>

<span data-ttu-id="ea15a-115">Для разработки сценариев дескриптор безопасности задачи указывается с помощью свойства [**регистратионинфо. SecurityDescriptor**](registrationinfo-securitydescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="ea15a-115">For scripting development, the security descriptor of a task is specified using the [**RegistrationInfo.SecurityDescriptor**](registrationinfo-securitydescriptor.md) property.</span></span>

<span data-ttu-id="ea15a-116">Для разработки на C++ дескриптор безопасности задачи указывается с помощью свойства [**ирегистратионинфо:: SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="ea15a-116">For C++ development, the security descriptor of a task is specified using the [**IRegistrationInfo::SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea15a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ea15a-117">Requirements</span></span>



| <span data-ttu-id="ea15a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ea15a-118">Requirement</span></span> | <span data-ttu-id="ea15a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ea15a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ea15a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea15a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ea15a-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea15a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ea15a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea15a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ea15a-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea15a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea15a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea15a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea15a-125">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="ea15a-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ea15a-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="ea15a-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





