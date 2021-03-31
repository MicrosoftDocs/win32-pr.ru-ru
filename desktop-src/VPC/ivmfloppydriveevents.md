---
title: Интерфейс Ивмфлоппидрививентс (Впккоминтерфацес. h)
description: Определяет интерфейс исходящего события для интерфейса Ивмфлоппидриве. Клиент реализует эти методы для получения событий, отправленных из Ивмфлоппидриве.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Виртуальный ПК с интерфейсом Ивмфлоппидрививентс
- Ивмфлоппидрививентс интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137486"
---
# <a name="ivmfloppydriveevents-interface"></a><span data-ttu-id="795e8-106">Интерфейс Ивмфлоппидрививентс</span><span class="sxs-lookup"><span data-stu-id="795e8-106">IVMFloppyDriveEvents interface</span></span>

<span data-ttu-id="795e8-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="795e8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="795e8-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="795e8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="795e8-109">Определяет интерфейс исходящего события для интерфейса [**ивмфлоппидриве**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="795e8-109">Defines the outgoing event interface for the [**IVMFloppyDrive**](ivmfloppydrive.md) interface.</span></span> <span data-ttu-id="795e8-110">Клиент реализует эти методы для получения событий, отправленных из **ивмфлоппидриве**.</span><span class="sxs-lookup"><span data-stu-id="795e8-110">The client implements these methods to receive events sent from **IVMFloppyDrive**.</span></span>

## <a name="members"></a><span data-ttu-id="795e8-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="795e8-111">Members</span></span>

<span data-ttu-id="795e8-112">Интерфейс **ивмфлоппидрививентс** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="795e8-112">The **IVMFloppyDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="795e8-113">**Ивмфлоппидрививентс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="795e8-113">**IVMFloppyDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="795e8-114">Методы</span><span class="sxs-lookup"><span data-stu-id="795e8-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="795e8-115">Методы</span><span class="sxs-lookup"><span data-stu-id="795e8-115">Methods</span></span>

<span data-ttu-id="795e8-116">Интерфейс **ивмфлоппидрививентс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="795e8-116">The **IVMFloppyDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="795e8-117">Метод</span><span class="sxs-lookup"><span data-stu-id="795e8-117">Method</span></span>                                                      | <span data-ttu-id="795e8-118">Описание</span><span class="sxs-lookup"><span data-stu-id="795e8-118">Description</span></span>                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="795e8-119">**онмедиаежект**</span><span class="sxs-lookup"><span data-stu-id="795e8-119">**OnMediaEject**</span></span>](ivmfloppydriveevents-onmediaeject.md)   | <span data-ttu-id="795e8-120">Получает уведомление о том, что носитель был извлечен с диска.</span><span class="sxs-lookup"><span data-stu-id="795e8-120">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="795e8-121">**онмедиаинсерт**</span><span class="sxs-lookup"><span data-stu-id="795e8-121">**OnMediaInsert**</span></span>](ivmfloppydriveevents-onmediainsert.md) | <span data-ttu-id="795e8-122">Получает уведомление о том, что носитель вставлен в диск.</span><span class="sxs-lookup"><span data-stu-id="795e8-122">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="795e8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="795e8-123">Requirements</span></span>



| <span data-ttu-id="795e8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="795e8-124">Requirement</span></span> | <span data-ttu-id="795e8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="795e8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="795e8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="795e8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="795e8-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="795e8-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="795e8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="795e8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="795e8-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="795e8-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="795e8-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="795e8-130">End of client support</span></span><br/>    | <span data-ttu-id="795e8-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="795e8-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="795e8-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="795e8-132">Product</span></span><br/>                  | <span data-ttu-id="795e8-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="795e8-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="795e8-134">Header</span><span class="sxs-lookup"><span data-stu-id="795e8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="795e8-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="795e8-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="795e8-136">IID</span><span class="sxs-lookup"><span data-stu-id="795e8-136">IID</span></span><br/>                      | <span data-ttu-id="795e8-137">ДИИД \_ ивмфлоппидрививентс определяется как a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="795e8-137">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



 

