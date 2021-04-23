---
title: Интерфейс Иделиверйоптимизатионфиле
description: Реализуйте интерфейс Иделиверйоптимизатионфиле, чтобы узнать состояние определенного файла.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Интерфейс Иделиверйоптимизатионфиле
- Интерфейс Иделиверйоптимизатионфиле, описание
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710475"
---
# <a name="ideliveryoptimizationfile-interface"></a><span data-ttu-id="2ef6c-105">Интерфейс Иделиверйоптимизатионфиле</span><span class="sxs-lookup"><span data-stu-id="2ef6c-105">IDeliveryOptimizationFile interface</span></span>

<span data-ttu-id="2ef6c-106">Реализуйте интерфейс **иделиверйоптимизатионфиле** , чтобы узнать состояние определенного файла.</span><span class="sxs-lookup"><span data-stu-id="2ef6c-106">Implement the **IDeliveryOptimizationFile** interface to identify the status of a specific file.</span></span>

## <a name="members"></a><span data-ttu-id="2ef6c-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="2ef6c-107">Members</span></span>

<span data-ttu-id="2ef6c-108">Интерфейс **иделиверйоптимизатионфиле** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2ef6c-108">The **IDeliveryOptimizationFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2ef6c-109">**Иделиверйоптимизатионфиле** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2ef6c-109">**IDeliveryOptimizationFile** also has these types of members:</span></span>

-   [<span data-ttu-id="2ef6c-110">Методы</span><span class="sxs-lookup"><span data-stu-id="2ef6c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2ef6c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="2ef6c-111">Methods</span></span>

<span data-ttu-id="2ef6c-112">Интерфейс **иделиверйоптимизатионфиле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2ef6c-112">The **IDeliveryOptimizationFile** interface has these methods.</span></span>



| <span data-ttu-id="2ef6c-113">Метод</span><span class="sxs-lookup"><span data-stu-id="2ef6c-113">Method</span></span>                                                 | <span data-ttu-id="2ef6c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2ef6c-114">Description</span></span>                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="2ef6c-115">**GetStats**</span><span class="sxs-lookup"><span data-stu-id="2ef6c-115">**GetStats**</span></span>](ideliveryoptimizationfile-getstats.md) | <span data-ttu-id="2ef6c-116">Возвращает статистику загрузки и передачи для указанного файла.</span><span class="sxs-lookup"><span data-stu-id="2ef6c-116">Returns download and upload stats for a specific file.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="2ef6c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2ef6c-117">Requirements</span></span>

| <span data-ttu-id="2ef6c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2ef6c-118">Requirement</span></span> | <span data-ttu-id="2ef6c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2ef6c-119">Value</span></span> |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2ef6c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ef6c-120">Minimum supported client</span></span>      | <span data-ttu-id="2ef6c-121">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="2ef6c-121">Windows 10, version 1709 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="2ef6c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ef6c-122">Minimum supported server</span></span>      | <span data-ttu-id="2ef6c-123">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="2ef6c-123">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="2ef6c-124">Header</span><span class="sxs-lookup"><span data-stu-id="2ef6c-124">Header</span></span>                        | <span data-ttu-id="2ef6c-125">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="2ef6c-125">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="2ef6c-126">IDL</span><span class="sxs-lookup"><span data-stu-id="2ef6c-126">IDL</span></span>                           | <span data-ttu-id="2ef6c-127">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="2ef6c-127">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="2ef6c-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ef6c-128">Library</span></span>                       | <span data-ttu-id="2ef6c-129">Досвк. lib</span><span class="sxs-lookup"><span data-stu-id="2ef6c-129">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="2ef6c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2ef6c-130">DLL</span></span>                           | <span data-ttu-id="2ef6c-131">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="2ef6c-131">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="2ef6c-132">IID</span><span class="sxs-lookup"><span data-stu-id="2ef6c-132">IID</span></span>                           | <span data-ttu-id="2ef6c-133">IID_IDeliveryOptimizationFile определен как B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="2ef6c-133">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span> |
