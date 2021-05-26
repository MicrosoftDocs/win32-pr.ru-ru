---
title: Стандартные версии элементов управления
description: В этом разделе перечислены доступные версии библиотеки общих элементов управления (ComCtl32.dll), описаны способы определения версии, используемой приложением, и объясняется, как выбрать целевое приложение для конкретной версии.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1131466bd4d3afcaae3a241a6f7854fd5a49450
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423964"
---
# <a name="common-control-versions"></a><span data-ttu-id="3ab3a-103">Стандартные версии элементов управления</span><span class="sxs-lookup"><span data-stu-id="3ab3a-103">Common Control Versions</span></span>

<span data-ttu-id="3ab3a-104">В этом разделе перечислены доступные версии библиотеки общих элементов управления (ComCtl32.dll), описаны способы определения версии, используемой приложением, и объясняется, как выбрать целевое приложение для конкретной версии.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-104">This topic lists the available versions of the Common Control library (ComCtl32.dll), describes how to identify the version that your application is using, and explains how to target your application for a specific version.</span></span>

<span data-ttu-id="3ab3a-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3ab3a-106">Номера версий библиотеки общих элементов управления</span><span class="sxs-lookup"><span data-stu-id="3ab3a-106">Common Control DLL Versions Numbers</span></span>](#common-control-dll-versions-numbers)
-   [<span data-ttu-id="3ab3a-107">Размеры структуры для различных стандартных версий элементов управления</span><span class="sxs-lookup"><span data-stu-id="3ab3a-107">Structure Sizes for Different Common Control Versions</span></span>](#structure-sizes-for-different-common-control-versions)
-   [<span data-ttu-id="3ab3a-108">Определение номера версии с помощью Дллжетверсион</span><span class="sxs-lookup"><span data-stu-id="3ab3a-108">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
-   [<span data-ttu-id="3ab3a-109">Версии проекта</span><span class="sxs-lookup"><span data-stu-id="3ab3a-109">Project Versions</span></span>](#project-versions)
-   [<span data-ttu-id="3ab3a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="3ab3a-110">Related topics</span></span>](#related-topics)

## <a name="common-control-dll-versions-numbers"></a><span data-ttu-id="3ab3a-111">Номера версий библиотеки общих элементов управления</span><span class="sxs-lookup"><span data-stu-id="3ab3a-111">Common Control DLL Versions Numbers</span></span>

<span data-ttu-id="3ab3a-112">Поддержка стандартных элементов управления обеспечивается ComCtl32.dll, которые включают в себя все 32-разрядные и 64-разрядные версии Windows.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-112">Support for common controls is provided by ComCtl32.dll, which all 32-bit and 64-bit versions of Windows include.</span></span> <span data-ttu-id="3ab3a-113">Каждая последовательная версия библиотеки DLL поддерживает функции и API более ранних версий и добавляет новые функции.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-113">Each successive version of the DLL supports the features and API of earlier versions and adds new features.</span></span>

<span data-ttu-id="3ab3a-114">Поскольку различные версии ComCtl32.dll были распространены с помощью Internet Explorer, активная версия иногда отличается от версии, поставляемой с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-114">Because various versions of ComCtl32.dll were distributed with Internet Explorer, the version that is active is sometimes different from the version that was shipped with the operating system.</span></span> <span data-ttu-id="3ab3a-115">Поэтому приложение должно напрямую определить, какая версия ComCtl32.dll установлена.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-115">Therefore, your application must directly determine which version of ComCtl32.dll is present.</span></span>

<span data-ttu-id="3ab3a-116">В справочной документации по общим элементам управления во многих программных элементах указывается минимальный поддерживаемый номер версии DLL.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-116">In the common controls reference documentation, many programming elements specify a minimum supported DLL version number.</span></span> <span data-ttu-id="3ab3a-117">Этот номер версии указывает, что программный элемент реализован в этой версии и последующих версиях библиотеки DLL, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-117">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="3ab3a-118">Если номер версии не указан, программный элемент реализуется во всех существующих версиях библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-118">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="3ab3a-119">В следующей таблице приведены различные версии библиотек DLL и их распределение по поддерживаемым ОС.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-119">The following table outlines the different DLL versions and how they were distributed on supported OSes.</span></span>



<span data-ttu-id="3ab3a-120">ComCtl32.dll</span><span class="sxs-lookup"><span data-stu-id="3ab3a-120">ComCtl32.dll</span></span>

<span data-ttu-id="3ab3a-121">Версия</span><span class="sxs-lookup"><span data-stu-id="3ab3a-121">Version</span></span>

<span data-ttu-id="3ab3a-122">Платформа распространения</span><span class="sxs-lookup"><span data-stu-id="3ab3a-122">Distribution Platform</span></span>

<span data-ttu-id="3ab3a-123">5,81</span><span class="sxs-lookup"><span data-stu-id="3ab3a-123">5.81</span></span>

<span data-ttu-id="3ab3a-124">Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 и Microsoft Internet Explorer 6</span><span class="sxs-lookup"><span data-stu-id="3ab3a-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5, and Microsoft Internet Explorer 6</span></span>

<span data-ttu-id="3ab3a-125">5,82</span><span class="sxs-lookup"><span data-stu-id="3ab3a-125">5.82</span></span>

<span data-ttu-id="3ab3a-126">Windows Server 2003, Windows Vista, Windows Server 2008 и Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ab3a-126">Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7</span></span>

<span data-ttu-id="3ab3a-127">6,0</span><span class="sxs-lookup"><span data-stu-id="3ab3a-127">6.0</span></span>

<span data-ttu-id="3ab3a-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ab3a-128">Windows Server 2003</span></span>

<span data-ttu-id="3ab3a-129">6.10</span><span class="sxs-lookup"><span data-stu-id="3ab3a-129">6.10</span></span>

<span data-ttu-id="3ab3a-130">Windows Vista, Windows Server 2008 и Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ab3a-130">Windows Vista, Windows Server 2008, and Windows 7</span></span>



 

## <a name="structure-sizes-for-different-common-control-versions"></a><span data-ttu-id="3ab3a-131">Размеры структуры для различных стандартных версий элементов управления</span><span class="sxs-lookup"><span data-stu-id="3ab3a-131">Structure Sizes for Different Common Control Versions</span></span>

<span data-ttu-id="3ab3a-132">Текущие усовершенствования стандартных элементов управления приводят к необходимости расширения многих структур.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-132">Ongoing enhancements to common controls have resulted in the need to extend many of the structures.</span></span> <span data-ttu-id="3ab3a-133">По этой причине размер структур изменился между различными версиями Коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-133">For this reason, the size of the structures has changed between different versions of Commctrl.h.</span></span> <span data-ttu-id="3ab3a-134">Так как большая часть общих структур управления принимает размер структуры как один из параметров, сообщение или функция может завершиться ошибкой, если размер не распознан.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-134">Because most of the common control structures take a structure size as one of the parameters, a message or function can fail if the size is not recognized.</span></span> <span data-ttu-id="3ab3a-135">Чтобы устранить эту проблему, были определены константы размера структуры, чтобы помочь в нацеливании на другую версию ComCtl32.dll.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-135">To remedy this, structure size constants have been defined to aid in targeting different version of ComCtl32.dll.</span></span> <span data-ttu-id="3ab3a-136">В следующем списке определяются константы размера структуры.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-136">The following list defines the structure size constants.</span></span>



|    <span data-ttu-id="3ab3a-137">Константа размера структуры</span><span class="sxs-lookup"><span data-stu-id="3ab3a-137">Structure Size Constant</span></span>                           |     <span data-ttu-id="3ab3a-138">Определение</span><span class="sxs-lookup"><span data-stu-id="3ab3a-138">Definition</span></span>                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab3a-139">\_Размер хдитем v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-139">HDITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="3ab3a-140">Размер структуры [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-140">The size of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="3ab3a-141">\_Размер имажелистдравпарамс v3 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-141">IMAGELISTDRAWPARAMS\_V3\_SIZE</span></span> | <span data-ttu-id="3ab3a-142">Размер структуры [**имажелистдравпарамс**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) в версии 5,9.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-142">The size of the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) structure in version 5.9.</span></span> |
| <span data-ttu-id="3ab3a-143">\_Размер LVCOLUMN v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-143">LVCOLUMN\_V1\_SIZE</span></span>            | <span data-ttu-id="3ab3a-144">Размер структуры [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-144">The size of the [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="3ab3a-145">\_Размер лвграуп V5 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-145">LVGROUP\_V5\_SIZE</span></span>             | <span data-ttu-id="3ab3a-146">Размер структуры [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) в версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-146">The size of the [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure in version 6.0.</span></span>                         |
| <span data-ttu-id="3ab3a-147">\_Размер лвхиттестинфо v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-147">LVHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="3ab3a-148">Размер структуры [**лвхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-148">The size of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="3ab3a-149">\_Размер лвитем v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-149">LVITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="3ab3a-150">Размер структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-150">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="3ab3a-151">\_Размер лвитем V5 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-151">LVITEM\_V5\_SIZE</span></span>              | <span data-ttu-id="3ab3a-152">Размер структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) в версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-152">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 6.0.</span></span>                           |
| <span data-ttu-id="3ab3a-153">\_Размер лвтилеинфо V5 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-153">LVTILEINFO\_V5\_SIZE</span></span>          | <span data-ttu-id="3ab3a-154">Размер структуры [**лвтилеинфо**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) в версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-154">The size of the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure in version 6.0.</span></span>                   |
| <span data-ttu-id="3ab3a-155">\_Размер мчиттестинфо v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-155">MCHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="3ab3a-156">Размер структуры [**мчиттестинфо**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-156">The size of the [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="3ab3a-157">\_Размер нмлвкустомдрав v3 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-157">NMLVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="3ab3a-158">Размер структуры [**нмлвкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) в версии 4,7.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-158">The size of the [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="3ab3a-159">\_Размер нмттдиспинфо v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-159">NMTTDISPINFO\_V1\_SIZE</span></span>        | <span data-ttu-id="3ab3a-160">Размер структуры [**нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-160">The size of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure in version 4.0.</span></span>               |
| <span data-ttu-id="3ab3a-161">\_Размер нмтвкустомдрав v3 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-161">NMTVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="3ab3a-162">Размер структуры [**нмтвкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) в версии 4,7.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-162">The size of the [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="3ab3a-163">\_Размер пропшисеадер v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-163">PROPSHEETHEADER\_V1\_SIZE</span></span>     | <span data-ttu-id="3ab3a-164">Размер структуры [**пропшисеадер**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-164">The size of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure in version 4.0.</span></span>         |
| <span data-ttu-id="3ab3a-165">\_Размер пропшитпаже v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-165">PROPSHEETPAGE\_V1\_SIZE</span></span>       | <span data-ttu-id="3ab3a-166">Размер структуры [**пропшитпаже**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-166">The size of the [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) structure in version 4.0.</span></span>             |
| <span data-ttu-id="3ab3a-167">\_Размер ребарбандинфо v3 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-167">REBARBANDINFO\_V3\_SIZE</span></span>       | <span data-ttu-id="3ab3a-168">Размер структуры [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) в версии 4,7.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-168">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 4.7.</span></span>             |
| <span data-ttu-id="3ab3a-169">\_Размер ребарбандинфо V6 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-169">REBARBANDINFO\_V6\_SIZE</span></span>       | <span data-ttu-id="3ab3a-170">Размер структуры [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) в версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-170">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 6.0.</span></span>             |
| <span data-ttu-id="3ab3a-171">\_Размер тттулинфо v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-171">TTTOOLINFO\_V1\_SIZE</span></span>          | <span data-ttu-id="3ab3a-172">Размер структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-172">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="3ab3a-173">\_Размер тттулинфо v2 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-173">TTTOOLINFO\_V2\_SIZE</span></span>          | <span data-ttu-id="3ab3a-174">Размер структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) в версии 4,7.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-174">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.7.</span></span>                       |
| <span data-ttu-id="3ab3a-175">\_Размер тттулинфо v3 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-175">TTTOOLINFO\_V3\_SIZE</span></span>          | <span data-ttu-id="3ab3a-176">Размер структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) в версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-176">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 6.0.</span></span>                       |
| <span data-ttu-id="3ab3a-177">\_Размер твинсертструкт v1 \_</span><span class="sxs-lookup"><span data-stu-id="3ab3a-177">TVINSERTSTRUCT\_V1\_SIZE</span></span>      | <span data-ttu-id="3ab3a-178">Размер структуры [**твинсертструкт**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) в версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-178">The size of the [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure in version 4.0.</span></span>           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="3ab3a-179">Определение номера версии с помощью Дллжетверсион</span><span class="sxs-lookup"><span data-stu-id="3ab3a-179">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="3ab3a-180">Функция [**дллжетверсион**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) может быть вызвана приложением для определения версии библиотеки DLL, имеющейся в системе.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-180">The [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function can be called by an application to determine which DLL version is present on the system.</span></span>

<span data-ttu-id="3ab3a-181">[**Дллжетверсион**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) возвращает структуру [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="3ab3a-181">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="3ab3a-182">Помимо информации, предоставляемой через [**дллверсионинфо**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** также предоставляет номер исправления, который определяет последний установленный пакет обновления, что обеспечивает более надежный способ сравнения номеров версий.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-182">In addition to the information provided through [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="3ab3a-183">Поскольку первый элемент **DLLVERSIONINFO2** является структурой **дллверсионинфо** , более поздняя структура является обратно совместимой.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-183">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>


<span data-ttu-id="3ab3a-184">Следующий пример функции `GetVersion` загружает указанную библиотеку DLL и пытается вызвать ее функцию [**дллжетверсион**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="3ab3a-184">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="3ab3a-185">В случае успеха он использует макрос для упаковки основного и дополнительного номеров версий из структуры [**дллверсионинфо**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) в **DWORD** , возвращаемый вызывающему приложению.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-185">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="3ab3a-186">Если библиотека DLL не экспортирует **дллжетверсион**, функция возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-186">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="3ab3a-187">Вы можете изменить функцию, чтобы она обрабатывала вероятность того, что **дллжетверсион** возвращает структуру [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="3ab3a-187">You can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="3ab3a-188">Если это так, используйте сведения в элементе **уллверсион** структуры **DLLVERSIONINFO2** для сравнения версий, номеров сборки и выпусков пакетов обновления.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-188">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="3ab3a-189">Макрос [**македллверулл**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) упрощает задачу сравнения этих значений с ними в **уллверсион**.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-189">The [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="3ab3a-190">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может представлять угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-190">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="3ab3a-191">Сведения о правильной загрузке библиотек DLL с разными версиями Windows см. в документации по **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="3ab3a-191">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

 


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```



<span data-ttu-id="3ab3a-192">В следующем примере кода показано, как можно использовать `GetVersion` , чтобы проверить, имеет ли ComCtl32.dll версию 6,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-192">The following code example shows how you can use `GetVersion` to test whether ComCtl32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a><span data-ttu-id="3ab3a-193">Версии проекта</span><span class="sxs-lookup"><span data-stu-id="3ab3a-193">Project Versions</span></span>

<span data-ttu-id="3ab3a-194">Чтобы обеспечить совместимость приложения с различными целевыми версиями DLL-файла, в файлах заголовков есть макросы версии.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-194">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="3ab3a-195">Эти макросы используются для определения, исключения или переопределения определенных определений для различных версий библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-195">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="3ab3a-196">Подробное описание этих макросов см. в разделе [Использование заголовков Windows](/windows/desktop/WinProg/using-the-windows-headers) .</span><span class="sxs-lookup"><span data-stu-id="3ab3a-196">See [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers) for an in-depth description of these macros.</span></span>

<span data-ttu-id="3ab3a-197">Например, имя макроса **\_ Win32 \_ IE** обычно находится в более старых заголовках.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-197">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="3ab3a-198">Вы несете ответственность за определение макроса в виде шестнадцатеричного числа.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-198">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="3ab3a-199">Этот номер версии определяет целевую версию приложения, использующего библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-199">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="3ab3a-200">В следующей таблице показаны доступные номера версий и их воздействие на приложение.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-200">The following table shows the available version numbers and the effect each has on your application.</span></span>



| <span data-ttu-id="3ab3a-201">Версия</span><span class="sxs-lookup"><span data-stu-id="3ab3a-201">Version</span></span> | <span data-ttu-id="3ab3a-202">Описание</span><span class="sxs-lookup"><span data-stu-id="3ab3a-202">Description</span></span>                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab3a-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="3ab3a-203">0x0300</span></span>  | <span data-ttu-id="3ab3a-204">Приложение совместимо с ComCtl32.dll версии 4,70 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-204">The application is compatible with ComCtl32.dll version 4.70 and later.</span></span> <span data-ttu-id="3ab3a-205">Приложение не может реализовывать функции, которые были добавлены после версии 4,70.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-205">The application cannot implement features that were added after version 4.70.</span></span> |
| <span data-ttu-id="3ab3a-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="3ab3a-206">0x0400</span></span>  | <span data-ttu-id="3ab3a-207">Приложение совместимо с ComCtl32.dll версии 4,71 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-207">The application is compatible with ComCtl32.dll version 4.71 and later.</span></span> <span data-ttu-id="3ab3a-208">Приложение не может реализовывать функции, которые были добавлены после версии 4,71.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-208">The application cannot implement features that were added after version 4.71.</span></span> |
| <span data-ttu-id="3ab3a-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="3ab3a-209">0x0401</span></span>  | <span data-ttu-id="3ab3a-210">Приложение совместимо с ComCtl32.dll версии 4,72 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-210">The application is compatible with ComCtl32.dll version 4.72 and later.</span></span> <span data-ttu-id="3ab3a-211">Приложение не может реализовывать функции, которые были добавлены после версии 4,72.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-211">The application cannot implement features that were added after version 4.72.</span></span> |
| <span data-ttu-id="3ab3a-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="3ab3a-212">0x0500</span></span>  | <span data-ttu-id="3ab3a-213">Приложение совместимо с ComCtl32.dll версии 5,80 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-213">The application is compatible with ComCtl32.dll version 5.80 and later.</span></span> <span data-ttu-id="3ab3a-214">Приложение не может реализовывать функции, которые были добавлены после версии 5,80.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-214">The application cannot implement features that were added after version 5.80.</span></span> |
| <span data-ttu-id="3ab3a-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="3ab3a-215">0x0501</span></span>  | <span data-ttu-id="3ab3a-216">Приложение совместимо с ComCtl32.dll версии 5,81 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-216">The application is compatible with ComCtl32.dll version 5.81 and later.</span></span> <span data-ttu-id="3ab3a-217">Приложение не может реализовывать функции, которые были добавлены после версии 5,81.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-217">The application cannot implement features that were added after version 5.81.</span></span> |
| <span data-ttu-id="3ab3a-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="3ab3a-218">0x0600</span></span>  | <span data-ttu-id="3ab3a-219">Приложение совместимо с ComCtl32.dll версии 6,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-219">The application is compatible with ComCtl32.dll version 6.0 and later.</span></span> <span data-ttu-id="3ab3a-220">Приложение не может реализовывать функции, которые были добавлены после версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-220">The application cannot implement features that were added after version 6.0.</span></span>   |



 

<span data-ttu-id="3ab3a-221">Если в проекте не определен макрос **\_ Win32 \_ IE** , он автоматически определяется как 0x0500.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="3ab3a-222">Чтобы определить другое значение, можно добавить следующий объект в директивы компилятора в файле make. Замените требуемый номер версии для 0x0400.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>


```C++
/D _WIN32_IE=0x0400
```



<span data-ttu-id="3ab3a-223">Другой способ — добавить строку, аналогичную приведенной ниже, в исходный код перед включением файлов заголовков оболочки.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="3ab3a-224">Замените требуемый номер версии для 0x0400.</span><span class="sxs-lookup"><span data-stu-id="3ab3a-224">Substitute the desired version number for 0x0400.</span></span>


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a><span data-ttu-id="3ab3a-225">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3ab3a-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ab3a-226">Общие сведения об элементах управления</span><span class="sxs-lookup"><span data-stu-id="3ab3a-226">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 