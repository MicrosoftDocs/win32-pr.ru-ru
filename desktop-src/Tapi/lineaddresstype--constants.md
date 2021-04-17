---
description: Тип адреса определяет формат адреса, например Стандартный номер телефона или адрес электронной почты. Только приложения, которые согласовывают TAPI версии 3,0 или выше, могут использовать типы адресов.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: Константы LINEADDRESSTYPE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675422"
---
# <a name="lineaddresstype_-constants"></a><span data-ttu-id="6ea8e-104">\_Константы линеаддресстипе</span><span class="sxs-lookup"><span data-stu-id="6ea8e-104">LINEADDRESSTYPE\_ Constants</span></span>

<span data-ttu-id="6ea8e-105">Тип адреса определяет формат адреса, например Стандартный номер телефона или адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6ea8e-105">The address type identifies address format, such as standard phone number or e-mail address.</span></span> <span data-ttu-id="6ea8e-106">Только приложения, которые согласовывают TAPI версии 3,0 или выше, могут использовать типы адресов.</span><span class="sxs-lookup"><span data-stu-id="6ea8e-106">Only applications that negotiate TAPI version 3.0 or higher can use address types.</span></span>

<dl> <dt>

<span data-ttu-id="6ea8e-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**ЛИНЕАДДРЕССТИПЕ \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="6ea8e-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE\_PHONENUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea8e-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6ea8e-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="6ea8e-109">Тип адреса — это стандартный номер телефона.</span><span class="sxs-lookup"><span data-stu-id="6ea8e-109">Address type is a standard phone number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ea8e-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**ЛИНЕАДДРЕССТИПЕ \_ SDP**</span><span class="sxs-lookup"><span data-stu-id="6ea8e-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE\_SDP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea8e-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6ea8e-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="6ea8e-112">Тип адреса — конференция "Протокол описания сеанса (SDP)".</span><span class="sxs-lookup"><span data-stu-id="6ea8e-112">Address type is Session Description Protocol (SDP) conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ea8e-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**ЛИНЕАДДРЕССТИПЕ \_ емаилнаме**</span><span class="sxs-lookup"><span data-stu-id="6ea8e-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE\_EMAILNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea8e-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6ea8e-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="6ea8e-115">Тип адреса — это имя электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6ea8e-115">Address type is an e-mail name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ea8e-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**ЛИНЕАДДРЕССТИПЕ \_ имя_домена**</span><span class="sxs-lookup"><span data-stu-id="6ea8e-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea8e-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6ea8e-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="6ea8e-118">Тип адреса — имя домена.</span><span class="sxs-lookup"><span data-stu-id="6ea8e-118">Address type is a domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ea8e-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**\_IP-адрес линеаддресстипе**</span><span class="sxs-lookup"><span data-stu-id="6ea8e-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE\_IPADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea8e-120">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ea8e-120">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="6ea8e-121">Тип адреса — это IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="6ea8e-121">Address type is an IP address.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ea8e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6ea8e-122">Requirements</span></span>



| <span data-ttu-id="6ea8e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6ea8e-123">Requirement</span></span> | <span data-ttu-id="6ea8e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6ea8e-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6ea8e-125">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="6ea8e-125">TAPI version</span></span><br/> | <span data-ttu-id="6ea8e-126">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6ea8e-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6ea8e-127">Header</span><span class="sxs-lookup"><span data-stu-id="6ea8e-127">Header</span></span><br/>       | <dl> <span data-ttu-id="6ea8e-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ea8e-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




