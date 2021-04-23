---
description: Эта структура содержит сведения о встроенном по устройства.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: Структура STORAGE_HW_FIRMWARE_INFO (Виниоктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: 5d611df1708059b0ee636a64f55026caf8801fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664277"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="904ea-103">\_ \_ \_ Структура сведений о встроенном по оборудования хранилища</span><span class="sxs-lookup"><span data-stu-id="904ea-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="904ea-104">Эта структура содержит сведения о встроенном по устройства.</span><span class="sxs-lookup"><span data-stu-id="904ea-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="904ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="904ea-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a><span data-ttu-id="904ea-106">Члены</span><span class="sxs-lookup"><span data-stu-id="904ea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="904ea-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="904ea-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-108">Версия этой структуры.</span><span class="sxs-lookup"><span data-stu-id="904ea-108">The version of this structure.</span></span> <span data-ttu-id="904ea-109">Для этого параметра должно быть задано значение sizeof ( \_ \_ сведения о встроенном по оборудования хранилища \_ ).</span><span class="sxs-lookup"><span data-stu-id="904ea-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="904ea-110">**Размер**</span><span class="sxs-lookup"><span data-stu-id="904ea-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-111">Размер этой структуры в виде буфера, включая слот.</span><span class="sxs-lookup"><span data-stu-id="904ea-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="904ea-112">**суппортупграде**</span><span class="sxs-lookup"><span data-stu-id="904ea-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-113">Указывает, что это встроенное по поддерживает обновление.</span><span class="sxs-lookup"><span data-stu-id="904ea-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="904ea-114">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="904ea-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-115">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="904ea-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="904ea-116">**слоткаунт**</span><span class="sxs-lookup"><span data-stu-id="904ea-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-117">Число слотов встроенного по на устройстве.</span><span class="sxs-lookup"><span data-stu-id="904ea-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="904ea-118">Это измерение массива слотов.</span><span class="sxs-lookup"><span data-stu-id="904ea-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="904ea-119">Некоторые устройства могут хранить более 1 образа встроенного по, если они имеют более одного слота встроенного по.</span><span class="sxs-lookup"><span data-stu-id="904ea-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="904ea-120">**активеслот**</span><span class="sxs-lookup"><span data-stu-id="904ea-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-121">Слот встроенного по, содержащий активный или выполняемый в данный момент образ встроенного по.</span><span class="sxs-lookup"><span data-stu-id="904ea-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="904ea-122">**пендингактиватеслот**</span><span class="sxs-lookup"><span data-stu-id="904ea-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-123">Слот встроенного по, ожидающий активации.</span><span class="sxs-lookup"><span data-stu-id="904ea-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="904ea-124">**фирмварешаред**</span><span class="sxs-lookup"><span data-stu-id="904ea-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-125">Указывает, что встроенное по относится как к устройству, так и к контроллеру или адаптеру, например SSD NVMe.</span><span class="sxs-lookup"><span data-stu-id="904ea-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="904ea-126">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="904ea-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-127">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="904ea-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="904ea-128">**имажепайлоадалигнмент**</span><span class="sxs-lookup"><span data-stu-id="904ea-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-129">Выравнивание полезных данных изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="904ea-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="904ea-130">Максимальное значение — \_ Размер страницы.</span><span class="sxs-lookup"><span data-stu-id="904ea-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="904ea-131">Размер перемещения — это множественные этого размера.</span><span class="sxs-lookup"><span data-stu-id="904ea-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="904ea-132">Для некоторых протоколов требуется по крайней мере размер сектора.</span><span class="sxs-lookup"><span data-stu-id="904ea-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="904ea-133">Если это значение равно 0, это означает, что это значение является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="904ea-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="904ea-134">**имажепайлоадмакссизе**</span><span class="sxs-lookup"><span data-stu-id="904ea-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-135">Максимальный размер полезных данных образа используется для одной команды.</span><span class="sxs-lookup"><span data-stu-id="904ea-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="904ea-136">**Слот**</span><span class="sxs-lookup"><span data-stu-id="904ea-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="904ea-137">Содержит сведения о слотах для каждого слота на устройстве, тип [**данных \_ \_ \_ слот \_ встроенного по аппаратного обеспечения хранилища**](storage-hw-firmware-slot-info.md).</span><span class="sxs-lookup"><span data-stu-id="904ea-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="904ea-138">Требования</span><span class="sxs-lookup"><span data-stu-id="904ea-138">Requirements</span></span>



| <span data-ttu-id="904ea-139">Требование</span><span class="sxs-lookup"><span data-stu-id="904ea-139">Requirement</span></span> | <span data-ttu-id="904ea-140">Значение</span><span class="sxs-lookup"><span data-stu-id="904ea-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="904ea-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="904ea-141">Minimum supported client</span></span><br/> | <span data-ttu-id="904ea-142">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="904ea-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="904ea-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="904ea-143">Minimum supported server</span></span><br/> | <span data-ttu-id="904ea-144">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="904ea-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="904ea-145">Header</span><span class="sxs-lookup"><span data-stu-id="904ea-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="904ea-146"><dt>Виниоктл. h. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="904ea-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904ea-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="904ea-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904ea-148">**\_ \_ Активация встроенного по службы хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="904ea-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="904ea-149">**\_ \_ Активация встроенного по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="904ea-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="904ea-150">**\_ \_ скачивание встроенного по для хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="904ea-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="904ea-151">**\_ \_ Загрузка встроенного по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="904ea-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="904ea-152">**\_ \_ \_ Получение сведений о встроенном по для хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="904ea-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="904ea-153">**\_ \_ \_ запрос сведений о встроенном по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="904ea-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="904ea-154">**\_ \_ \_ сведения о слоте встроенного по оборудования хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="904ea-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




