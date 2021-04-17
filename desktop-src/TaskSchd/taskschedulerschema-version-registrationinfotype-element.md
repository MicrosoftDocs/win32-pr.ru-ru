---
title: Version (Регистратионинфотипе), элемент
description: Указывает номер версии задачи.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- планировщик задач элемента Version
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb1ae5094ad6f69a61e86da1716169a1b7929e3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681786"
---
# <a name="version-registrationinfotype-element"></a><span data-ttu-id="d3205-104">Version (Регистратионинфотипе), элемент</span><span class="sxs-lookup"><span data-stu-id="d3205-104">Version (registrationInfoType) Element</span></span>

<span data-ttu-id="d3205-105">Указывает номер версии задачи.</span><span class="sxs-lookup"><span data-stu-id="d3205-105">Specifies the version number of the task.</span></span>

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="d3205-106">Элемент **Version** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d3205-106">The **Version** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d3205-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="d3205-107">Parent element</span></span>



| <span data-ttu-id="d3205-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d3205-108">Element</span></span>                                                                           | <span data-ttu-id="d3205-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="d3205-109">Derived from</span></span>                                                                         | <span data-ttu-id="d3205-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d3205-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3205-111">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="d3205-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="d3205-112">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="d3205-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="d3205-113">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="d3205-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d3205-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3205-114">Remarks</span></span>

<span data-ttu-id="d3205-115">Для разработки скриптов версия задачи указывается с помощью свойства [**регистратионинфо. Version**](registrationinfo-version.md) .</span><span class="sxs-lookup"><span data-stu-id="d3205-115">For scripting development, the version of a task is specified using [**RegistrationInfo.Version**](registrationinfo-version.md) property.</span></span>

<span data-ttu-id="d3205-116">Для разработки на C++ версия задачи указывается с помощью свойства [**ирегистратионинфо:: Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) .</span><span class="sxs-lookup"><span data-stu-id="d3205-116">For C++ development, the version of a task is specified using [**IRegistrationInfo::Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) property.</span></span>

## <a name="examples"></a><span data-ttu-id="d3205-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="d3205-117">Examples</span></span>

<span data-ttu-id="d3205-118">Следующий код XML определяет версию задачи.</span><span class="sxs-lookup"><span data-stu-id="d3205-118">The following XML defines the version of a task.</span></span>


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="d3205-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d3205-119">Requirements</span></span>



| <span data-ttu-id="d3205-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d3205-120">Requirement</span></span> | <span data-ttu-id="d3205-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d3205-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3205-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3205-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3205-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3205-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d3205-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3205-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3205-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3205-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3205-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3205-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3205-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="d3205-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d3205-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d3205-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





