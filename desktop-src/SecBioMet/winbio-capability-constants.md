---
title: Константы WINBIO_CAPABILITY (Винбио \_ types. h)
description: Подтипы датчика отпечатков пальцев.
ms.assetid: D447273E-2A02-484E-B0E4-69FEADD15797
topic_type:
- apiref
api_name:
- WINBIO_CAPABILITY_SENSOR
- WINBIO_CAPABILITY_MATCHING
- WINBIO_CAPABILITY_DATABASE
- WINBIO_CAPABILITY_PROCESSING
- WINBIO_CAPABILITY_ENCRYPTION
- WINBIO_CAPABILITY_NAVIGATION
- WINBIO_CAPABILITY_INDICATOR
- WINBIO_CAPABILITY_VIRTUAL_SENSOR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16de3f496e5c3723722bb7aae22c81eb27c968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891973"
---
# <a name="winbio_capability-constants"></a><span data-ttu-id="ac306-103">\_Константы возможностей винбио</span><span class="sxs-lookup"><span data-stu-id="ac306-103">WINBIO\_CAPABILITY Constants</span></span>

<span data-ttu-id="ac306-104">Следующие подтипы датчика отпечатков пальцев — это значения **\_ возможностей винбио** , которые можно использовать в качестве битовой маски для параметра *CAPABILITIES* структуры [**\_ \_ схемы единицы винбио**](winbio-unit-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="ac306-104">The following fingerprint sensor sub types are **WINBIO\_CAPABILITIES** values that can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="ac306-105">Они относятся к возможностям встроенного датчика.</span><span class="sxs-lookup"><span data-stu-id="ac306-105">These refer to the onboard sensor capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="ac306-106">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="ac306-106">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="ac306-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ac306-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_SENSOR"></span><span id="winbio_capability_sensor"></span><dl> <span data-ttu-id="ac306-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="ac306-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ac306-109">Датчик может записывать биометрические данные.</span><span class="sxs-lookup"><span data-stu-id="ac306-109">The sensor can capture biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_MATCHING"></span><span id="winbio_capability_matching"></span><dl> <span data-ttu-id="ac306-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="ac306-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ac306-111">Датчик может сопоставлять биометрические данные с удостоверением.</span><span class="sxs-lookup"><span data-stu-id="ac306-111">The sensor can match biometric data to an identity.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_DATABASE"></span><span id="winbio_capability_database"></span><dl> <span data-ttu-id="ac306-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="ac306-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ac306-113">Датчик содержит встроенную базу данных.</span><span class="sxs-lookup"><span data-stu-id="ac306-113">The sensor contains an onboard database.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_PROCESSING"></span><span id="winbio_capability_processing"></span><dl> <span data-ttu-id="ac306-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="ac306-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ac306-115">Датчик может выполнять биометрическую обработку.</span><span class="sxs-lookup"><span data-stu-id="ac306-115">The sensor can perform biometric processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_ENCRYPTION"></span><span id="winbio_capability_encryption"></span><dl> <span data-ttu-id="ac306-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="ac306-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ac306-117">Датчик может шифровать биометрические данные.</span><span class="sxs-lookup"><span data-stu-id="ac306-117">The sensor can encrypt biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_NAVIGATION"></span><span id="winbio_capability_navigation"></span><dl> <span data-ttu-id="ac306-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="ac306-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ac306-119">Датчик может работать как клавиатура мыши.</span><span class="sxs-lookup"><span data-stu-id="ac306-119">The sensor can act as a mouse pad.</span></span> <span data-ttu-id="ac306-120">В настоящее время это не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ac306-120">This is currently not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_INDICATOR"></span><span id="winbio_capability_indicator"></span><dl> <span data-ttu-id="ac306-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="ac306-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ac306-122">Датчик содержит индикатор индикатора.</span><span class="sxs-lookup"><span data-stu-id="ac306-122">The sensor contains an indicator light.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_VIRTUAL_SENSOR"></span><span id="winbio_capability_virtual_sensor"></span><dl> <span data-ttu-id="ac306-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="ac306-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="ac306-124">Адаптер датчика управляет собственным подключением к биометрической оборудованию.</span><span class="sxs-lookup"><span data-stu-id="ac306-124">The sensor adapter manages its own connection to the biometric hardware.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ac306-125">Эта константа применяется только для Windows 10 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="ac306-125">This constant applies only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="ac306-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ac306-126">Requirements</span></span>



| <span data-ttu-id="ac306-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ac306-127">Requirement</span></span> | <span data-ttu-id="ac306-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ac306-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac306-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac306-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ac306-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ac306-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="ac306-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac306-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ac306-132">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac306-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                  |
| <span data-ttu-id="ac306-133">Header</span><span class="sxs-lookup"><span data-stu-id="ac306-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac306-134"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="ac306-134"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac306-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac306-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac306-136">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="ac306-136">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="ac306-137">**\_схема единицы \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="ac306-137">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





