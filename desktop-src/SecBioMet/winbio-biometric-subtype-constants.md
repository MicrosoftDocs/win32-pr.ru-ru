---
title: Константы WINBIO_BIOMETRIC_SUBTYPE (Винбио \_ types. h)
description: Укажите сведения о биометрического измерения.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988877"
---
# <a name="winbio_biometric_subtype-constants"></a><span data-ttu-id="239c4-103">\_Константы ПОДтипа БИОметрической метрики винбио \_</span><span class="sxs-lookup"><span data-stu-id="239c4-103">WINBIO\_BIOMETRIC\_SUBTYPE Constants</span></span>

<span data-ttu-id="239c4-104">**Винбио \_ Константы \_ ПОДтипа БИОметрической метрики** используются во всех биометрическая платформа Windows для предоставления дополнительных сведений о биометрических измерениях.</span><span class="sxs-lookup"><span data-stu-id="239c4-104">**WINBIO\_BIOMETRIC\_SUBTYPE** constants are used throughout the Windows Biometric Framework to provide additional information about a biometric measurement.</span></span> <span data-ttu-id="239c4-105">Следующие константы можно использовать, если ни один подтип не является обязательным или если требуется какой-либо подтип.</span><span class="sxs-lookup"><span data-stu-id="239c4-105">The following constants can be used when no subtype is required or when any subtype is required.</span></span>



| <span data-ttu-id="239c4-106">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="239c4-106">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="239c4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="239c4-107">Description</span></span>                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <span data-ttu-id="239c4-108"><dt>**Винбио \_ ПОДТИП \_ нет \_ сведений**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="239c4-108"><dt>**WINBIO\_SUBTYPE\_NO\_INFORMATION**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="239c4-109">Нет сведений о подтипе.</span><span class="sxs-lookup"><span data-stu-id="239c4-109">No subtype information.</span></span><br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <span data-ttu-id="239c4-110"><dt>**Винбио \_ ПОДТИП \_ любой**</dt> <dt>0xFF</dt></span><span class="sxs-lookup"><span data-stu-id="239c4-110"><dt>**WINBIO\_SUBTYPE\_ANY**</dt> <dt>0xFF</dt></span></span> </dl>                                   | <span data-ttu-id="239c4-111">Любой подтип.</span><span class="sxs-lookup"><span data-stu-id="239c4-111">Any subtype.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="239c4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="239c4-112">Remarks</span></span>

<span data-ttu-id="239c4-113">Чтобы найти доступные биометрические подтипы для конкретного биометрического типа, используйте следующую таблицу:</span><span class="sxs-lookup"><span data-stu-id="239c4-113">To find the available biometric subtypes for a particular biometric type, use the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="239c4-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> значение</span><span class="sxs-lookup"><span data-stu-id="239c4-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> value</span></span></th>
<th><span data-ttu-id="239c4-115">Разделы для поиска <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> значений</span><span class="sxs-lookup"><span data-stu-id="239c4-115">Topic(s) to find <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="239c4-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span><span class="sxs-lookup"><span data-stu-id="239c4-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span></span></td>
<td><span data-ttu-id="239c4-117"><a href="winbio-ansi-385-face-constants.md"><strong>Константы WINBIO_ANSI_385_FACE</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="239c4-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="239c4-118">Эти значения применяются только к Windows 10 и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="239c4-118">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="239c4-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span><span class="sxs-lookup"><span data-stu-id="239c4-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span></span></td>
<td><span data-ttu-id="239c4-120">Один из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="239c4-120">One of the following topics:</span></span>
<ul>
<li><span data-ttu-id="239c4-121"><a href="winbio-ansi-381-format-constants.md"><strong>Константы WINBIO_ANSI_381_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="239c4-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT Constants</strong></a></span></span></li>
<li><span data-ttu-id="239c4-122"><a href="winbio-ansi-381-img-constants.md"><strong>Константы WINBIO_ANSI_381_IMG</strong></a></span><span class="sxs-lookup"><span data-stu-id="239c4-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG Constants</strong></a></span></span></li>
<li><span data-ttu-id="239c4-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>Константы WINBIO_ANSI_381_IMG_ACQ</strong></a></span><span class="sxs-lookup"><span data-stu-id="239c4-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ Constants</strong></a></span></span></li>
<li><span data-ttu-id="239c4-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>Константы WINBIO_ANSI_381_IMP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="239c4-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE Constants</strong></a></span></span></li>
<li><span data-ttu-id="239c4-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>Константы WINBIO_ANSI_381_PIXELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="239c4-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS Constants</strong></a></span></span></li>
<li><span data-ttu-id="239c4-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>Константы отпечатка WINBIO_ANSI_381_POS</strong></a></span><span class="sxs-lookup"><span data-stu-id="239c4-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerprint Constants</strong></a></span></span></li>
<li><span data-ttu-id="239c4-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>Константы WINBIO_ANSI_381_POS_Palm</strong></a></span><span class="sxs-lookup"><span data-stu-id="239c4-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm Constants</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="239c4-128"><strong>WINBIO_TYPE_IRIS</strong></span><span class="sxs-lookup"><span data-stu-id="239c4-128"><strong>WINBIO_TYPE_IRIS</strong></span></span></td>
<td><span data-ttu-id="239c4-129"><a href="winbio-iris-constants.md"><strong>Константы WINBIO_IRIS</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="239c4-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="239c4-130">Эти значения применяются только к Windows 10 и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="239c4-130">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="239c4-131"><strong>WINBIO_TYPE_VOICE</strong></span><span class="sxs-lookup"><span data-stu-id="239c4-131"><strong>WINBIO_TYPE_VOICE</strong></span></span></td>
<td><span data-ttu-id="239c4-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>Константы WINBIO_VOICE</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="239c4-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="239c4-133">Эти значения применяются только к Windows 10 и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="239c4-133">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="239c4-134">Дополнительные сведения см. в разделе [константы клиентского приложения](client-application-constants.md).</span><span class="sxs-lookup"><span data-stu-id="239c4-134">For more information, see [Client Application Constants](client-application-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="239c4-135">Требования</span><span class="sxs-lookup"><span data-stu-id="239c4-135">Requirements</span></span>



| <span data-ttu-id="239c4-136">Требование</span><span class="sxs-lookup"><span data-stu-id="239c4-136">Requirement</span></span> | <span data-ttu-id="239c4-137">Значение</span><span class="sxs-lookup"><span data-stu-id="239c4-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239c4-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="239c4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="239c4-139">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="239c4-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="239c4-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="239c4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="239c4-141">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="239c4-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="239c4-142">Header</span><span class="sxs-lookup"><span data-stu-id="239c4-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="239c4-143"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="239c4-143"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





