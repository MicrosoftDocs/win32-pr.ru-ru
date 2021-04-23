---
title: Сообщения Bluetooth и WM_DEVICECHANGE
description: Bluetooth включает определенные \_ сообщения WM девицечанже, которые позволяют разработчикам получать сообщения при изменении состояния устройства Bluetooth.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987597"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a><span data-ttu-id="bbceb-103">Сообщения Bluetooth и WM \_ девицечанже</span><span class="sxs-lookup"><span data-stu-id="bbceb-103">Bluetooth and WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="bbceb-104">Bluetooth включает определенные сообщения [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) , которые позволяют разработчикам получать сообщения при изменении состояния устройства Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="bbceb-104">Bluetooth includes specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages that enable developers to obtain messages when Bluetooth devices undergo status changes.</span></span> <span data-ttu-id="bbceb-105">В этом разделе описывается, как получить специальные сообщения **WM \_ Девицечанже** для Bluetooth и список сообщений, связанных с Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="bbceb-105">This topic describes how to receive Bluetooth-specific **WM\_DEVICECHANGE** messages and lists Bluetooth-specific messages.</span></span>

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a><span data-ttu-id="bbceb-106">Получение сообщений девицечанже WM, относящихся к Bluetooth \_</span><span class="sxs-lookup"><span data-stu-id="bbceb-106">Receiving Bluetooth-specific WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="bbceb-107">Чтобы получать сообщения [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) , необходимо сначала открыть обработчик для локального радио.</span><span class="sxs-lookup"><span data-stu-id="bbceb-107">To receive [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages, a handle to the local radio must first be opened.</span></span> <span data-ttu-id="bbceb-108">Для этого используйте один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="bbceb-108">To do this, use one of the following methods:</span></span>

-   <span data-ttu-id="bbceb-109">Используйте функцию [сетупдижетклассдевс](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) со следующими параметрами: (GUID \_ бспорт \_ \_ интерфейс устройства,..., дигкф \_ Present \| дигкф \_ девицеинтерфаце), а затем используйте функции [сетупдиенумдевицеинтерфацес](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)и [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .</span><span class="sxs-lookup"><span data-stu-id="bbceb-109">Use the [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) function with the following parameters: (GUID\_BTHPORT\_DEVICE\_INTERFACE, …, DIGCF\_PRESENT \| DIGCF\_DEVICEINTERFACE), then use the [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), and the [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) functions.</span></span>
-   <span data-ttu-id="bbceb-110">Используйте функции [**блуетусфиндфирстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**блуетусфинднекстрадио**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)и [**блуетусфиндрадиоклосе**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .</span><span class="sxs-lookup"><span data-stu-id="bbceb-110">Use the [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio), and [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) functions.</span></span>

<span data-ttu-id="bbceb-111">При открытии обработчика радиосигнала Bluetooth вызовите функцию [**регистердевиценотификатион**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) и зарегистрируйте для получения уведомлений об этом маркере с помощью **ДБТ \_ девтип \_ Handle** в качестве типа устройства.</span><span class="sxs-lookup"><span data-stu-id="bbceb-111">When the Bluetooth radio handle is opened, call the [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) function and register for notifications on the handle using **DBT\_DEVTYP\_HANDLE** as the devicetype.</span></span> <span data-ttu-id="bbceb-112">При регистрации отправляются следующие идентификаторы GUID, и элемент **\_ данных** [**dev \_ Broadcast \_ Handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle):: дбч является связанным буфером.</span><span class="sxs-lookup"><span data-stu-id="bbceb-112">When registered, the following GUIDs are sent, and the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch\_data** member is the associated buffer.</span></span>

## <a name="bluetooth-specific-messages"></a><span data-ttu-id="bbceb-113">Сообщения, относящиеся к Bluetooth</span><span class="sxs-lookup"><span data-stu-id="bbceb-113">Bluetooth-specific Messages</span></span>

<span data-ttu-id="bbceb-114">В следующей таблице перечислены сообщения [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) , относящиеся к Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="bbceb-114">The following table lists Bluetooth-specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages.</span></span>

| <span data-ttu-id="bbceb-115">Код GUID</span><span class="sxs-lookup"><span data-stu-id="bbceb-115">GUID</span></span>                                   | <span data-ttu-id="bbceb-116">BUFFER</span><span class="sxs-lookup"><span data-stu-id="bbceb-116">BUFFER</span></span>                                                  | <span data-ttu-id="bbceb-117">Описание</span><span class="sxs-lookup"><span data-stu-id="bbceb-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbceb-118">GUID \_ Bluetooth \_ хЦи, \_ событие</span><span class="sxs-lookup"><span data-stu-id="bbceb-118">GUID\_BLUETOOTH\_HCI\_EVENT</span></span>            | [<span data-ttu-id="bbceb-119">**\_ \_ сведения о событии БС хЦи \_**</span><span class="sxs-lookup"><span data-stu-id="bbceb-119">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | <span data-ttu-id="bbceb-120">Это сообщение отправляется при подключении или отключении удаленного устройства Bluetooth на уровне ACL.</span><span class="sxs-lookup"><span data-stu-id="bbceb-120">This message is sent when a remote Bluetooth device connects or disconnects at the ACL level.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="bbceb-121">GUID \_ Bluetooth \_ L2CAP, \_ событие</span><span class="sxs-lookup"><span data-stu-id="bbceb-121">GUID\_BLUETOOTH\_L2CAP\_EVENT</span></span>          | [<span data-ttu-id="bbceb-122">**\_ \_ Сведения о событии БС L2CAP \_**</span><span class="sxs-lookup"><span data-stu-id="bbceb-122">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | <span data-ttu-id="bbceb-123">Это сообщение отправляется при установке или завершении канала L2CAP между локальным радио и удаленным устройством Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="bbceb-123">This message is sent when an L2CAP channel between the local radio and a remote Bluetooth device has been established or terminated.</span></span> <span data-ttu-id="bbceb-124">Для каналов L2CAP, которые являются мультиплексорами, например RFCOMM, это сообщение отправляется только при установке базового канала, а не при установке или завершении каждого мультиплексированного канала, такого как канал RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="bbceb-124">For L2CAP channels that are multiplexers, such as RFCOMM, this message is only sent when the underlying channel is established, not when each multiplexed channel, such as an RFCOMM channel, is established or terminated.</span></span> |
| <span data-ttu-id="bbceb-125">GUID \_ \_ запрос ПИН-кода Bluetooth \_</span><span class="sxs-lookup"><span data-stu-id="bbceb-125">GUID\_BLUETOOTH\_PIN\_REQUEST</span></span>          | <span data-ttu-id="bbceb-126">Не применяется</span><span class="sxs-lookup"><span data-stu-id="bbceb-126">Not applicable.</span></span>                                         | <span data-ttu-id="bbceb-127">Это сообщение должно игнорироваться приложением.</span><span class="sxs-lookup"><span data-stu-id="bbceb-127">This message should be ignored by the application.</span></span> <span data-ttu-id="bbceb-128">Если приложение должно получать запросы на получение ПИН-кода, следует использовать функцию [**блуетусрегистерфораусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .</span><span class="sxs-lookup"><span data-stu-id="bbceb-128">If the application must receive PIN requests, the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function should be used.</span></span>                                                                                                                                                   |
| <span data-ttu-id="bbceb-129">GUID \_ \_ радиомодуля Bluetooth \_ в \_ диапазоне</span><span class="sxs-lookup"><span data-stu-id="bbceb-129">GUID\_BLUETOOTH\_RADIO\_IN\_RANGE</span></span>      | [<span data-ttu-id="bbceb-130">**\_радио БС \_ в \_ диапазоне**</span><span class="sxs-lookup"><span data-stu-id="bbceb-130">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | <span data-ttu-id="bbceb-131">Это сообщение отправляется при изменении любого из следующих атрибутов удаленного устройства Bluetooth: обнаружено устройство, класс устройства, имя, состояние подключения или сохраненное состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="bbceb-131">This message is sent when any of the following attributes of a remote Bluetooth device has changed: the device has been discovered, the class of device, name, connected state, or device remembered state.</span></span> <span data-ttu-id="bbceb-132">Это сообщение также отправляется, если эти атрибуты заданы или сняты.</span><span class="sxs-lookup"><span data-stu-id="bbceb-132">This message is also sent when these attributes are set or cleared.</span></span>                                                                                  |
| <span data-ttu-id="bbceb-133">GUID \_ \_ радиомодуля \_ Bluetooth \_ вне \_ допустимого диапазона</span><span class="sxs-lookup"><span data-stu-id="bbceb-133">GUID\_BLUETOOTH\_RADIO\_OUT\_OF\_RANGE</span></span> | [<span data-ttu-id="bbceb-134">**\_адрес Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="bbceb-134">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | <span data-ttu-id="bbceb-135">Это сообщение отправляется, когда ранее обнаруженное устройство не было найдено после завершения последнего запроса.</span><span class="sxs-lookup"><span data-stu-id="bbceb-135">This message is sent when a previously discovered device has not been found after the completion of the last inquiry.</span></span> <span data-ttu-id="bbceb-136">Это сообщение не будет отправлено для сохраненных устройств.</span><span class="sxs-lookup"><span data-stu-id="bbceb-136">This message will not be sent for remembered devices.</span></span> <span data-ttu-id="bbceb-137">Структура **\_ адреса БС** — это адрес устройства, которое не было найдено.</span><span class="sxs-lookup"><span data-stu-id="bbceb-137">The **BTH\_ADDRESS** structure is the address of the device that was not found.</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="bbceb-138">См. также</span><span class="sxs-lookup"><span data-stu-id="bbceb-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbceb-139">**блуетусфиндфирстрадио**</span><span class="sxs-lookup"><span data-stu-id="bbceb-139">**BluetoothFindFirstRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[<span data-ttu-id="bbceb-140">**блуетусфинднекстрадио**</span><span class="sxs-lookup"><span data-stu-id="bbceb-140">**BluetoothFindNextRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[<span data-ttu-id="bbceb-141">**блуетусфиндрадиоклосе**</span><span class="sxs-lookup"><span data-stu-id="bbceb-141">**BluetoothFindRadioClose**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[<span data-ttu-id="bbceb-142">**регистердевиценотификатион**</span><span class="sxs-lookup"><span data-stu-id="bbceb-142">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[<span data-ttu-id="bbceb-143">сетупдидестройдевицеинфолист</span><span class="sxs-lookup"><span data-stu-id="bbceb-143">SetupDiDestroyDeviceInfoList</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[<span data-ttu-id="bbceb-144">сетупдиенумдевицеинтерфацес</span><span class="sxs-lookup"><span data-stu-id="bbceb-144">SetupDiEnumDeviceInterfaces</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[<span data-ttu-id="bbceb-145">сетупдижетклассдевс</span><span class="sxs-lookup"><span data-stu-id="bbceb-145">SetupDiGetClassDevs</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[<span data-ttu-id="bbceb-146">**\_адрес Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="bbceb-146">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[<span data-ttu-id="bbceb-147">**\_ \_ сведения о событии БС хЦи \_**</span><span class="sxs-lookup"><span data-stu-id="bbceb-147">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[<span data-ttu-id="bbceb-148">**\_ \_ Сведения о событии БС L2CAP \_**</span><span class="sxs-lookup"><span data-stu-id="bbceb-148">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[<span data-ttu-id="bbceb-149">**\_радио БС \_ в \_ диапазоне**</span><span class="sxs-lookup"><span data-stu-id="bbceb-149">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[<span data-ttu-id="bbceb-150">**\_обработчик вещания для разработчиков \_**</span><span class="sxs-lookup"><span data-stu-id="bbceb-150">**DEV\_BROADCAST\_HANDLE**</span></span>](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[<span data-ttu-id="bbceb-151">**WM \_ девицечанже**</span><span class="sxs-lookup"><span data-stu-id="bbceb-151">**WM\_DEVICECHANGE**</span></span>](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 