---
title: Интерфейс IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Этот интерфейс используется для запроса или установки нескольких необязательных поведений задания.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Интерфейс IBackgroundCopyJob5
- Интерфейс IBackgroundCopyJob5, описание
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136995"
---
# <a name="ibackgroundcopyjob5-interface"></a><span data-ttu-id="9add9-105">Интерфейс IBackgroundCopyJob5</span><span class="sxs-lookup"><span data-stu-id="9add9-105">IBackgroundCopyJob5 interface</span></span>

<span data-ttu-id="9add9-106">Этот интерфейс используется для запроса или установки нескольких необязательных поведений задания.</span><span class="sxs-lookup"><span data-stu-id="9add9-106">Use this interface to query or set several optional behaviors of a job.</span></span>

<span data-ttu-id="9add9-107">Чтобы получить этот интерфейс, вызовите метод **использованием метода ibackgroundcopyjob:: QueryInterface** , используя в `__uuidof(IBackgroundCopyJob5)` качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9add9-107">To get this interface, call the **IBackgroundCopyJob::QueryInterface** method using `__uuidof(IBackgroundCopyJob5)` as the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="9add9-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="9add9-108">Members</span></span>

<span data-ttu-id="9add9-109">Интерфейс **IBackgroundCopyJob5** наследует от [**использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md).</span><span class="sxs-lookup"><span data-stu-id="9add9-109">The **IBackgroundCopyJob5** interface inherits from [**IBackgroundCopyJob**](ibackgroundcopyjob-.md).</span></span> <span data-ttu-id="9add9-110">**IBackgroundCopyJob5** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9add9-110">**IBackgroundCopyJob5** also has these types of members:</span></span>

-   [<span data-ttu-id="9add9-111">Методы</span><span class="sxs-lookup"><span data-stu-id="9add9-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9add9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="9add9-112">Methods</span></span>

<span data-ttu-id="9add9-113">Интерфейс **IBackgroundCopyJob5** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9add9-113">The **IBackgroundCopyJob5** interface has these methods.</span></span>



| <span data-ttu-id="9add9-114">Метод</span><span class="sxs-lookup"><span data-stu-id="9add9-114">Method</span></span>                                                 | <span data-ttu-id="9add9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9add9-115">Description</span></span>                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="9add9-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="9add9-116">**GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md) | <span data-ttu-id="9add9-117">Универсальный метод для получения свойств задания.</span><span class="sxs-lookup"><span data-stu-id="9add9-117">A generic method for getting DO job properties.</span></span><br/> |
| [<span data-ttu-id="9add9-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="9add9-118">**SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md) | <span data-ttu-id="9add9-119">Универсальный метод для настройки свойств задания.</span><span class="sxs-lookup"><span data-stu-id="9add9-119">A generic method for setting DO job properties.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9add9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9add9-120">Requirements</span></span>



| <span data-ttu-id="9add9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9add9-121">Requirement</span></span> | <span data-ttu-id="9add9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9add9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9add9-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9add9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9add9-124">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="9add9-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9add9-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9add9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9add9-126">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="9add9-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9add9-127">Header</span><span class="sxs-lookup"><span data-stu-id="9add9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9add9-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9add9-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9add9-129">IDL</span><span class="sxs-lookup"><span data-stu-id="9add9-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9add9-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9add9-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9add9-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9add9-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9add9-132"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9add9-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9add9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9add9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9add9-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9add9-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9add9-135">IID</span><span class="sxs-lookup"><span data-stu-id="9add9-135">IID</span></span><br/>                      | <span data-ttu-id="9add9-136">IID_IBackgroundCopyJob5 определяется как E847030C-БББА-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="9add9-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="9add9-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9add9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9add9-138">**Использованием метода ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="9add9-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





