---
title: Функция Мпсканстарт (Мпклиент. h)
description: Запускает операцию сканирования.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Функции Мпсканстарт устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988922"
---
# <a name="mpscanstart-function"></a><span data-ttu-id="b53d8-104">Функция Мпсканстарт</span><span class="sxs-lookup"><span data-stu-id="b53d8-104">MpScanStart function</span></span>

<span data-ttu-id="b53d8-105">Запускает операцию сканирования.</span><span class="sxs-lookup"><span data-stu-id="b53d8-105">Starts a scanning operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b53d8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b53d8-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a><span data-ttu-id="b53d8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b53d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b53d8-108">*хмфандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b53d8-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d8-109">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="b53d8-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="b53d8-110">Обработчик для интерфейса диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="b53d8-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="b53d8-111">Этот маркер возвращается функцией [**мпманажеропен**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="b53d8-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b53d8-112">*Скантипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b53d8-112">*ScanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d8-113">Тип: **[ **мпскан \_ тип**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="b53d8-113">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

<span data-ttu-id="b53d8-114">Указывает тип проверки.</span><span class="sxs-lookup"><span data-stu-id="b53d8-114">Specifies the type of scan.</span></span> <span data-ttu-id="b53d8-115">Этот параметр должен быть одним из членов [**\_ типа мпскан**](mpscan-type.md) енуератион.</span><span class="sxs-lookup"><span data-stu-id="b53d8-115">This parameter must be one of the members of the [**MPSCAN\_TYPE**](mpscan-type.md) enueration.</span></span>

</dd> <dt>

<span data-ttu-id="b53d8-116">*двсканоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b53d8-116">*dwScanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d8-117">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b53d8-117">Type: **DWORD**</span></span>

<span data-ttu-id="b53d8-118">Указывает различные параметры для операции сканирования.</span><span class="sxs-lookup"><span data-stu-id="b53d8-118">Specifies various options for scanning operation.</span></span>



| <span data-ttu-id="b53d8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b53d8-119">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="b53d8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b53d8-120">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <span data-ttu-id="b53d8-121"><dt>**\_параметр мпскан \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-121"><dt>**MPSCAN\_OPTION\_NONE**</dt></span></span> </dl>                               | <span data-ttu-id="b53d8-122">Конкретный параметр не запрашивается.</span><span class="sxs-lookup"><span data-stu-id="b53d8-122">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <span data-ttu-id="b53d8-123"><dt>**\_параметр мпскан \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-123"><dt>**MPSCAN\_OPTION\_ASYNC**</dt></span></span> </dl>                            | <span data-ttu-id="b53d8-124">Операция просмотра должна быть асинхронной, где **мпсканстарт** возвращается сразу после успешного запуска проверки.</span><span class="sxs-lookup"><span data-stu-id="b53d8-124">The scan operation is to be asynchronous, where **MpScanStart** returns immediately after the successful initiation of scanning.</span></span> <span data-ttu-id="b53d8-125">(По умолчанию операция сканирования является синхронной, то есть **мпсканстарт** будет возвращаться только после завершения проверки.)</span><span class="sxs-lookup"><span data-stu-id="b53d8-125">(By default the scan operation is synchronous, meaning **MpScanStart** will return only after the scan is finished.)</span></span><br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <span data-ttu-id="b53d8-126"><dt>**\_ \_ ход выполнения параметра мпскан**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-126"><dt>**MPSCAN\_OPTION\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="b53d8-127">Вызывающий объект заинтересован в получении сведений о ходе проверки с помощью обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b53d8-127">The caller is interested in receiving scan progress information via a callback.</span></span><br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <span data-ttu-id="b53d8-128"><dt>**МПСКАН, \_ параметр \_ ловприорити**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-128"><dt>**MPSCAN\_OPTION\_LOWPRIORITY**</dt></span></span> </dl>          | <span data-ttu-id="b53d8-129">Выполните проверку с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="b53d8-129">Perform the scan with low priority.</span></span> <span data-ttu-id="b53d8-130">(По умолчанию операция просмотра выполняется с обычным приоритетом.)</span><span class="sxs-lookup"><span data-stu-id="b53d8-130">(By default the scan operation is performed with normal priority.)</span></span><br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <span data-ttu-id="b53d8-131"><dt>**МПСКАН, \_ параметр \_ паккедексес**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-131"><dt>**MPSCAN\_OPTION\_PACKEDEXES**</dt></span></span> </dl>             | <span data-ttu-id="b53d8-132">Проверьте Упакованные исполняемые файлы для возможных угроз.</span><span class="sxs-lookup"><span data-stu-id="b53d8-132">Scan packed executables for possible threats.</span></span><br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <span data-ttu-id="b53d8-133"><dt>**\_ \_ архивы параметров мпскан**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-133"><dt>**MPSCAN\_OPTION\_ARCHIVES**</dt></span></span> </dl>                   | <span data-ttu-id="b53d8-134">Проверьте содержимое архива на предмет возможных угроз.</span><span class="sxs-lookup"><span data-stu-id="b53d8-134">Scan archive contents for possible threats.</span></span> <span data-ttu-id="b53d8-135">Архивы — это файлы с расширениями, такими как ZIP, CAB или tar.</span><span class="sxs-lookup"><span data-stu-id="b53d8-135">Archives are files with extensions such as .zip, .cab, or .tar.</span></span><br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <span data-ttu-id="b53d8-136"><dt>**\_ \_ эвристика параметра мпскан**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-136"><dt>**MPSCAN\_OPTION\_HEURISTICS**</dt></span></span> </dl>             | <span data-ttu-id="b53d8-137">Включить проверку на основе эвристики.</span><span class="sxs-lookup"><span data-stu-id="b53d8-137">Enable heuristics-based scanning.</span></span> <span data-ttu-id="b53d8-138">Будет проверяться наличие угроз с типом обнаружения Эвристика.</span><span class="sxs-lookup"><span data-stu-id="b53d8-138">This will scan for threats with detection type set to heuristics.</span></span><br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <span data-ttu-id="b53d8-139"><dt>**МПСКАН, \_ параметр \_ репортфриендли**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-139"><dt>**MPSCAN\_OPTION\_REPORTFRIENDLY**</dt></span></span> </dl> | <span data-ttu-id="b53d8-140">Отчитываться о понятных элементах при просмотре ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b53d8-140">Report friendly items in a resource scan.</span></span> <span data-ttu-id="b53d8-141">Это предназначено только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="b53d8-141">This is intended for internal use only.</span></span><br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <span data-ttu-id="b53d8-142"><dt>**МПСКАН, \_ параметр \_ репортункновн**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-142"><dt>**MPSCAN\_OPTION\_REPORTUNKNOWN**</dt></span></span> </dl>    | <span data-ttu-id="b53d8-143">Сообщать об неизвестных элементах при просмотре ресурса.</span><span class="sxs-lookup"><span data-stu-id="b53d8-143">Report unknown items in a resource scan.</span></span> <span data-ttu-id="b53d8-144">Это предназначено только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="b53d8-144">This is intended for internal use only.</span></span><br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <span data-ttu-id="b53d8-145"><dt>**МПСКАН \_ параметр \_ объединения**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-145"><dt>**MPSCAN\_OPTION\_NOCONSOLIDATE**</dt></span></span> </dl>    | <span data-ttu-id="b53d8-146">Не объединяйте результаты проверки с глобальным представлением угроз.</span><span class="sxs-lookup"><span data-stu-id="b53d8-146">Do not consolidate scan results with global threat view.</span></span> <span data-ttu-id="b53d8-147">Это полезно для клиента (например, почтового клиента), который хочет управлять автоматическим интерфейсом, а не допускает очистку от вредоносных программ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b53d8-147">This is useful for a client (such as an email client) which wants to control cleaning UX by itself rather than allowing default anti-malware cleaning UX.</span></span> <span data-ttu-id="b53d8-148">Это предназначено только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="b53d8-148">This is intended for internal use only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b53d8-149">*псканресаурцес* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b53d8-149">*pScanResources* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d8-150">Тип: **пмпскан \_ Resources**</span><span class="sxs-lookup"><span data-stu-id="b53d8-150">Type: **PMPSCAN\_RESOURCES**</span></span>

<span data-ttu-id="b53d8-151">Указатель на сведения о ресурсе сканирования.</span><span class="sxs-lookup"><span data-stu-id="b53d8-151">A pointer to the scan resource information.</span></span> <span data-ttu-id="b53d8-152">Для быстрой проверки этот параметр должен иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="b53d8-152">This parameter must be **NULL** for a quick scan.</span></span> <span data-ttu-id="b53d8-153">Это необязательный параметр для полной проверки.</span><span class="sxs-lookup"><span data-stu-id="b53d8-153">This is an optional parameter for a full scan.</span></span> <span data-ttu-id="b53d8-154">Для просмотра ресурсов этот параметр должен быть указан по крайней мере с одной структурой сведений о ресурсах.</span><span class="sxs-lookup"><span data-stu-id="b53d8-154">For a resource scan this parameter must be specified with at least one resource information structure.</span></span> <span data-ttu-id="b53d8-155">Для сканирования конкретных ресурсов вызывающий объект должен **иметь \_ универсальное** разрешение на чтение для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b53d8-155">To scan specific resources the caller must have **GENERIC\_READ** permission for the resource.</span></span> <span data-ttu-id="b53d8-156">См. раздел [**\_ ресурсы мпскан**](mpscan-resources.md).</span><span class="sxs-lookup"><span data-stu-id="b53d8-156">See [**MPSCAN\_RESOURCES**](mpscan-resources.md).</span></span>

</dd> <dt>

<span data-ttu-id="b53d8-157">*пкаллбаккинфо* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b53d8-157">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d8-158">Тип: **пмпкаллбакк \_ info** .</span><span class="sxs-lookup"><span data-stu-id="b53d8-158">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="b53d8-159">Указатель на сведения о обратном вызове, используемые для передачи клиенту изменений состояния сканирования (например, запуск и завершение) и сведений о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="b53d8-159">A pointer to the callback information used to feed the client with scan state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="b53d8-160">[**\_ Данные мпкаллбакк**](mpcallback-data.md) , переданные в функцию обратного вызова, сообщают о фактическом состоянии сканирования и сведениях о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="b53d8-160">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual scan state and progress-related information.</span></span> <span data-ttu-id="b53d8-161">Ниже приведен список возможных обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="b53d8-161">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="b53d8-162">Значение</span><span class="sxs-lookup"><span data-stu-id="b53d8-162">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="b53d8-163">Значение</span><span class="sxs-lookup"><span data-stu-id="b53d8-163">Meaning</span></span>                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <span data-ttu-id="b53d8-164"><dt>**\_Начало СКАНИРОВАНИЯ \_ мпнотифи**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-164"><dt>**MPNOTIFY\_SCAN\_START**</dt></span></span> </dl>                            | <span data-ttu-id="b53d8-165">Операция сканирования запущена.</span><span class="sxs-lookup"><span data-stu-id="b53d8-165">Scan operation started.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <span data-ttu-id="b53d8-166"><dt>**\_сканирование мпнотифи \_ завершено**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-166"><dt>**MPNOTIFY\_SCAN\_COMPLETE**</dt></span></span> </dl>                   | <span data-ttu-id="b53d8-167">Операция сканирования завершена.</span><span class="sxs-lookup"><span data-stu-id="b53d8-167">Scan operation completed.</span></span> <span data-ttu-id="b53d8-168">Дополнительные сведения можно получить с помощью структуры [**\_ данных мпскан**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="b53d8-168">Additional information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <span data-ttu-id="b53d8-169"><dt>**МПНОТИФИ \_ сканирование \_ приостановлено**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-169"><dt>**MPNOTIFY\_SCAN\_PAUSED**</dt></span></span> </dl>                         | <span data-ttu-id="b53d8-170">Операция сканирования приостановлена.</span><span class="sxs-lookup"><span data-stu-id="b53d8-170">Scan operation is paused.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <span data-ttu-id="b53d8-171"><dt>**\_сканирование мпнотифи \_ возобновлено**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-171"><dt>**MPNOTIFY\_SCAN\_RESUMED**</dt></span></span> </dl>                      | <span data-ttu-id="b53d8-172">Операция сканирования возобновлена после приостановки.</span><span class="sxs-lookup"><span data-stu-id="b53d8-172">Scan operation resumed from pause.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <span data-ttu-id="b53d8-173"><dt>**\_Отмена СКАНИРОВАНИЯ \_ мпнотифи**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-173"><dt>**MPNOTIFY\_SCAN\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="b53d8-174">Операция сканирования была отменена.</span><span class="sxs-lookup"><span data-stu-id="b53d8-174">Scan operation was cancelled.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <span data-ttu-id="b53d8-175"><dt>**\_ \_ ход выполнения сканирования мпнотифи**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-175"><dt>**MPNOTIFY\_SCAN\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="b53d8-176">Сведения о ходе сканирования.</span><span class="sxs-lookup"><span data-stu-id="b53d8-176">Scan progress information.</span></span> <span data-ttu-id="b53d8-177">Дополнительные сведения (например, Статистика ресурсов) доступны через структуру [**\_ данных мпскан**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="b53d8-177">Additional information (such as resource statistics) is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <span data-ttu-id="b53d8-178"><dt>**\_Ошибка СКАНИРОВАНИЯ \_ мпнотифи**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-178"><dt>**MPNOTIFY\_SCAN\_ERROR**</dt></span></span> </dl>                            | <span data-ttu-id="b53d8-179">Просмотр сведений об ошибках для определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="b53d8-179">Scan error information for a specific resource.</span></span> <span data-ttu-id="b53d8-180">Сведения о конкретных ресурсах доступны через [**структуру \_ данных мпскан**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="b53d8-180">The specific resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <span data-ttu-id="b53d8-181"><dt>**МПНОТИФИ \_ сканирование с \_ заражением**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-181"><dt>**MPNOTIFY\_SCAN\_INFECTED**</dt></span></span> </dl>                   | <span data-ttu-id="b53d8-182">Проверка обнаружила зараженный ресурс.</span><span class="sxs-lookup"><span data-stu-id="b53d8-182">Scan found an infected resource.</span></span> <span data-ttu-id="b53d8-183">Обратите внимание, что в большинстве случаев это приведет к тому, что в конце сканирования будет отправлено несколько угроз.</span><span class="sxs-lookup"><span data-stu-id="b53d8-183">Note that in most of the cases this will result in some threat reported at the end of the scan.</span></span> <span data-ttu-id="b53d8-184">Иногда он может не материализоваться как угроза из-за исключений.</span><span class="sxs-lookup"><span data-stu-id="b53d8-184">Sometimes it may not materialize as a threat because of exclusions.</span></span> <span data-ttu-id="b53d8-185">Дополнительные сведения о зараженных ресурсах доступны через структуру [**\_ данных мпскан**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="b53d8-185">Additional infected resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <span data-ttu-id="b53d8-186"><dt>**МПНОТИФИ \_ Scan \_ мемористарт**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-186"><dt>**MPNOTIFY\_SCAN\_MEMORYSTART**</dt></span></span> </dl>          | <span data-ttu-id="b53d8-187">Запущена Быстрая проверка части полной проверки.</span><span class="sxs-lookup"><span data-stu-id="b53d8-187">Quick scan portion of the full scan has started.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <span data-ttu-id="b53d8-188"><dt>**МПНОТИФИ \_ Scan \_ меморикомплете**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-188"><dt>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="b53d8-189">Часть быстрой проверки завершена.</span><span class="sxs-lookup"><span data-stu-id="b53d8-189">Quick scan portion of the full scan has completed.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="b53d8-190"><dt>**\_внутренний \_ сбой мпнотифи**</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-190"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>          | <span data-ttu-id="b53d8-191">Операция сканирования обнаружила общий сбой.</span><span class="sxs-lookup"><span data-stu-id="b53d8-191">Scan operation has encountered a generic failure.</span></span> <span data-ttu-id="b53d8-192">Значение *hResult* в [**мпкаллбакк \_ данных**](mpcallback-data.md) имеет конкретный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b53d8-192">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="b53d8-193">*фсканхандле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b53d8-193">*phScanHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d8-194">Тип: **пмфандле**</span><span class="sxs-lookup"><span data-stu-id="b53d8-194">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="b53d8-195">Возвращенный обработчик сканирования, который обозначает инициированную в данный момент проверку.</span><span class="sxs-lookup"><span data-stu-id="b53d8-195">Returned scan handle which identifies the currently initiated scan.</span></span> <span data-ttu-id="b53d8-196">Этот маркер можно использовать в последующих вызовах функций, например для получения результатов проверки.</span><span class="sxs-lookup"><span data-stu-id="b53d8-196">This handle can be used in subsequent function calls, such as to retrieve a scan result.</span></span> <span data-ttu-id="b53d8-197">Этот маркер должен быть закрыт функцией [**мфандлеклосе**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="b53d8-197">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b53d8-198">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b53d8-198">Return value</span></span>

<span data-ttu-id="b53d8-199">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b53d8-199">Type: **HRESULT**</span></span>

<span data-ttu-id="b53d8-200">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="b53d8-200">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="b53d8-201">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b53d8-201">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="b53d8-202">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b53d8-202">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b53d8-203">Требования</span><span class="sxs-lookup"><span data-stu-id="b53d8-203">Requirements</span></span>



| <span data-ttu-id="b53d8-204">Требование</span><span class="sxs-lookup"><span data-stu-id="b53d8-204">Requirement</span></span> | <span data-ttu-id="b53d8-205">Значение</span><span class="sxs-lookup"><span data-stu-id="b53d8-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b53d8-206">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b53d8-206">Minimum supported client</span></span><br/> | <span data-ttu-id="b53d8-207">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b53d8-207">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b53d8-208">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b53d8-208">Minimum supported server</span></span><br/> | <span data-ttu-id="b53d8-209">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b53d8-209">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b53d8-210">Header</span><span class="sxs-lookup"><span data-stu-id="b53d8-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="b53d8-211"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-211"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b53d8-212">DLL</span><span class="sxs-lookup"><span data-stu-id="b53d8-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b53d8-213"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b53d8-213"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b53d8-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b53d8-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b53d8-215">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="b53d8-215">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="b53d8-216">**мфандлеклосе**</span><span class="sxs-lookup"><span data-stu-id="b53d8-216">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="b53d8-217">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="b53d8-217">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="b53d8-218">**\_данные мпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b53d8-218">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="b53d8-219">**\_данные мпскан**</span><span class="sxs-lookup"><span data-stu-id="b53d8-219">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="b53d8-220">**\_ресурсы мпскан**</span><span class="sxs-lookup"><span data-stu-id="b53d8-220">**MPSCAN\_RESOURCES**</span></span>](mpscan-resources.md)
</dt> <dt>

[<span data-ttu-id="b53d8-221">**\_тип мпскан**</span><span class="sxs-lookup"><span data-stu-id="b53d8-221">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> </dl>

 

 





