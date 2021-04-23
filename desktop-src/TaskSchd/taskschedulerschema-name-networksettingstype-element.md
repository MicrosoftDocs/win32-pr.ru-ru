---
title: Элемент Name (Нетворксеттингстипе)
description: Содержит имя сетевого профиля. Имя используется в целях показа.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Элемент Name планировщик задач
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534457"
---
# <a name="name-networksettingstype-element"></a><span data-ttu-id="bcfb0-105">Элемент Name (Нетворксеттингстипе)</span><span class="sxs-lookup"><span data-stu-id="bcfb0-105">Name (networkSettingsType) Element</span></span>

<span data-ttu-id="bcfb0-106">Содержит имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-106">Contains the name of a network profile.</span></span> <span data-ttu-id="bcfb0-107">Имя используется в целях показа.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-107">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

<span data-ttu-id="bcfb0-108">Элемент **Name** определяется сложным типом [**нетворксеттингстипе**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bcfb0-108">The **Name** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bcfb0-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="bcfb0-109">Parent element</span></span>



| <span data-ttu-id="bcfb0-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="bcfb0-110">Element</span></span>                                                                                            | <span data-ttu-id="bcfb0-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="bcfb0-111">Derived from</span></span>                                                                       | <span data-ttu-id="bcfb0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="bcfb0-112">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcfb0-113">**Нетворксеттингс (Сеттингстипе)**</span><span class="sxs-lookup"><span data-stu-id="bcfb0-113">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="bcfb0-114">**нетворксеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="bcfb0-114">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="bcfb0-115">Содержит параметры, используемые службой планировщик задач для получения сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-115">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="bcfb0-116">Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="bcfb0-116">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bcfb0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bcfb0-117">Remarks</span></span>

<span data-ttu-id="bcfb0-118">Сведения о разработке на языке C++ см. в разделе [**свойство Name объекта инетворксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span><span class="sxs-lookup"><span data-stu-id="bcfb0-118">For C++ development, see [**Name Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).</span></span>

<span data-ttu-id="bcfb0-119">Сведения о разработке сценариев см. в разделе [**NetworkSettings.Name**](networksettings-name.md).</span><span class="sxs-lookup"><span data-stu-id="bcfb0-119">For script development, see [**NetworkSettings.Name**](networksettings-name.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcfb0-120">Требования</span><span class="sxs-lookup"><span data-stu-id="bcfb0-120">Requirements</span></span>



| <span data-ttu-id="bcfb0-121">Требование</span><span class="sxs-lookup"><span data-stu-id="bcfb0-121">Requirement</span></span> | <span data-ttu-id="bcfb0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bcfb0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bcfb0-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcfb0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bcfb0-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcfb0-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bcfb0-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcfb0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bcfb0-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bcfb0-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





