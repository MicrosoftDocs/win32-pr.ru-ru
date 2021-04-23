---
title: Hidden (Сеттингстипе), элемент
description: Указывает, что задача не будет отображаться в пользовательском интерфейсе по умолчанию.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- планировщик задач скрытого элемента
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672903"
---
# <a name="hidden-settingstype-element"></a><span data-ttu-id="a541f-104">Hidden (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="a541f-104">Hidden (settingsType) Element</span></span>

<span data-ttu-id="a541f-105">Указывает, что задача не будет отображаться в пользовательском интерфейсе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a541f-105">Specifies that the task will not be visible in the UI by default.</span></span> <span data-ttu-id="a541f-106">Однако администраторы могут переопределить этот параметр с помощью "главного коммутатора", который делает все задачи видимыми в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="a541f-106">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="a541f-107">**Скрытый** элемент определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a541f-107">The **Hidden** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a541f-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a541f-108">Parent element</span></span>



| <span data-ttu-id="a541f-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="a541f-109">Element</span></span>                                                           | <span data-ttu-id="a541f-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="a541f-110">Derived from</span></span>                                                         | <span data-ttu-id="a541f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a541f-111">Description</span></span>                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="a541f-112">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="a541f-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="a541f-113">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="a541f-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="a541f-114">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="a541f-114">Contains the settings that Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a541f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a541f-115">Remarks</span></span>

<span data-ttu-id="a541f-116">Сведения о разработке с + + см. в разделе [**свойство Hidden объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span><span class="sxs-lookup"><span data-stu-id="a541f-116">For C++ development, see [**Hidden Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span></span>

<span data-ttu-id="a541f-117">Сведения о разработке сценариев см. в разделе [**тасксеттингс. Hidden**](tasksettings-hidden.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-117">For script development, see [**TaskSettings.Hidden**](tasksettings-hidden.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a541f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a541f-118">Requirements</span></span>



| <span data-ttu-id="a541f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a541f-119">Requirement</span></span> | <span data-ttu-id="a541f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a541f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a541f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a541f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a541f-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a541f-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a541f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a541f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a541f-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a541f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a541f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a541f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a541f-126">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="a541f-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





