---
title: Элемент Documentation (Регистратионинфотипе)
description: Указывает любую дополнительную документацию для задачи.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Элемент Documentation планировщик задач
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682136"
---
# <a name="documentation-registrationinfotype-element"></a><span data-ttu-id="3a64f-104">Элемент Documentation (Регистратионинфотипе)</span><span class="sxs-lookup"><span data-stu-id="3a64f-104">Documentation (registrationInfoType) Element</span></span>

<span data-ttu-id="3a64f-105">Указывает любую дополнительную документацию для задачи.</span><span class="sxs-lookup"><span data-stu-id="3a64f-105">Specifies any additional documentation for the task.</span></span>

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="3a64f-106">Элемент **Documentation** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3a64f-106">The **Documentation** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3a64f-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="3a64f-107">Parent element</span></span>



| <span data-ttu-id="3a64f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="3a64f-108">Element</span></span>                                                                           | <span data-ttu-id="3a64f-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="3a64f-109">Derived from</span></span>                                                                         | <span data-ttu-id="3a64f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3a64f-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a64f-111">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="3a64f-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="3a64f-112">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="3a64f-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="3a64f-113">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="3a64f-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3a64f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a64f-114">Remarks</span></span>

<span data-ttu-id="3a64f-115">Для приложений со скриптами дополнительная документация по задачам указывается с помощью свойства [**RegistrationInfo.Docументатион**](registrationinfo-documentation.md) .</span><span class="sxs-lookup"><span data-stu-id="3a64f-115">For scripting applications, additional task documentation is specified using the using the [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) property.</span></span>

<span data-ttu-id="3a64f-116">Для приложений C++ Дополнительная документация по задачам указывается с помощью свойства [**ирегистратионинфо::D kumentace**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) .</span><span class="sxs-lookup"><span data-stu-id="3a64f-116">For C++ applications, additional task documentation is specified using the using the [**IRegistrationInfo::Documentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a64f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3a64f-117">Requirements</span></span>



| <span data-ttu-id="3a64f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3a64f-118">Requirement</span></span> | <span data-ttu-id="3a64f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3a64f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a64f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a64f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a64f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a64f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a64f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a64f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a64f-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a64f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a64f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a64f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a64f-125">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="3a64f-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





