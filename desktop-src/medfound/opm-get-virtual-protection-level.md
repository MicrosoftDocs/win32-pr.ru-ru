---
description: Возвращает уровень виртуальной защиты для указанного механизма защиты.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692588"
---
# <a name="opm_get_virtual_protection_level"></a><span data-ttu-id="35fd0-103">ОПМ \_ получить \_ \_ уровень защиты \_ виртуальной системы</span><span class="sxs-lookup"><span data-stu-id="35fd0-103">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="35fd0-104">Возвращает уровень виртуальной защиты для указанного механизма защиты.</span><span class="sxs-lookup"><span data-stu-id="35fd0-104">Returns the virtual protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="35fd0-105">Уровень защиты *виртуальной* системы — это уровень, запрошенный приложением во время текущего сеанса исходящего Protection Manager (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="35fd0-105">The *virtual* protection level is the level requested by the application during the current Output Protection Manager (OPM) session.</span></span> <span data-ttu-id="35fd0-106">Драйвер может применять более высокий уровень из-за событий за пределами этого сеанса ОПМ.</span><span class="sxs-lookup"><span data-stu-id="35fd0-106">The driver might apply a higher level, due to events outside of this OPM session.</span></span> <span data-ttu-id="35fd0-107">Чтобы найти фактический действующий уровень защиты, отправьте запрос на [**ОПМ \_ Получение \_ фактического \_ \_ уровня защиты**](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="35fd0-107">To find the actual protection level that is in effect, send the [**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**](opm-get-actual-protection-level.md) query.</span></span>



| <span data-ttu-id="35fd0-108">Требование</span><span class="sxs-lookup"><span data-stu-id="35fd0-108">Requirement</span></span> | <span data-ttu-id="35fd0-109">Значение</span><span class="sxs-lookup"><span data-stu-id="35fd0-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fd0-110">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="35fd0-110">Request GUID</span></span> | <span data-ttu-id="35fd0-111">ОПМ \_ получить \_ \_ уровень защиты \_ виртуальной системы</span><span class="sxs-lookup"><span data-stu-id="35fd0-111">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                          |
| <span data-ttu-id="35fd0-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="35fd0-112">Input data</span></span>   | <span data-ttu-id="35fd0-113">Механизм защиты для запроса, заданный как 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="35fd0-113">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="35fd0-114">Значение интерпретируется как член [**флагов типа защиты ОПМ**](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="35fd0-114">The value is interpreted as a member of the [**OPM Protection Type Flags**](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="35fd0-115">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="35fd0-115">Return data</span></span>  | <span data-ttu-id="35fd0-116">[**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="35fd0-116">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="35fd0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35fd0-117">Remarks</span></span>

<span data-ttu-id="35fd0-118">Уровень защиты возвращается в элементе **улинформатион** [**\_ \_ информационной структуры ОПМ Standard**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="35fd0-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="35fd0-119">Значение этого параметра зависит от механизма защиты, к которому выполняется запрос.</span><span class="sxs-lookup"><span data-stu-id="35fd0-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="35fd0-120">Для каждого механизма защиты значение **улинформатион** является флагом из другого перечисления, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="35fd0-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="35fd0-121">Механизм защиты</span><span class="sxs-lookup"><span data-stu-id="35fd0-121">Protection mechanism</span></span> | <span data-ttu-id="35fd0-122">Перечисление</span><span class="sxs-lookup"><span data-stu-id="35fd0-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="35fd0-123">ACP</span><span class="sxs-lookup"><span data-stu-id="35fd0-123">ACP</span></span>                  | [<span data-ttu-id="35fd0-124">**\_ \_ уровень защиты ОПМ \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="35fd0-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="35fd0-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="35fd0-125">CGMS-A</span></span>               | [<span data-ttu-id="35fd0-126">**Флаги защиты CGMS-A**</span><span class="sxs-lookup"><span data-stu-id="35fd0-126">**CGMS-A Protection Flags**</span></span>](cgms-a-protection-flags.md)        |
| <span data-ttu-id="35fd0-127">дпкп</span><span class="sxs-lookup"><span data-stu-id="35fd0-127">DPCP</span></span>                 | [<span data-ttu-id="35fd0-128">**\_ \_ уровень защиты ОПМ \_ ДПКП**</span><span class="sxs-lookup"><span data-stu-id="35fd0-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="35fd0-129">ПОДДЕРЖИВАЮЩ</span><span class="sxs-lookup"><span data-stu-id="35fd0-129">HDCP</span></span>                 | [<span data-ttu-id="35fd0-130">**\_ \_ уровень защиты ОПМ \_ HDCP**</span><span class="sxs-lookup"><span data-stu-id="35fd0-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="35fd0-131">Этот запрос эквивалентен \_ запросу дксва коппкуерилокалпротектионлевел, используемому в сертифицированном протоколе защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="35fd0-131">This query is equivalent to the DXVA\_COPPQueryLocalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="35fd0-132">Требования</span><span class="sxs-lookup"><span data-stu-id="35fd0-132">Requirements</span></span>



| <span data-ttu-id="35fd0-133">Требование</span><span class="sxs-lookup"><span data-stu-id="35fd0-133">Requirement</span></span> | <span data-ttu-id="35fd0-134">Значение</span><span class="sxs-lookup"><span data-stu-id="35fd0-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="35fd0-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35fd0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="35fd0-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35fd0-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="35fd0-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35fd0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="35fd0-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35fd0-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="35fd0-139">Header</span><span class="sxs-lookup"><span data-stu-id="35fd0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fd0-140"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="35fd0-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fd0-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35fd0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fd0-142">**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**</span><span class="sxs-lookup"><span data-stu-id="35fd0-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="35fd0-143">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="35fd0-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="35fd0-144">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="35fd0-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




