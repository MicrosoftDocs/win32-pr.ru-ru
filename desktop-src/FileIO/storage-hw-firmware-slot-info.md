---
description: Эта структура содержит сведения о слоте на устройстве.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: Структура STORAGE_HW_FIRMWARE_SLOT_INFO (Виниоктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682915"
---
# <a name="storage_hw_firmware_slot_info-structure"></a><span data-ttu-id="73278-103">\_ \_ \_ Структура сведений о слоте встроенного по АППАРАТного обеспечения хранилища \_</span><span class="sxs-lookup"><span data-stu-id="73278-103">STORAGE\_HW\_FIRMWARE\_SLOT\_INFO structure</span></span>

<span data-ttu-id="73278-104">Эта структура содержит сведения о слоте на устройстве.</span><span class="sxs-lookup"><span data-stu-id="73278-104">This structure contains information about a slot on a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="73278-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73278-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a><span data-ttu-id="73278-106">Члены</span><span class="sxs-lookup"><span data-stu-id="73278-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="73278-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="73278-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="73278-108">Версия этой структуры.</span><span class="sxs-lookup"><span data-stu-id="73278-108">The version of this structure.</span></span> <span data-ttu-id="73278-109">Для этого параметра должно быть задано значение sizeof ( \_ \_ \_ сведения о слоте встроенного по оборудования хранилища \_ ).</span><span class="sxs-lookup"><span data-stu-id="73278-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_SLOT\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="73278-110">**Размер**</span><span class="sxs-lookup"><span data-stu-id="73278-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="73278-111">Размер этой структуры.</span><span class="sxs-lookup"><span data-stu-id="73278-111">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="73278-112">**SlotNumber**</span><span class="sxs-lookup"><span data-stu-id="73278-112">**SlotNumber**</span></span>
</dt> <dd>

<span data-ttu-id="73278-113">Номер слота этого слота.</span><span class="sxs-lookup"><span data-stu-id="73278-113">The slot number of this slot.</span></span>

</dd> <dt>

<span data-ttu-id="73278-114">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="73278-114">**ReadOnly**</span></span>
</dt> <dd>

<span data-ttu-id="73278-115">Указывает, доступен ли этот слот только для чтения.</span><span class="sxs-lookup"><span data-stu-id="73278-115">Indicates whether this slot is read-only or not.</span></span>

</dd> <dt>

<span data-ttu-id="73278-116">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="73278-116">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="73278-117">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="73278-117">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="73278-118">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="73278-118">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="73278-119">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="73278-119">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="73278-120">**Редакции**</span><span class="sxs-lookup"><span data-stu-id="73278-120">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="73278-121">Редакция встроенного по этого слота.</span><span class="sxs-lookup"><span data-stu-id="73278-121">The revision of the firmware on this slot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73278-122">Требования</span><span class="sxs-lookup"><span data-stu-id="73278-122">Requirements</span></span>



| <span data-ttu-id="73278-123">Требование</span><span class="sxs-lookup"><span data-stu-id="73278-123">Requirement</span></span> | <span data-ttu-id="73278-124">Значение</span><span class="sxs-lookup"><span data-stu-id="73278-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73278-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73278-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73278-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="73278-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="73278-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73278-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73278-128">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="73278-128">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="73278-129">Header</span><span class="sxs-lookup"><span data-stu-id="73278-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="73278-130"><dt>Виниоктл. h. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73278-130"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73278-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73278-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73278-132">**\_ \_ Активация встроенного по службы хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="73278-132">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="73278-133">**\_ \_ Активация встроенного по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="73278-133">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="73278-134">**\_ \_ скачивание встроенного по для хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="73278-134">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="73278-135">**\_ \_ Загрузка встроенного по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="73278-135">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="73278-136">**\_ \_ \_ Получение сведений о встроенном по для хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="73278-136">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="73278-137">**\_ \_ сведения о встроенном по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="73278-137">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="73278-138">**\_ \_ \_ запрос сведений о встроенном по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="73278-138">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




