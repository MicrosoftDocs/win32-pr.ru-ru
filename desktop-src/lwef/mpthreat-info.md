---
title: Структура MPTHREAT_INFO (Мпклиент. h)
description: Содержит сведения об угрозе.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO структуры устаревшие функции среды Windows
- Функции PMPTHREAT_INFO указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492630"
---
# <a name="mpthreat_info-structure"></a><span data-ttu-id="9b9a2-105">\_Структура сведений о мпсреат</span><span class="sxs-lookup"><span data-stu-id="9b9a2-105">MPTHREAT\_INFO structure</span></span>

<span data-ttu-id="9b9a2-106">Содержит сведения об угрозе.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-106">Contains information about a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9a2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b9a2-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a><span data-ttu-id="9b9a2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9b9a2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9b9a2-109">**среатид**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-110">Тип: **мпсреат \_ ID**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-111">Идентификатор угрозы.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-111">Threat identifier.</span></span> <span data-ttu-id="9b9a2-112">Верхний бит задан для выявления угроз, связанных с антивирусной программой.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-113">**детектионид**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-113">**DetectionID**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-114">Тип: **GUID**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-114">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-115">Идентификатор обнаружения.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-115">Detection ID.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-116">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-117">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-118">Имя угрозы.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-118">Threat name.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-119">**среаттипе**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-119">**ThreatType**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-120">Тип: **[ **мпсреат \_ тип**](mpthreat-type.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-120">Type: **[**MPTHREAT\_TYPE**](mpthreat-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-121">Тип угрозы.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-121">Threat type.</span></span> <span data-ttu-id="9b9a2-122">Используется для различения различных типов угроз, таких как известные плохие, неизвестные или известные хорошие проблемы.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-122">Used to differentiate among different threat types such as known bad, unknown, or known good.</span></span> <span data-ttu-id="9b9a2-123">См. раздел [**\_ тип мпсреат**](mpthreat-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-123">See [**MPTHREAT\_TYPE**](mpthreat-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-124">**среаткритикалити**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-124">**ThreatCriticality**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-125">Тип: **[ **мпсреат \_ серьезность**](mpthreat-severity.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-125">Type: **[**MPTHREAT\_SEVERITY**](mpthreat-severity.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-126">Критические угрозы.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-126">Threat criticality.</span></span> <span data-ttu-id="9b9a2-127">См. раздел [**мпсреат \_ Severity**](mpthreat-severity.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-127">See [**MPTHREAT\_SEVERITY**](mpthreat-severity.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-128">**ThreatCategory**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-128">**ThreatCategory**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-129">Тип: **[ **мпсреат \_ Category**](mpthreat-category.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-129">Type: **[**MPTHREAT\_CATEGORY**](mpthreat-category.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-130">Категория угроз, например Троян или троянская Keylogger.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-130">Threat category, such as a trojan or a keylogger.</span></span> <span data-ttu-id="9b9a2-131">См [**. \_ раздел Категория мпсреат**](mpthreat-category.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-131">See [**MPTHREAT\_CATEGORY**](mpthreat-category.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-132">**среатшортдескриптионид**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-132">**ThreatShortDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-133">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-133">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-134">Идентификатор краткого описания угрозы.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-134">Threat short description ID.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-135">**среатадвиседескриптионид**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-135">**ThreatAdviseDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-136">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-136">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-137">ИДЕНТИФИКАТОР описания рекомендации по угрозе.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-137">Threat advise description ID.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-138">**ThreatStatus**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-138">**ThreatStatus**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-139">Тип: **[ **\_ состояние мпсреат**](mpthreat-status.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-139">Type: **[**MPTHREAT\_STATUS**](mpthreat-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-140">Состояние угрозы, например обнаружено, очищено или помещено в карантин.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-140">Threat status such as detected, cleaned, or quarantined.</span></span> <span data-ttu-id="9b9a2-141">См. сведения [**\_ о состоянии мпсреат**](mpthreat-status.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-141">See [**MPTHREAT\_STATUS**](mpthreat-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-142">**сугжестедактионкаунт**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-142">**SuggestedActionCount**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-143">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-143">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-144">Число предлагаемых действий в **сугжестедактионаррай**.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-144">Count of suggested actions in **SuggestedActionArray**.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-145">**сугжестедактионаррай**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-145">**SuggestedActionArray**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-146">Тип: **[**мпсреат \_ Action**](mpthreat-action.md) \[ MP \_ Max ( \_ рекомендации)\]**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-146">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)\[MP\_MAX\_SUGGESTIONS\]**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-147">Массив предлагаемых действий.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-147">Array of suggested actions.</span></span> <span data-ttu-id="9b9a2-148">См. раздел [**\_ действие мпсреат**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-148">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-149">**ResourceCount**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-149">**ResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-150">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-150">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-151">Число ресурсов в **ресаурцелист**.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-151">Count of resources in **ResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-152">**ресаурцелист**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-152">**ResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-153">Введите: \**пмпресаурце \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="9b9a2-153">Type: \**PMPRESOURCE\_INFO\** _</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-154">Список ресурсов, определенных с помощью угрозы.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-154">List of resources identified with the threat.</span></span> <span data-ttu-id="9b9a2-155">См. раздел [_ *мпресаурце \_ info* \*](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-155">See [_ *MPRESOURCE\_INFO*\*](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-156">**среатстатустиме**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-156">**ThreatStatusTime**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-157">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-157">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-158">Время последнего изменения состояния угрозы.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-158">Time when threat status last changed.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-159">**среатстатускоде**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-159">**ThreatStatusCode**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-160">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-160">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-161">Код состояния, связанный с состоянием угрозы.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-161">Status code associated with the threat status.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-162">**среатдетектион**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-162">**ThreatDetection**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-163">Тип: **[ **\_ Обнаружение мпсреат**](mpthreat-detection.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-163">Type: **[**MPTHREAT\_DETECTION**](mpthreat-detection.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-164">Тип обнаружения угроз, например бетон, подозрительный или универсальный.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-164">Threat detection type, such as concrete, suspicious, or generic.</span></span> <span data-ttu-id="9b9a2-165">См. раздел [**мпсреат \_ Detection**](mpthreat-detection.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-165">See [**MPTHREAT\_DETECTION**](mpthreat-detection.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-166">**куарантинегуид**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-166">**QuarantineGuid**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-167">Тип: **GUID**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-167">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-168">Идентификатор GUID карантина.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-168">Quarantine guid.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-169">**ExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-169">**ExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-170">Тип: **[ **\_ состояние мпексекутион**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-170">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-171">Состояние выполнения угрозы, например неизвестная, заблокированная или активная.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-171">Execution status of the threat, such as not known, blocked, or active.</span></span> <span data-ttu-id="9b9a2-172">См. сведения [**\_ о состоянии мпексекутион**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-172">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-173">**Data**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-173">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-174">Дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-174">Extra information.</span></span> <span data-ttu-id="9b9a2-175">Указатель на соответствующую структуру зависит от значения **среаттипе**.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-175">The pointer to the appropriate structure depends on the value of **ThreatType**.</span></span>

<dl> <dt>

<span data-ttu-id="9b9a2-176">**пкновнбад**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-176">**pKnownBad**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-177">Тип: **пмпсреат \_ инфоекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-177">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-178">Если **среаттипе**  ==  **мпсреат \_ Type \_ кновнбад**.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-178">When **ThreatType** == **MPTHREAT\_TYPE\_KNOWNBAD**.</span></span> <span data-ttu-id="9b9a2-179">См. раздел [**мпсреат \_ инфоекс не \_ используется**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-179">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-180">**пбехавиор**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-180">**pBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-181">Тип: **пмпсреат \_ инфоекс \_ BEHAVIOR** .</span><span class="sxs-lookup"><span data-stu-id="9b9a2-181">Type: **PMPTHREAT\_INFOEX\_BEHAVIOR**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-182">Когда   ==  **\_ \_ поведение типа мпсреат** среаттипе.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-182">When **ThreatType** == **MPTHREAT\_TYPE\_BEHAVIOR**.</span></span> <span data-ttu-id="9b9a2-183">См. раздел [**мпсреат \_ инфоекс \_ BEHAVIOR**](mpthreat-infoex-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-183">See [**MPTHREAT\_INFOEX\_BEHAVIOR**](mpthreat-infoex-behavior.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-184">**pUnknown**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-184">**pUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-185">Тип: **пмпсреат \_ инфоекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-185">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-186">Если   ==  **тип мпсреат \_ среаттипе \_ неизвестен**.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-186">When **ThreatType** == **MPTHREAT\_TYPE\_UNKNOWN**.</span></span> <span data-ttu-id="9b9a2-187">См. раздел [**мпсреат \_ инфоекс не \_ используется**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-187">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-188">**пкновнгуд**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-188">**pKnownGood**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-189">Тип: **пмпсреат \_ инфоекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-189">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-190">Если **среаттипе** = = мпсреат \_ Type \_ кновнгуд.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-190">When **ThreatType** == MPTHREAT\_TYPE\_KNOWNGOOD.</span></span> <span data-ttu-id="9b9a2-191">См. раздел [**мпсреат \_ инфоекс не \_ используется**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-191">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-192">**пнис**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-192">**pNis**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-193">Тип: **пмпсреат \_ инфоекс \_ NIS** .</span><span class="sxs-lookup"><span data-stu-id="9b9a2-193">Type: **PMPTHREAT\_INFOEX\_NIS**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-194">При **среаттипе**  ==  **мпсреат \_ введите \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-194">When **ThreatType** == **MPTHREAT\_TYPE\_NIS**.</span></span> <span data-ttu-id="9b9a2-195">См. раздел [**мпсреат \_ инфоекс \_ NIS**](mpthreat-infoex-nis.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-195">See [**MPTHREAT\_INFOEX\_NIS**](mpthreat-infoex-nis.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9b9a2-196">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-196">**State**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-197">Тип: **[ **\_ состояние мпдетектион**](mpdetection-state.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-197">Type: **[**MPDETECTION\_STATE**](mpdetection-state.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-198">Текущее состояние обнаружения.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-198">The current state of the detection.</span></span> <span data-ttu-id="9b9a2-199">См. [**мпдетектион \_ State**](mpdetection-state.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-199">See [**MPDETECTION\_STATE**](mpdetection-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-200">**детектионусер**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-200">**DetectionUser**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-201">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-201">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-202">Пользователь, связанный с обнаружением, в формате "домен/пользователь".</span><span class="sxs-lookup"><span data-stu-id="9b9a2-202">The user associated with the detection, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-203">**детектионсаурце**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-203">**DetectionSource**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-204">Тип: **[ **мпсаурце**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-204">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-205">Источник обнаружения.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-205">The source of the detection.</span></span> <span data-ttu-id="9b9a2-206">См. [**мпсаурце**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-206">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-207">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-207">**ProcessName**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-208">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-208">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-209">Имя процесса, связанное с обнаружением.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-209">Process name associated with the detection.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-210">**детектионоригин**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-210">**DetectionOrigin**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-211">Тип: **[ **мпдетектион \_ Origin**](mpdetection-origin.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-211">Type: **[**MPDETECTION\_ORIGIN**](mpdetection-origin.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-212">Источник обнаружения, например локальный или сетевой.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-212">The origin of the detection, such as local or network.</span></span> <span data-ttu-id="9b9a2-213">См. раздел [**мпдетектион \_ Origin**](mpdetection-origin.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-213">See [**MPDETECTION\_ORIGIN**](mpdetection-origin.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-214">**reserved1**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-214">**reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-215">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-215">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-216">Зарезервированные метаданные об обнаружении.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-216">Reserved metadata about the detection.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-217">**детектионтиме**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-217">**DetectionTime**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-218">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-218">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-219">Время первоначального обнаружения.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-219">The time of the initial detection.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-220">**приксекутионстатус**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-220">**PreExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-221">Тип: **[ **\_ состояние мпексекутион**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-221">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-222">Состояние выполнения непосредственно перед исправлением.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-222">Execution status right before remediation.</span></span> <span data-ttu-id="9b9a2-223">См. сведения [**\_ о состоянии мпексекутион**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-223">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-224">**ремедиатионтиме**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-224">**RemediationTime**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-225">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-225">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-226">Возникло исправление времени.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-226">The time remediation occured.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-227">**постексекутионстатус**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-227">**PostExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-228">Тип: **[ **\_ состояние мпексекутион**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-228">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-229">Состояние выполнения после исправления.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-229">Execution status after remediation.</span></span> <span data-ttu-id="9b9a2-230">См. сведения [**\_ о состоянии мпексекутион**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-230">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-231">**CriticalFailure**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-231">**CriticalFailure**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-232">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="9b9a2-232">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-233">Значение true, если сбой исправления был критически важным.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-233">True if the remediation failure was critical.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-234">**нонкритикалреасон**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-234">**NonCriticalReason**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-235">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-235">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-236">Причина сбоя исправления не является критической.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-236">The reason the remediation failure is not critical.</span></span> <span data-ttu-id="9b9a2-237">В будущем это не обязательно будет поддерживаться.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-237">This is not guaranteed to be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-238">**ремедиатионусер**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-238">**RemediationUser**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-239">Тип: **\_ \_ строка MP MIDL, LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-239">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-240">Пользователь, запросивший исправление, в формате "домен/пользователь".</span><span class="sxs-lookup"><span data-stu-id="9b9a2-240">User that requested the remediation, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-241">**ремедиатионресаурцекаунт**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-241">**RemediationResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-242">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-242">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-243">Число ресурсов в **ремедиатионресаурцелист**.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-243">Count of resources in **RemediationResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-244">**ремедиатионресаурцелист**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-244">**RemediationResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-245">Тип: **пмпресаурце \_ info \[ ремедиатионресаурцекаунт \]**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-245">Type: **PMPRESOURCE\_INFO\[RemediationResourceCount\]**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-246">Список ресурсов, которые завершились сбоем во время исправления.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-246">List of resources that failed during remediation.</span></span> <span data-ttu-id="9b9a2-247">См [**. \_ сведения о мпресаурце**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-247">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-248">**фаилурересолвед**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-248">**FailureResolved**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-249">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="9b9a2-249">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-250">Значение true, если ошибка исправления устранена.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-250">True if remediation failure been resolved.</span></span> <span data-ttu-id="9b9a2-251">Контейнер будет перемещен в завершенное или дополнительное действие.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-251">This will move the bucket to either complete or an additional action.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-252">**ресолведреасон**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-252">**ResolvedReason**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-253">Тип: **[ **\_ Причина мпресолвед**](mpresolved-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-253">Type: **[**MPRESOLVED\_REASON**](mpresolved-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-254">Причина разрешения ошибки исправления.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-254">Reason for remediation failure being resolved.</span></span> <span data-ttu-id="9b9a2-255">Это причина, по которой обнаружение перешло с сбоя на дополнительное действие или завершено.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-255">This is the reason the detection moved from failed to additional action or finished.</span></span> <span data-ttu-id="9b9a2-256">См [**. \_ причину мпресолвед**](mpresolved-reason.md).</span><span class="sxs-lookup"><span data-stu-id="9b9a2-256">See [**MPRESOLVED\_REASON**](mpresolved-reason.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-257">**аддитионалактионс**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-257">**AdditionalActions**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-258">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-258">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-259">Требуются дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-259">Are additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-260">**ресолведактионс**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-260">**ResolvedActions**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-261">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-261">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-262">Любые дополнительные действия, которые были выполнены.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-262">Any additional actions that have been performed.</span></span>

</dd> <dt>

<span data-ttu-id="9b9a2-263">**двсреатстатусфлаг**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-263">**dwThreatStatusFlag**</span></span>
</dt> <dd>

<span data-ttu-id="9b9a2-264">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-264">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9b9a2-265">Дополнительные сведения об обнаружении угроз.</span><span class="sxs-lookup"><span data-stu-id="9b9a2-265">Additonal information about the threat detection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b9a2-266">Требования</span><span class="sxs-lookup"><span data-stu-id="9b9a2-266">Requirements</span></span>



| <span data-ttu-id="9b9a2-267">Требование</span><span class="sxs-lookup"><span data-stu-id="9b9a2-267">Requirement</span></span> | <span data-ttu-id="9b9a2-268">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9a2-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9a2-269">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b9a2-269">Minimum supported client</span></span><br/> | <span data-ttu-id="9b9a2-270">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9b9a2-270">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9b9a2-271">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b9a2-271">Minimum supported server</span></span><br/> | <span data-ttu-id="9b9a2-272">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9b9a2-272">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b9a2-273">Header</span><span class="sxs-lookup"><span data-stu-id="9b9a2-273">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b9a2-274"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b9a2-274"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b9a2-275">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b9a2-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b9a2-276">**мпфримемори**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-276">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-277">**мпсреатенумерате**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-277">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-278">**мпсреаткуери**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-278">**MpThreatQuery**</span></span>](mpthreatquery.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-279">**\_источник мпдетектион**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-279">**MPDETECTION\_ORIGIN**</span></span>](mpdetection-origin.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-280">**\_состояние мпдетектион**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-280">**MPDETECTION\_STATE**</span></span>](mpdetection-state.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-281">**\_состояние мпексекутион**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-281">**MPEXECUTION\_STATUS**</span></span>](mpexecution-status.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-282">**\_Причина мпресолвед**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-282">**MPRESOLVED\_REASON**</span></span>](mpresolved-reason.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-283">**\_сведения о мпресаурце**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-283">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-284">**мпсаурце**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-284">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-285">**\_действие мпсреат**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-285">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-286">**\_Категория мпсреат**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-286">**MPTHREAT\_CATEGORY**</span></span>](mpthreat-category.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-287">**\_Обнаружение мпсреат**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-287">**MPTHREAT\_DETECTION**</span></span>](mpthreat-detection.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-288">**\_поведение ИНФОЕКС \_ мпсреат**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-288">**MPTHREAT\_INFOEX\_BEHAVIOR**</span></span>](mpthreat-infoex-behavior.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-289">**МПСРЕАТ \_ инфоекс \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-289">**MPTHREAT\_INFOEX\_NIS**</span></span>](mpthreat-infoex-nis.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-290">**МПСРЕАТ \_ инфоекс не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-290">**MPTHREAT\_INFOEX\_UNUSED**</span></span>](mpthreat-infoex-unused.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-291">**МПСРЕАТ \_ серьезность**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-291">**MPTHREAT\_SEVERITY**</span></span>](mpthreat-severity.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-292">**\_состояние мпсреат**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-292">**MPTHREAT\_STATUS**</span></span>](mpthreat-status.md)
</dt> <dt>

[<span data-ttu-id="9b9a2-293">**\_тип мпсреат**</span><span class="sxs-lookup"><span data-stu-id="9b9a2-293">**MPTHREAT\_TYPE**</span></span>](mpthreat-type.md)
</dt> </dl>

 

 





