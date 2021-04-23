---
title: Author (Регистратионинфотипе), элемент
description: Указывает автора задачи.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Элемент Author планировщик задач
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988873"
---
# <a name="author-registrationinfotype-element"></a><span data-ttu-id="c1695-104">Author (Регистратионинфотипе), элемент</span><span class="sxs-lookup"><span data-stu-id="c1695-104">Author (registrationInfoType) Element</span></span>

<span data-ttu-id="c1695-105">Указывает автора задачи.</span><span class="sxs-lookup"><span data-stu-id="c1695-105">Specifies the author of the task.</span></span>

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="c1695-106">Элемент **Author** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c1695-106">The **Author** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c1695-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c1695-107">Parent element</span></span>



| <span data-ttu-id="c1695-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="c1695-108">Element</span></span>                                                                           | <span data-ttu-id="c1695-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="c1695-109">Derived from</span></span>                                                                         | <span data-ttu-id="c1695-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c1695-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1695-111">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="c1695-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="c1695-112">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="c1695-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="c1695-113">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="c1695-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c1695-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1695-114">Remarks</span></span>

<span data-ttu-id="c1695-115">Для разработки сценариев автор задачи указывается с помощью свойства [**регистратионинфо. Author**](registrationinfo-author.md) .</span><span class="sxs-lookup"><span data-stu-id="c1695-115">For scripting development, the author of the task is specified using the [**RegistrationInfo.Author**](registrationinfo-author.md) property.</span></span>

<span data-ttu-id="c1695-116">Для разработки на C++ автор задачи указывается с помощью свойства [**ирегистратионинфо:: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) .</span><span class="sxs-lookup"><span data-stu-id="c1695-116">For C++ development, the author of the task is specified using the [**IRegistrationInfo::Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c1695-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="c1695-117">Examples</span></span>

<span data-ttu-id="c1695-118">Следующий XML-код определяет автора задачи.</span><span class="sxs-lookup"><span data-stu-id="c1695-118">The following XML defines the author of a task.</span></span>


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="c1695-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c1695-119">Requirements</span></span>



| <span data-ttu-id="c1695-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c1695-120">Requirement</span></span> | <span data-ttu-id="c1695-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c1695-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1695-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1695-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c1695-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1695-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1695-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1695-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c1695-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1695-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1695-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1695-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1695-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="c1695-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c1695-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="c1695-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





