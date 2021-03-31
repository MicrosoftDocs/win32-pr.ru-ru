---
title: Нетворксеттингс (Сеттингстипе), элемент
description: Содержит параметры, используемые службой планировщик задач для получения сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента Рунонлифнетворкаваилабле задано значение true.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- планировщик задач элемента Нетворксеттингс
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7861d91cbc2647d241bc41753efbebcc346759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491355"
---
# <a name="networksettings-settingstype-element"></a><span data-ttu-id="a6ad6-105">Нетворксеттингс (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="a6ad6-105">NetworkSettings (settingsType) Element</span></span>

<span data-ttu-id="a6ad6-106">Содержит параметры, используемые службой планировщик задач для получения сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-106">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="a6ad6-107">Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-107">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span>

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="a6ad6-108">Элемент **нетворксеттингс** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a6ad6-108">The **NetworkSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a6ad6-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a6ad6-109">Parent element</span></span>



| <span data-ttu-id="a6ad6-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="a6ad6-110">Element</span></span>                                                                      | <span data-ttu-id="a6ad6-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="a6ad6-111">Derived from</span></span>                                                         | <span data-ttu-id="a6ad6-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a6ad6-112">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6ad6-113">**Параметры (taskType)**</span><span class="sxs-lookup"><span data-stu-id="a6ad6-113">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="a6ad6-114">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="a6ad6-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="a6ad6-115">Задает параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="a6ad6-115">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a6ad6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6ad6-116">Remarks</span></span>

<span data-ttu-id="a6ad6-117">Сведения о разработке на языке C++ см. в разделе [**свойство нетворксеттингс объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span><span class="sxs-lookup"><span data-stu-id="a6ad6-117">For C++ development, see [**NetworkSettings Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).</span></span>

<span data-ttu-id="a6ad6-118">Сведения о разработке сценариев см. в разделе [**тасксеттингс. нетворксеттингс**](tasksettings-networksettings.md).</span><span class="sxs-lookup"><span data-stu-id="a6ad6-118">For script development, see [**TaskSettings.NetworkSettings**](tasksettings-networksettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ad6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a6ad6-119">Requirements</span></span>



| <span data-ttu-id="a6ad6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a6ad6-120">Requirement</span></span> | <span data-ttu-id="a6ad6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a6ad6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a6ad6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6ad6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ad6-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6ad6-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a6ad6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6ad6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ad6-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6ad6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





