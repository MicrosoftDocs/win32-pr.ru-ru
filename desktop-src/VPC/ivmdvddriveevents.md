---
title: Интерфейс Ивмдвддрививентс (Впккоминтерфацес. h)
description: Определяет интерфейс исходящего события для интерфейса Ивмдвддриве.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Виртуальный ПК с интерфейсом Ивмдвддрививентс
- Ивмдвддрививентс интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492903"
---
# <a name="ivmdvddriveevents-interface"></a><span data-ttu-id="e6755-105">Интерфейс Ивмдвддрививентс</span><span class="sxs-lookup"><span data-stu-id="e6755-105">IVMDVDDriveEvents interface</span></span>

<span data-ttu-id="e6755-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6755-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e6755-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e6755-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e6755-108">Определяет интерфейс исходящего события для интерфейса [**ивмдвддриве**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="e6755-108">Defines the outgoing event interface for the [**IVMDVDDrive**](ivmdvddrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="e6755-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="e6755-109">Members</span></span>

<span data-ttu-id="e6755-110">Интерфейс **ивмдвддрививентс** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e6755-110">The **IVMDVDDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e6755-111">**Ивмдвддрививентс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e6755-111">**IVMDVDDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="e6755-112">Методы</span><span class="sxs-lookup"><span data-stu-id="e6755-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e6755-113">Методы</span><span class="sxs-lookup"><span data-stu-id="e6755-113">Methods</span></span>

<span data-ttu-id="e6755-114">Интерфейс **ивмдвддрививентс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e6755-114">The **IVMDVDDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="e6755-115">Метод</span><span class="sxs-lookup"><span data-stu-id="e6755-115">Method</span></span>                                                   | <span data-ttu-id="e6755-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e6755-116">Description</span></span>                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="e6755-117">**онмедиаежект**</span><span class="sxs-lookup"><span data-stu-id="e6755-117">**OnMediaEject**</span></span>](ivmdvddriveevents-onmediaeject.md)   | <span data-ttu-id="e6755-118">Получает уведомление о том, что носитель был извлечен с диска.</span><span class="sxs-lookup"><span data-stu-id="e6755-118">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="e6755-119">**онмедиаинсерт**</span><span class="sxs-lookup"><span data-stu-id="e6755-119">**OnMediaInsert**</span></span>](ivmdvddriveevents-onmediainsert.md) | <span data-ttu-id="e6755-120">Получает уведомление о том, что носитель вставлен в диск.</span><span class="sxs-lookup"><span data-stu-id="e6755-120">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e6755-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e6755-121">Requirements</span></span>



| <span data-ttu-id="e6755-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e6755-122">Requirement</span></span> | <span data-ttu-id="e6755-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e6755-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6755-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6755-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6755-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e6755-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6755-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6755-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6755-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e6755-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e6755-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e6755-128">End of client support</span></span><br/>    | <span data-ttu-id="e6755-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6755-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e6755-130">Продукт</span><span class="sxs-lookup"><span data-stu-id="e6755-130">Product</span></span><br/>                  | <span data-ttu-id="e6755-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e6755-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e6755-132">Header</span><span class="sxs-lookup"><span data-stu-id="e6755-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6755-133"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6755-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e6755-134">IID</span><span class="sxs-lookup"><span data-stu-id="e6755-134">IID</span></span><br/>                      | <span data-ttu-id="e6755-135">ДИИД \_ ивмдвддрививентс определяется как c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="e6755-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



 

