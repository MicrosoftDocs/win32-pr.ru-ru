---
description: Определите набор действий для \_ хранилища ioctl \_ Управление \_ \_ атрибутами набора данных с помощью \_ управляющего кода.
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (Виниоктл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895873"
---
# <a name="device_data_management_set_action"></a><span data-ttu-id="2aa80-103">\_ \_ \_ действие установки управления данными \_ устройства</span><span class="sxs-lookup"><span data-stu-id="2aa80-103">DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION</span></span>

<span data-ttu-id="2aa80-104">Следующие константные значения — это набор возможных значений для типа **\_ \_ \_ \_ действия set для управления данными устройств** , который определен как тип **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2aa80-104">The following constant values are the set of possible values for the **DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION** type, which is defined as type **DWORD**.</span></span>

<dl> <dt>

<span data-ttu-id="2aa80-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**Девицедсмактион \_ None**</span><span class="sxs-lookup"><span data-stu-id="2aa80-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction\_None**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aa80-106">0</span><span class="sxs-lookup"><span data-stu-id="2aa80-106">0</span></span>
</dt> <dt>



<span data-ttu-id="2aa80-107">Никакие действия не выполняются.</span><span class="sxs-lookup"><span data-stu-id="2aa80-107">No action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2aa80-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**Девицедсмактион \_ обрезать**</span><span class="sxs-lookup"><span data-stu-id="2aa80-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction\_Trim**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aa80-109">1</span><span class="sxs-lookup"><span data-stu-id="2aa80-109">1</span></span>
</dt> <dt>



<span data-ttu-id="2aa80-110">Выполняется действие усечения.</span><span class="sxs-lookup"><span data-stu-id="2aa80-110">A trim action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2aa80-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**\_Уведомление девицедсмактион**</span><span class="sxs-lookup"><span data-stu-id="2aa80-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**DeviceDsmAction\_Notification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aa80-112">2 \| **девицедсмактионфлага, \_ обратимая** (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="2aa80-112">2 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000002)</span></span>
</dt> <dt>



<span data-ttu-id="2aa80-113">Выполняется действие уведомления.</span><span class="sxs-lookup"><span data-stu-id="2aa80-113">A notification action is performed.</span></span> <span data-ttu-id="2aa80-114">Параметры находятся в структуре [**\_ \_ \_ параметров уведомлений DSM устройства**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) .</span><span class="sxs-lookup"><span data-stu-id="2aa80-114">The parameters are in a [**DEVICE\_DSM\_NOTIFICATION\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) structure.</span></span> <span data-ttu-id="2aa80-115">**\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.</span><span class="sxs-lookup"><span data-stu-id="2aa80-115">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2aa80-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**Девицедсмактион \_ оффлоадреад**</span><span class="sxs-lookup"><span data-stu-id="2aa80-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction\_OffloadRead**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aa80-117">3 \| **Девицедсмактионфлагая \_ обратимость** (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="2aa80-117">3 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000003)</span></span>
</dt> <dt>



<span data-ttu-id="2aa80-118">Выполняется действие разгрузки чтения.</span><span class="sxs-lookup"><span data-stu-id="2aa80-118">An offload read action is performed.</span></span> <span data-ttu-id="2aa80-119">Параметры находятся в структуре [**\_ \_ \_ \_ параметров чтения модуля DSM устройства разгрузки**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) .</span><span class="sxs-lookup"><span data-stu-id="2aa80-119">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_READ\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) structure.</span></span> <span data-ttu-id="2aa80-120">Выходные данные находятся в структуре [**хранения, \_ разгрузкой для \_ \_ выходных данных чтения**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) .</span><span class="sxs-lookup"><span data-stu-id="2aa80-120">The output is in a [**STORAGE\_OFFLOAD\_READ\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) structure.</span></span> <span data-ttu-id="2aa80-121">**\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.</span><span class="sxs-lookup"><span data-stu-id="2aa80-121">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="2aa80-122">**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2aa80-122">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2aa80-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**Девицедсмактион \_ оффлоадврите**</span><span class="sxs-lookup"><span data-stu-id="2aa80-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction\_OffloadWrite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aa80-124">4</span><span class="sxs-lookup"><span data-stu-id="2aa80-124">4</span></span>
</dt> <dt>



<span data-ttu-id="2aa80-125">Выполняется действие разгрузки записи.</span><span class="sxs-lookup"><span data-stu-id="2aa80-125">An offload write action is performed.</span></span> <span data-ttu-id="2aa80-126">Параметры находятся в структуре [**\_ \_ \_ \_ параметров записи для разгрузки модуля DSM устройства**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) .</span><span class="sxs-lookup"><span data-stu-id="2aa80-126">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_WRITE\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) structure.</span></span> <span data-ttu-id="2aa80-127">Выходные данные находятся в структуре [**\_ \_ \_ выходных данных разгрузки хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .</span><span class="sxs-lookup"><span data-stu-id="2aa80-127">The output is in a [**STORAGE\_OFFLOAD\_WRITE\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) structure.</span></span>

<span data-ttu-id="2aa80-128">**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2aa80-128">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2aa80-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**\_Выделение девицедсмактион**</span><span class="sxs-lookup"><span data-stu-id="2aa80-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**DeviceDsmAction\_Allocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aa80-130">5 \| **девицедсмактионфлаг \_** (0x80000005)</span><span class="sxs-lookup"><span data-stu-id="2aa80-130">5 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000005)</span></span>
</dt> <dt>



<span data-ttu-id="2aa80-131">Для первого переданного диапазона набора данных возвращается битовая карта выделения.</span><span class="sxs-lookup"><span data-stu-id="2aa80-131">An allocation bitmap is returned for the first data set range passed in.</span></span> <span data-ttu-id="2aa80-132">Выходные данные находятся в структуре [**\_ \_ \_ \_ \_ состояния подготовки балансировки нагрузки данных устройства**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) .</span><span class="sxs-lookup"><span data-stu-id="2aa80-132">The output is in a [**DEVICE\_DATA\_SET\_LB\_PROVISIONING\_STATE**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) structure.</span></span> <span data-ttu-id="2aa80-133">**\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.</span><span class="sxs-lookup"><span data-stu-id="2aa80-133">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="2aa80-134">**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2aa80-134">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2aa80-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**\_Восстановление девицедсмактион**</span><span class="sxs-lookup"><span data-stu-id="2aa80-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction\_Repair**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aa80-136">6 \| **девицедсмактионфлаг \_** (0x80000006)</span><span class="sxs-lookup"><span data-stu-id="2aa80-136">6 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000006)</span></span>
</dt> <dt>



<span data-ttu-id="2aa80-137">Выполняется действие по восстановлению.</span><span class="sxs-lookup"><span data-stu-id="2aa80-137">A repair action is performed.</span></span> <span data-ttu-id="2aa80-138">**\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.</span><span class="sxs-lookup"><span data-stu-id="2aa80-138">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="2aa80-139">**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2aa80-139">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2aa80-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**\_Очистка девицедсмактион**</span><span class="sxs-lookup"><span data-stu-id="2aa80-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction\_Scrub**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aa80-141">7 \| **девицедсмактионфлаг \_** (0x80000007)</span><span class="sxs-lookup"><span data-stu-id="2aa80-141">7 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000007)</span></span>
</dt> <dt>



<span data-ttu-id="2aa80-142">Выполняется действие очистки.</span><span class="sxs-lookup"><span data-stu-id="2aa80-142">A scrub action is performed.</span></span> <span data-ttu-id="2aa80-143">**\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.</span><span class="sxs-lookup"><span data-stu-id="2aa80-143">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="2aa80-144">**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2aa80-144">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2aa80-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**\_Устойчивость девицедсмактион**</span><span class="sxs-lookup"><span data-stu-id="2aa80-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**DeviceDsmAction\_Resiliency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aa80-146">8 \| **девицедсмактионфлаг \_** (0x80000008)</span><span class="sxs-lookup"><span data-stu-id="2aa80-146">8 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000008)</span></span>
</dt> <dt>



<span data-ttu-id="2aa80-147">Выполняется действие устойчивости.</span><span class="sxs-lookup"><span data-stu-id="2aa80-147">A resiliency action is performed.</span></span> <span data-ttu-id="2aa80-148">**\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.</span><span class="sxs-lookup"><span data-stu-id="2aa80-148">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="2aa80-149">**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2aa80-149">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2aa80-150">Требования</span><span class="sxs-lookup"><span data-stu-id="2aa80-150">Requirements</span></span>



| <span data-ttu-id="2aa80-151">Требование</span><span class="sxs-lookup"><span data-stu-id="2aa80-151">Requirement</span></span> | <span data-ttu-id="2aa80-152">Значение</span><span class="sxs-lookup"><span data-stu-id="2aa80-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa80-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2aa80-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa80-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2aa80-154">Windows 7</span></span><br/>                                                                                      |
| <span data-ttu-id="2aa80-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2aa80-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa80-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2aa80-156">Windows Server 2008 R2</span></span><br/>                                                                         |
| <span data-ttu-id="2aa80-157">Header</span><span class="sxs-lookup"><span data-stu-id="2aa80-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aa80-158"><dt>Виниоктл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2aa80-158"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



 

 




