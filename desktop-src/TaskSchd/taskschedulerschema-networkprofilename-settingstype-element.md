---
title: Нетворкпрофиленаме (Сеттингстипе), элемент
description: Содержит имя сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента Рунонлифнетворкаваилабле задано значение true. Имя используется в целях показа.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- планировщик задач элемента Нетворкпрофиленаме
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802770"
---
# <a name="networkprofilename-settingstype-element"></a><span data-ttu-id="7757c-106">Нетворкпрофиленаме (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="7757c-106">NetworkProfileName (settingsType) Element</span></span>

<span data-ttu-id="7757c-107">Содержит имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="7757c-107">Contains the name of a network profile.</span></span> <span data-ttu-id="7757c-108">Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="7757c-108">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="7757c-109">Имя используется в целях показа.</span><span class="sxs-lookup"><span data-stu-id="7757c-109">The name is used for display purposes.</span></span>

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="7757c-110">Элемент **нетворкпрофиленаме** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7757c-110">The **NetworkProfileName** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7757c-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="7757c-111">Parent element</span></span>



| <span data-ttu-id="7757c-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="7757c-112">Element</span></span>                                                                      | <span data-ttu-id="7757c-113">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="7757c-113">Derived from</span></span>                                                         | <span data-ttu-id="7757c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7757c-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="7757c-115">**Параметры (taskType)**</span><span class="sxs-lookup"><span data-stu-id="7757c-115">**Settings (taskType)**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="7757c-116">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="7757c-116">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="7757c-117">Задает параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="7757c-117">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7757c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7757c-118">Requirements</span></span>



| <span data-ttu-id="7757c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7757c-119">Requirement</span></span> | <span data-ttu-id="7757c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7757c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7757c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7757c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7757c-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7757c-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7757c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7757c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7757c-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7757c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





