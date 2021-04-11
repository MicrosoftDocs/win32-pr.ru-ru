---
description: Приложения, включая службы, могут регистрироваться для получения уведомлений о событиях устройства.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: События устройства (Иоевент. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce58ba5dd21cdd505e945687603ddb54e77b2440
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262498"
---
# <a name="device-events-ioeventh"></a><span data-ttu-id="41c86-103">События устройства (Иоевент. h)</span><span class="sxs-lookup"><span data-stu-id="41c86-103">Device Events (IoEvent.h)</span></span>

<span data-ttu-id="41c86-104">Приложения, включая службы, могут регистрироваться для получения уведомлений о событиях устройства.</span><span class="sxs-lookup"><span data-stu-id="41c86-104">Applications, including services, can register to receive notification of device events.</span></span> <span data-ttu-id="41c86-105">Например, служба каталога может получить уведомление о том, что тома подключены или отключены, чтобы можно было настроить пути к файлам на томе.</span><span class="sxs-lookup"><span data-stu-id="41c86-105">For example, a catalog service can receive notice of volumes being mounted or dismounted so it can adjust the paths to files on the volume.</span></span> <span data-ttu-id="41c86-106">Система уведомляет приложение о том, что произошло событие устройства, отправив приложению сообщение [**\_ девицечанже WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="41c86-106">The system notifies an application that a device event has occurred by sending the application a [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="41c86-107">Система уведомляет службу о том, что произошло событие устройства, вызывая функцию обработчика событий службы [**хандлерекс**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="41c86-107">The system notifies a service that a device event has occurred by invoking the service's event handler function, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="41c86-108">Чтобы получить уведомления о событиях устройства, вызовите функцию [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) с помощью [**структуры \_ \_ обработчика вещания для dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="41c86-108">To receive device event notices, call the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function with a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span> <span data-ttu-id="41c86-109">Не забудьте задать для **элемента \_ Handle дбч** маркер устройства, полученный из функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="41c86-109">Be sure to set the **dbch\_handle** member to the device handle obtained from the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="41c86-110">Кроме того, присвойте элементу **\_ типа устройства Дбч** значение **ДБТ \_ девтип \_**.</span><span class="sxs-lookup"><span data-stu-id="41c86-110">Also, set the **dbch\_devicetype** member to **DBT\_DEVTYP\_HANDLE**.</span></span> <span data-ttu-id="41c86-111">Функция возвращает маркер уведомления устройства.</span><span class="sxs-lookup"><span data-stu-id="41c86-111">The function returns a device notification handle.</span></span> <span data-ttu-id="41c86-112">Обратите внимание, что это не то же самое, что и маркер тома.</span><span class="sxs-lookup"><span data-stu-id="41c86-112">Note that this is not the same as the volume handle.</span></span>

<span data-ttu-id="41c86-113">Когда приложение получает уведомление, если тип события — [ДБТ \_ CUSTOMEVENT](dbt-customevent.md), возможно, вы получили одно из событий устройства, определенных в иоевент. h.</span><span class="sxs-lookup"><span data-stu-id="41c86-113">When your application receives notification, if the event type is [DBT\_CUSTOMEVENT](dbt-customevent.md), you may have received one of the device events defined in IoEvent.h.</span></span> <span data-ttu-id="41c86-114">Чтобы определить, произошло ли одно из этих событий, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="41c86-114">To determine if one of these events has occurred, use the following steps.</span></span>

1.  <span data-ttu-id="41c86-115">Рассматривайте данные события как структуру [**\_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -данных для разработки.</span><span class="sxs-lookup"><span data-stu-id="41c86-115">Treat the event data as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="41c86-116">Убедитесь, что для элемента **\_ типа устройства дбч** задано значение **ДБТ \_ девтип \_ Handle**.</span><span class="sxs-lookup"><span data-stu-id="41c86-116">Verify that the **dbch\_devicetype** member is set to **DBT\_DEVTYP\_HANDLE**.</span></span>
2.  <span data-ttu-id="41c86-117">Если **дбч \_ типа устройства** **ДБТ \_ девтип \_**, то данные события являются указателем на структуру [**\_ \_ обработчика вещания для разработки**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="41c86-117">If **dbch\_devicetype** is **DBT\_DEVTYP\_HANDLE**, the event data is really a pointer to a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span>
3.  <span data-ttu-id="41c86-118">Сравните элемент **\_ евентгуид Дбч** с **идентификаторами GUID**, перечисленными в следующей таблице, с помощью функции [**исекуалгуид**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) .</span><span class="sxs-lookup"><span data-stu-id="41c86-118">Compare the **dbch\_eventguid** member to the **GUID** s listed in the following table using the [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) function.</span></span>

<dl> <dt>

<span data-ttu-id="41c86-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID \_ операций ввода-вывода с \_ \_ монопольной \_ блокировкой**</span><span class="sxs-lookup"><span data-stu-id="41c86-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span><span class="sxs-lookup"><span data-stu-id="41c86-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span></span>
</dt> <dt>



<span data-ttu-id="41c86-121">Устройство чтения компакт-дисков заблокировано для монопольного доступа.</span><span class="sxs-lookup"><span data-stu-id="41c86-121">The CD-ROM device has been locked for exclusive access.</span></span>

<span data-ttu-id="41c86-122">**Windows Server 2003 и Windows XP:** Для поддержки этого значения требуется IMAPI 2,0.</span><span class="sxs-lookup"><span data-stu-id="41c86-122">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="41c86-123">Дополнительные сведения см. в разделе API для создания [образов](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="41c86-123">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ операций ввода-вывода с \_ \_ эксклюзивным доступом \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span><span class="sxs-lookup"><span data-stu-id="41c86-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span></span>
</dt> <dt>



<span data-ttu-id="41c86-126">Устройство чтения компакт-дисков, заблокированное для монопольного доступа, было разблокировано.</span><span class="sxs-lookup"><span data-stu-id="41c86-126">A CD-ROM device that was locked for exclusive access has been unlocked.</span></span>

<span data-ttu-id="41c86-127">**Windows Server 2003 и Windows XP:** Для поддержки этого значения требуется IMAPI 2,0.</span><span class="sxs-lookup"><span data-stu-id="41c86-127">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="41c86-128">Дополнительные сведения см. в разделе API для создания [образов](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="41c86-128">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**\_устройство ввода-вывода GUID \_ \_ становится \_ готовым**</span><span class="sxs-lookup"><span data-stu-id="41c86-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID\_IO\_DEVICE\_BECOMING\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="41c86-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="41c86-131">Выполняется регулятор мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="41c86-131">Media spin-up is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**\_ \_ \_ внешний запрос устройства ввода-вывода GUID \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**GUID\_IO\_DEVICE\_EXTERNAL\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="41c86-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="41c86-134">Существует несколько возможных причин этого события. Дополнительные сведения см. в разделе Спецификация T10 MMC команды уведомления о состоянии события в [https://www.t10.org/](https://www.t10.org/) .</span><span class="sxs-lookup"><span data-stu-id="41c86-134">There are several possible causes for this event; for more information, refer to T10 MMC specification of the GET EVENT STATUS NOTIFICATION Command, at [https://www.t10.org/](https://www.t10.org/).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**\_ \_ Получение носителя с идентификатором GUID ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID\_IO\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="41c86-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="41c86-137">На устройство добавлен съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="41c86-137">Removable media has been added to the device.</span></span> <span data-ttu-id="41c86-138">Элемент **\_ данных дбч** является указателем на структуру [**\_ \_ \_ контекста изменения мультимедиа класса**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="41c86-138">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="41c86-139">Элемент **NewState** предоставляет сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="41c86-139">The **NewState** member provides status information.</span></span> <span data-ttu-id="41c86-140">Например, значение **медиаунаваилабле** указывает, что носитель недоступен (например, из-за активного сеанса записи).</span><span class="sxs-lookup"><span data-stu-id="41c86-140">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="41c86-141">**Windows XP:** Элемент **\_ данных дбч** — это значение типа **ulong** , представляющее количество изменений мультимедиа с момента запуска системы.</span><span class="sxs-lookup"><span data-stu-id="41c86-141">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_запрос на \_ \_ Извлечение носителя GUID ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID\_IO\_MEDIA\_EJECT\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="41c86-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="41c86-144">Устройство съемного носителя получило от пользователя запрос на извлечение указанного слота или носителя.</span><span class="sxs-lookup"><span data-stu-id="41c86-144">The removable media's drive has received a request from the user to eject the specified slot or media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID \_ операции \_ \_ удаления носителя**</span><span class="sxs-lookup"><span data-stu-id="41c86-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID\_IO\_MEDIA\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="41c86-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="41c86-147">Съемный носитель был удален с устройства или недоступен.</span><span class="sxs-lookup"><span data-stu-id="41c86-147">Removable media has been removed from the device or is unavailable.</span></span> <span data-ttu-id="41c86-148">Элемент **\_ данных дбч** является указателем на структуру [**\_ \_ \_ контекста изменения мультимедиа класса**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="41c86-148">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="41c86-149">Элемент **NewState** предоставляет сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="41c86-149">The **NewState** member provides status information.</span></span> <span data-ttu-id="41c86-150">Например, значение **медиаунаваилабле** указывает, что носитель недоступен (например, из-за активного сеанса записи).</span><span class="sxs-lookup"><span data-stu-id="41c86-150">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="41c86-151">**Windows XP:** Элемент **\_ данных дбч** — это значение типа **ulong** , представляющее количество изменений мультимедиа с момента запуска системы.</span><span class="sxs-lookup"><span data-stu-id="41c86-151">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID \_ \_ изменение тома ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID\_IO\_VOLUME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-153">7373654a-812a-11d0-bec7-08002be2092f</span><span class="sxs-lookup"><span data-stu-id="41c86-153">7373654a-812a-11d0-bec7-08002be2092f</span></span>
</dt> <dt>



<span data-ttu-id="41c86-154">Метка тома изменена.</span><span class="sxs-lookup"><span data-stu-id="41c86-154">The volume label has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_Размер GUID \_ для \_ изменения тома ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID\_IO\_VOLUME\_CHANGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span><span class="sxs-lookup"><span data-stu-id="41c86-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span></span>
</dt> <dt>



<span data-ttu-id="41c86-157">Изменился размер файловой системы на томе.</span><span class="sxs-lookup"><span data-stu-id="41c86-157">The size of the file system on the volume has changed.</span></span>

<span data-ttu-id="41c86-158">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41c86-158">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID \_ \_ отключения тома ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID\_IO\_VOLUME\_DISMOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="41c86-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="41c86-161">Выполняется попытка отключения тома.</span><span class="sxs-lookup"><span data-stu-id="41c86-161">An attempt to dismount the volume is in progress.</span></span> <span data-ttu-id="41c86-162">Необходимо закрыть все дескрипторы файлов и каталогов на томе.</span><span class="sxs-lookup"><span data-stu-id="41c86-162">You should close all handles to files and directories on the volume.</span></span> <span data-ttu-id="41c86-163">Этому событию не обязательно предшествует событие **\_ \_ \_ блокировки тома ввода-вывода GUID** .</span><span class="sxs-lookup"><span data-stu-id="41c86-163">This event will not necessarily be preceded by a **GUID\_IO\_VOLUME\_LOCK** event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_ \_ \_ Сбой отключения тома ввода-вывода GUID \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**GUID\_IO\_VOLUME\_DISMOUNT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="41c86-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="41c86-166">Сбой при отключении тома.</span><span class="sxs-lookup"><span data-stu-id="41c86-166">An attempt to dismount a volume failed.</span></span> <span data-ttu-id="41c86-167">Это часто происходит из-за того, что другой процесс не ответил на уведомление об отключении **\_ \_ тома \_ ввода-вывода GUID** , закрывая необработанные дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="41c86-167">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_DISMOUNT** notice by closing its outstanding handles.</span></span> <span data-ttu-id="41c86-168">Из-за сбоя отключения вы можете повторно открыть любые дескрипторы для соответствующего тома.</span><span class="sxs-lookup"><span data-stu-id="41c86-168">Because the dismount failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**\_ \_ \_ \_ изменение состояния ФВЕ тома ввода-вывода GUID \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID\_IO\_VOLUME\_FVE\_STATUS\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span><span class="sxs-lookup"><span data-stu-id="41c86-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span></span>
</dt> <dt>



<span data-ttu-id="41c86-171">Состояние шифрование диска BitLocker тома изменилось.</span><span class="sxs-lookup"><span data-stu-id="41c86-171">The volume's BitLocker Drive Encryption status has changed.</span></span> <span data-ttu-id="41c86-172">Это событие сообщает, когда BitLocker включен или отключен, или когда шифрование начинается, завершается, приостанавливается или возобновляется.</span><span class="sxs-lookup"><span data-stu-id="41c86-172">This event is signaled when BitLocker is enabled or disabled, or when encryption begins, ends, pauses, or resumes.</span></span>

<span data-ttu-id="41c86-173">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41c86-173">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID \_ \_ Блокировка тома \_ IO**</span><span class="sxs-lookup"><span data-stu-id="41c86-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID\_IO\_VOLUME\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-175">50708874-c9af-11D1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="41c86-175">50708874-c9af-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="41c86-176">Другой процесс пытается заблокировать том.</span><span class="sxs-lookup"><span data-stu-id="41c86-176">Another process is attempting to lock the volume.</span></span> <span data-ttu-id="41c86-177">Необходимо закрыть все дескрипторы файлов и каталогов на томе.</span><span class="sxs-lookup"><span data-stu-id="41c86-177">You should close all handles to files and directories on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**\_ \_ \_ сбой блокировки тома ввода-вывода GUID \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID\_IO\_VOLUME\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="41c86-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="41c86-180">Сбой при попытке заблокировать том.</span><span class="sxs-lookup"><span data-stu-id="41c86-180">An attempt to lock a volume failed.</span></span> <span data-ttu-id="41c86-181">Это часто происходит из-за того, что другому процессу не удалось ответить на событие **\_ \_ \_ блокировки тома ввода-вывода GUID** , закрыв необработанные дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="41c86-181">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_LOCK** event by closing its outstanding handles.</span></span> <span data-ttu-id="41c86-182">Так как блокировка не удалась, вы можете повторно открыть любые дескрипторы соответствующего тома.</span><span class="sxs-lookup"><span data-stu-id="41c86-182">Because the lock failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID \_ \_ Подключение тома \_ IO**</span><span class="sxs-lookup"><span data-stu-id="41c86-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID\_IO\_VOLUME\_MOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="41c86-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="41c86-185">Том был подключен другим процессом.</span><span class="sxs-lookup"><span data-stu-id="41c86-185">The volume has been mounted by another process.</span></span> <span data-ttu-id="41c86-186">Вы можете открыть один или несколько дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="41c86-186">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**\_ \_ \_ изменение имени тома ввода-вывода GUID \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID\_IO\_VOLUME\_NAME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-188">2de97f83-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="41c86-188">2de97f83-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="41c86-189">Имя тома было изменено.</span><span class="sxs-lookup"><span data-stu-id="41c86-189">The volume name has been changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**для \_ тома ввода-вывода GUID \_ \_ требуется \_ chkdsk**</span><span class="sxs-lookup"><span data-stu-id="41c86-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID\_IO\_VOLUME\_NEED\_CHKDSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span><span class="sxs-lookup"><span data-stu-id="41c86-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span></span>
</dt> <dt>



<span data-ttu-id="41c86-192">Файловая система обнаружила повреждение тома.</span><span class="sxs-lookup"><span data-stu-id="41c86-192">A file system has detected corruption on the volume.</span></span> <span data-ttu-id="41c86-193">Приложение должно запустить программу CHKDSK на томе или уведомить пользователя о необходимости.</span><span class="sxs-lookup"><span data-stu-id="41c86-193">The application should run CHKDSK on the volume or notify the user to do so.</span></span>

<span data-ttu-id="41c86-194">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41c86-194">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**\_ \_ \_ \_ изменение физической конфигурации тома ввода-вывода GUID \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**GUID\_IO\_VOLUME\_PHYSICAL\_CONFIGURATION\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-196">2de97f84-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="41c86-196">2de97f84-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="41c86-197">Физическое описывающего или текущее физическое состояние тома изменилось.</span><span class="sxs-lookup"><span data-stu-id="41c86-197">The physical makeup or current physical state of the volume has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID при подготовке к отслеживанию \_ тома ввода-вывода \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID\_IO\_VOLUME\_PREPARING\_EJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span><span class="sxs-lookup"><span data-stu-id="41c86-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span></span>
</dt> <dt>



<span data-ttu-id="41c86-200">Файловая система готовит диск для извлечения.</span><span class="sxs-lookup"><span data-stu-id="41c86-200">The file system is preparing the disc to be ejected.</span></span> <span data-ttu-id="41c86-201">Например, файловая система останавливает операцию форматирования в фоновом режиме или закрывает сеанс на носителе с однократным входом.</span><span class="sxs-lookup"><span data-stu-id="41c86-201">For example, the file system is stopping a background formatting operation or closing the session on write-once media.</span></span>

<span data-ttu-id="41c86-202">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41c86-202">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_ \_ \_ изменение уникального \_ идентификатора GUID тома ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**GUID\_IO\_VOLUME\_UNIQUE\_ID\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-204">af39da42-6622-41f5-970b-139d092fa3d9</span><span class="sxs-lookup"><span data-stu-id="41c86-204">af39da42-6622-41f5-970b-139d092fa3d9</span></span>
</dt> <dt>



<span data-ttu-id="41c86-205">Уникальный идентификатор тома был изменен.</span><span class="sxs-lookup"><span data-stu-id="41c86-205">The volume's unique identifier has been changed.</span></span> <span data-ttu-id="41c86-206">Дополнительные сведения о уникальном идентификаторе см. в разделе [**ioctl \_ маунтдев \_ запрос \_ уникального \_ идентификатора**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span><span class="sxs-lookup"><span data-stu-id="41c86-206">For more information about the unique identifier, see [**IOCTL\_MOUNTDEV\_QUERY\_UNIQUE\_ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span></span>

<span data-ttu-id="41c86-207">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Это значение не поддерживается до Windows Server 2008 R2 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="41c86-207">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID \_ \_ разблокировки тома ввода-вывода \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID\_IO\_VOLUME\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="41c86-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="41c86-210">Том был разблокирован другим процессом.</span><span class="sxs-lookup"><span data-stu-id="41c86-210">The volume has been unlocked by another process.</span></span> <span data-ttu-id="41c86-211">Вы можете открыть один или несколько дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="41c86-211">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c86-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID \_ \_ людьми тома ввода-вывода \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID\_IO\_VOLUME\_WEARING\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c86-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span><span class="sxs-lookup"><span data-stu-id="41c86-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span></span>
</dt> <dt>



<span data-ttu-id="41c86-214">Носитель людьми. Это событие отправляется, когда файловая система определяет, что частота ошибок в томе слишком высока, или почти исчерпано пространство для замены дефектов.</span><span class="sxs-lookup"><span data-stu-id="41c86-214">The media is wearing out. This event is sent when a file system determines that the error rate on a volume is too high, or its defect replacement space is almost exhausted.</span></span>

<span data-ttu-id="41c86-215">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41c86-215">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41c86-216">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41c86-216">Remarks</span></span>

<span data-ttu-id="41c86-217">События **\_ \_ \_ \_ сбоя** тома ввода-вывода GUID и отключения тома ввода-вывода с кодами GUID отправляются, так же как и событие сбоя блокировки тома ввода- **\_ вывода \_ \_ GUID** и **\_ \_ \_ \_ Блокировка тома ввода-вывода GUID** . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c86-217">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** events are related, as are the **GUID\_IO\_VOLUME\_LOCK** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** event.</span></span> <span data-ttu-id="41c86-218">События **\_ \_ \_ блокировки** тома **ввода-вывода GUID и \_ \_ \_ отключения** томов ввода-вывода GUID указывают на попытку выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="41c86-218">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_LOCK** events indicate that an operation is being attempted.</span></span> <span data-ttu-id="41c86-219">Необходимо принять воееся уведомление о событии и зафиксировать выполняемые действия.</span><span class="sxs-lookup"><span data-stu-id="41c86-219">You should act on the event notification, and record the action taken.</span></span> <span data-ttu-id="41c86-220">**\_ \_ \_ \_ Сбой отключения тома ввода-вывода GUID** и события **\_ \_ \_ \_ сбоя блокировки тома ввода-вывода GUID** указывают на сбой попытки выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="41c86-220">The **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** events indicate that the attempted operation failed.</span></span> <span data-ttu-id="41c86-221">Затем вы можете использовать запись для отмены действий, выполненных в ответ на операцию.</span><span class="sxs-lookup"><span data-stu-id="41c86-221">You may then use your record to undo the actions you made in response to the operation.</span></span>

<span data-ttu-id="41c86-222">Элемент **\_ хдевнотифи дбч** структуры [**\_ \_ Handle для dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) указывает на затронутое устройство.</span><span class="sxs-lookup"><span data-stu-id="41c86-222">The **dbch\_hdevnotify** member of the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure indicates the affected device.</span></span> <span data-ttu-id="41c86-223">Обратите внимание, что это маркер уведомления устройства, возвращенный [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), а не маркер тома.</span><span class="sxs-lookup"><span data-stu-id="41c86-223">Note that this is the device notification handle returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), not a volume handle.</span></span> <span data-ttu-id="41c86-224">Чтобы выполнить операции с томом, сопоставьте этот обработчик с соответствующим маркером тома.</span><span class="sxs-lookup"><span data-stu-id="41c86-224">To perform operations on the volume, map this handle to the corresponding volume handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c86-225">Требования</span><span class="sxs-lookup"><span data-stu-id="41c86-225">Requirements</span></span>



| <span data-ttu-id="41c86-226">Требование</span><span class="sxs-lookup"><span data-stu-id="41c86-226">Requirement</span></span> | <span data-ttu-id="41c86-227">Значение</span><span class="sxs-lookup"><span data-stu-id="41c86-227">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41c86-228">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41c86-228">Minimum supported client</span></span><br/> | <span data-ttu-id="41c86-229">Windows XP</span><span class="sxs-lookup"><span data-stu-id="41c86-229">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="41c86-230">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41c86-230">Minimum supported server</span></span><br/> | <span data-ttu-id="41c86-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41c86-231">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="41c86-232">Header</span><span class="sxs-lookup"><span data-stu-id="41c86-232">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c86-233"><dt>Иоевент. h</dt></span><span class="sxs-lookup"><span data-stu-id="41c86-233"><dt>IoEvent.h</dt></span></span> </dl> |



 

