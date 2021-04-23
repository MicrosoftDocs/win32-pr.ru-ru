---
title: Интерфейс Ибаккграундкопиманажер (Deliveryoptimization. h)
description: Создает задания перемещения, извлекает объект перечислителя, содержащий задания в очереди, и получает отдельные задания из очереди.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Интерфейс Ибаккграундкопиманажер
- Интерфейс Ибаккграундкопиманажер, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988777"
---
# <a name="ibackgroundcopymanager-interface"></a><span data-ttu-id="a7603-105">Интерфейс Ибаккграундкопиманажер</span><span class="sxs-lookup"><span data-stu-id="a7603-105">IBackgroundCopyManager interface</span></span>

<span data-ttu-id="a7603-106">Создает задания перемещения, извлекает объект перечислителя, содержащий задания в очереди, и получает отдельные задания из очереди.</span><span class="sxs-lookup"><span data-stu-id="a7603-106">Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.</span></span>

## <a name="members"></a><span data-ttu-id="a7603-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="a7603-107">Members</span></span>

<span data-ttu-id="a7603-108">Интерфейс **ибаккграундкопиманажер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a7603-108">The **IBackgroundCopyManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a7603-109">**Ибаккграундкопиманажер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a7603-109">**IBackgroundCopyManager** also has these types of members:</span></span>

-   [<span data-ttu-id="a7603-110">Методы</span><span class="sxs-lookup"><span data-stu-id="a7603-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a7603-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a7603-111">Methods</span></span>

<span data-ttu-id="a7603-112">Интерфейс **ибаккграундкопиманажер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a7603-112">The **IBackgroundCopyManager** interface has these methods.</span></span>



| <span data-ttu-id="a7603-113">Метод</span><span class="sxs-lookup"><span data-stu-id="a7603-113">Method</span></span>                                                | <span data-ttu-id="a7603-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a7603-114">Description</span></span>                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="a7603-115">**CreateJob**</span><span class="sxs-lookup"><span data-stu-id="a7603-115">**CreateJob**</span></span>](ibackgroundcopymanager-createjob.md) | <span data-ttu-id="a7603-116">Создает задание перемещения.</span><span class="sxs-lookup"><span data-stu-id="a7603-116">Creates a transfer job.</span></span><br/>                   |
| [<span data-ttu-id="a7603-117">**жетжоб**</span><span class="sxs-lookup"><span data-stu-id="a7603-117">**GetJob**</span></span>](ibackgroundcopymanager-getjob.md)       | <span data-ttu-id="a7603-118">Извлекает указанное задание из очереди.</span><span class="sxs-lookup"><span data-stu-id="a7603-118">Retrieves a specified job from the queue.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a7603-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a7603-119">Requirements</span></span>



| <span data-ttu-id="a7603-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a7603-120">Requirement</span></span> | <span data-ttu-id="a7603-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a7603-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7603-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7603-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a7603-123">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a7603-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a7603-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7603-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a7603-125">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a7603-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a7603-126">Header</span><span class="sxs-lookup"><span data-stu-id="a7603-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7603-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7603-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7603-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a7603-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7603-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7603-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a7603-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7603-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7603-131"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7603-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a7603-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a7603-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7603-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7603-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a7603-134">IID</span><span class="sxs-lookup"><span data-stu-id="a7603-134">IID</span></span><br/>                      | <span data-ttu-id="a7603-135">IID_IBackgroundCopyManager определен как 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="a7603-135">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a7603-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7603-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7603-137">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="a7603-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

