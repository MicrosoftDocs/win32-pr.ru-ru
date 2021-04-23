---
title: Значения синтаксиса приложения SNMP (SNMP. h)
description: Значения синтаксиса приложения SNMP используются приложениями управления, которые используют API управления Microsoft SNMP.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135658"
---
# <a name="snmp-application-syntax-values"></a><span data-ttu-id="a752e-103">Значения синтаксиса приложения SNMP</span><span class="sxs-lookup"><span data-stu-id="a752e-103">SNMP Application Syntax Values</span></span>

<span data-ttu-id="a752e-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a752e-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a752e-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="a752e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a752e-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="a752e-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="a752e-107">Значения синтаксиса приложения SNMP используются приложениями управления, которые используют API управления Microsoft SNMP.</span><span class="sxs-lookup"><span data-stu-id="a752e-107">The SNMP Application Syntax Values are used by management applications that employ the Microsoft SNMP Management API.</span></span>



| <span data-ttu-id="a752e-108">Константа</span><span class="sxs-lookup"><span data-stu-id="a752e-108">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="a752e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a752e-109">Description</span></span>                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <span data-ttu-id="a752e-110"><dt>**ASN \_ IPAddress**</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-110"><dt>**ASN\_IPADDRESS**</dt></span></span> </dl>                             | <span data-ttu-id="a752e-111">Указывает переменную IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="a752e-111">Indicates an IP address variable.</span></span><br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <span data-ttu-id="a752e-112"><dt>**ASN \_ COUNTER32**</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-112"><dt>**ASN\_COUNTER32**</dt></span></span> </dl>                             | <span data-ttu-id="a752e-113">Указывает переменную счетчика.</span><span class="sxs-lookup"><span data-stu-id="a752e-113">Indicates a counter variable.</span></span><br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <span data-ttu-id="a752e-114"><dt>**ASN \_ значение Gauge32**</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-114"><dt>**ASN\_GAUGE32**</dt></span></span> </dl>                                   | <span data-ttu-id="a752e-115">Указывает переменную датчика.</span><span class="sxs-lookup"><span data-stu-id="a752e-115">Indicates a gauge variable.</span></span> <span data-ttu-id="a752e-116">Эта переменная описывает тип Unsigned32 в согласовании с RFC 1902.</span><span class="sxs-lookup"><span data-stu-id="a752e-116">This variable describes an Unsigned32 type in conformance with RFC 1902.</span></span><br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <span data-ttu-id="a752e-117"><dt>**ASN \_ значение TIMETICKS**</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-117"><dt>**ASN\_TIMETICKS**</dt></span></span> </dl>                             | <span data-ttu-id="a752e-118">Указывает переменную значение TIMETICKS.</span><span class="sxs-lookup"><span data-stu-id="a752e-118">Indicates a timeticks variable.</span></span><br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <span data-ttu-id="a752e-119"><dt>**непрозрачный ASN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-119"><dt>**ASN\_OPAQUE**</dt></span></span> </dl>                                      | <span data-ttu-id="a752e-120">Указывает непрозрачную переменную.</span><span class="sxs-lookup"><span data-stu-id="a752e-120">Indicates an opaque variable.</span></span><br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <span data-ttu-id="a752e-121"><dt>**ASN \_ COUNTER64**</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-121"><dt>**ASN\_COUNTER64**</dt></span></span> </dl>                             | <span data-ttu-id="a752e-122">Указывает переменную счетчика, которая увеличивается до достижения максимального значения (2 ^ 64)-1.</span><span class="sxs-lookup"><span data-stu-id="a752e-122">Indicates a counter variable that increases until it reaches a maximum value of (2^64) - 1.</span></span><br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <span data-ttu-id="a752e-123"><dt>**ASN \_ UINTEGER32**</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-123"><dt>**ASN\_UINTEGER32**</dt></span></span> </dl>                          | <span data-ttu-id="a752e-124">Указывает на 32-разрядную переменную целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="a752e-124">Indicates a 32-bit unsigned integer variable.</span></span> <span data-ttu-id="a752e-125">Эта переменная описывает тип UInteger32 в согласовании с RFC 1442.</span><span class="sxs-lookup"><span data-stu-id="a752e-125">This variable describes a UInteger32 type in conformance with RFC 1442.</span></span><br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <span data-ttu-id="a752e-126"><dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-126"><dt>**ASN\_RFC2578\_UNSIGNED32**</dt></span></span> </dl> | <span data-ttu-id="a752e-127">См. раздел ASN \_ значение Gauge32.</span><span class="sxs-lookup"><span data-stu-id="a752e-127">See ASN\_GAUGE32.</span></span><br/>                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="a752e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a752e-128">Requirements</span></span>



| <span data-ttu-id="a752e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a752e-129">Requirement</span></span> | <span data-ttu-id="a752e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a752e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a752e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a752e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a752e-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a752e-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="a752e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a752e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a752e-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a752e-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a752e-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a752e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a752e-136"><dt>Протокол SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-136"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a752e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a752e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a752e-138">Обзор протокола SNMP</span><span class="sxs-lookup"><span data-stu-id="a752e-138">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="a752e-139">Справочник по SNMP</span><span class="sxs-lookup"><span data-stu-id="a752e-139">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="a752e-140">Константы SNMP</span><span class="sxs-lookup"><span data-stu-id="a752e-140">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

