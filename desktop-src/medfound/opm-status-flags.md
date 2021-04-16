---
description: Флаги в следующей таблице определяют состояние сеанса вывода диспетчера (ОПМ).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Флаги состояния ОПМ (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543855"
---
# <a name="opm-status-flags"></a><span data-ttu-id="471f1-103">Флаги состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="471f1-103">OPM Status Flags</span></span>

<span data-ttu-id="471f1-104">Флаги в следующей таблице определяют состояние сеанса вывода диспетчера (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="471f1-104">The flags in the following table specify the status of an Output Protection Manager (OPM) session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="471f1-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="471f1-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="471f1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="471f1-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <span data-ttu-id="471f1-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span><span class="sxs-lookup"><span data-stu-id="471f1-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="471f1-108">Нормальное состояние.</span><span class="sxs-lookup"><span data-stu-id="471f1-108">Normal status.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <span data-ttu-id="471f1-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span><span class="sxs-lookup"><span data-stu-id="471f1-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="471f1-110">Целостность подключения скомпрометирована.</span><span class="sxs-lookup"><span data-stu-id="471f1-110">The integrity of the connection has been compromised.</span></span> <span data-ttu-id="471f1-111">Ниже приведены примеры событий, которые вызывают установку драйвером этого флага.</span><span class="sxs-lookup"><span data-stu-id="471f1-111">Examples of events that cause the driver to set this flag include:</span></span><br/>
<ul>
<li><span data-ttu-id="471f1-112">Драйвер больше не может применить текущий уровень защиты.</span><span class="sxs-lookup"><span data-stu-id="471f1-112">The driver can no longer enforce the current protection level.</span></span></li>
<li><span data-ttu-id="471f1-113">Драйвер обнаружил внутреннюю ошибку целостности.</span><span class="sxs-lookup"><span data-stu-id="471f1-113">The driver detected an internal integrity error.</span></span></li>
<li><span data-ttu-id="471f1-114">Соединитель между компьютером и устройством дисплея был отсоединен.</span><span class="sxs-lookup"><span data-stu-id="471f1-114">The connector between the computer and the display device was unplugged.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <span data-ttu-id="471f1-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span><span class="sxs-lookup"><span data-stu-id="471f1-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="471f1-116">Конфигурация подключения изменилась.</span><span class="sxs-lookup"><span data-stu-id="471f1-116">The connection configuration has changed.</span></span> <span data-ttu-id="471f1-117">Например, пользователь изменил режим экрана рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="471f1-117">For example, the user has changed the desktop display mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <span data-ttu-id="471f1-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span><span class="sxs-lookup"><span data-stu-id="471f1-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="471f1-119">Графический адаптер или драйвер были изменены.</span><span class="sxs-lookup"><span data-stu-id="471f1-119">The graphics adapter or the driver has been tampered with.</span></span><br/> <span data-ttu-id="471f1-120">Этот флаг не используется в <em>режиме эмуляции Копп</em>.</span><span class="sxs-lookup"><span data-stu-id="471f1-120">This flag is not used in <em>COPP emulation mode</em>.</span></span> <span data-ttu-id="471f1-121">Вместо этого выходные данные видео задают флаг OPM_STATUS_LINK_LOST, если он обнаруживает несанкционированный вызов.</span><span class="sxs-lookup"><span data-stu-id="471f1-121">Instead, the video output will set the OPM_STATUS_LINK_LOST flag if it detects tampering.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <span data-ttu-id="471f1-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span><span class="sxs-lookup"><span data-stu-id="471f1-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="471f1-123">Отозванное High-Bandwidth устройства с цифровой Защита содержимого (HDCP) прикрепляется к выходным данным видео.</span><span class="sxs-lookup"><span data-stu-id="471f1-123">A revoked High-Bandwidth Digital Content Protection (HDCP) device is attached to the video output.</span></span><br/> <span data-ttu-id="471f1-124">Этот флаг состояния может быть возвращен из запроса <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> или <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> .</span><span class="sxs-lookup"><span data-stu-id="471f1-124">This status flag can be returned from an <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> or <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> query.</span></span> <br/> <span data-ttu-id="471f1-125">Отозванное устройство может быть подключено непосредственно к выходным данным видео или косвенно через повторитель HDCP.</span><span class="sxs-lookup"><span data-stu-id="471f1-125">The revoked device might be attached directly to the video output, or indirectly through an HDCP repeater.</span></span> <span data-ttu-id="471f1-126">Для обнаружения этого состояния в то время, когда HDCP включен, требуется вывод видео, но в противном случае — нет.</span><span class="sxs-lookup"><span data-stu-id="471f1-126">A video output is required to detect this condition while HDCP is enabled, but not otherwise.</span></span><br/> <span data-ttu-id="471f1-127">Этот флаг не используется в <em>режиме эмуляции Копп</em>, так как видеопотокы не обнаруживают отозванные устройства в этом режиме.</span><span class="sxs-lookup"><span data-stu-id="471f1-127">This flag is not used in <em>COPP emulation mode</em>, because the video output does not detect revoked devices in that mode.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="471f1-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="471f1-128">Remarks</span></span>

<span data-ttu-id="471f1-129">Некоторые из этих констант эквивалентны значениям из перечисления **Копп \_ статусфлагс** , используемого в сертифицированном протоколе защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="471f1-129">Some of these constants are equivalent to values from the **COPP\_StatusFlags** enumeration used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="471f1-130">Требования</span><span class="sxs-lookup"><span data-stu-id="471f1-130">Requirements</span></span>



| <span data-ttu-id="471f1-131">Требование</span><span class="sxs-lookup"><span data-stu-id="471f1-131">Requirement</span></span> | <span data-ttu-id="471f1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="471f1-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="471f1-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="471f1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="471f1-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="471f1-134">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="471f1-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="471f1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="471f1-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="471f1-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="471f1-137">Header</span><span class="sxs-lookup"><span data-stu-id="471f1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="471f1-138"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="471f1-138"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="471f1-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="471f1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471f1-140">Перечисления ОПМ</span><span class="sxs-lookup"><span data-stu-id="471f1-140">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




