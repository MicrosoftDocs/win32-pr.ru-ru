---
title: Рабочий процесс адаптера
description: В этом разделе описывается рабочий процесс регистрации с точки зрения подключаемых модулей адаптера.
ms.assetid: 0392124A-78CF-49E3-A52A-1E2E3A100E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68f93146e1d6cedd42094876547bfe0c945d6a7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661623"
---
# <a name="adapter-workflow"></a><span data-ttu-id="001d1-103">Рабочий процесс адаптера</span><span class="sxs-lookup"><span data-stu-id="001d1-103">Adapter Workflow</span></span>

<span data-ttu-id="001d1-104">В этом разделе описывается рабочий процесс регистрации с точки зрения подключаемых модулей адаптера.</span><span class="sxs-lookup"><span data-stu-id="001d1-104">This section describes the enrollment workflow from the perspective of the adapter plugins.</span></span>

<span data-ttu-id="001d1-105">В Windows 10 реализован интерфейс механизма V4, который предоставляет 2 новые функции адаптера ядра, [**енгинеадаптеркреатекэй**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) и [**енгинеадаптеридентифифеатуресетсекуре**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn).</span><span class="sxs-lookup"><span data-stu-id="001d1-105">In Windows 10, we ve implemented a V4 engine interface that provides 2 new engine adapter functions, [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) and [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn).</span></span> <span data-ttu-id="001d1-106">Эти новые функции обеспечивают поддержку безопасных биометрических данных с помощью TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="001d1-106">These new functions allow support for secure biometrics using TPM 2.0.</span></span> <span data-ttu-id="001d1-107">В следующей таблице показан рабочий процесс регистрации на стороне адаптера.</span><span class="sxs-lookup"><span data-stu-id="001d1-107">The following table shows the adapter-side enrollment workflow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="001d1-108">API клиента</span><span class="sxs-lookup"><span data-stu-id="001d1-108">Client API</span></span></td>
<td><span data-ttu-id="001d1-109">Методы адаптера</span><span class="sxs-lookup"><span data-stu-id="001d1-109">Adapter Methods</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="001d1-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>Винбиожетпроперти (EXTENDED_ENGINE_INFO)</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty(EXTENDED_ENGINE_INFO)</strong></a></span></span></td>
<td><span data-ttu-id="001d1-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>енгинеадаптеркуерекстендединфо</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="001d1-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>винбиоенроллбегин</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="001d1-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>сторажеадаптеркуерибисубжект</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></span></span></li>
<li><span data-ttu-id="001d1-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>сенсорадаптерклеарконтекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="001d1-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>енгинеадаптерклеарконтекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="001d1-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>сторажеадаптерклеарконтекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="001d1-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>енгинеадаптеркреатинроллмент</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="001d1-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>енгинеадаптерсетенроллментпараметерс</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="001d1-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>винбиоенроллкаптуре</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>WinBioEnrollCapture</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="001d1-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>сенсорадаптерстарткаптуре</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></span></span></li>
<li><span data-ttu-id="001d1-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>сенсорадаптерфинишкаптуре</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></span></span></li>
<li><span data-ttu-id="001d1-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>Сенсорадаптерпушдататоенгине</strong></a><strong>[-></strong> <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>енгинеадаптеракцептсампледата</strong></a>]</span><span class="sxs-lookup"><span data-stu-id="001d1-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[-></strong><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</span></span></li>
<li><span data-ttu-id="001d1-123">Если S_OK или WINBIO_I_MORE_DATA</span><span class="sxs-lookup"><span data-stu-id="001d1-123">If S_OK or WINBIO_I_MORE_DATA</span></span>
<ol>
<li><span data-ttu-id="001d1-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>енгинеадаптерупдатинроллмент</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="001d1-125">[Выполняется регистрация вызывающего объекта]</span><span class="sxs-lookup"><span data-stu-id="001d1-125">[Caller continues enrollment]</span></span></li>
</ol></li>
<li><span data-ttu-id="001d1-126">Иначе, если WINBIO_E_BAD_CAPTURE [вызывающий объект отображает отзыв об отклонении, продолжение регистрации]</span><span class="sxs-lookup"><span data-stu-id="001d1-126">Else if WINBIO_E_BAD_CAPTURE [Caller displays reject feedback, continues enrollment]</span></span> <br/></li>
<li><span data-ttu-id="001d1-127">Else, если другая ошибка</span><span class="sxs-lookup"><span data-stu-id="001d1-127">Else if other ERROR</span></span>
<ol>
<li><span data-ttu-id="001d1-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>енгинеадаптерклеарконтекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="001d1-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>сторажеадаптерклеарконтекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="001d1-130">[Служба биографии прерывает регистрацию]</span><span class="sxs-lookup"><span data-stu-id="001d1-130">[Bio service aborts enrollment]</span></span></li>
</ol></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="001d1-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>Винбиожетпроперти (EXTENDED_ENROLLMENT_STATUS)</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS)</strong></a></span></span></td>
<td><span data-ttu-id="001d1-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>енгинеадаптеркуерекстендеденроллментстатус</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="001d1-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>винбиоенроллкоммит</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="001d1-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>енгинеадаптерчеккфордупликате</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></span></span></li>
<li><span data-ttu-id="001d1-135">Если СЪЕМная база данных</span><span class="sxs-lookup"><span data-stu-id="001d1-135">If REMOVABLE DATABASE</span></span>
<ol>
<li><span data-ttu-id="001d1-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>енгинеадаптержетенроллменсаш</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></span></span></li>
<li><span data-ttu-id="001d1-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>енгинеадаптеркоммитенроллмент</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span></li>
</ol></li>
<li><span data-ttu-id="001d1-138">Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>енгинеадаптеркоммитенроллмент</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-138">Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="001d1-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>винбиоенроллдискард</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>WinBioEnrollDiscard</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="001d1-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>енгинеадаптердискарденроллмент</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="001d1-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>енгинеадаптерклеарконтекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="001d1-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>сторажеадаптерклеарконтекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="001d1-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 





