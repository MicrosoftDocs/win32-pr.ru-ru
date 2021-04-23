---
title: Элемент ID (Нетворксеттингстипе)
description: Содержит значение идентификатора GUID, определяющее сетевой профиль.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Элемент ID планировщик задач
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137691"
---
# <a name="id-networksettingstype-element"></a><span data-ttu-id="e5628-104">Элемент ID (Нетворксеттингстипе)</span><span class="sxs-lookup"><span data-stu-id="e5628-104">Id (networkSettingsType) Element</span></span>

<span data-ttu-id="e5628-105">Содержит значение идентификатора GUID, определяющее сетевой профиль.</span><span class="sxs-lookup"><span data-stu-id="e5628-105">Contains a GUID value that identifies a network profile.</span></span>

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

<span data-ttu-id="e5628-106">Элемент **ID** определяется сложным типом [**нетворксеттингстипе**](taskschedulerschema-networksettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e5628-106">The **Id** element is defined by the [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e5628-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e5628-107">Parent element</span></span>



| <span data-ttu-id="e5628-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="e5628-108">Element</span></span>                                                                                            | <span data-ttu-id="e5628-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="e5628-109">Derived from</span></span>                                                                       | <span data-ttu-id="e5628-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e5628-110">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5628-111">**Нетворксеттингс (Сеттингстипе)**</span><span class="sxs-lookup"><span data-stu-id="e5628-111">**NetworkSettings (settingsType)**</span></span>](taskschedulerschema-networksettings-settingstype-element.md) | [<span data-ttu-id="e5628-112">**нетворксеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="e5628-112">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md) | <span data-ttu-id="e5628-113">Содержит параметры, используемые службой планировщик задач для получения сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="e5628-113">Contains the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="e5628-114">Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="e5628-114">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e5628-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5628-115">Remarks</span></span>

<span data-ttu-id="e5628-116">Сведения о разработке на языке C++ см. в разделе [**свойство ID объекта инетворксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span><span class="sxs-lookup"><span data-stu-id="e5628-116">For C++ development, see [**Id Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).</span></span>

<span data-ttu-id="e5628-117">Сведения о разработке сценариев см. в разделе [**NetworkSettings.ID**](networksettings-id.md).</span><span class="sxs-lookup"><span data-stu-id="e5628-117">For script development, see [**NetworkSettings.Id**](networksettings-id.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5628-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e5628-118">Requirements</span></span>



| <span data-ttu-id="e5628-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e5628-119">Requirement</span></span> | <span data-ttu-id="e5628-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e5628-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e5628-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5628-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e5628-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5628-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e5628-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5628-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e5628-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5628-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





