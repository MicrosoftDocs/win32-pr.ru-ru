---
description: Структура STORAGE_HW_FIRMWARE_INFO_QUERY — эта структура содержит сведения о встроенном по устройства.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: Структура STORAGE_HW_FIRMWARE_INFO_QUERY (Виниоктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: ffda37d918406a696a29a9bf2903424523c3b830
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119402"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="40848-103">\_ \_ \_ Структура запроса сведений о встроенном по оборудования хранилища \_</span><span class="sxs-lookup"><span data-stu-id="40848-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="40848-104">Эта структура содержит сведения о встроенном по устройства.</span><span class="sxs-lookup"><span data-stu-id="40848-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="40848-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40848-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="40848-106">Члены</span><span class="sxs-lookup"><span data-stu-id="40848-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="40848-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="40848-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="40848-108">Версия этой структуры.</span><span class="sxs-lookup"><span data-stu-id="40848-108">The version of this structure.</span></span> <span data-ttu-id="40848-109">Для этого параметра должно быть задано значение sizeof ( \_ \_ \_ запрос сведений о встроенном по аппаратного обеспечения хранилища \_ )</span><span class="sxs-lookup"><span data-stu-id="40848-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="40848-110">**Размер**</span><span class="sxs-lookup"><span data-stu-id="40848-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="40848-111">Размер этой структуры в виде буфера.</span><span class="sxs-lookup"><span data-stu-id="40848-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="40848-112">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="40848-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="40848-113">Флаги, связанные с запросом.</span><span class="sxs-lookup"><span data-stu-id="40848-113">The flags associated with the query.</span></span> <span data-ttu-id="40848-114">Ниже приведены флаги, которые можно задать в этом элементе.</span><span class="sxs-lookup"><span data-stu-id="40848-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="40848-115">Flag</span><span class="sxs-lookup"><span data-stu-id="40848-115">Flag</span></span>                                             | <span data-ttu-id="40848-116">Описание</span><span class="sxs-lookup"><span data-stu-id="40848-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40848-117">\_ \_ \_ \_ контроллер флага запроса встроенного по аппаратного обеспечения хранилища \_</span><span class="sxs-lookup"><span data-stu-id="40848-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="40848-118">Указывает, что целевой объект запроса отличается от самого устройства.</span><span class="sxs-lookup"><span data-stu-id="40848-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="40848-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="40848-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="40848-120">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="40848-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40848-121">Требования</span><span class="sxs-lookup"><span data-stu-id="40848-121">Requirements</span></span>



| <span data-ttu-id="40848-122">Требование</span><span class="sxs-lookup"><span data-stu-id="40848-122">Requirement</span></span> | <span data-ttu-id="40848-123">Значение</span><span class="sxs-lookup"><span data-stu-id="40848-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40848-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40848-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40848-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="40848-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="40848-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40848-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40848-127">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="40848-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="40848-128">Header</span><span class="sxs-lookup"><span data-stu-id="40848-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="40848-129"><dt>Виниоктл. h. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40848-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40848-130">См. также</span><span class="sxs-lookup"><span data-stu-id="40848-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40848-131">**\_ \_ Активация встроенного по службы хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="40848-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="40848-132">**\_ \_ Активация встроенного по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="40848-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="40848-133">**\_ \_ скачивание встроенного по для хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="40848-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="40848-134">**\_ \_ Загрузка встроенного по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="40848-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="40848-135">**\_ \_ \_ Получение сведений о встроенном по для хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="40848-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="40848-136">**\_ \_ сведения о встроенном по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="40848-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="40848-137">**\_ \_ \_ сведения о слоте встроенного по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="40848-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




