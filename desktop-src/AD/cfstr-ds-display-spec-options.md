---
title: CFSTR_DS_DISPLAY_SPEC_OPTIONS (DSClient. h)
description: '\_ \_ \_ Формат буфера обмена параметров отображаемой спецификации КФСТР DS содержит \_ ХГЛОБАЛ, содержащий структуру дсдисплайспекоптионс.'
ms.assetid: 98e033e4-14fe-44ed-83d5-a97e00ecce4c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DS_DISPLAY_SPEC_OPTIONS
- CFSTR_DSDISPLAYSPECOPTIONS
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81f3a229971be5ecfb9ec2c86e166af27f94e01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071469"
---
# <a name="cfstr_ds_display_spec_options"></a><span data-ttu-id="50345-103">\_ \_ Параметры отображаемой \_ спецификации кфстр DS \_</span><span class="sxs-lookup"><span data-stu-id="50345-103">CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS</span></span>

<dl> <dt>

<span data-ttu-id="50345-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**\_ \_ Параметры отображаемой \_ спецификации кфстр DS \_**</span><span class="sxs-lookup"><span data-stu-id="50345-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50345-105">"Дсдисплайспекоптионс"</span><span class="sxs-lookup"><span data-stu-id="50345-105">"DsDisplaySpecOptions"</span></span>
</dt> <dt>



<span data-ttu-id="50345-106">Active Directory пользователи и компьютеры, Active Directory сайты и службы, а также оснастки домены и доверия Active Directory поддерживают формат буфера обмена с **\_ \_ \_ \_ параметрами спецификации кфстр DS** .</span><span class="sxs-lookup"><span data-stu-id="50345-106">The Active Directory Users and Computers, the Active Directory Sites and Services, and the Active Directory Domains and Trusts snap-ins support the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span> <span data-ttu-id="50345-107">Формат буфера обмена **\_ \_ \_ \_ параметров отображаемой спецификации кфстр DS** содержит **хглобал** , содержащий структуру [**дсдисплайспекоптионс**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) .</span><span class="sxs-lookup"><span data-stu-id="50345-107">The **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format provides an **HGLOBAL** that contains a [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) structure.</span></span> <span data-ttu-id="50345-108">**Дсдисплайспекоптионс** содержит данные конфигурации для использования расширением.</span><span class="sxs-lookup"><span data-stu-id="50345-108">The **DSDISPLAYSPECOPTIONS** contains configuration data for use by the extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="50345-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**КФСТР \_ дсдисплайспекоптионс**</span><span class="sxs-lookup"><span data-stu-id="50345-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**CFSTR\_DSDISPLAYSPECOPTIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="50345-110">Формат буфера обмена **кфстр \_ дсдисплайспекоптионс** идентичен формату " **\_ \_ Параметры отображаемой \_ спецификации \_ " кфстр DS** .</span><span class="sxs-lookup"><span data-stu-id="50345-110">The **CFSTR\_DSDISPLAYSPECOPTIONS** clipboard format is identical to the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50345-111">Требования</span><span class="sxs-lookup"><span data-stu-id="50345-111">Requirements</span></span>



| <span data-ttu-id="50345-112">Требование</span><span class="sxs-lookup"><span data-stu-id="50345-112">Requirement</span></span> | <span data-ttu-id="50345-113">Значение</span><span class="sxs-lookup"><span data-stu-id="50345-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50345-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50345-114">Minimum supported client</span></span><br/> | <span data-ttu-id="50345-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50345-115">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="50345-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50345-116">Minimum supported server</span></span><br/> | <span data-ttu-id="50345-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50345-117">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="50345-118">Header</span><span class="sxs-lookup"><span data-stu-id="50345-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="50345-119"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="50345-119"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50345-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50345-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50345-121">**дсдисплайспекоптионс**</span><span class="sxs-lookup"><span data-stu-id="50345-121">**DSDISPLAYSPECOPTIONS**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions)
</dt> </dl>

 

 





