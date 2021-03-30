---
title: Тасксеттингс. Нетворксеттингс, свойство
description: Для создания скриптов Возвращает или задает объект параметров сети, который содержит идентификатор и имя сетевого профиля.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- планировщик задач свойства Нетворксеттингс
- Планировщик задач свойства Нетворксеттингс, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Нетворксеттингс
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801469"
---
# <a name="tasksettingsnetworksettings-property"></a><span data-ttu-id="fc987-106">Тасксеттингс. Нетворксеттингс, свойство</span><span class="sxs-lookup"><span data-stu-id="fc987-106">TaskSettings.NetworkSettings property</span></span>

<span data-ttu-id="fc987-107">Для создания скриптов Возвращает или задает объект параметров сети, который содержит идентификатор и имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="fc987-107">For scripting, gets or sets the network settings object that contains a network profile identifier and name.</span></span> <span data-ttu-id="fc987-108">Если свойство [**рунонлифнетворкаваилабле**](tasksettings-runonlyifnetworkavailable.md) объекта [**Тасксеттингс**](tasksettings.md) имеет **значение true** и в свойстве **нетворксеттингс** указан сетевой пропфиле, задача будет запущена только в том случае, если доступен указанный сетевой профиль.</span><span class="sxs-lookup"><span data-stu-id="fc987-108">If the [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) property of [**TaskSettings**](tasksettings.md) is **True** and a network propfile is specified in the **NetworkSettings** property, then the task will run only if the specified network profile is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc987-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc987-109">Syntax</span></span>


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a><span data-ttu-id="fc987-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fc987-110">Property value</span></span>

<span data-ttu-id="fc987-111">Объект [**нетворксеттингс**](networksettings.md) , содержащий идентификатор и имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="fc987-111">A [**NetworkSettings**](networksettings.md) object that contains a network profile identifier and name.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc987-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fc987-112">Requirements</span></span>



| <span data-ttu-id="fc987-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fc987-113">Requirement</span></span> | <span data-ttu-id="fc987-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fc987-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc987-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc987-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fc987-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc987-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fc987-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc987-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fc987-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc987-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc987-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fc987-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc987-120"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fc987-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fc987-121">DLL</span><span class="sxs-lookup"><span data-stu-id="fc987-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc987-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc987-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc987-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc987-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc987-124">**тасксеттингс**</span><span class="sxs-lookup"><span data-stu-id="fc987-124">**TaskSettings**</span></span>](tasksettings.md)
</dt> <dt>

[<span data-ttu-id="fc987-125">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="fc987-125">**NetworkSettings**</span></span>](networksettings.md)
</dt> </dl>

 

 





