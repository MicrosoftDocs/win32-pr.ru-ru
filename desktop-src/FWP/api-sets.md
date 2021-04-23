---
title: API WFP
description: API платформы фильтрации Windows (WFP) состоит из следующих компонентов.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "105681714"
---
# <a name="wfp-api"></a><span data-ttu-id="bfadd-103">API WFP</span><span class="sxs-lookup"><span data-stu-id="bfadd-103">WFP API</span></span>

<span data-ttu-id="bfadd-104">API платформы фильтрации Windows (WFP) состоит из следующих компонентов.</span><span class="sxs-lookup"><span data-stu-id="bfadd-104">The Windows Filtering Platform (WFP) API is divided into the following components.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bfadd-105">Компонент</span><span class="sxs-lookup"><span data-stu-id="bfadd-105">Component</span></span></th>
<th><span data-ttu-id="bfadd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bfadd-106">Description</span></span></th>
<th><span data-ttu-id="bfadd-107">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bfadd-107">Header Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="bfadd-108"><a href="/windows-hardware/drivers/ddi/_netvista/">API выноски</a> (фвпс) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="bfadd-108"><a href="/windows-hardware/drivers/ddi/_netvista/">Callout API</a> (FWPS)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bfadd-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Типы данных</a> , используемые в выносках. <strong>Примечание</strong>  .  Эти типы данных описаны в пакете средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="bfadd-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Data types</a> used by callouts.<strong>Note</strong>  These data types are documented in the Microsoft Windows Driver Development Kit (DDK).</span></span><br/></td>
<td><dl> <span data-ttu-id="bfadd-110">фвпстипес. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-110">fwpstypes.h</span></span><br />
<span data-ttu-id="bfadd-111">фвпстипес. idl</span><span class="sxs-lookup"><span data-stu-id="bfadd-111">fwpstypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfadd-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Функции</a> и <a href="/windows-hardware/drivers/ddi/_netvista/">перечислимые типы</a> , используемые для реализации вызовов. <strong>Примечание</strong>  .  Эти функции и перечислимые типы описаны в DDK.</span><span class="sxs-lookup"><span data-stu-id="bfadd-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Functions</a> and <a href="/windows-hardware/drivers/ddi/_netvista/">enumerated types</a> used to implement callouts.<strong>Note</strong>  These functions and enumerated types are documented in the DDK.</span></span><br/></td>
<td><dl> <span data-ttu-id="bfadd-113">фвпсу. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-113">fwpsu.h</span></span><br />
<span data-ttu-id="bfadd-114">фвпск. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-114">fwpsk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="bfadd-115">API IKE/AuthIP (IKEEXT) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="bfadd-115">IKE/AuthIP API (IKEEXT)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bfadd-116"><a href="fwp-enums.md">Перечислимые типы</a> и <a href="fwp-structs.md">структуры</a> , используемые для управления политиками IKE и политики основного режима AuthIP (mm) и сопоставлениями безопасности.</span><span class="sxs-lookup"><span data-stu-id="bfadd-116"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IKE and AuthIP main mode (MM) policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="bfadd-117">икетипес. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-117">iketypes.h</span></span><br />
<span data-ttu-id="bfadd-118">икетипес. idl</span><span class="sxs-lookup"><span data-stu-id="bfadd-118">iketypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfadd-119"><a href="fwp-ike-functions.md">Функции</a> , используемые для управления политикой и сопоставлениями безопасности IKE и AuthIP mm.</span><span class="sxs-lookup"><span data-stu-id="bfadd-119"><a href="fwp-ike-functions.md">Functions</a> used for managing IKE and AuthIP MM policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="bfadd-120">фвпму. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-120">fwpmu.h</span></span><br />
<span data-ttu-id="bfadd-121">фвпмк. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-121">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="bfadd-122">API IPsec $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="bfadd-122">IPsec API (IPSEC)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bfadd-123"><a href="fwp-enums.md">Перечислимые типы</a> и <a href="fwp-structs.md">структуры</a> , используемые для управления политиками IPSec и сопоставлениями безопасности.</span><span class="sxs-lookup"><span data-stu-id="bfadd-123"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="bfadd-124">ипсектипес. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-124">ipsectypes.h</span></span><br />
<span data-ttu-id="bfadd-125">ипсектипес. idl</span><span class="sxs-lookup"><span data-stu-id="bfadd-125">ipsectypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfadd-126"><a href="fwp-ipsec-functions.md">Функции</a> , используемые для управления политиками IPSec и сопоставлениями безопасности.</span><span class="sxs-lookup"><span data-stu-id="bfadd-126"><a href="fwp-ipsec-functions.md">Functions</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="bfadd-127">фвпму. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-127">fwpmu.h</span></span><br />
<span data-ttu-id="bfadd-128">фвпмк. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-128">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="bfadd-129">API управления (ФВПМ) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="bfadd-129">Management API (FWPM)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="bfadd-130"><a href="fwp-enums.md">Перечислимые типы</a> и <a href="fwp-structs.md">структуры</a> , используемые для управления обработчиком фильтров.</span><span class="sxs-lookup"><span data-stu-id="bfadd-130"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing the filter engine.</span></span></td>
<td><dl> <span data-ttu-id="bfadd-131">фвпмтипес. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-131">fwpmtypes.h</span></span><br />
<span data-ttu-id="bfadd-132">фвпмтипес. idl</span><span class="sxs-lookup"><span data-stu-id="bfadd-132">fwpmtypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfadd-133"><a href="fwp-mgmt-functions.md">Функции</a> , используемые для управления обработчиком фильтров.</span><span class="sxs-lookup"><span data-stu-id="bfadd-133"><a href="fwp-mgmt-functions.md">Functions</a> used for managing the filter engine.</span></span> <span data-ttu-id="bfadd-134">Эти функции используются для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="bfadd-134">These functions are used to perform the following tasks:</span></span><br/>
<ul>
<li><span data-ttu-id="bfadd-135">Установка и Фильтрация запросов, поставщиков и выносок.</span><span class="sxs-lookup"><span data-stu-id="bfadd-135">Set and query filters, providers, and callouts.</span></span></li>
<li><span data-ttu-id="bfadd-136">Получение статистики IPsec.</span><span class="sxs-lookup"><span data-stu-id="bfadd-136">Retrieve IPsec statistics.</span></span></li>
<li><span data-ttu-id="bfadd-137">Настройка платформы фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="bfadd-137">Configure the Windows Filtering Platform.</span></span></li>
</ul></td>
<td><dl> <span data-ttu-id="bfadd-138">фвпму. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-138">fwpmu.h</span></span><br />
<span data-ttu-id="bfadd-139">фвпмк. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-139">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="bfadd-140">Общий API (FWP)</span><span class="sxs-lookup"><span data-stu-id="bfadd-140">Shared API (FWP)</span></span></td>
<td><span data-ttu-id="bfadd-141">Фундаментальные <a href="fwp-enums.md">перечислимые типы</a> и <a href="fwp-structs.md">структуры</a> , общие для платформы фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="bfadd-141">Fundamental <a href="fwp-enums.md">enumerated types</a> and <a href="fwp-structs.md">structures</a> shared across the Windows Filtering Platform.</span></span></td>
<td><dl> <span data-ttu-id="bfadd-142">фвптипес. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-142">fwptypes.h</span></span><br />
<span data-ttu-id="bfadd-143">фвптипес. idl</span><span class="sxs-lookup"><span data-stu-id="bfadd-143">fwptypes.idl</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bfadd-144">Имена типов данных — это все символы в верхнем регистре и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="bfadd-144">Data type names are all upper-case and underscore-delimited.</span></span> <span data-ttu-id="bfadd-145">Имя всегда начинается с префикса, определяющего свою группу компонентов, например [**фвпм \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span><span class="sxs-lookup"><span data-stu-id="bfadd-145">The name always begins with a prefix that identifies its component group, such as [**FWPM\_PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span></span>

<span data-ttu-id="bfadd-146">Имена функций являются символами в смешанном регистре и регистром.</span><span class="sxs-lookup"><span data-stu-id="bfadd-146">Function names are mixed-case and case-delimited.</span></span> <span data-ttu-id="bfadd-147">Имя всегда начинается с префикса, определяющего свою группу компонентов, например [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span><span class="sxs-lookup"><span data-stu-id="bfadd-147">The name always begins with a prefix that identifies its component group, such as [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span></span>

<span data-ttu-id="bfadd-148">Большинство имен данных и функций заканчиваются номером версии.</span><span class="sxs-lookup"><span data-stu-id="bfadd-148">Most data and function names end with a version number.</span></span> <span data-ttu-id="bfadd-149">Файл заголовка фвпви. h сопоставляет независимые от версии данные и имена функций с версией, которая подходит для использования с данной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="bfadd-149">The fwpvi.h header file maps version-independent data and function names to the version that is appropriate for use with a given operating system.</span></span> <span data-ttu-id="bfadd-150">Дополнительные сведения см. в разделе [имена Version-Independent WFP и нацеливание на конкретные версии Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="bfadd-150">For more information, see [WFP Version-Independent Names and Targeting Specific Versions of Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span></span>

<span data-ttu-id="bfadd-151">Каждый компонент не является изолированным.</span><span class="sxs-lookup"><span data-stu-id="bfadd-151">Each component does not stand alone.</span></span> <span data-ttu-id="bfadd-152">Например, политики IKE в основном режиме (MM) определяются в компоненте IKEEXT, но хранятся в контексте поставщика и связаны с фильтром, который находится в компоненте API ФВПМ.</span><span class="sxs-lookup"><span data-stu-id="bfadd-152">For example, IKE main mode (MM) policies are defined in the IKEEXT component, but are stored in a provider context and are associated with a filter both of which are found in the FWPM API component.</span></span>

## <a name="user-mode-and-kernel-mode-public-header-files"></a><span data-ttu-id="bfadd-153">Файлы общедоступных заголовков User-Mode и Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="bfadd-153">User-Mode and Kernel-Mode Public Header Files</span></span>

<span data-ttu-id="bfadd-154">Большинство функций WFP можно вызывать из пользовательского режима или режима ядра.</span><span class="sxs-lookup"><span data-stu-id="bfadd-154">Most of the WFP functions can be called from either user mode or kernel mode.</span></span> <span data-ttu-id="bfadd-155">Однако функции пользовательского режима возвращают значение **DWORD** , представляющее код ошибки Win32, тогда как функции режима ядра возвращают значение **NTSTATUS** , представляющее код состояния NT.</span><span class="sxs-lookup"><span data-stu-id="bfadd-155">However, user-mode functions return a **DWORD** value that represents a Win32 error code, whereas kernel-mode functions return an **NTSTATUS** value that represents an NT status code.</span></span> <span data-ttu-id="bfadd-156">В результате имена функций и семантика идентичны в пользовательском режиме и режиме ядра, но сигнатуры функций не являются.</span><span class="sxs-lookup"><span data-stu-id="bfadd-156">As a result, function names and semantics are identical between user mode and kernel mode, but function signatures are not.</span></span> <span data-ttu-id="bfadd-157">Для этого требуются отдельные заголовки, относящиеся к пользовательскому режиму и режиму ядра, для прототипов функций.</span><span class="sxs-lookup"><span data-stu-id="bfadd-157">This requires separate user-mode and kernel-mode specific headers for the function prototypes.</span></span> <span data-ttu-id="bfadd-158">Имена файлов заголовков пользовательского режима заканчиваются на "u", а имена файлов заголовков в режиме ядра заканчиваются на "k".</span><span class="sxs-lookup"><span data-stu-id="bfadd-158">User-mode header file names end in "u" and kernel-mode header file names end in "k".</span></span>

<span data-ttu-id="bfadd-159">В следующей таблице перечислены файлы заголовков Win32, которые определяют функции WFP.</span><span class="sxs-lookup"><span data-stu-id="bfadd-159">The following table lists the Win32 header files that define the WFP functions.</span></span>

| <span data-ttu-id="bfadd-160">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bfadd-160">Header Files</span></span> | <span data-ttu-id="bfadd-161">Описание</span><span class="sxs-lookup"><span data-stu-id="bfadd-161">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfadd-162">фвпмк. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-162">fwpmk.h</span></span>      | <span data-ttu-id="bfadd-163">Прототипы функций в режиме ядра для компонентов ФВПМ, IPsec и IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="bfadd-163">Kernel-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="bfadd-164">Доступно только в DDK.</span><span class="sxs-lookup"><span data-stu-id="bfadd-164">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="bfadd-165">фвпму. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-165">fwpmu.h</span></span>      | <span data-ttu-id="bfadd-166">Прототипы функций пользовательского режима для компонентов ФВПМ, IPsec и IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="bfadd-166">User-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="bfadd-167">Доступно только в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bfadd-167">Available in the Microsoft Windows Software Development Kit (SDK) only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="bfadd-168">фвпск. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-168">fwpsk.h</span></span>      | <span data-ttu-id="bfadd-169">Прототипы функций и перечислимые типы для компонента ФВПС в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="bfadd-169">Kernel-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="bfadd-170">Доступно только в DDK.</span><span class="sxs-lookup"><span data-stu-id="bfadd-170">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="bfadd-171">фвпсу. h</span><span class="sxs-lookup"><span data-stu-id="bfadd-171">fwpsu.h</span></span>      | <span data-ttu-id="bfadd-172">Прототипы функций пользовательского режима и перечислимые типы для компонента ФВПС.</span><span class="sxs-lookup"><span data-stu-id="bfadd-172">User-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="bfadd-173">Доступно только в Windows SDK. **Примечание**  .  Перечисляемые типы ФВПС в пользовательском режиме идентичны перечисленным типам ФВПС в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="bfadd-173">Available in the Windows SDK only.**Note**  The user-mode FWPS enumerated types are identical to the kernel-mode FWPS enumerated types.</span></span> <span data-ttu-id="bfadd-174">В итоге эти типы описаны только в DDK.</span><span class="sxs-lookup"><span data-stu-id="bfadd-174">In consequence, these types are documented in the DDK only.</span></span><br/> <span data-ttu-id="bfadd-175">**Примечание**  .  Прототипы функций ФВПС в пользовательском режиме идентичны прототипам функций ФВПС в режиме ядра, за исключением кода возврата.</span><span class="sxs-lookup"><span data-stu-id="bfadd-175">**Note**  The user-mode FWPS function prototypes are identical to the kernel-mode FWPS function prototypes with the exception of the return code.</span></span> <span data-ttu-id="bfadd-176">Функции ФВПС пользовательского режима возвращают **DWORD**, тогда как функции фвпс в режиме ядра возвращают **NTSTATUS**.</span><span class="sxs-lookup"><span data-stu-id="bfadd-176">User-mode FWPS functions return a **DWORD**, whereas kernel-mode FWPS functions return an **NTSTATUS**.</span></span> <span data-ttu-id="bfadd-177">В итоге эти функции описаны только в DDK.</span><span class="sxs-lookup"><span data-stu-id="bfadd-177">In consequence, these functions are documented in the DDK only.</span></span><br/> |



 

<span data-ttu-id="bfadd-178">Все функции пользовательского режима экспортируются из fwpuclnt.dll.</span><span class="sxs-lookup"><span data-stu-id="bfadd-178">All user-mode functions are exported from fwpuclnt.dll.</span></span> <span data-ttu-id="bfadd-179">Все функции режима ядра экспортируются из fwpkclnt.sys.</span><span class="sxs-lookup"><span data-stu-id="bfadd-179">All kernel-mode functions are exported from fwpkclnt.sys.</span></span>

### <a name="management-fwpm-and-callout-fwps-data-types"></a><span data-ttu-id="bfadd-180">Типы данных управления (ФВПМ) и выноски (ФВПС)</span><span class="sxs-lookup"><span data-stu-id="bfadd-180">Management (FWPM) and Callout (FWPS) Data Types</span></span>

<span data-ttu-id="bfadd-181">Большинство типов данных ФВПМ, которые используются для задач управления, таких как Добавление фильтров или выносок из приложения или драйвера, имеют аналоги ФВПС.</span><span class="sxs-lookup"><span data-stu-id="bfadd-181">Most FWPM data types, which are used for management tasks such as adding filters or callouts from an application or driver, have FWPS counterparts.</span></span> <span data-ttu-id="bfadd-182">Типы данных ФВПС используются во время фактической фильтрации сетевого трафика в контексте подпрограммы выноски для классификации.</span><span class="sxs-lookup"><span data-stu-id="bfadd-182">The FWPS data types are used during the actual filtering of network traffic, in the context of a callout routine for classification.</span></span>

<span data-ttu-id="bfadd-183">Например, чтобы добавить фильтр к определенному слою механизма фильтрации, программист должен использовать тип ФВПМ, например: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` .</span><span class="sxs-lookup"><span data-stu-id="bfadd-183">For example, in order to add a filter to a certain filtering engine layer, the programmer should use an FWPM type, like: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET`.</span></span> <span data-ttu-id="bfadd-184">Чтобы проверить, из какого слоя вызывается выноска, программист должен использовать соответствующий тип ФВПС: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .</span><span class="sxs-lookup"><span data-stu-id="bfadd-184">To check which layer a callout is being called from, the programmer should use the corresponding FWPS type: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)`.</span></span>

<span data-ttu-id="bfadd-185">Некоторые ФВПС аналоги с типами данных ФВПМ расширяют исходные типы данных ФВПМ.</span><span class="sxs-lookup"><span data-stu-id="bfadd-185">Some FWPS counterparts to FWPM data types are expanding the original FWPM data types.</span></span> <span data-ttu-id="bfadd-186">Например, чтобы добавить условие фильтра на многих уровнях механизма фильтрации, программист определяет `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` независимо от слоя механизма фильтрации.</span><span class="sxs-lookup"><span data-stu-id="bfadd-186">For example, to add a filter condition at many filtering engine layers, the programmer specifies the `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` regardless of the filtering engine layer.</span></span> <span data-ttu-id="bfadd-187">Чтобы найти значение условия фильтра, программист указывает тип ФВПС, относящийся к слою, например: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .</span><span class="sxs-lookup"><span data-stu-id="bfadd-187">To find a filter condition value, the programmer specifies a layer specific FWPS type, like: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]`.</span></span>

<span data-ttu-id="bfadd-188">Типы данных ФВПС обычно меньше, чем их аналоги ФВПМ.</span><span class="sxs-lookup"><span data-stu-id="bfadd-188">The FWPS data types are generally smaller than their FWPM counterparts.</span></span> <span data-ttu-id="bfadd-189">Например, [**идентификаторы слоя фильтрации фвпм**](management-filtering-layer-identifiers-.md) — **GUID** s (16-bytes), в то время как [идентификаторы слоя фильтрации фвпс](/windows-hardware/drivers/network/management-filtering-layer-identifiers) — **UINT16** (16 бит).</span><span class="sxs-lookup"><span data-stu-id="bfadd-189">For example, the [**FWPM filtering layer identifiers**](management-filtering-layer-identifiers-.md) are **GUID** s (16-bytes) whereas the [FWPS filtering layer identifiers](/windows-hardware/drivers/network/management-filtering-layer-identifiers) are **UINT16** (16-bits).</span></span> <span data-ttu-id="bfadd-190">Меньший размер для типов данных ФВПС повышает производительность системы, так как сравнения целых чисел перевешивают сравнения **GUID** для трафика в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="bfadd-190">The smaller size for FWPS data types improves system performance since integer comparisons outweigh **GUID** comparisons for real-time traffic.</span></span> <span data-ttu-id="bfadd-191">Кроме того, память ядра используется эффективно, так как все типы ФВПС используются в ядре для управления фильтрами, в то время как типы ФВПМ хранятся в пользовательском режиме для управления различными слоями.</span><span class="sxs-lookup"><span data-stu-id="bfadd-191">Also, the kernel memory is used efficiently since the FWPS types are all used in the kernel for managing the filters, whereas the FWPM types are stored in user-mode to manage the different layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfadd-192">См. также</span><span class="sxs-lookup"><span data-stu-id="bfadd-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfadd-193">Объектная модель API WFP</span><span class="sxs-lookup"><span data-stu-id="bfadd-193">WFP API Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="bfadd-194">Управление объектами API WFP</span><span class="sxs-lookup"><span data-stu-id="bfadd-194">WFP API Object Management</span></span>](object-management.md)
</dt> </dl>

