---
title: Интерфейс IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 поддерживает настройку и получение необязательных свойств файла.
keywords:
- Интерфейс IDeliveryOptimizationFile2
- Интерфейс IDeliveryOptimizationFile2, описание
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071393"
---
# <a name="ideliveryoptimizationfile2-interface"></a><span data-ttu-id="98257-105">Интерфейс IDeliveryOptimizationFile2</span><span class="sxs-lookup"><span data-stu-id="98257-105">IDeliveryOptimizationFile2 interface</span></span>

<span data-ttu-id="98257-106">**IDeliveryOptimizationFile2** поддерживает настройку и получение необязательных свойств файла.</span><span class="sxs-lookup"><span data-stu-id="98257-106">The **IDeliveryOptimizationFile2** supports setting and getting optional file properties.</span></span> 

## <a name="members"></a><span data-ttu-id="98257-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="98257-107">Members</span></span>

<span data-ttu-id="98257-108">Интерфейс **IDeliveryOptimizationFile2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="98257-108">The **IDeliveryOptimizationFile2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="98257-109">**IDeliveryOptimizationFile2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="98257-109">**IDeliveryOptimizationFile2** also has these types of members:</span></span>

- [<span data-ttu-id="98257-110">Методы</span><span class="sxs-lookup"><span data-stu-id="98257-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="98257-111">Методы</span><span class="sxs-lookup"><span data-stu-id="98257-111">Methods</span></span>

<span data-ttu-id="98257-112">Интерфейс **IDeliveryOptimizationFile2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="98257-112">The **IDeliveryOptimizationFile2** interface has these methods.</span></span>

| <span data-ttu-id="98257-113">Метод</span><span class="sxs-lookup"><span data-stu-id="98257-113">Method</span></span>                                                 | <span data-ttu-id="98257-114">Описание</span><span class="sxs-lookup"><span data-stu-id="98257-114">Description</span></span>                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="98257-115">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="98257-115">**GetProperty**</span></span>](ideliveryoptimizationfile2-getproperty.md)  | <span data-ttu-id="98257-116">Этот метод возвращает одно свойство файла DO.</span><span class="sxs-lookup"><span data-stu-id="98257-116">This method returns a single property of the DO file.</span></span> |
| [<span data-ttu-id="98257-117">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="98257-117">**SetProperty**</span></span>](ideliveryoptimizationfile2-setproperty.md)  | <span data-ttu-id="98257-118">Этот метод задает одно свойство для файла DO.</span><span class="sxs-lookup"><span data-stu-id="98257-118">This method sets a single property of the DO file.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="98257-119">Требования</span><span class="sxs-lookup"><span data-stu-id="98257-119">Requirements</span></span>

| <span data-ttu-id="98257-120">Требование</span><span class="sxs-lookup"><span data-stu-id="98257-120">Requirement</span></span> | <span data-ttu-id="98257-121">Значение</span><span class="sxs-lookup"><span data-stu-id="98257-121">Value</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="98257-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98257-122">Minimum supported client</span></span>      | <span data-ttu-id="98257-123">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="98257-123">Windows 10, version 1803 \[desktop apps only\]</span></span>                                    |
| <span data-ttu-id="98257-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98257-124">Minimum supported server</span></span>      | <span data-ttu-id="98257-125">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="98257-125">Windows Server, version 1709 \[desktop apps only\]</span></span>                                |
| <span data-ttu-id="98257-126">Header</span><span class="sxs-lookup"><span data-stu-id="98257-126">Header</span></span>                        | <span data-ttu-id="98257-127">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="98257-127">Deliveryoptimization.h</span></span>                                                            |
| <span data-ttu-id="98257-128">IDL</span><span class="sxs-lookup"><span data-stu-id="98257-128">IDL</span></span>                           | <span data-ttu-id="98257-129">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="98257-129">DeliveryOptimization.idl</span></span>                                                          |
| <span data-ttu-id="98257-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="98257-130">Library</span></span>                       | <span data-ttu-id="98257-131">Досвк. lib</span><span class="sxs-lookup"><span data-stu-id="98257-131">Dosvc.lib</span></span>                                                                         |
| <span data-ttu-id="98257-132">DLL</span><span class="sxs-lookup"><span data-stu-id="98257-132">DLL</span></span>                           | <span data-ttu-id="98257-133">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="98257-133">Dosvc.dll</span></span>                                                                         |
| <span data-ttu-id="98257-134">IID</span><span class="sxs-lookup"><span data-stu-id="98257-134">IID</span></span>                           | <span data-ttu-id="98257-135">IID_IDeliveryOptimizationFile2 определен как 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span><span class="sxs-lookup"><span data-stu-id="98257-135">IID_IDeliveryOptimizationFile2 is defined as 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span></span> |
