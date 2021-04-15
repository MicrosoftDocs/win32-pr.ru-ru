---
description: После назначения адреса TAPI назначает идентификаторы адресов.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Идентификаторы адресов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682541"
---
# <a name="address-identifiers"></a><span data-ttu-id="936ea-103">Идентификаторы адресов</span><span class="sxs-lookup"><span data-stu-id="936ea-103">Address Identifiers</span></span>

<span data-ttu-id="936ea-104">После назначения адреса TAPI назначает идентификаторы адресов.</span><span class="sxs-lookup"><span data-stu-id="936ea-104">After address assignment, TAPI assigns address identifiers to the addresses.</span></span> <span data-ttu-id="936ea-105">*Идентификатор адреса* — это число от 0 до количества адресов в строке минус единица.</span><span class="sxs-lookup"><span data-stu-id="936ea-105">An *address identifier* is a number between 0 and the number of addresses on the line minus one.</span></span> <span data-ttu-id="936ea-106">Идентификатор адреса — это постоянное число, назначенное данному устройству, и остается постоянным даже при обновлении операционной системы.</span><span class="sxs-lookup"><span data-stu-id="936ea-106">An address identifier is a permanent number assigned to a given device and remains constant even across operating system upgrades.</span></span> <span data-ttu-id="936ea-107">Сочетание [идентификатора устройства](device-identifier-ovr.md) и идентификатора адреса однозначно определяет заданный адрес.</span><span class="sxs-lookup"><span data-stu-id="936ea-107">The combination of [device identifier](device-identifier-ovr.md) and address identifier uniquely identifies a given address.</span></span>

<span data-ttu-id="936ea-108">**Интерфейс TAPI 2. x:** Приложения получают идентификатор адреса (и идентификатор устройства) во время вызова [**линемакекалл**](/windows/win32/api/tapi/nf-tapi-linemakecall) или [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), в структуре [**Линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo) или в вызове [**линежетаддрессид**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).</span><span class="sxs-lookup"><span data-stu-id="936ea-108">**TAPI 2.x:** Applications obtain an address identifier (and device identifier) during a call to [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) or [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), in the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure, or in a call to [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).</span></span>

<span data-ttu-id="936ea-109">**Интерфейс TAPI 3. x:** [**Итаддресскапабилитиес:: Get \_ аддресскапабилити**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) с именем *аддресскап* , установленным в параметре [**адреса AC \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) **\_ ADDRESSID** , будет возвращать, если для параметра *плкапабилити* задано значение текущего идентификатора адреса.</span><span class="sxs-lookup"><span data-stu-id="936ea-109">**TAPI 3.x:** The [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) called *AddressCap* set to the **AC\_ADDRESSID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) will return with the *plCapability* parameter set to the current address ID.</span></span>

 

 
