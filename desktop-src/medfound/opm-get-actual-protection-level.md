---
description: Возвращает глобальный уровень защиты для указанного механизма защиты.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080431"
---
# <a name="opm_get_actual_protection_level"></a><span data-ttu-id="46f64-103">ОПМ \_ получить \_ фактический \_ \_ уровень защиты</span><span class="sxs-lookup"><span data-stu-id="46f64-103">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="46f64-104">Возвращает глобальный уровень защиты для указанного механизма защиты.</span><span class="sxs-lookup"><span data-stu-id="46f64-104">Returns the global protection level for a specified protection mechanism.</span></span>



| <span data-ttu-id="46f64-105">Требование</span><span class="sxs-lookup"><span data-stu-id="46f64-105">Requirement</span></span> | <span data-ttu-id="46f64-106">Значение</span><span class="sxs-lookup"><span data-stu-id="46f64-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f64-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="46f64-107">Request GUID</span></span> | <span data-ttu-id="46f64-108">ОПМ \_ получить \_ фактический \_ \_ уровень защиты</span><span class="sxs-lookup"><span data-stu-id="46f64-108">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                       |
| <span data-ttu-id="46f64-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="46f64-109">Input data</span></span>   | <span data-ttu-id="46f64-110">Механизм защиты для запроса, заданный как 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="46f64-110">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="46f64-111">Значение интерпретируется как член [флагов типа защиты ОПМ](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="46f64-111">The value is interpreted as a member of the [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="46f64-112">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="46f64-112">Return data</span></span>  | <span data-ttu-id="46f64-113">[**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="46f64-113">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="46f64-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46f64-114">Remarks</span></span>

<span data-ttu-id="46f64-115">Глобальный уровень защиты — это уровень защиты, применяемый в данный момент к соединителю, независимо от того, каким способом был назначен драйвер графики для применения защиты.</span><span class="sxs-lookup"><span data-stu-id="46f64-115">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="46f64-116">Например, приложение может установить уровень защиты ACP, вызвав функцию **чанжедисплайсеттингсекс** .</span><span class="sxs-lookup"><span data-stu-id="46f64-116">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="46f64-117">В этом случае уровень глобальной защиты будет отражать этот параметр, даже если он не был запрошен с помощью Output Protection Manager (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="46f64-117">In that case, the global protection level would reflect this setting, even though it was not requested through Output Protection Manager (OPM).</span></span>

<span data-ttu-id="46f64-118">Уровень защиты возвращается в элементе **улинформатион** [**\_ \_ информационной структуры ОПМ Standard**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="46f64-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="46f64-119">Значение этого параметра зависит от механизма защиты, к которому выполняется запрос.</span><span class="sxs-lookup"><span data-stu-id="46f64-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="46f64-120">Для каждого механизма защиты значение **улинформатион** является флагом из другого перечисления, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="46f64-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="46f64-121">Механизм защиты</span><span class="sxs-lookup"><span data-stu-id="46f64-121">Protection mechanism</span></span> | <span data-ttu-id="46f64-122">Перечисление</span><span class="sxs-lookup"><span data-stu-id="46f64-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="46f64-123">ACP</span><span class="sxs-lookup"><span data-stu-id="46f64-123">ACP</span></span>                  | [<span data-ttu-id="46f64-124">**\_ \_ уровень защиты ОПМ \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="46f64-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="46f64-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="46f64-125">CGMS-A</span></span>               | [<span data-ttu-id="46f64-126">Флаги защиты CGMS-A</span><span class="sxs-lookup"><span data-stu-id="46f64-126">CGMS-A Protection Flags</span></span>](cgms-a-protection-flags.md)            |
| <span data-ttu-id="46f64-127">дпкп</span><span class="sxs-lookup"><span data-stu-id="46f64-127">DPCP</span></span>                 | [<span data-ttu-id="46f64-128">**\_ \_ уровень защиты ОПМ \_ ДПКП**</span><span class="sxs-lookup"><span data-stu-id="46f64-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="46f64-129">ПОДДЕРЖИВАЮЩ</span><span class="sxs-lookup"><span data-stu-id="46f64-129">HDCP</span></span>                 | [<span data-ttu-id="46f64-130">**\_ \_ уровень защиты ОПМ \_ HDCP**</span><span class="sxs-lookup"><span data-stu-id="46f64-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="46f64-131">Этот запрос эквивалентен \_ запросу дксва коппкуериглобалпротектионлевел, используемому в сертифицированном протоколе защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="46f64-131">This query is equivalent to the DXVA\_COPPQueryGlobalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="46f64-132">Требования</span><span class="sxs-lookup"><span data-stu-id="46f64-132">Requirements</span></span>



| <span data-ttu-id="46f64-133">Требование</span><span class="sxs-lookup"><span data-stu-id="46f64-133">Requirement</span></span> | <span data-ttu-id="46f64-134">Значение</span><span class="sxs-lookup"><span data-stu-id="46f64-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46f64-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46f64-135">Minimum supported client</span></span><br/> | <span data-ttu-id="46f64-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46f64-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="46f64-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46f64-137">Minimum supported server</span></span><br/> | <span data-ttu-id="46f64-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46f64-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="46f64-139">Header</span><span class="sxs-lookup"><span data-stu-id="46f64-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="46f64-140"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="46f64-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46f64-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46f64-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f64-142">**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**</span><span class="sxs-lookup"><span data-stu-id="46f64-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="46f64-143">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="46f64-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="46f64-144">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="46f64-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




