---
title: RunLevel (Рунлевелтипе), элемент
description: Содержит значение, указывающее уровень контекста безопасности для выполнения задачи.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- планировщик задач элемента RunLevel
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341305"
---
# <a name="runlevel-runleveltype-element"></a><span data-ttu-id="5d904-104">RunLevel (Рунлевелтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="5d904-104">RunLevel (runLevelType) Element</span></span>

<span data-ttu-id="5d904-105">Содержит значение, указывающее уровень контекста безопасности для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="5d904-105">Contains a value that specifies the security context level for running the task.</span></span> <span data-ttu-id="5d904-106">Можно указать, чтобы запустить задачу с использованием минимальных привилегий или повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="5d904-106">You can specify to run a task using least privileges or elevated privileges.</span></span> <span data-ttu-id="5d904-107">Значение 0 указывает, что задача запускается с наименьшими привилегиями, а значение 1 указывает на выполнение задачи с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="5d904-107">A value of 0 specifies to run the task with lowest privileges, and a value of 1 specifies to run the task with elevated privileges.</span></span>

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

<span data-ttu-id="5d904-108">Элемент **runlevel** определяется простым типом [**рунлевелтипе**](taskschedulerschema-runleveltype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="5d904-108">The **RunLevel** element is defined by the [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5d904-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="5d904-109">Parent element</span></span>



| <span data-ttu-id="5d904-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="5d904-110">Element</span></span>                                                                                  | <span data-ttu-id="5d904-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="5d904-111">Derived from</span></span>                                                           | <span data-ttu-id="5d904-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5d904-112">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d904-113">**Субъект (ПринЦипалтипе)**</span><span class="sxs-lookup"><span data-stu-id="5d904-113">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="5d904-114">**principalType**</span><span class="sxs-lookup"><span data-stu-id="5d904-114">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="5d904-115">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="5d904-115">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="5d904-116">Эти учетные данные определяют контекст безопасности, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="5d904-116">These credentials define the security context that a task runs under.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="5d904-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d904-117">Remarks</span></span>

<span data-ttu-id="5d904-118">Сведения о разработке C++ см. в разделе [**свойство runlevel класса IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span><span class="sxs-lookup"><span data-stu-id="5d904-118">For C++ development, see [**RunLevel Property of IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span></span>

<span data-ttu-id="5d904-119">Сведения о разработке сценариев см. в разделе [**Principal. runlevel**](principal-runlevel.md).</span><span class="sxs-lookup"><span data-stu-id="5d904-119">For script development, see [**Principal.RunLevel**](principal-runlevel.md).</span></span>

<span data-ttu-id="5d904-120">Если задача зарегистрирована с помощью **встроенной \\** учетной записи администратора или учетных записей [LocalSystem](/windows/desktop/Services/localsystem-account) или [LocalService](/windows/desktop/Services/localservice-account) , свойство [**runlevel**](principal-runlevel.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="5d904-120">If a task is registered using the **Builtin\\Administrator** account or the [LocalSystem](/windows/desktop/Services/localsystem-account) or [LocalService](/windows/desktop/Services/localservice-account) accounts, the [**RunLevel**](principal-runlevel.md) property is ignored.</span></span> <span data-ttu-id="5d904-121">Значение атрибута также будет игнорироваться, если отключен [контроль учетных записей](/windows/desktop/SecAuthZ/user-account-control) (UAC).</span><span class="sxs-lookup"><span data-stu-id="5d904-121">The attribute value will also be ignored if [User Account Control](/windows/desktop/SecAuthZ/user-account-control) (UAC) is turned off.</span></span>

<span data-ttu-id="5d904-122">Если задача зарегистрирована с помощью группы **администраторов** для контекста безопасности задачи, необходимо также задать для свойства [**runlevel**](principal-runlevel.md) значение "highestAvailable", чтобы запустить задачу.</span><span class="sxs-lookup"><span data-stu-id="5d904-122">If a task is registered using the **Administrators** group for the security context of the task, then you must also set the [**RunLevel**](principal-runlevel.md) property to "HighestAvailable" to run the task.</span></span> <span data-ttu-id="5d904-123">Дополнительные сведения см. в разделе [контексты безопасности для задач](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="5d904-123">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d904-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5d904-124">Requirements</span></span>



| <span data-ttu-id="5d904-125">Требование</span><span class="sxs-lookup"><span data-stu-id="5d904-125">Requirement</span></span> | <span data-ttu-id="5d904-126">Значение</span><span class="sxs-lookup"><span data-stu-id="5d904-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5d904-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d904-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5d904-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d904-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5d904-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d904-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5d904-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d904-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

