---
title: Рестартонидле (Идлесеттингстипе), элемент
description: Указывает, перезапускается ли задача, когда компьютер циклически перегружается в состояние простоя.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- планировщик задач элемента Рестартонидле
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682130"
---
# <a name="restartonidle-idlesettingstype-element"></a><span data-ttu-id="bc557-104">Рестартонидле (Идлесеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="bc557-104">RestartOnIdle (idleSettingsType) Element</span></span>

<span data-ttu-id="bc557-105">Указывает, перезапускается ли задача, когда компьютер циклически перегружается в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="bc557-105">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="bc557-106">Элемент **рестартонидле** определяется сложным типом [**идлесеттингстипе**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bc557-106">The **RestartOnIdle** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bc557-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="bc557-107">Parent element</span></span>



| <span data-ttu-id="bc557-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="bc557-108">Element</span></span>                                                                       | <span data-ttu-id="bc557-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="bc557-109">Derived from</span></span>                                                                 | <span data-ttu-id="bc557-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bc557-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc557-111">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="bc557-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="bc557-112">**идлесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="bc557-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="bc557-113">Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="bc557-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bc557-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc557-114">Remarks</span></span>

<span data-ttu-id="bc557-115">Этот элемент используется только в том случае, если для элемента [**терминатеонидлинд**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) задано значение true.</span><span class="sxs-lookup"><span data-stu-id="bc557-115">This element is used only if the [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element is set to True.</span></span>

<span data-ttu-id="bc557-116">Для разработки скриптов эти параметры задач указываются с помощью свойства [**идлесеттингс. рестартонидле**](idlesettings-restartonidle.md) .</span><span class="sxs-lookup"><span data-stu-id="bc557-116">For script development, this task settings is specified using the [**IdleSettings.RestartOnIdle**](idlesettings-restartonidle.md) property.</span></span>

<span data-ttu-id="bc557-117">Для разработки на C++ эти параметры задачи указываются с помощью свойства [**иидлесеттингс:: рестартонидле**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .</span><span class="sxs-lookup"><span data-stu-id="bc557-117">For C++ development, this task settings is specified using the [**IIdleSettings::RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) property.</span></span>

## <a name="examples"></a><span data-ttu-id="bc557-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="bc557-118">Examples</span></span>

<span data-ttu-id="bc557-119">Следующий XML-код определяет параметр простоя, который указывает, что задачу не следует перезапускать при цикле условия простоя.</span><span class="sxs-lookup"><span data-stu-id="bc557-119">The following XML defines an idle setting that indicates that the task should not be restarted when the idle condition cycles.</span></span>


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="bc557-120">Требования</span><span class="sxs-lookup"><span data-stu-id="bc557-120">Requirements</span></span>



| <span data-ttu-id="bc557-121">Требование</span><span class="sxs-lookup"><span data-stu-id="bc557-121">Requirement</span></span> | <span data-ttu-id="bc557-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bc557-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc557-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc557-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc557-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc557-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bc557-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc557-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc557-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc557-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc557-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc557-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc557-128">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="bc557-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bc557-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="bc557-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





