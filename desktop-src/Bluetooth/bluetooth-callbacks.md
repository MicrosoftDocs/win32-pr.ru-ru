---
title: Обратные вызовы Bluetooth
description: Функции обратного вызова Bluetooth в этом разделе используются в сочетании с функциями, которые позволяют управлять устройствами и службами Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773649"
---
# <a name="bluetooth-callbacks"></a><span data-ttu-id="3120a-103">Обратные вызовы Bluetooth</span><span class="sxs-lookup"><span data-stu-id="3120a-103">Bluetooth Callbacks</span></span>

<span data-ttu-id="3120a-104">Функции обратного вызова Bluetooth в этом разделе используются в сочетании с функциями, которые позволяют управлять устройствами и службами Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="3120a-104">The Bluetooth callback functions in this section are used in combination with functions that make it possible to manage Bluetooth devices and services.</span></span>

<span data-ttu-id="3120a-105">Bluetooth также поддерживается с помощью программного интерфейса сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="3120a-105">Bluetooth is also supported by using the Windows Sockets programming interface.</span></span> <span data-ttu-id="3120a-106">Дополнительные сведения о программировании Bluetooth с помощью интерфейса сокетов Windows см. в разделе [Поддержка сокетов Windows для Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="3120a-106">For more information about programming Bluetooth by using the Windows Sockets interface, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>



| <span data-ttu-id="3120a-107">Section</span><span class="sxs-lookup"><span data-stu-id="3120a-107">Section</span></span>                                                                                      | <span data-ttu-id="3120a-108">Содержимое</span><span class="sxs-lookup"><span data-stu-id="3120a-108">Content</span></span>                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3120a-109">**\_обратный вызов проверки подлинности PFN \_**</span><span class="sxs-lookup"><span data-stu-id="3120a-109">**PFN\_AUTHENTICATION\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | <span data-ttu-id="3120a-110">Используется в сочетании с функцией [**блуетусрегистерфораусентикатион**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .</span><span class="sxs-lookup"><span data-stu-id="3120a-110">Used in conjunction with the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function.</span></span>                                                  |
| [<span data-ttu-id="3120a-111">**\_обратный вызов проверки подлинности pfn, \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="3120a-111">**PFN\_AUTHENTICATION\_CALLBACK\_EX**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | <span data-ttu-id="3120a-112">Используется в сочетании с функцией [**блуетусрегистерфораусентикатионекс**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .</span><span class="sxs-lookup"><span data-stu-id="3120a-112">Used in conjunction with the [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) function.</span></span>                                              |
| [<span data-ttu-id="3120a-113">**\_ \_ \_ обратный вызов атрибутов перечисления PFN Bluetooth \_**</span><span class="sxs-lookup"><span data-stu-id="3120a-113">**PFN\_BLUETOOTH\_ENUM\_ATTRIBUTES\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | <span data-ttu-id="3120a-114">Вызывается один раз для каждого атрибута, найденного в параметре *псдпстреам* , который передается в вызов функции [**блуетуссдпенуматтрибутес**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) .</span><span class="sxs-lookup"><span data-stu-id="3120a-114">Called once for each attribute found in the *pSDPStream* parameter that is passed to the [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) function call.</span></span> |
| [<span data-ttu-id="3120a-115">**\_ \_ обратный вызов устройства PFN**</span><span class="sxs-lookup"><span data-stu-id="3120a-115">**PFN\_DEVICE\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | <span data-ttu-id="3120a-116">Используется в связи с выбором устройств Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="3120a-116">Used in association with selecting Bluetooth devices.</span></span>                                                                                                                    |



 

 

 




