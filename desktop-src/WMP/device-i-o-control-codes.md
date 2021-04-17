---
title: Управляющие коды устройств ввода-вывода
description: Управляющие коды устройств ввода-вывода
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Управляющие коды устройств ввода-вывода в проигрывателе Windows Media
- Проигрыватель Windows Media, управляющие коды
- диспетчер устройств Windows Media
- управляющие коды устройств ввода-вывода
- управляющие коды
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691305"
---
# <a name="device-io-control-codes"></a><span data-ttu-id="f891d-108">Управляющие коды устройств ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="f891d-108">Device I/O Control Codes</span></span>

<span data-ttu-id="f891d-109">Проигрыватель Windows Media 10 или более поздней версии определяет управляющие коды ввода-вывода устройств Windows Media диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="f891d-109">Windows Media Player 10 or later defines Windows Media Device Manager device I/O control codes.</span></span> <span data-ttu-id="f891d-110">В следующей таблице содержатся коды управления и их описания.</span><span class="sxs-lookup"><span data-stu-id="f891d-110">The following table contains the control codes and their descriptions.</span></span>



| <span data-ttu-id="f891d-111">Управляющий код ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="f891d-111">I/O control code</span></span>                      | <span data-ttu-id="f891d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f891d-112">Value</span></span>      | <span data-ttu-id="f891d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f891d-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f891d-114">**\_ \_ \_ цикл \_ обработки метаданных WMP через ioctl**</span><span class="sxs-lookup"><span data-stu-id="f891d-114">**IOCTL\_WMP\_METADATA\_ROUND\_TRIP**</span></span> | <span data-ttu-id="f891d-115">0x31504d57</span><span class="sxs-lookup"><span data-stu-id="f891d-115">0x31504d57</span></span> | <span data-ttu-id="f891d-116">Управляет передачей сведений об изменениях, произошедших в значениях метаданных.</span><span class="sxs-lookup"><span data-stu-id="f891d-116">Manages transfer of information about changes that occurred to metadata values.</span></span> <span data-ttu-id="f891d-117">См. раздел [расширения устройств для ускорения перемещения метаданных](device-extensions-for-accelerated-metadata-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="f891d-117">See [Device Extensions for Accelerated Metadata Transfer](device-extensions-for-accelerated-metadata-transfer.md).</span></span>                                                                                                                                                                          |
| <span data-ttu-id="f891d-118">**\_Синхронизация ioctl \_ устройства \_ WMP \_**</span><span class="sxs-lookup"><span data-stu-id="f891d-118">**IOCTL\_WMP\_DEVICE\_CAN\_SYNC**</span></span>     | <span data-ttu-id="f891d-119">0x32504d57</span><span class="sxs-lookup"><span data-stu-id="f891d-119">0x32504d57</span></span> | <span data-ttu-id="f891d-120">Указывает, поддерживает ли портативное устройство автоматическую синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="f891d-120">Indicates whether a portable device supports automatic synchronization.</span></span> <span data-ttu-id="f891d-121">Проигрыватель Windows Media 10 или более поздней версии не предоставляет входной буфер. Выходной буфер должен возвращать значение **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f891d-121">Windows Media Player 10 or later provides no input buffer.The output buffer must return a **DWORD** value.</span></span> <span data-ttu-id="f891d-122">Значение 1 означает, что устройство поддерживает синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="f891d-122">A value of 1 means the device supports synchronization.</span></span> <span data-ttu-id="f891d-123">Значение 0 означает, что устройство не поддерживает автоматическую синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="f891d-123">A value of 0 means the device does not support automatic synchronization.</span></span><br/> <span data-ttu-id="f891d-124">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="f891d-124">See Remarks for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f891d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f891d-125">Remarks</span></span>

<span data-ttu-id="f891d-126">Эти управляющие коды определены в вмпдевицес. h.</span><span class="sxs-lookup"><span data-stu-id="f891d-126">These control codes are defined in wmpdevices.h.</span></span>

<span data-ttu-id="f891d-127">Если устройство не поддерживает функцию **ioctl \_ WMP \_ \_ для \_ синхронизации**, проигрыватель Windows Media 10 или более поздней версии предполагает, что устройство поддерживает автоматическую синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="f891d-127">If the device does not support **IOCTL\_WMP\_DEVICE\_CAN\_SYNC**, Windows Media Player 10 or later assumes the device supports automatic synchronization.</span></span> <span data-ttu-id="f891d-128">Обратите внимание, что хотя это значение может запретить автоматическую синхронизацию, существуют дополнительные условия, позволяющие определить, поддерживает ли устройство автоматическую синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="f891d-128">Note that while this value can disallow automatic synchronization, there are additional criteria used to determine whether the device supports automatic synchronization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f891d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f891d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f891d-130">**Расширения устройств для ускоренной пересылки метаданных**</span><span class="sxs-lookup"><span data-stu-id="f891d-130">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[<span data-ttu-id="f891d-131">**Проигрыватель Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f891d-131">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 





