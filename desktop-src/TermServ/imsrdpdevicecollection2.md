---
title: Интерфейс IMsRdpDeviceCollection2
description: Представляет коллекцию объектов Device. Это усовершенствование интерфейса Имсрдпдевицеколлектион.
ms.assetid: df4d704c-e031-4df1-aed1-11aacf8a6992
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpDeviceCollection2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceCollection2, описание
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea35c0a66ad8bf5d291062eafb7be3ceae4ac58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681972"
---
# <a name="imsrdpdevicecollection2-interface"></a><span data-ttu-id="ddddd-106">Интерфейс IMsRdpDeviceCollection2</span><span class="sxs-lookup"><span data-stu-id="ddddd-106">IMsRdpDeviceCollection2 interface</span></span>

<span data-ttu-id="ddddd-107">Представляет коллекцию объектов Device.</span><span class="sxs-lookup"><span data-stu-id="ddddd-107">Represents a collection of device objects.</span></span> <span data-ttu-id="ddddd-108">Это усовершенствование интерфейса [**имсрдпдевицеколлектион**](imsrdpdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ddddd-108">This is an enhancement to the [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="ddddd-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="ddddd-109">Members</span></span>

<span data-ttu-id="ddddd-110">Интерфейс **IMsRdpDeviceCollection2** наследует от [**имсрдпдевицеколлектион**](imsrdpdevicecollection.md).</span><span class="sxs-lookup"><span data-stu-id="ddddd-110">The **IMsRdpDeviceCollection2** interface inherits from [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span></span> <span data-ttu-id="ddddd-111">**IMsRdpDeviceCollection2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ddddd-111">**IMsRdpDeviceCollection2** also has these types of members:</span></span>

-   [<span data-ttu-id="ddddd-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ddddd-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ddddd-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ddddd-113">Methods</span></span>

<span data-ttu-id="ddddd-114">Интерфейс **IMsRdpDeviceCollection2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ddddd-114">The **IMsRdpDeviceCollection2** interface has these methods.</span></span>



| <span data-ttu-id="ddddd-115">Метод</span><span class="sxs-lookup"><span data-stu-id="ddddd-115">Method</span></span>                                                                         | <span data-ttu-id="ddddd-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ddddd-116">Description</span></span>                                                                                                 |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddddd-117">**адддевицебинстанцеид**</span><span class="sxs-lookup"><span data-stu-id="ddddd-117">**AddDeviceByInstanceId**</span></span>](imsrdpdevicecollection2-adddevicebyinstanceid.md) | <span data-ttu-id="ddddd-118">Добавляет устройство, не имеющее список, в коллекцию устройств.</span><span class="sxs-lookup"><span data-stu-id="ddddd-118">Adds an unlisted device to the device collection.</span></span><br/>                                                |
| [<span data-ttu-id="ddddd-119">**редиректнов**</span><span class="sxs-lookup"><span data-stu-id="ddddd-119">**RedirectNow**</span></span>](imsrdpdevicecollection2-redirectnow.md)                     | <span data-ttu-id="ddddd-120">Принудительное перенаправление или удаление устройств, которые были выбраны или отменены из коллекции.</span><span class="sxs-lookup"><span data-stu-id="ddddd-120">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ddddd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ddddd-121">Requirements</span></span>



| <span data-ttu-id="ddddd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ddddd-122">Requirement</span></span> | <span data-ttu-id="ddddd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ddddd-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddddd-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddddd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ddddd-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ddddd-125">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="ddddd-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddddd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ddddd-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ddddd-127">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="ddddd-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ddddd-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="ddddd-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddddd-129"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="ddddd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ddddd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddddd-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddddd-131"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="ddddd-132">IID</span><span class="sxs-lookup"><span data-stu-id="ddddd-132">IID</span></span><br/>                      | <span data-ttu-id="ddddd-133">IID \_ IMsRdpDeviceCollection2 определен как e0e5d68a-f2e7-4350-adfe-ac0e08d74de0</span><span class="sxs-lookup"><span data-stu-id="ddddd-133">IID\_IMsRdpDeviceCollection2 is defined as e0e5d68a-f2e7-4350-adfe-ac0e08d74de0</span></span><br/> |



 

 





