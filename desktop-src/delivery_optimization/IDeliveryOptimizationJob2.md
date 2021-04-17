---
title: Интерфейс IDeliveryOptimizationJob2
description: 'Дополнительные сведения о: интерфейс IDeliveryOptimizationJob2'
keywords:
- Интерфейс IDeliveryOptimizationJob2
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710757"
---
# <a name="ideliveryoptimizationjob2-interface"></a><span data-ttu-id="43766-104">Интерфейс IDeliveryOptimizationJob2</span><span class="sxs-lookup"><span data-stu-id="43766-104">IDeliveryOptimizationJob2 interface</span></span>

<span data-ttu-id="43766-105">IDeliveryOptimizationJob2 позволяет добавить один файл в задание загрузки и немедленно получить его.</span><span class="sxs-lookup"><span data-stu-id="43766-105">The IDeliveryOptimizationJob2 enables adding a single file to the download job, and retrieving the file immediately.</span></span> <span data-ttu-id="43766-106">Этот интерфейс также поддерживает настройку и получение дополнительных свойств задания.</span><span class="sxs-lookup"><span data-stu-id="43766-106">This interface also supports setting and getting optional job properties.</span></span>

## <a name="members"></a><span data-ttu-id="43766-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="43766-107">Members</span></span>

<span data-ttu-id="43766-108">Интерфейс **IDeliveryOptimizationJob2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="43766-108">The **IDeliveryOptimizationJob2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="43766-109">**IDeliveryOptimizationJob2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="43766-109">**IDeliveryOptimizationJob2** also has these types of members:</span></span>

- [<span data-ttu-id="43766-110">Методы</span><span class="sxs-lookup"><span data-stu-id="43766-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="43766-111">Методы</span><span class="sxs-lookup"><span data-stu-id="43766-111">Methods</span></span>

<span data-ttu-id="43766-112">Интерфейс **IDeliveryOptimizationJob2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="43766-112">The **IDeliveryOptimizationJob2** interface has these methods.</span></span>

| <span data-ttu-id="43766-113">Метод</span><span class="sxs-lookup"><span data-stu-id="43766-113">Method</span></span>                                              | <span data-ttu-id="43766-114">Описание</span><span class="sxs-lookup"><span data-stu-id="43766-114">Description</span></span>                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="43766-115">**AddFile**</span><span class="sxs-lookup"><span data-stu-id="43766-115">**AddFile**</span></span>](ideliveryoptimizationjob2-addfile.md) | <span data-ttu-id="43766-116">Метод AddFile добавляет один файл к существующему заданию DO.</span><span class="sxs-lookup"><span data-stu-id="43766-116">The AddFile method adds a single file to an existing DO job.</span></span>         |
| [<span data-ttu-id="43766-117">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="43766-117">**GetProperty**</span></span>](ideliveryoptimizationjob2-getproperty.md) | <span data-ttu-id="43766-118">Метод AddFile добавляет один файл к существующему заданию DO.</span><span class="sxs-lookup"><span data-stu-id="43766-118">The AddFile method adds a single file to an existing DO job.</span></span> |
| [<span data-ttu-id="43766-119">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="43766-119">**SetProperty**</span></span>](ideliveryoptimizationjob2-setproperty.md) | <span data-ttu-id="43766-120">Этот метод не используется.</span><span class="sxs-lookup"><span data-stu-id="43766-120">This method is unused.</span></span>                                       |

## <a name="requirements"></a><span data-ttu-id="43766-121">Требования</span><span class="sxs-lookup"><span data-stu-id="43766-121">Requirements</span></span>

| <span data-ttu-id="43766-122">Требование</span><span class="sxs-lookup"><span data-stu-id="43766-122">Requirement</span></span> | <span data-ttu-id="43766-123">Значение</span><span class="sxs-lookup"><span data-stu-id="43766-123">Value</span></span> |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="43766-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43766-124">Minimum supported client</span></span> | <span data-ttu-id="43766-125">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="43766-125">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="43766-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43766-126">Minimum supported server</span></span> | <span data-ttu-id="43766-127">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="43766-127">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="43766-128">Header</span><span class="sxs-lookup"><span data-stu-id="43766-128">Header</span></span>                   | <span data-ttu-id="43766-129">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="43766-129">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="43766-130">IDL</span><span class="sxs-lookup"><span data-stu-id="43766-130">IDL</span></span>                      | <span data-ttu-id="43766-131">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="43766-131">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="43766-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43766-132">Library</span></span>                  | <span data-ttu-id="43766-133">Досвк. lib</span><span class="sxs-lookup"><span data-stu-id="43766-133">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="43766-134">DLL</span><span class="sxs-lookup"><span data-stu-id="43766-134">DLL</span></span>                      | <span data-ttu-id="43766-135">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="43766-135">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="43766-136">IID</span><span class="sxs-lookup"><span data-stu-id="43766-136">IID</span></span>                      | <span data-ttu-id="43766-137">IID_IDeliveryOptimizationJob2 определен как 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="43766-137">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |
