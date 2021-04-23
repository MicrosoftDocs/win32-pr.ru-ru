---
description: Тип адреса определяет формат, необходимый для адреса. Например, если тип — ЛИНЕАДДРЕССТИПЕ \_ PHONENUMBER, адрес, используемый для набора номера в сеансе, должен быть номером телефона.
ms.assetid: bea48bde-927a-400a-9a7e-a77e30ba35eb
title: Тип адреса для сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42499c19a08d67ce2e6e7ea5741053686c32aa6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673860"
---
# <a name="address-type-for-a-session"></a><span data-ttu-id="191ce-104">Тип адреса для сеанса</span><span class="sxs-lookup"><span data-stu-id="191ce-104">Address Type for a Session</span></span>

<span data-ttu-id="191ce-105">[**Тип адреса**](lineaddresstype--constants.md) определяет формат, необходимый для адреса.</span><span class="sxs-lookup"><span data-stu-id="191ce-105">The [**address type**](lineaddresstype--constants.md) identifies the format required for an address.</span></span> <span data-ttu-id="191ce-106">Например, если тип — ЛИНЕАДДРЕССТИПЕ \_ PHONENUMBER, адрес, используемый для набора номера в сеансе, должен быть номером телефона.</span><span class="sxs-lookup"><span data-stu-id="191ce-106">For example, if the type is LINEADDRESSTYPE\_PHONENUMBER, the address used to dial on the session must be a phone number.</span></span>

<span data-ttu-id="191ce-107">Данное устройство и поставщик услуг поддерживают один или несколько типов адресов.</span><span class="sxs-lookup"><span data-stu-id="191ce-107">A given device and service provider supports one or more address types.</span></span> <span data-ttu-id="191ce-108">Сведения о том, как опросить устройство для поддерживаемых форматов адресов, см. в разделе [типы адресов для устройства](address-type-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="191ce-108">See the [address types for a device](address-type-ovr.md) for information on how to poll a device for the address formats it supports.</span></span>

<span data-ttu-id="191ce-109">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **Дваддресстипе** Member of [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="191ce-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwAddressType** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="191ce-110">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), который вызывается с помощью элемента **CIL \_ Каллеридаддресстипе**, **CIL \_ калледидаддресстипе** или **CIL \_ коннектедидаддресстипе** [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="191ce-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_CALLERIDADDRESSTYPE**, **CIL\_CALLEDIDADDRESSTYPE**, or **CIL\_CONNECTEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
