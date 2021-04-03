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
# <a name="device_data_management_set_action"></a>\_ \_ \_ действие установки управления данными \_ устройства

Следующие константные значения — это набор возможных значений для типа **\_ \_ \_ \_ действия set для управления данными устройств** , который определен как тип **DWORD**.

<dl> <dt>

<span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**Девицедсмактион \_ None**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Никакие действия не выполняются.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**Девицедсмактион \_ обрезать**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Выполняется действие усечения.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**\_Уведомление девицедсмактион**
</dt> <dd> <dl> <dt>

2 \| **девицедсмактионфлага, \_ обратимая** (0x80000002)
</dt> <dt>



Выполняется действие уведомления. Параметры находятся в структуре [**\_ \_ \_ параметров уведомлений DSM устройства**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) . **\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**Девицедсмактион \_ оффлоадреад**
</dt> <dd> <dl> <dt>

3 \| **Девицедсмактионфлагая \_ обратимость** (0x80000003)
</dt> <dt>



Выполняется действие разгрузки чтения. Параметры находятся в структуре [**\_ \_ \_ \_ параметров чтения модуля DSM устройства разгрузки**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) . Выходные данные находятся в структуре [**хранения, \_ разгрузкой для \_ \_ выходных данных чтения**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) . **\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.

**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**Девицедсмактион \_ оффлоадврите**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Выполняется действие разгрузки записи. Параметры находятся в структуре [**\_ \_ \_ \_ параметров записи для разгрузки модуля DSM устройства**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) . Выходные данные находятся в структуре [**\_ \_ \_ выходных данных разгрузки хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .

**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**\_Выделение девицедсмактион**
</dt> <dd> <dl> <dt>

5 \| **девицедсмактионфлаг \_** (0x80000005)
</dt> <dt>



Для первого переданного диапазона набора данных возвращается битовая карта выделения. Выходные данные находятся в структуре [**\_ \_ \_ \_ \_ состояния подготовки балансировки нагрузки данных устройства**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) . **\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.

**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**\_Восстановление девицедсмактион**
</dt> <dd> <dl> <dt>

6 \| **девицедсмактионфлаг \_** (0x80000006)
</dt> <dt>



Выполняется действие по восстановлению. **\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.

**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**\_Очистка девицедсмактион**
</dt> <dd> <dl> <dt>

7 \| **девицедсмактионфлаг \_** (0x80000007)
</dt> <dt>



Выполняется действие очистки. **\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.

**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**\_Устойчивость девицедсмактион**
</dt> <dd> <dl> <dt>

8 \| **девицедсмактионфлаг \_** (0x80000008)
</dt> <dt>



Выполняется действие устойчивости. **\_ Неразрушающий** (0x80000000) девицедсмактионфлаг — это битовый флаг, указывающий стеку драйверов на то, что эта операция не разрушается.

**Windows 7 и Windows Server 2008 R2:** Это значение не поддерживается до Windows 8 и Windows Server 2012.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                         |
| Header<br/>                   | <dl> <dt>Виниоктл. h (включение Windows. h)</dt> </dl> |



 

 




