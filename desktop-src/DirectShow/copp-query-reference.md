---
description: Справочник по запросам Копп
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Справочник по запросам Копп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072321"
---
# <a name="copp-query-reference"></a><span data-ttu-id="b1652-103">Справочник по запросам Копп</span><span class="sxs-lookup"><span data-stu-id="b1652-103">COPP Query Reference</span></span>

<span data-ttu-id="b1652-104">В этом разделе описываются запросы состояния, поддерживаемые протоколом сертифицированной защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="b1652-104">This section describes the status queries that are supported by Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="b1652-105">Для каждого запроса отображается идентификатор GUID, определяющий запрос, а также входные данные и возвращаемые данные.</span><span class="sxs-lookup"><span data-stu-id="b1652-105">For each query, the GUID that defines the query is listed, along with the input data and return data.</span></span>



| <span data-ttu-id="b1652-106">Запрос</span><span class="sxs-lookup"><span data-stu-id="b1652-106">Query</span></span>                   | <span data-ttu-id="b1652-107">Код GUID</span><span class="sxs-lookup"><span data-stu-id="b1652-107">GUID</span></span>                                     |
|-------------------------|------------------------------------------|
| <span data-ttu-id="b1652-108">Данные шины</span><span class="sxs-lookup"><span data-stu-id="b1652-108">Bus Data</span></span>                | <span data-ttu-id="b1652-109">**ДКСВА \_ коппкуерибусдата**</span><span class="sxs-lookup"><span data-stu-id="b1652-109">**DXVA\_COPPQueryBusData**</span></span>               |
| <span data-ttu-id="b1652-110">Тип соединителя</span><span class="sxs-lookup"><span data-stu-id="b1652-110">Connector Type</span></span>          | <span data-ttu-id="b1652-111">**ДКСВА \_ коппкуериконнектортипе**</span><span class="sxs-lookup"><span data-stu-id="b1652-111">**DXVA\_COPPQueryConnectorType**</span></span>         |
| <span data-ttu-id="b1652-112">Отображение данных</span><span class="sxs-lookup"><span data-stu-id="b1652-112">Display Data</span></span>            | <span data-ttu-id="b1652-113">**ДКСВА \_ коппкуеридисплайдата**</span><span class="sxs-lookup"><span data-stu-id="b1652-113">**DXVA\_COPPQueryDisplayData**</span></span>           |
| <span data-ttu-id="b1652-114">Данные ключа HDCP</span><span class="sxs-lookup"><span data-stu-id="b1652-114">HDCP Key Data</span></span>           | <span data-ttu-id="b1652-115">**ДКСВА \_ коппкуерихдкпкэйдата**</span><span class="sxs-lookup"><span data-stu-id="b1652-115">**DXVA\_COPPQueryHDCPKeyData**</span></span>           |
| <span data-ttu-id="b1652-116">Глобальный уровень защиты</span><span class="sxs-lookup"><span data-stu-id="b1652-116">Global Protection Level</span></span> | <span data-ttu-id="b1652-117">**ДКСВА \_ коппкуериглобалпротектионлевел**</span><span class="sxs-lookup"><span data-stu-id="b1652-117">**DXVA\_COPPQueryGlobalProtectionLevel**</span></span> |
| <span data-ttu-id="b1652-118">Локальный уровень защиты</span><span class="sxs-lookup"><span data-stu-id="b1652-118">Local Protection Level</span></span>  | <span data-ttu-id="b1652-119">**ДКСВА \_ коппкуерилокалпротектионлевел**</span><span class="sxs-lookup"><span data-stu-id="b1652-119">**DXVA\_COPPQueryLocalProtectionLevel**</span></span>  |
| <span data-ttu-id="b1652-120">Тип защиты</span><span class="sxs-lookup"><span data-stu-id="b1652-120">Protection Type</span></span>         | <span data-ttu-id="b1652-121">**ДКСВА \_ коппкуерипротектионтипе**</span><span class="sxs-lookup"><span data-stu-id="b1652-121">**DXVA\_COPPQueryProtectionType**</span></span>        |
| <span data-ttu-id="b1652-122">Сигнальный NaN</span><span class="sxs-lookup"><span data-stu-id="b1652-122">Signaling</span></span>               | <span data-ttu-id="b1652-123">**ДКСВА \_ коппкуерисигналинг**</span><span class="sxs-lookup"><span data-stu-id="b1652-123">**DXVA\_COPPQuerySignaling**</span></span>             |



 

<span data-ttu-id="b1652-124">Запрос данных шины</span><span class="sxs-lookup"><span data-stu-id="b1652-124">Bus Data Query</span></span>

<span data-ttu-id="b1652-125">Возвращает тип шины ввода-вывода, используемой графическим адаптером.</span><span class="sxs-lookup"><span data-stu-id="b1652-125">Returns the type of I/O bus used by the graphics adapter.</span></span>

-   <span data-ttu-id="b1652-126">**GUID**: дксва \_ коппкуерибусдата</span><span class="sxs-lookup"><span data-stu-id="b1652-126">**GUID**: DXVA\_COPPQueryBusData</span></span>
-   <span data-ttu-id="b1652-127">**Входные данные**: нет.</span><span class="sxs-lookup"><span data-stu-id="b1652-127">**Input data**: None.</span></span>
-   <span data-ttu-id="b1652-128">**Возвращаемые данные**: возвращает [**структуру \_ коппстатусдата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="b1652-128">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="b1652-129">Тип шины возвращается в члене **двдата** в виде флага из перечисления [**Копп \_ BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) .</span><span class="sxs-lookup"><span data-stu-id="b1652-129">The bus type is returned in the **dwData** member as a flag from the [**COPP\_BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) enumeration.</span></span>

<span data-ttu-id="b1652-130">Запрос типа соединителя</span><span class="sxs-lookup"><span data-stu-id="b1652-130">Connector Type Query</span></span>

<span data-ttu-id="b1652-131">Возвращает тип физического соединителя.</span><span class="sxs-lookup"><span data-stu-id="b1652-131">Returns the physical connector type.</span></span>

-   <span data-ttu-id="b1652-132">**GUID**: дксва \_ коппкуериконнектортипе</span><span class="sxs-lookup"><span data-stu-id="b1652-132">**GUID**: DXVA\_COPPQueryConnectorType</span></span>
-   <span data-ttu-id="b1652-133">**Входные данные**: нет.</span><span class="sxs-lookup"><span data-stu-id="b1652-133">**Input data**: None.</span></span>
-   <span data-ttu-id="b1652-134">**Возвращаемые данные**: возвращает [**структуру \_ коппстатусдата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="b1652-134">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="b1652-135">Тип соединителя возвращается в члене **двдата** в виде флага из перечисления [**Копп \_ коннектортипе**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) .</span><span class="sxs-lookup"><span data-stu-id="b1652-135">The connector type is returned in the **dwData** member as a flag from the [**COPP\_ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) enumeration.</span></span>

<span data-ttu-id="b1652-136">Запрос на отображение данных</span><span class="sxs-lookup"><span data-stu-id="b1652-136">Display Data Query</span></span>

<span data-ttu-id="b1652-137">Возвращает описание видеосигнала, передаваемого через соединитель.</span><span class="sxs-lookup"><span data-stu-id="b1652-137">Returns a description of the video signal that is being transmitted over the connector.</span></span>

<span data-ttu-id="b1652-138">Видеосигнал, передаваемый через соединитель, не обязательно имеет тот же формат, что и режим экрана рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b1652-138">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="b1652-139">Например, режим экрана рабочего стола может составлять 1024x768 пикселей в 85 Гц, а соединитель может быть соединителем S-Video, передающий видеосигналы в 720x480 пикселях, 60/1.01 Гц с чередованием.</span><span class="sxs-lookup"><span data-stu-id="b1652-139">For example, the desktop display mode might be 1024x768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720x480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="b1652-140">В этом случае драйвер вернет разрешение видеосигнала S-Video, а не разрешение рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b1652-140">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

-   <span data-ttu-id="b1652-141">**GUID**: дксва \_ коппкуеридисплайдата</span><span class="sxs-lookup"><span data-stu-id="b1652-141">**GUID**: DXVA\_COPPQueryDisplayData</span></span>
-   <span data-ttu-id="b1652-142">**Входные данные**: нет.</span><span class="sxs-lookup"><span data-stu-id="b1652-142">**Input data**: None.</span></span>
-   <span data-ttu-id="b1652-143">**Возвращаемые данные**: возвращает [**структуру \_ коппстатусдисплайдата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) .</span><span class="sxs-lookup"><span data-stu-id="b1652-143">**Return data**: Returns a [**DXVA\_COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) structure.</span></span>

<span data-ttu-id="b1652-144">Запрос данных ключа HDCP</span><span class="sxs-lookup"><span data-stu-id="b1652-144">HDCP Key Data Query</span></span>

<span data-ttu-id="b1652-145">Возвращает вектор выбора ключа HDCP устройства (B-КСВ).</span><span class="sxs-lookup"><span data-stu-id="b1652-145">Returns the device's HDCP key selection vector (B-KSV).</span></span>

<span data-ttu-id="b1652-146">КСВ — это идентификатор, предоставленный изготовителю устройства и используемый в процессе проверки подлинности и установки HDCP.</span><span class="sxs-lookup"><span data-stu-id="b1652-146">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="b1652-147">Приложение должно проверить это значение в списке отозванных КСВС.</span><span class="sxs-lookup"><span data-stu-id="b1652-147">The application should check this value against the list of revoked KSVs.</span></span> <span data-ttu-id="b1652-148">Механизм получения списка отзыва КСВ выходит за пределы области действия протокола Копп.</span><span class="sxs-lookup"><span data-stu-id="b1652-148">The mechanism for obtaining the KSV revocation list is outside the scope of the COPP protocol.</span></span> <span data-ttu-id="b1652-149">Дополнительные сведения см. в спецификации HDCP.</span><span class="sxs-lookup"><span data-stu-id="b1652-149">For more information, consult the HDCP specification.</span></span>

<span data-ttu-id="b1652-150">Этот запрос также определяет, является ли подключенное устройство HDCP монитором или повторителем HDCP.</span><span class="sxs-lookup"><span data-stu-id="b1652-150">This query also determines whether the connected HDCP device is a monitor or an HDCP repeater.</span></span> <span data-ttu-id="b1652-151">Приложение не должно воспроизводить защищенное содержимое, если устройство HDCP является повторителем HDCP, так как оно не поддерживается Копп.</span><span class="sxs-lookup"><span data-stu-id="b1652-151">The application should not play protected content if the HDCP device is an HDCP repeater, because these are not supported by COPP.</span></span>

-   <span data-ttu-id="b1652-152">**GUID**: дксва \_ коппкуерихдкпкэйдата</span><span class="sxs-lookup"><span data-stu-id="b1652-152">**GUID**: DXVA\_COPPQueryHDCPKeyData</span></span>
-   <span data-ttu-id="b1652-153">**Входные данные**: нет.</span><span class="sxs-lookup"><span data-stu-id="b1652-153">**Input data**: None.</span></span>
-   <span data-ttu-id="b1652-154">**Возвращаемые данные**: возвращает [**структуру \_ коппстатушдкпкэйдата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) .</span><span class="sxs-lookup"><span data-stu-id="b1652-154">**Return data**: Returns a [**DXVA\_COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) structure.</span></span>

<span data-ttu-id="b1652-155">Запрос уровня глобальной защиты</span><span class="sxs-lookup"><span data-stu-id="b1652-155">Global Protection Level Query</span></span>

<span data-ttu-id="b1652-156">Возвращает глобальный уровень защиты для указанного механизма защиты.</span><span class="sxs-lookup"><span data-stu-id="b1652-156">Returns the global protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="b1652-157">Глобальный уровень защиты — это уровень защиты, применяемый в данный момент к соединителю, независимо от того, каким способом был назначен драйвер графики для применения защиты.</span><span class="sxs-lookup"><span data-stu-id="b1652-157">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="b1652-158">Например, приложение может установить уровень защиты ACP, вызвав функцию **чанжедисплайсеттингсекс** .</span><span class="sxs-lookup"><span data-stu-id="b1652-158">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="b1652-159">В этом случае уровень глобальной защиты будет отражать этот параметр, даже если он не был запрошен через Копп.</span><span class="sxs-lookup"><span data-stu-id="b1652-159">In that case, the global protection level would reflect this setting, even though it was not requested through COPP.</span></span>

-   <span data-ttu-id="b1652-160">**GUID**: дксва \_ коппкуериглобалпротектионлевел</span><span class="sxs-lookup"><span data-stu-id="b1652-160">**GUID**: DXVA\_COPPQueryGlobalProtectionLevel</span></span>
-   <span data-ttu-id="b1652-161">**Входные данные**: механизм защиты для запроса, заданный как 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="b1652-161">**Input data**: The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="b1652-162">См. раздел [Флаги типа защиты Копп](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b1652-162">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="b1652-163">**Возвращаемые данные**: возвращает [**структуру \_ коппстатусдата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="b1652-163">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="b1652-164">Текущий уровень защиты возвращается в элементе **двдата** .</span><span class="sxs-lookup"><span data-stu-id="b1652-164">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="b1652-165">Значение этого параметра зависит от механизма защиты, к которому выполняется запрос.</span><span class="sxs-lookup"><span data-stu-id="b1652-165">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="b1652-166">Для каждого механизма защиты значение элемента **двдата** является флагом из другого перечисления, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b1652-166">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="b1652-167">Механизм защиты</span><span class="sxs-lookup"><span data-stu-id="b1652-167">Protection mechanism</span></span> | <span data-ttu-id="b1652-168">Перечисление</span><span class="sxs-lookup"><span data-stu-id="b1652-168">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="b1652-169">ACP</span><span class="sxs-lookup"><span data-stu-id="b1652-169">ACP</span></span>                  | [<span data-ttu-id="b1652-170">**\_ \_ Уровень защиты Копп \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="b1652-170">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="b1652-171">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="b1652-171">CGMS-A</span></span>               | [<span data-ttu-id="b1652-172">**\_ \_ Уровень защиты Копп \_ кгмса**</span><span class="sxs-lookup"><span data-stu-id="b1652-172">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="b1652-173">ПОДДЕРЖИВАЮЩ</span><span class="sxs-lookup"><span data-stu-id="b1652-173">HDCP</span></span>                 | [<span data-ttu-id="b1652-174">**\_ \_ Уровень защиты Копп \_ HDCP**</span><span class="sxs-lookup"><span data-stu-id="b1652-174">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="b1652-175">Локальный запрос уровня защиты</span><span class="sxs-lookup"><span data-stu-id="b1652-175">Local Protection Level Query</span></span>

<span data-ttu-id="b1652-176">Возвращает локальный уровень защиты для указанного механизма защиты.</span><span class="sxs-lookup"><span data-stu-id="b1652-176">Returns the local protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="b1652-177">Локальный уровень защиты — это уровень защиты, запрошенный в текущем сеансе Копп.</span><span class="sxs-lookup"><span data-stu-id="b1652-177">The local protection level is the protection level that was requested through the current COPP session.</span></span> <span data-ttu-id="b1652-178">Драйвер может установить более высокий уровень защиты.</span><span class="sxs-lookup"><span data-stu-id="b1652-178">The driver might set a higher protection level.</span></span>

-   <span data-ttu-id="b1652-179">**GUID**: дксва \_ коппкуерилокалпротектионлевел</span><span class="sxs-lookup"><span data-stu-id="b1652-179">**GUID**: DXVA\_COPPQueryLocalProtectionLevel</span></span>
-   <span data-ttu-id="b1652-180">**Входные данные**: механизм защиты для запроса в виде 32-разрядного целого числа.</span><span class="sxs-lookup"><span data-stu-id="b1652-180">**Input data**: The protection mechanism to query, as a 32-bit integer.</span></span> <span data-ttu-id="b1652-181">См. раздел [Флаги типа защиты Копп](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b1652-181">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="b1652-182">**Возвращаемые данные**: возвращает [**структуру \_ коппстатусдата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="b1652-182">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="b1652-183">Текущий уровень защиты возвращается в элементе **двдата** .</span><span class="sxs-lookup"><span data-stu-id="b1652-183">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="b1652-184">Значение этого параметра зависит от механизма защиты, к которому выполняется запрос.</span><span class="sxs-lookup"><span data-stu-id="b1652-184">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="b1652-185">Для каждого механизма защиты значение элемента **двдата** является флагом из другого перечисления, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b1652-185">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="b1652-186">Механизм защиты</span><span class="sxs-lookup"><span data-stu-id="b1652-186">Protection mechanism</span></span> | <span data-ttu-id="b1652-187">Перечисление</span><span class="sxs-lookup"><span data-stu-id="b1652-187">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="b1652-188">ACP</span><span class="sxs-lookup"><span data-stu-id="b1652-188">ACP</span></span>                  | [<span data-ttu-id="b1652-189">**\_ \_ Уровень защиты Копп \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="b1652-189">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="b1652-190">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="b1652-190">CGMS-A</span></span>               | [<span data-ttu-id="b1652-191">**\_ \_ Уровень защиты Копп \_ кгмса**</span><span class="sxs-lookup"><span data-stu-id="b1652-191">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="b1652-192">ПОДДЕРЖИВАЮЩ</span><span class="sxs-lookup"><span data-stu-id="b1652-192">HDCP</span></span>                 | [<span data-ttu-id="b1652-193">**\_ \_ Уровень защиты Копп \_ HDCP**</span><span class="sxs-lookup"><span data-stu-id="b1652-193">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="b1652-194">Запрос типа защиты</span><span class="sxs-lookup"><span data-stu-id="b1652-194">Protection Type Query</span></span>

<span data-ttu-id="b1652-195">Возвращает механизмы защиты, доступные для соединителя.</span><span class="sxs-lookup"><span data-stu-id="b1652-195">Returns the protection mechanisms that are available for the connector.</span></span>

-   <span data-ttu-id="b1652-196">**GUID**: дксва \_ коппкуерипротектионтипе</span><span class="sxs-lookup"><span data-stu-id="b1652-196">**GUID**: DXVA\_COPPQueryProtectionType</span></span>
-   <span data-ttu-id="b1652-197">**Входные данные**: нет.</span><span class="sxs-lookup"><span data-stu-id="b1652-197">**Input data**: None.</span></span>
-   <span data-ttu-id="b1652-198">**Возвращаемые данные**: возвращает [**структуру \_ коппстатусдата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="b1652-198">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="b1652-199">Механизмы защиты возвращаются в члене **двдата** как сочетание одного или нескольких флагов.</span><span class="sxs-lookup"><span data-stu-id="b1652-199">The protection mechanisms are returned in the **dwData** member as a combination of zero or more flags.</span></span> <span data-ttu-id="b1652-200">См. раздел [Флаги типа защиты Копп](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b1652-200">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span> <span data-ttu-id="b1652-201">Если доступно более одного механизма защиты, флаги объединяются с побитовой **или**.</span><span class="sxs-lookup"><span data-stu-id="b1652-201">If more than one protection mechanism is available, the flags are combined with a bitwise **OR**.</span></span>

<span data-ttu-id="b1652-202">Запрос сигнала</span><span class="sxs-lookup"><span data-stu-id="b1652-202">Signaling Query</span></span>

<span data-ttu-id="b1652-203">Возвращает список всех стандартов защиты, поддерживаемых драйвером, стандарт, который активен в данный момент, а также текущие пропорции и другие данные о сигналах.</span><span class="sxs-lookup"><span data-stu-id="b1652-203">Returns a list of all the protection standards that are supported by the driver, the standard that is currently active, and the current aspect ratio or other signaling data.</span></span>

-   <span data-ttu-id="b1652-204">**GUID**: дксва \_ коппкуерисигналинг</span><span class="sxs-lookup"><span data-stu-id="b1652-204">**GUID**: DXVA\_COPPQuerySignaling</span></span>
-   <span data-ttu-id="b1652-205">**Входные данные**: нет.</span><span class="sxs-lookup"><span data-stu-id="b1652-205">**Input data**: None.</span></span>
-   <span data-ttu-id="b1652-206">**Возвращаемые данные**: возвращает [**структуру \_ коппстатуссигналингкмддата дксва**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="b1652-206">**Return data**: Returns a [**DXVA\_COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1652-207">См. также</span><span class="sxs-lookup"><span data-stu-id="b1652-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1652-208">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="b1652-208">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



