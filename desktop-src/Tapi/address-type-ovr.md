---
description: Тип адреса устройства описывает формы адресации, допустимые для адреса, например номер телефона или IP-адрес.
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: Тип адреса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674031"
---
# <a name="address-type"></a><span data-ttu-id="70b0d-103">Тип адреса</span><span class="sxs-lookup"><span data-stu-id="70b0d-103">Address Type</span></span>

<span data-ttu-id="70b0d-104">Тип адреса устройства описывает формы адресации, допустимые для адреса, например номер телефона или IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="70b0d-104">The device address type describes the forms of addressing permissible on an address, such as a phone number or an IP address.</span></span> <span data-ttu-id="70b0d-105">Данное устройство будет распознавать один или несколько типов адресов.</span><span class="sxs-lookup"><span data-stu-id="70b0d-105">A given device will understand one or more address types.</span></span> <span data-ttu-id="70b0d-106">Список типов адресов, поддерживаемых TAPI, см. в разделе [ \_ константы линеаддресстипе](lineaddresstype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="70b0d-106">For a list of address types supported by TAPI, see [LINEADDRESSTYPE\_ Constants](lineaddresstype--constants.md).</span></span> <span data-ttu-id="70b0d-107">[Преобразование адреса](initiate-a-session-ovr.md) можно использовать для преобразования адреса из одного типа в другой.</span><span class="sxs-lookup"><span data-stu-id="70b0d-107">[Address translation](initiate-a-session-ovr.md) may be used to convert an address from one type to another.</span></span>

<span data-ttu-id="70b0d-108">Общие сведения [об адресах см. в](address-ovr.md) разделе [категории устройств](device-categories.md).</span><span class="sxs-lookup"><span data-stu-id="70b0d-108">For general information on addresses, see [Address](address-ovr.md) under [Device Categories](device-categories.md).</span></span>

<span data-ttu-id="70b0d-109">[Тип адреса для сеанса](address-type-for-a-session-ovr.md) будет подмножеством типов адресов устройств.</span><span class="sxs-lookup"><span data-stu-id="70b0d-109">The [address type for a session](address-type-for-a-session-ovr.md) will be a subset of the device address types.</span></span>

<span data-ttu-id="70b0d-110">**Интерфейс TAPI 2. x:** См. раздел [**линежетдевкапс**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) и элемент **дваддресстипе** в [**линедевкапс**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="70b0d-110">**TAPI 2.x:** See [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) and the **dwAddressType** member of [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span></span>

<span data-ttu-id="70b0d-111">**Интерфейс TAPI 3. x:** См. раздел [**итаддресскапабилитиес:: Get \_ аддресскапабилити**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability)с параметром *аддресскап* , равным входящему в [**адрес \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) **AC \_ аддресстипес** .</span><span class="sxs-lookup"><span data-stu-id="70b0d-111">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), with *AddressCap* set to the **AC\_ADDRESSTYPES** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span></span>

 

 
