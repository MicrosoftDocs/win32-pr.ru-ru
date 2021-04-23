---
title: Процесстокенсидтипе (ПринЦипалтипе), элемент
description: Указывает тип задачи «определение безопасности процесса» (SID).
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- планировщик задач элемента Процесстокенсидтипе
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875da055f2719afca454d225c3bebd13b404b3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136534"
---
# <a name="processtokensidtype-principaltype-element"></a><span data-ttu-id="243b3-104">Процесстокенсидтипе (ПринЦипалтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="243b3-104">ProcessTokenSidType (principalType) Element</span></span>

<span data-ttu-id="243b3-105">Указывает тип задачи «определение безопасности процесса» (SID).</span><span class="sxs-lookup"><span data-stu-id="243b3-105">Specifies the process security identify (SID) type of the task.</span></span>

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="243b3-106">Элемент **процесстокенсидтипе** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="243b3-106">The **ProcessTokenSidType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="243b3-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="243b3-107">Parent element</span></span>



| <span data-ttu-id="243b3-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="243b3-108">Element</span></span>                                                                  | <span data-ttu-id="243b3-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="243b3-109">Derived from</span></span>                                                           | <span data-ttu-id="243b3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="243b3-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="243b3-111">**Основного**</span><span class="sxs-lookup"><span data-stu-id="243b3-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="243b3-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="243b3-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="243b3-113">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="243b3-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="243b3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="243b3-114">Remarks</span></span>

<span data-ttu-id="243b3-115">Для разработки на C++ тип идентификатора безопасности процесса указывается с помощью свойства [**IPrincipal2::P роцесстокенсидтипе**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) .</span><span class="sxs-lookup"><span data-stu-id="243b3-115">For C++ development, the process SID type is specified by using the [**IPrincipal2::ProcessTokenSidType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) property.</span></span>

## <a name="examples"></a><span data-ttu-id="243b3-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="243b3-116">Examples</span></span>

<span data-ttu-id="243b3-117">Следующий XML-код определяет тип идентификатора безопасности процесса задачи.</span><span class="sxs-lookup"><span data-stu-id="243b3-117">The following XML defines the process SID type of the task.</span></span>


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="243b3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="243b3-118">Requirements</span></span>



| <span data-ttu-id="243b3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="243b3-119">Requirement</span></span> | <span data-ttu-id="243b3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="243b3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="243b3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="243b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="243b3-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="243b3-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="243b3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="243b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="243b3-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="243b3-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="243b3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="243b3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243b3-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="243b3-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





